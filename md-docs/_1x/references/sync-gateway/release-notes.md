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

## 1.2.1 release

**Enhancements**

- [**#1646**](https://github.com/couchbase/sync_gateway/issues/1646) "Not Imported" warning should include additional diagnostic information

**Bugs**

- [**#1573**](https://github.com/couchbase/sync_gateway/issues/1573) Windows InstallShield installer fails when upgrading an existing SG 1.1.1 installation
- [**#1581**](https://github.com/couchbase/sync_gateway/issues/1581) _sync:"sequence" is set to 0 causing documents not to replicate to our shadow bucket
- [**#1632**](https://github.com/couchbase/sync_gateway/issues/1632) Use a ring buffer for storage of goroutineTracker snapshots
- [**#1638**](https://github.com/couchbase/sync_gateway/issues/1638) Sync_gateway does not respawn automatically under systemd
- [**#1645**](https://github.com/couchbase/sync_gateway/issues/1645) Upgrading from 1.1.1 to 1.2 on RHEL/CentOS does not install service

## 1.2 release

Sync Gateway 1.2 packs a comprehensive set of enhancements and bug fixes including:

- **Database Offline/Online Administration** - You can now take individual databases online/offline using the admin REST API for routine maintenance, upgrades, or to recover from datacenter network outages.
- **Sync Gateway Accelerator** - Optional service which enables your Sync Gateway applications to scale horizontally to meet demanding loads.
- **Database `_purge` Command** - Improve performance and reduce storage size by deleting tombstoned revisions from your Sync Gateway database.

**Performance Improvements**
- [**#1163**](https://github.com/couchbase/sync_gateway/issues/1163) _bulk_get uses compression inefficiently
- [**#1179**](https://github.com/couchbase/sync_gateway/issues/1179) Compress WebSocket _changes messages
- [**#1423**](https://github.com/couchbase/sync_gateway/issues/1423) Performance degradation in distributed index testing post-access work
- [**#1503**](https://github.com/couchbase/sync_gateway/issues/1503) First-time sync optimized backfill mode

**Enhancements**

- [**#479**](https://github.com/couchbase/sync_gateway/issues/479) Revisit service scripts to handle custom installations and multiple sync_gateway instances
- [**#545**](https://github.com/couchbase/sync_gateway/issues/545) Sync Gateway doesn't work with _doc_ids filter / Can't sync individual docs
- [**#748**](https://github.com/couchbase/sync_gateway/issues/748) Enable taking a bucket offline/online
- [**#881**](https://github.com/couchbase/sync_gateway/issues/881) -bucket param doesn't work in conjunction with config file where bucket not specified
- [**#884**](https://github.com/couchbase/sync_gateway/issues/884) Tool to collect sync gateway debugging info
- [**#899**](https://github.com/couchbase/sync_gateway/issues/899) Pass old current revision to 'document_changed' filter function
- [**#908**](https://github.com/couchbase/sync_gateway/issues/908) Allow an Admin to take a DB Offline
- [**#909**](https://github.com/couchbase/sync_gateway/issues/909) Allow Admin to take an Offline DB Online
- [**#910**](https://github.com/couchbase/sync_gateway/issues/910) Update _resync to use bucket online/offline
- [**#922**](https://github.com/couchbase/sync_gateway/issues/922) Channel Index - Feed Partitioning
- [**#923**](https://github.com/couchbase/sync_gateway/issues/923) Channel Index - Index Writes
- [**#925**](https://github.com/couchbase/sync_gateway/issues/925) Channel Index - Index Reads
- [**#948**](https://github.com/couchbase/sync_gateway/issues/948) SG as a service is not supported on Windows
- [**#969**](https://github.com/couchbase/sync_gateway/issues/969) Handle DCP stream end/reconnection
- [**#993**](https://github.com/couchbase/sync_gateway/issues/993) Channel Index - User and Role notification
- [**#1012**](https://github.com/couchbase/sync_gateway/issues/1012) Put bucket in offline mode for n seconds
- [**#1013**](https://github.com/couchbase/sync_gateway/issues/1013) Automatically put bucket in offline mode when lose TAP feed
- [**#1022**](https://github.com/couchbase/sync_gateway/issues/1022) Run the service installer during package installation on Linux
- [**#1065**](https://github.com/couchbase/sync_gateway/issues/1065) Managing hashed vector clock sequences
- [**#1066**](https://github.com/couchbase/sync_gateway/issues/1066) Refactoring changes feed processing to support clock-based sequences
- [**#1072**](https://github.com/couchbase/sync_gateway/issues/1072) Distributed index: deal with SG nodes going down
- [**#1073**](https://github.com/couchbase/sync_gateway/issues/1073) Distributed index: Only open single vbucket stream for cfg document
- [**#1075**](https://github.com/couchbase/sync_gateway/issues/1075) CBGT: Dead node detection autofailover
- [**#1084**](https://github.com/couchbase/sync_gateway/issues/1084) Channel backfill when using vector clock sequence
- [**#1087**](https://github.com/couchbase/sync_gateway/issues/1087) CBGT: Single manager per SG instance
- [**#1117**](https://github.com/couchbase/sync_gateway/issues/1117) Emit vbucket sequences from access views
- [**#1140**](https://github.com/couchbase/sync_gateway/issues/1140) [Distributed Index] Fix kvChangeIndex DocChanged() throughput bottleneck
- [**#1163**](https://github.com/couchbase/sync_gateway/issues/1163) _bulk_get uses compression inefficiently
- [**#1176**](https://github.com/couchbase/sync_gateway/issues/1176) Add WebHook notifications for bucket online/offline
- [**#1179**](https://github.com/couchbase/sync_gateway/issues/1179) Compress WebSocket _changes messages
- [**#1205**](https://github.com/couchbase/sync_gateway/issues/1205) Use bulk gocb operation for GetBulkRaw 
- [**#1208**](https://github.com/couchbase/sync_gateway/issues/1208) Avoid unnecessary channel clock retrieval 
- [**#1209**](https://github.com/couchbase/sync_gateway/issues/1209) Separate out `Server` header's functional version number from binary build number
- [**#1219**](https://github.com/couchbase/sync_gateway/issues/1219) Can't purge documents (_purge is not implemented)
- [**#1243**](https://github.com/couchbase/sync_gateway/issues/1243) Shard clocks to avoid write bottlenecks
- [**#1247**](https://github.com/couchbase/sync_gateway/issues/1247) Use single gocb BulkOp (BulkSet) for concurrent index writes
- [**#1298**](https://github.com/couchbase/sync_gateway/issues/1298) [Distributed Index] sync_gateway panic when starting without feed_type.num_shards
- [**#1321**](https://github.com/couchbase/sync_gateway/issues/1321) Consolidate feed_params and channel_index in config
- [**#1340**](https://github.com/couchbase/sync_gateway/issues/1340) Change log path used in RPM
- [**#1342**](https://github.com/couchbase/sync_gateway/issues/1342) Change config file path used in RPM
- [**#1349**](https://github.com/couchbase/sync_gateway/issues/1349) Integrate Windows service wrapper into installer
- [**#1479**](https://github.com/couchbase/sync_gateway/issues/1479) Support style=all_docs calls to _changes with a _doc_ids filter
- [**#1494**](https://github.com/couchbase/sync_gateway/issues/1494) Enable REST retrieval of a running SG config
- [**#1503**](https://github.com/couchbase/sync_gateway/issues/1503) First-time sync optimized backfill mode

**Bugs**

- [**#520**](https://github.com/couchbase/sync_gateway/issues/520) Fail to warn when sync_gateway user does not exist
- [**#787**](https://github.com/couchbase/sync_gateway/issues/787) RequireAccess throws even though user has access to "*"
- [**#792**](https://github.com/couchbase/sync_gateway/issues/792) Windows: MaxFileDescriptors console warning
- [**#807**](https://github.com/couchbase/sync_gateway/issues/807) Tests with large revs: http: panic serving [::1]:59607: can't find rev:
- [**#870**](https://github.com/couchbase/sync_gateway/issues/870) Documents missing when requesting _changes in SyncGateway
- [**#874**](https://github.com/couchbase/sync_gateway/issues/874) Sync Gateway sometimes returns incorrect last_seq
- [**#911**](https://github.com/couchbase/sync_gateway/issues/911) Detection of lost TAP feed impacting service availability
- [**#943**](https://github.com/couchbase/sync_gateway/issues/943) Some example JSON configs include non-UTF8 chars
- [**#959**](https://github.com/couchbase/sync_gateway/issues/959) Sync Gateway bucket shadowing crashes with error 'panic: parent id "xxx-xxxx" is missing'
- [**#976**](https://github.com/couchbase/sync_gateway/issues/976) Http: panic serving runtime error: index out of range on Sync Gateway 1.1 on Ubuntu 12.04.5 x86_64 cause sync failed
- [**#991**](https://github.com/couchbase/sync_gateway/issues/991) Panic if Origin header sent in request with no SG config
- [**#1007**](https://github.com/couchbase/sync_gateway/issues/1007) Large revs with no common parent. Panic serving, can't find rev
- [**#1033**](https://github.com/couchbase/sync_gateway/issues/1033) SG Panics if _bulk_get is passed empty JSON object
- [**#1049**](https://github.com/couchbase/sync_gateway/issues/1049) Session disappears immediately with large TTL
- [**#1072**](https://github.com/couchbase/sync_gateway/issues/1072) Distributed index: deal with SG nodes going down
- [**#1083**](https://github.com/couchbase/sync_gateway/issues/1083) MaxFileDescriptors setting shouldn't reduce the system defined values
- [**#1093**](https://github.com/couchbase/sync_gateway/issues/1093) Panic in (*DatabaseContext).getChangesInChannelFromView
- [**#1100**](https://github.com/couchbase/sync_gateway/issues/1100) [distributed_index] should we support old config format/settings for SG
- [**#1111**](https://github.com/couchbase/sync_gateway/issues/1111) [distributed_index] startup SG crash in sequence_clock 
- [**#1153**](https://github.com/couchbase/sync_gateway/issues/1153) SG can't be installed as a service on Couchbase SG AMI
- [**#1174**](https://github.com/couchbase/sync_gateway/issues/1174) LastPolled retrieval not working during performance testing
- [**#1200**](https://github.com/couchbase/sync_gateway/issues/1200) GET _design fails with "Internal error: http: read on closed response body"
- [**#1204**](https://github.com/couchbase/sync_gateway/issues/1204) Create sysv-init script for CentOS 5
- [**#1213**](https://github.com/couchbase/sync_gateway/issues/1213) Changes feed for \* channel missing entries
- [**#1230**](https://github.com/couchbase/sync_gateway/issues/1230) [distributed index] Empty channels trigger redundant clock lookups
- [**#1245**](https://github.com/couchbase/sync_gateway/issues/1245) Distributed-index changes feed requests has high latency as compared with old sync gateway
- [**#1248**](https://github.com/couchbase/sync_gateway/issues/1248) Duplicates in _changes feed with distributed index with multiple users and multiple channels
- [**#1253**](https://github.com/couchbase/sync_gateway/issues/1253) Gocb retry logic: _changes intermittently returning 0 results for distributed index 
- [**#1259**](https://github.com/couchbase/sync_gateway/issues/1259) Cbheartbeat start delay causes DCP stream to not be re-sharded when SG node killed quickly
- [**#1260**](https://github.com/couchbase/sync_gateway/issues/1260) Race condition in sequence hasher cache
- [**#1262**](https://github.com/couchbase/sync_gateway/issues/1262) Changes feed not returning the latest revision for few docs
- [**#1279**](https://github.com/couchbase/sync_gateway/issues/1279) [Distributed Index] Intermittent panic during start up
- [**#1281**](https://github.com/couchbase/sync_gateway/issues/1281) ConfigServer option and backticks for the sync function break
- [**#1286**](https://github.com/couchbase/sync_gateway/issues/1286) Removing a node from CB-cluster and rebalance causing writer SG to crash
- [**#1289**](https://github.com/couchbase/sync_gateway/issues/1289) Recover from gocb timeouts and queue overflow
- [**#1298**](https://github.com/couchbase/sync_gateway/issues/1298) [Distributed Index] sync_gateway panic when starting without feed_type.num_shards
- [**#1299**](https://github.com/couchbase/sync_gateway/issues/1299) [Distributed Index] Stale pindex files can cause sync_gateway to launch in an incorrect state
- [**#1305**](https://github.com/couchbase/sync_gateway/issues/1305) Getting error "Failed to establish a new connection" with Sync gateway when increased the throughput
- [**#1307**](https://github.com/couchbase/sync_gateway/issues/1307) [Distributed Index] Roles not assigning channels to users correctly
- [**#1309**](https://github.com/couchbase/sync_gateway/issues/1309) Sync_gateway is going in loop when client is asking for changes.
- [**#1317**](https://github.com/couchbase/sync_gateway/issues/1317) Non-writer node of SG crashes when launched with other index writer node sync gateways
- [**#1321**](https://github.com/couchbase/sync_gateway/issues/1321) Consolidate feed_params and channel_index in config
- [**#1329**](https://github.com/couchbase/sync_gateway/issues/1329) ChangeWaiters failing to release when changes feed closed
- [**#1336**](https://github.com/couchbase/sync_gateway/issues/1336) [DB Online / Offline] sync_gateway fails to launch intermittently because it is not yet online
- [**#1339**](https://github.com/couchbase/sync_gateway/issues/1339) Sharded clock cas writes don't retry on cas failure
- [**#1345**](https://github.com/couchbase/sync_gateway/issues/1345) Set-Cookie response header for SyncGatewaySession should contain path value with /{db}
- [**#1377**](https://github.com/couchbase/sync_gateway/issues/1377) [DB Online / Offline] - db not returning expected error codes after losing TAP feed and going offline
- [**#1379**](https://github.com/couchbase/sync_gateway/issues/1379) [Distributed Index]  _changes feed return incomplete response with invalid entries
- [**#1389**](https://github.com/couchbase/sync_gateway/issues/1389) Sync gateway not emitting webhook event when going to offline state
- [**#1391**](https://github.com/couchbase/sync_gateway/issues/1391) [Distributed Index] Writer memory continually growing during perf tests
- [**#1392**](https://github.com/couchbase/sync_gateway/issues/1392) [Distributed Index] Index writers intermittantly fail to register with CBGT
- [**#1405**](https://github.com/couchbase/sync_gateway/issues/1405) Index writer panics under heavy load
- [**#1419**](https://github.com/couchbase/sync_gateway/issues/1419) Use legacy compression for non-CBL 1.2 user agents
- [**#1423**](https://github.com/couchbase/sync_gateway/issues/1423) Performance degradation in distributed index testing post-access work
- [**#1434**](https://github.com/couchbase/sync_gateway/issues/1434) Sync_gateway not generating webhook event when bucket is deleted 
- [**#1440**](https://github.com/couchbase/sync_gateway/issues/1440) [Distributed Index] Intermittent empty results in continuous changes feed
- [**#1465**](https://github.com/couchbase/sync_gateway/issues/1465) [Distributed Index] Empty doc returned to continuous _changes feed - bulk set issue
- [**#1489**](https://github.com/couchbase/sync_gateway/issues/1489) Client passing -H "Accept-Encoding: gzip" to changes breaks CloseNotifier
- [**#1493**](https://github.com/couchbase/sync_gateway/issues/1493) Pass-thru view query is failing via admin api on view created with SG 1.1.1
- [**#1524**](https://github.com/couchbase/sync_gateway/issues/1524) TodoLite list wasn't correctly shared / deleted tasks didn't propagate using SG DI (pre test-fest)
- [**#1556**](https://github.com/couchbase/sync_gateway/issues/1556) Views failing if document indexed more than once in a design

**Known Issues**

- [**#422**](https://github.com/couchbase/sync_gateway/issues/422) Replication ordering dependencies can cause sync fn to reject updates
- [**#1264**](https://github.com/couchbase/sync_gateway/issues/1264) Sync Gateway memory usage climbs continously
- [**#1316**](https://github.com/couchbase/sync_gateway/issues/1316) Support _doc_ids filter when using distributed index
- [**#1371**](https://github.com/couchbase/sync_gateway/issues/1371) Not storing OpaqueSet values causes Sync Gateway panic during CBGT reshard
- [**#1382**](https://github.com/couchbase/sync_gateway/issues/1382) Resync operation only supported in offline state
- [**#1527**](https://github.com/couchbase/sync_gateway/issues/1527) Inbound REST calls which reset can prevent offline from draining
- [**#1536**](https://github.com/couchbase/sync_gateway/issues/1536) Improve logging when using sg_accel with non-writer config

## 1.1.1 release

**Enhancements**

- [**#945**](https://github.com/couchbase/sync_gateway/issues/945) Set no-caching headers on _changes HTTP response
- [**#942**](https://github.com/couchbase/sync_gateway/issues/942) Support an array of URLs for the "server" key in config JSON
- [**#904**](https://github.com/couchbase/sync_gateway/issues/904) Support for max heartbeat in Sync Gateway

**Bugs**

- [**#1027**](https://github.com/couchbase/sync_gateway/issues/1027) SG panics if _bulk_docs is passed empty JSON object
- [**#1011**](https://github.com/couchbase/sync_gateway/issues/1011) Uptake BucketUpdater for upgrade, stability
- [**#995**](https://github.com/couchbase/sync_gateway/issues/995) Error in sync function example: use of throw
- [**#986**](https://github.com/couchbase/sync_gateway/issues/986) Improve failure handling during invalidateChannels
- [**#936**](https://github.com/couchbase/sync_gateway/issues/936) High memory usage during push replication
- [**#916**](https://github.com/couchbase/sync_gateway/issues/916) _changes feed with "longpoll" and "since" sometimes returns empty results
- [**#895**](https://github.com/couchbase/sync_gateway/issues/895) Non int last_seq id in _changes request fails
- [**#768**](https://github.com/couchbase/sync_gateway/issues/768) Load balancer behavior results in high SG memory utilization

## 1.1.0 release

Sync Gateway 1.1 packs in a number of significant enhancements, including:

- **A new integration mechanism: Webhooks**. With this release, we are beginning to expose an event model to which you can add handlers. This makes it even easier to integrate Couchbase Mobile with line of business applications, 3rd party services and apps, etc.
- **Friendlier default configuration**. Now when you run Sync Gateway without providing any configuration options, the Guest user will be enabled and will have access to all documents. The trade off, for security reasons, is that Sync Gateway will default to listening on the local loopback interface only.
- **Production certification for Couchbase 3.1**, and non-production certification for using 4.0 (Beta 1). Sync Gateway users are encouraged to upgrade to 3.1 in order to take advantage of all the great improvements since the 2.5.2 release.

**Performance**

- [**#440**](https://github.com/couchbase/sync_gateway/issues/440) _all_docs still slow
- [**#409**](https://github.com/couchbase/sync_gateway/issues/409) Update sync gateway to better support CBS 3.0 view semantics

**Enhancements**

- [**#859**](https://github.com/couchbase/sync_gateway/issues/859) Uptake TCP keep-alive support for go-couchbase
- [**#763**](https://github.com/couchbase/sync_gateway/issues/763) Improve view creation by Sync Gateway
- [**#708**](https://github.com/couchbase/sync_gateway/issues/708) Insecure mode on default sync_gateway bucket
- [**#482**](https://github.com/couchbase/sync_gateway/issues/482) Sync Gateway web hooks
- [**#457**](https://github.com/couchbase/sync_gateway/issues/457) Add additional platform support for service installation scripts
- [**#404**](https://github.com/couchbase/sync_gateway/issues/404) Moving from TAP to DCP

**Bugs**

- [**#880**](https://github.com/couchbase/sync_gateway/issues/880) Changes feed fails to backfill channel under heavy access() load
- [**#878**](https://github.com/couchbase/sync_gateway/issues/878) sg doesn't properly handle config files with buckets '%' in the name
- [**#852**](https://github.com/couchbase/sync_gateway/issues/852) webhooks events can't POST for HTTPS servers using self-signed cert
- [**#850**](https://github.com/couchbase/sync_gateway/issues/850) Logging doesn't always use the same unit
- [**#847**](https://github.com/couchbase/sync_gateway/issues/847) Installing sync gateway service fails
- [**#821**](https://github.com/couchbase/sync_gateway/issues/821) Session API does not honor the password parameter
- [**#812**](https://github.com/couchbase/sync_gateway/issues/812) webhooks: Not all events are getting POSTed
- [**#811**](https://github.com/couchbase/sync_gateway/issues/811) webhook: Not all revision ids are sent with webhook events.
- [**#810**](https://github.com/couchbase/sync_gateway/issues/810) Sync Gateway crashes while processing webhook events
- [**#809**](https://github.com/couchbase/sync_gateway/issues/809) Sync Gateway crashes while processing the changes feed
- [**#808**](https://github.com/couchbase/sync_gateway/issues/808) The revision Id passed in the Etag header should be enclosed in quotes
- [**#783**](https://github.com/couchbase/sync_gateway/issues/783) Windows line breaks in sync function cause SG to fail
- [**#775**](https://github.com/couchbase/sync_gateway/issues/775) SG handling for mutations deduplicated by Couchbase feed
- [**#762**](https://github.com/couchbase/sync_gateway/issues/762) configurable CORS on login resources
- [**#745**](https://github.com/couchbase/sync_gateway/issues/745) Ignores heartbeat parameter in _changes POST request
- [**#691**](https://github.com/couchbase/sync_gateway/issues/691) Bucket name with percent symbol is not handled correctly in config file
- [**#687**](https://github.com/couchbase/sync_gateway/issues/687) Windows: Pull replication doesn't work on :4984 (no documents or changes returned)
- [**#679**](https://github.com/couchbase/sync_gateway/issues/679) Webhook does not give warning or error when http server delay response pass the timeout value
- [**#661**](https://github.com/couchbase/sync_gateway/issues/661) Webhook filter with invalid event type or event handler does not result in error or warning to users
- [**#653**](https://github.com/couchbase/sync_gateway/issues/653) Sync Gateway not starting first time
- [**#628**](https://github.com/couchbase/sync_gateway/issues/628) DCP events not appearing on changes feed
- [**#621**](https://github.com/couchbase/sync_gateway/issues/621) Changes Feed repeats all the changes when a change is made
- [**#563**](https://github.com/couchbase/sync_gateway/issues/563) SG service installation, when using --runas, update all paths that point to user home
- [**#562**](https://github.com/couchbase/sync_gateway/issues/562) PUT /db should not return 405; causes client replicator to fail
- [**#544**](https://github.com/couchbase/sync_gateway/issues/544) Sync_gateway service installation result in two data directories when there is an inactive service
- [**#535**](https://github.com/couchbase/sync_gateway/issues/535) sync_gateway_service_install.sh should explicitly state that command-line arguments require an '=' before the value
- [**#530**](https://github.com/couchbase/sync_gateway/issues/530) Some of the service install script parameters should be removed
- [**#525**](https://github.com/couchbase/sync_gateway/issues/525) SG TAP timeout issue
- [**#521**](https://github.com/couchbase/sync_gateway/issues/521) Fail to start sync_gateway service
- [**#513**](https://github.com/couchbase/sync_gateway/issues/513) When stopping Sync_gateway service on Centos 6 process is left running
- [**#501**](https://github.com/couchbase/sync_gateway/issues/501) Revision pruning isn't effective when history includes conflicts (even when tombstoned)
- [**#491**](https://github.com/couchbase/sync_gateway/issues/491) Items in SG channel not reflected in change feed.

## Where to get it

You can download this release from the [downloads page](http://www.couchbase.com/nosql-databases/downloads#couchbase-mobile).