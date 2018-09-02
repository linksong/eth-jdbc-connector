# Introduction 

[![Join the chat at https://gitter.im/Impetus/eth-jdbc-connector](https://badges.gitter.im/Impetus/eth-jdbc-connector.svg)](https://gitter.im/Impetus/eth-jdbc-connector?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
**[Join Google Group ](https://groups.google.com/forum/#!forum/ethereum-jdbc-driver)**

Ethereum JDBC driver implements a pure java, type 4 JDBC driver that executes SQL queries on Ethereum blockchain. It facilitates getting the data in and out of ethereum in JDBC compliant manner. The Ethereum JDBC driver can be used to  perform ETL, BI reporting and analytics using the familiar SQL language.

It uses [blkchn-sql-driver](https://github.com/Impetus/blkchn-sql-driver) to parse the query and create corresponding logical plan. This logical plan is then converted into an optimized physical plan. The driver extends and implements the physical plan using corresponding [web3j](https://github.com/web3j/web3j) calls to connect to Ethereum. The driver then converts the returned objects to a JDBC compliant result set and return it to the user.

# Tested with
| Dependency | Version |
|---|---|
| maven | 3.3.3 |
|java | 1.8 |
|web3j | 3.4.0 |
|spark | 2.0.0|

Features Added with Release 1.1.0
==========================

* [Smart contract support](https://github.com/Impetus/eth-jdbc-connector/wiki/Ethereum-Smart-Contract-Guide) -User can deploy smart contract and run its fuctions by using jdbc driver
* [Ethereum with Spark](https://github.com/Impetus/eth-jdbc-connector/wiki/Ethereum-with-Spark)
* [Batch Transaction](https://github.com/Impetus/eth-jdbc-connector/wiki/Batch-Transaction)- Initiating multiple transactions in a batch

Building ethereum-jdbc-connector
==========================
- [Download](https://github.com/Impetus/blkchn-sql-driver/archive/master.zip) or clone <b>blkchn-sql-driver</b> project `git clone https://github.com/Impetus/blkchn-sql-driver.git`
- build blkchn-sql-driver using `mvn clean install -Pgen-sources`
- [Download](https://github.com/Impetus/eth-jdbc-connector/archive/master.zip) sourcecode or use `git clone https://github.com/Impetus/eth-jdbc-connector.git`
- build it using `mvn clean install` 

# Getting Started
- Navigate to [examples](https://github.com/Impetus/eth-jdbc-connector/tree/master/eth-jdbc-examples) folder
- Run [`Query.java`](https://github.com/Impetus/eth-jdbc-connector/blob/master/eth-jdbc-examples/src/main/java/com/impetus/blkchn/eth/Query.java) and [`Insert.java`](https://github.com/Impetus/eth-jdbc-connector/blob/master/eth-jdbc-examples/src/main/java/com/impetus/blkchn/eth/Insert.java) for quick start

To use Ethereum JDBC connector in a maven project, add the following maven dependency in your project:
 
  
  ```
  <dependency>
    <groupId>com.impetus.eth</groupId>
    <artifactId>eth-jdbc-driver</artifactId>
    <version>${ethjdbcdriver.version}</version>
  </dependency>
  ```

Build your project with the above changes to your pom.xml.

# Connection and Querying

- Check [how to connect](https://github.com/Impetus/eth-jdbc-connector/wiki/Ethereum-Connection-Details) to ethereum
- [Supported queries](https://github.com/Impetus/eth-jdbc-connector/wiki/Ethereum-Query-Guide)

# How to Contribute

- [Contribution Guidelines](https://github.com/Impetus/eth-jdbc-connector/blob/master/CONTRIBUTING.md)

About Us
========
eth-jdbc-connector is backed by Impetus Labs - iLabs. iLabs is a R&D consulting division of [Impetus Technologies](http://www.impetus.com). iLabs focuses on innovations with next generation technologies and creates practice areas and new products around them. iLabs is actively involved working on blockchain technologies, neural networking, distributed/parallel computing and advanced analytics using spark and big data ecosystem. iLabs is also working on various other Open Source initiatives.
