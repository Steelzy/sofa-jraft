# SOFAJRaft

[![Build Status](https://travis-ci.com/sofastack/sofa-jraft.svg?branch=master)](https://travis-ci.com/sofastack/sofa-jraft)
![License](https://img.shields.io/badge/license-Apache--2.0-green.svg)
[![Maven Central](https://img.shields.io/maven-central/v/com.alipay.sofa/jraft-parent.svg?label=maven%20central)](https://search.maven.org/search?q=g:com.alipay.sofa%20AND%20sofa-jraft)

## Overview
SOFAJRaft is a production-level, high-performance Java implementation based on the [RAFT](https://raft.github.io/) consistency algorithm that supports MULTI-RAFT-GROUP for high-load, low-latency scenarios.
With SOFAJRaft you can focus on your business area. SOFAJRaft handles all RAFT-related technical challenges. SOFAJRaft is very user-friendly, which provides several examples, making it easy to understand and use.

## Features
- Leader election
- Log replication and recovery
- Snapshot and log compaction
- Cluster membership management, adding nodes, removing nodes, replacing nodes, etc.
- Mechanism of transfer leader for reboot, load balance scene, etc.
- Symmetric network partition tolerance
- Asymmetric network partition tolerance
- Fault tolerance, minority failure doesn't affect the overall availability of system
- Manual recovery cluster available for majority failure
- Linearizable read, ReadIndex/LeaseRead
- Replication pipeline
- Rich statistics to analyze the performance based on [Metrics](https://metrics.dropwizard.io/4.0.0/getting-started.html)
- Passed [Jepsen](https://github.com/jepsen-io/jepsen) consistency verification test
- SOFAJRaft includes an embedded distributed KV storage implementation

## Requirements
Compile requirement: JDK 8+ and Maven 3.2.5+ .

## Documents
- [User Guide](https://github.com/sofastack/sofa-jraft/wiki)
- [Counter Example Details](https://github.com/sofastack/sofa-jraft/wiki/Counter-%E4%BE%8B%E5%AD%90%E8%AF%A6%E8%A7%A3)
- [Release Notes](https://github.com/sofastack/sofa-jraft/wiki/%E7%89%88%E6%9C%AC%E5%8F%91%E8%A1%8C%E6%97%A5%E5%BF%97)

## Contribution
[How to contribute](https://github.com/sofastack/sofa-jraft/wiki/%E5%A6%82%E4%BD%95%E5%8F%82%E4%B8%8E-SOFAJRaft-%E4%BB%A3%E7%A0%81%E8%B4%A1%E7%8C%AE)

## Acknowledgement
SOFAJRaft was ported from Baidu's [braft](https://github.com/brpc/braft) with some optimizing and improvement. Thanks to the Baidu braft team for opening up such a great C++ RAFT implementation.

## License
SOFAJRaft is licensed under the [Apache License 2.0](./LICENSE). SOFAJRaft relies on some third-party components, and their open source protocol is also Apache License 2.0.
In addition, SOFAJRaft also directly references some code (possibly with minor changes), which open source protocol is Apache License 2.0, including
- NonBlockingHashMap/NonBlockingHashMapLong in [JCTools](https://github.com/JCTools/JCTools)
- HashedWheelTimer in [Netty](https://github.com/netty/netty), also referenced Netty's Pipeline design
- Efficient encoding/decoding of UTF8 String in [Protobuf](https://github.com/protocolbuffers/protobuf)
