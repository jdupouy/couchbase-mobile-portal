---
id: ios-release-notes
title: iOS release notes
---

## 1.4

__API change__

- An `isDeletion` property is now available on the `DatabaseChange` object to identify if a change is tombstone document.

__Performance Improvements__

- [__#1389__](https://github.com/couchbase/couchbase-lite-ios/issues/1389) Allow SQLite reads concurrently with writer
- [__#1497__](https://github.com/couchbase/couchbase-lite-ios/issues/1497) Update ForestDB to get improved compaction / space reuse

__Enhancements__

- [__#1538__](https://github.com/couchbase/couchbase-lite-ios/issues/1538) Make CBLDatabaseChange.isDeletion public?

__Bugs__

- [__#794__](https://github.com/couchbase/couchbase-lite-ios/issues/794) "!_changeTracker" assertion failure in -[CBLRestPuller startChangeTracker]
- [__#1207__](https://github.com/couchbase/couchbase-lite-ios/issues/1207) Push replication stops with error `400 bad_request`
- [__#1243__](https://github.com/couchbase/couchbase-lite-ios/issues/1243) Replication task missing source or target values
- [__#1285__](https://github.com/couchbase/couchbase-lite-ios/issues/1285) REST API does not allow GET on a db with "/" in its name
- [__#1343__](https://github.com/couchbase/couchbase-lite-ios/issues/1343) Need to close all other db handles before rekeying
- [__#1365__](https://github.com/couchbase/couchbase-lite-ios/issues/1365) Non-continuous push replication gets stuck in kCBLReplicationIdle status
- [__#1422__](https://github.com/couchbase/couchbase-lite-ios/issues/1422) ForestDB crashes frequently in the background because of protection data level
- [__#1429__](https://github.com/couchbase/couchbase-lite-ios/issues/1429) 1.3.1-6: crashed EXC_BAD_ACCESS KERN_INVALID_ADDRESS 0x0000000000000000
- [__#1442__](https://github.com/couchbase/couchbase-lite-ios/issues/1442) Collection class properties not propagating from CBLDocument to CBLModel after sync
- [__#1443__](https://github.com/couchbase/couchbase-lite-ios/issues/1443) Handle iOS file protection gracefully when in background
- [__#1461__](https://github.com/couchbase/couchbase-lite-ios/issues/1461) ForestDB: Assertion failure in -[MYBackgroundMonitor beginBackgroundTaskNamed:]() MYBackgroundMonitor.m:66
- [__#1467__](https://github.com/couchbase/couchbase-lite-ios/issues/1467) Memory leak caused by ref cycle between replicator and CBLRemoteSession
- [__#1556__](https://github.com/couchbase/couchbase-lite-ios/issues/1556) Assertion failed: (_changesTimeout > 0)
- [__#1557__](https://github.com/couchbase/couchbase-lite-ios/issues/1557) Exception caught in CBLDatabase transaction
- [__#1558__](https://github.com/couchbase/couchbase-lite-ios/issues/1558) Not all updates propagating while under load
- [__#1568__](https://github.com/couchbase/couchbase-lite-ios/issues/1568) Attachments failing to push after delete / create (ForestDB)
- [__#1579__](https://github.com/couchbase/couchbase-lite-ios/issues/1579) [NSLock lock]: deadlock when deleting database (ForestDB)
- [__#1580__](https://github.com/couchbase/couchbase-lite-ios/issues/1580) Wrong "reason" response for GET on purged documents
- [__#1621__](https://github.com/couchbase/couchbase-lite-ios/issues/1621) OIDC failing with Grocery Sync when creating new google project

__Deprecation notices__

The following features are being deprecated in Couchbase Mobile 1.4 and will be unsupported in 2.0.

- ForestDB
- Geo queries

The following platforms are being deprecated in Couchbase Mobile 1.4 and will be unsupported in 2.0.

- iOS 8

## Where to get it

You can download this release from the [downloads page](http://www.couchbase.com/nosql-databases/downloads#couchbase-mobile).

## 1.3.1

**Performance Improvements**

- [**#1379**](https://github.com/couchbase/couchbase-lite-ios/issues/1379) ForestDB update_seq on view query less than db's update_seq

**Enhancements**

- [**#1400**](https://github.com/couchbase/couchbase-lite-ios/issues/1400) Support for _oidc_refresh response without ID token

**Bugs**

- [**#1369**](https://github.com/couchbase/couchbase-lite-ios/issues/1369) PSWebSocket crash iOS 10
- [**#1379**](https://github.com/couchbase/couchbase-lite-ios/issues/1379) ForestDB update_seq on view query less than db's update_seq
- [**#1387**](https://github.com/couchbase/couchbase-lite-ios/issues/1387) TvOS Unit Test Build has a lot of warnings
- [**#1392**](https://github.com/couchbase/couchbase-lite-ios/issues/1392) When OIDC Refresh token failed, there is no replication change notification sent.
- [**#1403**](https://github.com/couchbase/couchbase-lite-ios/issues/1403) CBLSocketChangeTracker endless loop of JSON Parsing Errors
- [**#1406**](https://github.com/couchbase/couchbase-lite-ios/issues/1406) Encryption is a no-op with the system libsqlite3 on macOS 12 

### Where to get it

You can download this release from [Couchbase.com](http://www.couchbase.com/nosql-databases/downloads#Couchbase_Mobile)

## 1.3

**Performance Improvements**

- [**#1114**](https://github.com/couchbase/couchbase-lite-ios/issues/1114) LiveQuery shouldn't re-run query if view index didn't change
- [**#1150**](https://github.com/couchbase/couchbase-lite-ios/issues/1150) Optimize & animate CBLUITableController by using the Levenshtein algorithm
- [**#1165**](https://github.com/couchbase/couchbase-lite-ios/issues/1165) Incrementally purge oldest revisions in SQLite databases
- [**#1242**](https://github.com/couchbase/couchbase-lite-ios/issues/1242) Fix inefficiencies replicating docs with many revisions
- [**#1340**](https://github.com/couchbase/couchbase-lite-ios/issues/1340) Optimized multipart download performance

**Enhancements**

- [**#394**](https://github.com/couchbase/couchbase-lite-ios/issues/394) Start using NSURLSession in the replicator
- [**#984**](https://github.com/couchbase/couchbase-lite-ios/issues/984) Comparing CBLQuery objects
- [**#1100**](https://github.com/couchbase/couchbase-lite-ios/issues/1100) External property on kCBLDatabaseChangeNotification when CBL is remote
- [**#1107**](https://github.com/couchbase/couchbase-lite-ios/issues/1107) Logging overhaul
- [**#1117**](https://github.com/couchbase/couchbase-lite-ios/issues/1117) Redact passwords/tokens in URLs in log messages
- [**#1118**](https://github.com/couchbase/couchbase-lite-ios/issues/1118) API: Public method for inserting existing revisions (putExistingRevisionWithProperties:...)
- [**#1148**](https://github.com/couchbase/couchbase-lite-ios/issues/1148) API: Make -[View updateIndex] public; add async version
- [**#1150**](https://github.com/couchbase/couchbase-lite-ios/issues/1150) Optimize & animate CBLUITableController by using the Levenshtein algorithm
- [**#1165**](https://github.com/couchbase/couchbase-lite-ios/issues/1165) Incrementally purge oldest revisions in SQLite databases
- [**#1181**](https://github.com/couchbase/couchbase-lite-ios/issues/1181) API: Document expiration time (TTL)
- [**#1201**](https://github.com/couchbase/couchbase-lite-ios/issues/1201) Replicator should immediately fail if URL path is invalid
- [**#1245**](https://github.com/couchbase/couchbase-lite-ios/issues/1245) Expose server error messages in NSErrors from public API
- [**#1266**](https://github.com/couchbase/couchbase-lite-ios/issues/1266) OpenID Connect authenticator
- [**#1271**](https://github.com/couchbase/couchbase-lite-ios/issues/1271) Disable App Transport Security on Mac OSX LiteServ
- [**#1291**](https://github.com/couchbase/couchbase-lite-ios/issues/1291) Allow configuring revs_limit in LiteServ
- [**#1334**](https://github.com/couchbase/couchbase-lite-ios/issues/1334) Scope cookie storage by database, not by replication

**Bugs**

- [**#641**](https://github.com/couchbase/couchbase-lite-ios/issues/641) Enumerate sequence in descending order in CBForest not working
- [**#966**](https://github.com/couchbase/couchbase-lite-ios/issues/966) CBLIS : Data loss
- [**#1005**](https://github.com/couchbase/couchbase-lite-ios/issues/1005) Replication fails without starting on wifi if network depends on a proxy
- [**#1015**](https://github.com/couchbase/couchbase-lite-ios/issues/1015) Crash when [CBLRemoteRequest connection:didFailWithError:]
- [**#1045**](https://github.com/couchbase/couchbase-lite-ios/issues/1045) POST _bulk_docs does not support HTTPBodyStream
- [**#1071**](https://github.com/couchbase/couchbase-lite-ios/issues/1071) [Testfest] Items not showing up in offline mode
- [**#1085**](https://github.com/couchbase/couchbase-lite-ios/issues/1085) CBLIS : NSIncrementalStore accessed by multiple context dispatch queues
- [**#1095**](https://github.com/couchbase/couchbase-lite-ios/issues/1095) Obsolete rows left in view index when documentType is used (1.1.1)
- [**#1106**](https://github.com/couchbase/couchbase-lite-ios/issues/1106) CBLListener readOnly property prevents pulls from updating the database
- [**#1120**](https://github.com/couchbase/couchbase-lite-ios/issues/1120) Warn if map function calls emit(nil, ...)
- [**#1124**](https://github.com/couchbase/couchbase-lite-ios/issues/1124) Multipart Uploader cannot upload the attachment when using basic auth
- [**#1128**](https://github.com/couchbase/couchbase-lite-ios/issues/1128) Crash pushing docs with non-downloaded attachments
- [**#1129**](https://github.com/couchbase/couchbase-lite-ios/issues/1129) CBLIS: NSSet was mutated while being enumerated.
- [**#1131**](https://github.com/couchbase/couchbase-lite-ios/issues/1131) CBLVersion() incorrectly returns "(unofficial)" in official releases
- [**#1132**](https://github.com/couchbase/couchbase-lite-ios/issues/1132) CBLReplicator.isDocumentPending is inaccurate when replicator is offline
- [**#1138**](https://github.com/couchbase/couchbase-lite-ios/issues/1138) Continuous puller with WebSocket not responding with 401 error when changing password
- [**#1139**](https://github.com/couchbase/couchbase-lite-ios/issues/1139) ChangeTracker POST request are incompatible with CouchDB
- [**#1143**](https://github.com/couchbase/couchbase-lite-ios/issues/1143) Swift API glitches
- [**#1152**](https://github.com/couchbase/couchbase-lite-ios/issues/1152) CBLRestReplicator does not properly end bgTask when app is foregrounded
- [**#1163**](https://github.com/couchbase/couchbase-lite-ios/issues/1163) Fixed macOS 10.10 dependency & updated deployment version to 10.9
- [**#1180**](https://github.com/couchbase/couchbase-lite-ios/issues/1180) Doc can be saved with missing attachment file, leading to errors
- [**#1188**](https://github.com/couchbase/couchbase-lite-ios/issues/1188) CBForest bad memory access while purging doc
- [**#1191**](https://github.com/couchbase/couchbase-lite-ios/issues/1191) Liteserv crashes with Forestdb option when creating local docs after delete operation
- [**#1192**](https://github.com/couchbase/couchbase-lite-ios/issues/1192) Manual compaction returns error if auto-compact is already running
- [**#1200**](https://github.com/couchbase/couchbase-lite-ios/issues/1200) Replication rejects attachments generated by PouchDB with revpos:0
- [**#1216**](https://github.com/couchbase/couchbase-lite-ios/issues/1216) REST API: POST /_replicate can start/stop once, but not restart?
- [**#1228**](https://github.com/couchbase/couchbase-lite-ios/issues/1228) One-shot push from empty db never stops
- [**#1233**](https://github.com/couchbase/couchbase-lite-ios/issues/1233) Failure to encrypt SQLite database when using WAL journaling
- [**#1260**](https://github.com/couchbase/couchbase-lite-ios/issues/1260) Inconsistent response when no conflicts are present and ?conflicts=true
- [**#1263**](https://github.com/couchbase/couchbase-lite-ios/issues/1263) Incorrect "error" property in REST response for GET of deleted doc
- [**#1274**](https://github.com/couchbase/couchbase-lite-ios/issues/1274) PendingDocumentIDs is incorrect
- [**#1279**](https://github.com/couchbase/couchbase-lite-ios/issues/1279) Don't stop replicator if one doc gets an error
- [**#1292**](https://github.com/couchbase/couchbase-lite-ios/issues/1292) _replicate between 2 dbs on same LiteServ fails
- [**#1323**](https://github.com/couchbase/couchbase-lite-ios/issues/1323) Cannot push encrypted attachments when testing with ToDoLite
- [**#1325**](https://github.com/couchbase/couchbase-lite-ios/issues/1325) LiteServ crash when delete dbs asyncronously
- [**#1327**](https://github.com/couchbase/couchbase-lite-ios/issues/1327) Archive build is missing symbols in iOS frameworks
- [**#1335**](https://github.com/couchbase/couchbase-lite-ios/issues/1335) Database upgrades from 1.1 not copying "content_type" of attachments
- [**#1348**](https://github.com/couchbase/couchbase-lite-ios/issues/1348) OIDC tokens in Keychain should be per-database
- [**#1362**](https://github.com/couchbase/couchbase-lite-ios/issues/1362) App crashing on iOS 8.3 device
- [**#1370**](https://github.com/couchbase/couchbase-lite-ios/issues/1370) TodoLite showing wrong list when deleting tasks

### Where to get it

You can download this release from [Couchbase.com](http://www.couchbase.com/nosql-databases/downloads#Couchbase_Mobile)