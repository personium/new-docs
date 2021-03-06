---
id: version-1.7.21-personium_tests
title: Personium Tests
sidebar_label: Personium Tests
original_id: personium_tests
---

## Overview

Personium's automated tests are roughly categorized into two.

|Type|Description|
|:--|:--|
|Unit Test|Checks the behavior of each class / method.|
|Integration Test|Checks the Web API behavior.|


## Unit Test

Checks the behavior of each class / method. 
Keep the tests as simple as we can by using mocks.
Do not write Unit tests that communicate with external programs such as Personium Engine, MemCached, ElasticSearch or ActiveMQ.

### Package / Class / Method naming conventions

|Target|Convention|Note|
|:--|:--|:--|
|Package|same as test target class|io.personium.core.*|
|Class Name|{target class name}Test.java| |
|Method Name|{target Method name}\_{Conditions}\_{Result}| |

- Use English language for all of above.

## Integration Test

Test programs under io.personium.test.* packages.
They check the behavior of each Web API, communicating with external programs such as ElasticSearch, ActiveMQ.

### Preparation

Integration test can run correctly only after correct test data are prepared.
By running Setup#reset() and Setup#resetEventLog(), test data will be prepared.



