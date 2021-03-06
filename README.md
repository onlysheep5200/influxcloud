# influxCloud

[![Go Report Card](https://goreportcard.com/badge/github.com/zhexuany/influxcloud)](https://goreportcard.com/report/github.com/zhexuany/influxcloud) [![Build Status](https://travis-ci.org/zhexuany/influxcloud.svg?branch=master)](https://travis-ci.org/zhexuany/influxcloud)


## Status
`influx-meta` is ready to go. But this need corporate with `influxd`. Comparing with current `influxd`, we have to append a `cluster` service. In this way,
It enables the communication channel between `data` node and `meta` node.

## What is this prototype can do? 
- edit meta node including adding, updating and deleting 
- edit data node including adding, updating and deleting
- distributed data in a basic form of shards across nodes in cluster 
- distributed query across cluster if such query can not be done locally

## What is this prototype can not do but will add in future?
- Raft Algorithm Optimization
- Performance improvement
- Provide a way expand Shades inside ShardGroup. For now, once ShardGroup is created, there is no way that we can expand the size of Shards which means the capacity of writing will be limited.
- Add User and Role Creation and Authorization.
- Added Command that can know the status of cluster
- Bring docker into build
- add integration framework based on etcd's work.
- Buffer failed write into disk and retry until such buffer is empty. In order to improve the usage of disk, we need clean such buffer in some manner.
- Provide a way that can backup a cluster and restore it later.

## How to build
Well, you do not need worry this in a month. The prototype is still under implementing. But we promise, we will try hard to get things done quickly.

## Architeture
Please check the architeture.md for more details. Any inquiry and comments are welcome. You can find my email in my github's profile.
