[<img src="https://sling.apache.org/res/logos/sling.png"/>](https://sling.apache.org)

 [![Build Status](https://builds.apache.org/buildStatus/icon?job=Sling/sling-org-apache-sling-nosql-mongodb-resourceprovider/master)](https://builds.apache.org/job/Sling/job/sling-org-apache-sling-nosql-mongodb-resourceprovider/job/master) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.sling/org.apache.sling.nosql.mongodb-resourceprovider/badge.svg)](https://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.apache.sling%22%20a%3A%22org.apache.sling.nosql.mongodb-resourceprovider%22) [![JavaDocs](https://www.javadoc.io/badge/org.apache.sling/org.apache.sling.nosql.mongodb-resourceprovider.svg)](https://www.javadoc.io/doc/org.apache.sling/org.apache.sling.nosql.mongodb-resourceprovider) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![nosql](https://sling.apache.org/badges/group-nosql.svg)](https://github.com/apache/sling-aggregator/blob/master/docs/groups/nosql.md)

# Apache Sling NoSQL MongoDB Resource Provider

This module is part of the [Apache Sling](https://sling.apache.org) project.

Sling ResourceProvider implementation that uses [MongoDB](https://www.mongodb.org/) NoSQL database as persistence.

Based on the "Apache Sling NoSQL Generic Resource Provider".

All resource data is stored in one MongoDB database and one collection, using the path of the resource as "_id" property.


Configuration on deployment
---------------------------

* Create a factory configuration for "Apache Sling NoSQL MongoDB Resource Provider Factory" to define the root of the resource tree that should be stored in MongoDB, and MongoDB connection string, database name and collection name.


Run integration tests
---------------------

To run the integration tests you have to set up a real MongoDB server and run the tests with this command line (inserting the correct parameters):

```
mvn -Pmongodb-integration-test -DconnectionString=localhost:27017 -Ddatabase=sling -Dcollection=resources integration-test
```
