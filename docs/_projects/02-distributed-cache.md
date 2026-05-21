---
title: Distributed Cache Layer
subtitle: Custom consensus-based distributed caching system with automatic failover
tech:
  - Go
  - Raft Algorithm
  - gRPC
  - Docker
link: https://github.com
---

## Overview

A high-performance distributed cache built from scratch using the Raft consensus algorithm. This system provides strong consistency guarantees while maintaining exceptional throughput and minimal latency.

## Why Build From Scratch?

While off-the-shelf solutions exist, this project explores the fundamentals of distributed consensus and provides a learning opportunity into building resilient systems.

## Core Components

- **Raft Implementation** - Custom consensus for leader election and log replication
- **gRPC API** - Efficient binary protocol for client communication
- **Adaptive Replication** - Automatic rebalancing based on load
- **Comprehensive Testing** - Network partition simulation and chaos engineering

## Performance

- Sub-millisecond latency for cache hits
- 100K+ QPS per node
- Automatic recovery from node failures
- Zero data loss during graceful shutdowns

## Future Improvements

- Sharding support for horizontal scaling
- Compression for large values
- Integration with persistent storage
