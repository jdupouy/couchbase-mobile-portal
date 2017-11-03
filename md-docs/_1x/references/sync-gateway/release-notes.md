---
id: sg-release-notes
title: SG release notes
---

## 1.5 release

__Performance Improvements__

- [__#2218__](https://github.com/couchbase/sync_gateway/issues/2218) SyncGateway/SyncGateway replicator memory keeps growing continuosly and resulting in OOM crash
- [__#2651__](https://github.com/couchbase/sync_gateway/issues/2651) SG gets killed due to excessive memory usage with continuous doc update

__Enhancements__

- [__#1462__](https://github.com/couchbase/sync_gateway/issues/1462) Sync Gateway Accelerator is reporting itself as Sync Gateway
- [__#2151__](https://github.com/couchbase/sync_gateway/issues/2151) The /{db}/\_changes?include_docs=true request shouldn't return _user/user docs
- [__#2259__](https://github.com/couchbase/sync_gateway/issues/2259) Add support for RHEL in service install scripts

__Bugs__

- [__#2218__](https://github.com/couchbase/sync_gateway/issues/2218) SyncGateway/SyncGateway replicator memory keeps growing continuosly and resulting in OOM crash
- [__#2367__](https://github.com/couchbase/sync_gateway/issues/2367) Omitting the logFilePath property in the logging configuration of Sync Gateway results in a null pointer exception crash
- [__#2381__](https://github.com/couchbase/sync_gateway/issues/2381) SG Replicate stops when an attachment with no content type is replicated
- [__#2400__](https://github.com/couchbase/sync_gateway/issues/2400) SG collect info is not case sensitive on the config's logFilePath property
- [__#2421__](https://github.com/couchbase/sync_gateway/issues/2421) Discard new rev sequence if it is less than a docs current rev sequence, to avoid issues with caching
- [__#2500__](https://github.com/couchbase/sync_gateway/issues/2500) Webhook event not fired when using bucket shadowing
- [__#2565__](https://github.com/couchbase/sync_gateway/issues/2565) Non-empty oldDoc being sent to sync function during import
- [__#2626__](https://github.com/couchbase/sync_gateway/issues/2626) Active changes feeds not notified when deferred sequences get cached
- [__#2651__](https://github.com/couchbase/sync_gateway/issues/2651) SG gets killed due to excessive memory usage with continuous doc update
- [__#2677__](https://github.com/couchbase/sync_gateway/issues/2677) Unable to install SG 1.5.0 on Win 10

__Known issues__

- [__#2744__](https://github.com/couchbase/sync_gateway/pull/2744) Failures due to multi operation deletes
- [__#149__](https://github.com/couchbaselabs/sync-gateway-accel/issues/149) Changes missing on Sync Gateway Accelerator re-shard
- [__#2068__](https://github.com/couchbase/sync_gateway/issues/2068) Update user doc sequence for access-based channel grants
- [__#160__](https://github.com/couchbaselabs/sync-gateway-accel/issues/160) The `_doc_ids` changes feed filter doesn't work with Accelerator

## 1.4.1 release

__Enhancements__

- [__#2373__](https://github.com/couchbase/sync_gateway/issues/2373) Add sample config for SG running with Accel
- [__#2428__](https://github.com/couchbase/sync_gateway/issues/2428) Avoid document body unmarshalling on changes requests

__Bugs__

- [__#1518__](https://github.com/couchbase/sync_gateway/issues/1518) Data races detected in channel_cache.go
- [__#2364__](https://github.com/couchbase/sync_gateway/issues/2364) Omit doc during Changes+ logging
- [__#2365__](https://github.com/couchbase/sync_gateway/issues/2365) Account for unused sequences after CAS retry and subsequent cancel
- [__#2427__](https://github.com/couchbase/sync_gateway/issues/2427) CBSE: Data race in trimEncodedRevisionsToAncestor

## 1.4 release

__New features__

- [Sync Gateway Accelerator](../../guides/sync-gateway/accelerator.html)
- [Log rotation](../../guides/sync-gateway/deployment/index.html#built-in-log-rotation)

__Performance Improvements__

- [__#1514__](https://github.com/couchbase/sync_gateway/issues/1514) Run long-running performance tests against 1.4

__Enhancements__

- [__#1713__](https://github.com/couchbase/sync_gateway/issues/1713) [sg-accel] Use reference counts to track active channels
- [__#1925__](https://github.com/couchbase/sync_gateway/issues/1925) HTTP basic auth for webhooks
- [__#2098__](https://github.com/couchbase/sync_gateway/issues/2098) Upgrade build to go 1.7.1
- [__#2160__](https://github.com/couchbase/sync_gateway/issues/2160) Add log rotation capabilities into Sync Gateway
- [__#2255__](https://github.com/couchbase/sync_gateway/issues/2255) Update sgcollect_info to collect logs defined logging config
- [__#2298__](https://github.com/couchbase/sync_gateway/issues/2298) Update sgcollect_info to capture rotated logs

__Bugs__

- [__#1529__](https://github.com/couchbase/sync_gateway/issues/1529) Longpoll `_changes` request that returns no results, returns invalid sequence number for last_seq
- [__#1865__](https://github.com/couchbase/sync_gateway/issues/1865) One shot replication of granting access doc can lead to miss documents
- [__#1890__](https://github.com/couchbase/sync_gateway/issues/1890) Calling db `_online` when CBS bucket is not available results in "no such database" even when CBS bucket is available again
- [__#2080__](https://github.com/couchbase/sync_gateway/issues/2080) Startup error when config includes unsupported/user_views
- [__#2084__](https://github.com/couchbase/sync_gateway/issues/2084) Update Windows install folder for sg_accel
- [__#2102__](https://github.com/couchbase/sync_gateway/issues/2102) Protect against empty doc body in handlePutDoc
- [__#2139__](https://github.com/couchbase/sync_gateway/issues/2139) Sg_accel packages should use example config from sync-gateway-accel repo
- [__#2159__](https://github.com/couchbase/sync_gateway/issues/2159) Handle channel removal for coalesced feed updates
- [__#2187__](https://github.com/couchbase/sync_gateway/issues/2187) SG panic when upgrading keepalive http connection to WebSockets
- [__#2212__](https://github.com/couchbase/sync_gateway/issues/2212) Channel filtered sg-replicate stops due to channel removals
- [__#2270__](https://github.com/couchbase/sync_gateway/issues/2270) Starting sync gateway from command line does not always report the right status

__Known Issues__

- [__#2341__](https://github.com/couchbase/sync_gateway/issues/2341) Channel_index bucket authentication requires username

__Sync Gateway Accelerator Known Issues__

- [Sync Gateway Accel does not recover when removing a node from Couchbase Server Cluster](https://github.com/couchbaselabs/sync-gateway-accel/issues/17): removing a node from the Couchbase Server Cluster can cause Sync Gateway Accel to fail. Restarting the Accel node resolves the issue.
- [Client Rollback Support](https://github.com/couchbaselabs/sync-gateway-accel/issues/10): when Couchbase Server issues a rollback, Sync Gateway Accel handles that rollback and rolls back the data in the channel index bucket. However, we're not yet invalidating client sequence/since values that were sent to clients pre-rollback. As a result, clients may miss documents written to sequence values in the rollback window.
- [Add Index Document Inspection REST API](https://github.com/couchbaselabs/sync-gateway-accel/issues/126): the majority of the index bucket contents are stored as binary documents. Getting a human-readable version of the contents of these documents would be very useful while debugging some types of issues.

__Deprecation notices__

The following features are being deprecated in 1.4 and will be unsupported in an upcoming version (2.x) of Couchbase 
Mobile.

- Bucket Shadowing

## 1.3.1 release

**Enhancements**

- [**#1745**](https://github.com/couchbase/sync_gateway/issues/1745) Add retry when trying to connect to a server node in "warmup" state
- [**#2005**](https://github.com/couchbase/sync_gateway/issues/2005) Tombstones don't grant access, don't propagate to users granted access by the doc
- [**#2013**](https://github.com/couchbase/sync_gateway/issues/2013) Azure returns unsigned ID token in response to refresh request
- [**#2038**](https://github.com/couchbase/sync_gateway/issues/2038) Uptake expvar refactoring for perf usage into 1.3.1
- [**#2046**](https://github.com/couchbase/sync_gateway/issues/2046) Service install script enhancement for Ubuntu 16.04

**Bugs**

- [**#973**](https://github.com/couchbase/sync_gateway/issues/973) Can't initiate websocket connection
- [**#1554**](https://github.com/couchbase/sync_gateway/issues/1554) Panic: send on closed channel when closing database
- [**#1999**](https://github.com/couchbase/sync_gateway/issues/1999) Sync Gateway terminating changes requests

### Where to get it

You can download this release from [Couchbase.com](http://www.couchbase.com/nosql-databases/downloads#Couchbase_Mobile)

## 1.3.1 release

**Enhancements**

- [**#1745**](https://github.com/couchbase/sync_gateway/issues/1745) Add retry when trying to connect to a server node in "warmup" state
- [**#2005**](https://github.com/couchbase/sync_gateway/issues/2005) Tombstones don't grant access, don't propagate to users granted access by the doc
- [**#2013**](https://github.com/couchbase/sync_gateway/issues/2013) Azure returns unsigned ID token in response to refresh request
- [**#2038**](https://github.com/couchbase/sync_gateway/issues/2038) Uptake expvar refactoring for perf usage into 1.3.1
- [**#2046**](https://github.com/couchbase/sync_gateway/issues/2046) Service install script enhancement for Ubuntu 16.04

**Bugs**

- [**#973**](https://github.com/couchbase/sync_gateway/issues/973) Can't initiate websocket connection
- [**#1554**](https://github.com/couchbase/sync_gateway/issues/1554) Panic: send on closed channel when closing database
- [**#1999**](https://github.com/couchbase/sync_gateway/issues/1999) Sync Gateway terminating changes requests

## 1.3 release

__Performance Improvements__

- [__#1631__](https://github.com/couchbase/sync_gateway/issues/1631) Disable assimilator when autoImport=false and shadower=nil
- [__#1752__](https://github.com/couchbase/sync_gateway/issues/1752) Major inefficiencies replicating docs with many revisions

__Enhancements__

- [__#508__](https://github.com/couchbase/sync_gateway/issues/508) Feature Request:  Oauth2 Support
- [__#656__](https://github.com/couchbase/sync_gateway/issues/656) Special characters in channel names cause error
- [__#1326__](https://github.com/couchbase/sync_gateway/issues/1326) Map URI's without a trailing slash to the same handlers as the trailing backslash routes
- [__#1331__](https://github.com/couchbase/sync_gateway/issues/1331) Create and distribute a diagnostics tool
- [__#1623__](https://github.com/couchbase/sync_gateway/issues/1623) POST to _changes is incompatible with CouchDB's implementation
- [__#1634__](https://github.com/couchbase/sync_gateway/issues/1634) Querying a view via the Public REST API returns total row count
- [__#1663__](https://github.com/couchbase/sync_gateway/issues/1663) Add `_replicate` support to SG admin REST API
- [__#1680__](https://github.com/couchbase/sync_gateway/issues/1680) SGW /{db}/{doc}?revs_info=true doesn't show revision info
- [__#1683__](https://github.com/couchbase/sync_gateway/issues/1683) Allow forward slashes in attachment names
- [__#1685__](https://github.com/couchbase/sync_gateway/issues/1685) Misleading error message when trying to add attachment to unavailable document
- [__#1686__](https://github.com/couchbase/sync_gateway/issues/1686) New logging REST API endpoint
- [__#1688__](https://github.com/couchbase/sync_gateway/issues/1688) Implement OpenID Connect relying-party support
- [__#1710__](https://github.com/couchbase/sync_gateway/issues/1710) Ability for Sync Gateway to bring itself back online after unexpected offline
- [__#1774__](https://github.com/couchbase/sync_gateway/issues/1774) Functional tests for OIDC authentication
- [__#1926__](https://github.com/couchbase/sync_gateway/issues/1926) Handle invalid username characters in OIDC issuer, subject

__Bugs__

- [__#1024__](https://github.com/couchbase/sync_gateway/issues/1024) Sync Gateway not reporting changes
- [__#1034__](https://github.com/couchbase/sync_gateway/issues/1034) SyncGateway not looking up the ancestry to find an attachment
- [__#1051__](https://github.com/couchbase/sync_gateway/issues/1051) Couchbase Server indexing stuck on SG views
- [__#1286__](https://github.com/couchbase/sync_gateway/issues/1286) Removing a node from CB-cluster and rebalance causing writer SG to crash
- [__#1308__](https://github.com/couchbase/sync_gateway/issues/1308) [Distributed Index] User not getting docs in  _changes when given access via sync function
- [__#1384__](https://github.com/couchbase/sync_gateway/issues/1384) Changes feed returning duplicates for * channel
- [__#1388__](https://github.com/couchbase/sync_gateway/issues/1388) [Distributed Index] Panic when restarting sync_gateway
- [__#1471__](https://github.com/couchbase/sync_gateway/issues/1471) [Distributed Index] Panic when shutting down sg_accel while it is indexing
- [__#1575__](https://github.com/couchbase/sync_gateway/issues/1575) New warning happening on SG 1.2: "MultiChangesFeed: Terminator missing for Continuous/Wait mode"
- [__#1631__](https://github.com/couchbase/sync_gateway/issues/1631) Disable assimilator when autoImport=false and shadower=nil
- [__#1656__](https://github.com/couchbase/sync_gateway/issues/1656) Users can be created with empty password even though `allow_empty_password` is `False`
- [__#1691__](https://github.com/couchbase/sync_gateway/issues/1691) Latest gocb breaks go get
- [__#1702__](https://github.com/couchbase/sync_gateway/issues/1702) _changes with doc_ids filter does not return deleted docs
- [__#1706__](https://github.com/couchbase/sync_gateway/issues/1706) Attachments fail to sync if revpos ancestor on server has been compacted
- [__#1712__](https://github.com/couchbase/sync_gateway/issues/1712) Return an error for unsupported changes filter
- [__#1728__](https://github.com/couchbase/sync_gateway/issues/1728) Attachments still stored for documents rejected by sync function
- [__#1736__](https://github.com/couchbase/sync_gateway/issues/1736) Intermittent unit test failure - TestPostChangesChannelFilterClock
- [__#1751__](https://github.com/couchbase/sync_gateway/issues/1751) SG master doesn't compile on i386
- [__#1760__](https://github.com/couchbase/sync_gateway/issues/1760) Compiling for i386 fails in `pruneRevisions`
- [__#1769__](https://github.com/couchbase/sync_gateway/issues/1769) Filter by channel works with arrays only
- [__#1857__](https://github.com/couchbase/sync_gateway/issues/1857) Changes feed with doc_ids filter omits `deleted` properties

__Known Issues__

- [__#1979__](https://github.com/couchbase/sync_gateway/issues/1979) OIDC - Azure AD must be default provider when using multiple providers

## Where to get it

You can download this release from the [downloads page](http://www.couchbase.com/nosql-databases/downloads#couchbase-mobile).