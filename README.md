# Hadoop Ecosystem Programming Practise
> An early **hands-on** guide to Hadoop Ecosystem  

## Overview

Repository as the name suggests contains, the variety of *Hadoop Ecosystem* framework components, keeping in mind the *big data analytics students & and naive data engineers*. 

Programming implementations are done using *java* and *python* (depends upon the ease of using the underlying framework component), by keeping in mind the aspect of *modularity* and *readability*.

## Usage

The developed programs belong to following category of hadoop ecosystem components like:

> **Distributed file system and processing :** *hdfs* ( as dfs storage) and *mapreduce* (as dfs processing system, includes more like *pig*, *hive* etc)

> **NoSQL database :** *hbase* (using JAVA API)

> **In-Memory dfs framework :** *spark* (RDD using pyspark)

A few of them gives fair idea of using different components (with the probable choice of languages like spark with pyspark or hbase with java API) depends upon the choice of operation and workload.

Programs are named to represent an intuitive understanding about themselves, and are kept in the related directories (Vig. *ProductStoreSalesAnalytics* contains program for *analytics of sales store/product wise*). Additionaly supplied InputFile helps verifying the output. 

Detailed instructions for inputfile and program control flow is mentioned in the corresponding directory. Kindly read-through it for having help on underlying project, and related input/output. 

For example, In *ProductStoreSalesAnalytics* project:

    SalesPerStoreMapper.java [ MAPPER ] ---> [ REDUCER ] MaxSalesPerStoreReducer.java             
                                        ---> [ REDUCER ] TotalSalesValueAllStoresReducer.java
                                        ---> [ REDUCER ] MaxSalesPerStoreReducer.java 
    
    SalesPerProductMapper.java [ MAPPER ] -> [ REDUCER ] TotalSalesPerProductReducer.java
    
    myMapReduceDriver.java [ DRIVER ] 

**Note :** *driver* file is subject to change, depends upon the *mapper* and *reducer* to be executed.

## Conclusion

I am progressing to add more informatory files (vig. *README*) regarding input and operations used in programs. 

Programs are tested with datasets *reasonably close to real-world*, but can be subject to failure against *absolute real-world datasets*. And hence suitable for learning/initial hands-on purpose specifically (not for experts).


*Waiting to hear feedback/concerns.*
 
 
_Paritosh *( Parit )*
