Changes by Version
==================
Release Notes.

8.0.0
------------------

#### Project
* v3 protocol is added and implemented. All previous releases are incompatible with 8.x releases.
* Service, Instance, Endpoint register mechanism and inventory storage entities are removed.
* New GraphQL query protocol is provided, the legacy procotol is still supported(plan to remove at the end of this year).
* Support Prometheus network protocol. Metrics in Prometheus format could be transferred into SkyWalking.
* Python agent provided.
* All inventory caches have been removed.
* Apache ShardingSphere(4.0.0, 4.1.1) agent plugin provided.

#### Java Agent
* Add MariaDB plugin.
* Vert.x plugin enhancement. More cases are covered.
* Support v3 extension header.
* Fix ElasticSearch 5.x plugin TransportClient error.
* Support Correlation protocol v1.
* Fix Finagle plugin bug, in processing Noop Span.
* Make `CommandService` daemon to avoid blocking target application shutting down gracefully.

#### OAP-Backend
* Support meter system for Prometheus adoption. In future releases, we will add native meter APIs and MicroMeter(Sleuth) system.
* Support endpoint grouping.
* Add **SuperDataSet** annotation for storage entity. 
* Add **superDatasetIndexShardsFactor** in the ElasticSearch storage, to provide more shards for @SuperDataSet annotated entites. Typically TraceSegment.
* Support alarm settings for relationship of service, instance, and endpoint level metrics.
* Support alarm settings for database(conjecture node in tracing scenario).
* Data Model could be added in the runtime, don't depend on the bootstrap sequence anymore.
* Reduce the memory cost, due to no inventory caches.
* No buffer files in tracing and service mesh cases.
* New ReadWriteSafe cache implementation. Simplify codes.
* Provide default way for metrics query, even the metrics doesn't exist.
* New GraphQL query protocol is provided. Support the metrics type query.
* Set up length rule of service, instance, and endpoint.
* Adjust the default jks for ElasticSearch to empty.
* Fix Apdex function integer overflow issue. 
* Fix profile storage issue.
* Fix TTL issue.
* Fix H2 column type bug.
* Add JRE 8-14 test for the backend. 

#### UI
* UI dashboard is 100% configurable to adopt new metrics definited in the backend.

#### Document
* Add v8 upgrade document.
* Make the coverage accurate including UT and e2e tests.
* Add miss doc about collecting parameters in the profiled traces.

#### CVE
* Fix SQL Injection vulnerability in H2/MySQL implementation.
* Upgrade Nacos to avoid the FastJson CVE in high frequency.
* Upgrade jasckson-databind to 2.9.10. 


All issues and pull requests are [here](https://github.com/apache/skywalking/milestone/45?closed=1)

7.0.0 release
------------------
You could find all CHANGES of 7.0.0 at [here](https://github.com/apache/skywalking/blob/v7.0.0/CHANGES.md)

6.x releases
------------------
You could find all CHANGES of 6.x at [here](https://github.com/apache/skywalking/blob/6.x/CHANGES.md)

5.x releases
------------------
You could find all CHANGES of 5.x at [here](https://github.com/apache/skywalking/blob/5.x/CHANGES.md)
