---
id: java-release-notes
title: Java release notes
---

## 1.4

__API change__

- An `isDeletion` property is now available on the `DatabaseChange` object to identify if a change is tombstone document.

__Enhancements__

- [__#1087__](https://github.com/couchbase/couchbase-lite-java-core/issues/1087) LiteServ app for Java
- [__#1543__](https://github.com/couchbase/couchbase-lite-java-core/issues/1543) Make CBLDatabaseChange.isDeletion public?
- [__#1554__](https://github.com/couchbase/couchbase-lite-java-core/issues/1554) 1.0.2d is being rejected by Google Play

__Bugs__

- [__#911__](https://github.com/couchbase/couchbase-lite-java-core/issues/911) Multiple duplicate replication change events sent in pull replication
- [__#1334__](https://github.com/couchbase/couchbase-lite-java-core/issues/1334) Change tracker stopped during continuous replication error thrown when cookie expires
- [__#1385__](https://github.com/couchbase/couchbase-lite-java-core/issues/1385) CBLReplicatorExecutor still exists after stopping the replicator
- [__#1470__](https://github.com/couchbase/couchbase-lite-java-core/issues/1470) IOS pull replication from Android
- [__#1471__](https://github.com/couchbase/couchbase-lite-java-core/issues/1471) Attachments failed to replicate when deleted and recreated
- [__#1481__](https://github.com/couchbase/couchbase-lite-java-core/issues/1481) ConnectionError: ('Connection aborted.', error(54, 'Connection reset by peer'))
- [__#1493__](https://github.com/couchbase/couchbase-lite-java-core/issues/1493) Test failure ViewsTest.failingTestAllDocumentsLiveQuery on Jenkins
- [__#1495__](https://github.com/couchbase/couchbase-lite-java-core/issues/1495) Changes feed skipping changes on rapid long poll
- [__#1498__](https://github.com/couchbase/couchbase-lite-java-core/issues/1498) Was not able to delete the database directory, Status: 500 (HTTP 500 Internal Server Error)
- [__#1510__](https://github.com/couchbase/couchbase-lite-java-core/issues/1510) Mixing HashMap and TreeMap for properties in Document. HashMap allows to generate non-canonical JSON.
- [__#1534__](https://github.com/couchbase/couchbase-lite-java-core/issues/1534) Push Replication Fails With createTarget Set
- [__#1535__](https://github.com/couchbase/couchbase-lite-java-core/issues/1535) ForestDB Views Issue :Router: Router unable to route request to do_GET_DesignDocument(java.lang.NullPointerException)
- [__#1539__](https://github.com/couchbase/couchbase-lite-java-core/issues/1539) Small load - ConnectionError: ('Connection aborted.', error(54, 'Connection reset by peer'))
- [__#1540__](https://github.com/couchbase/couchbase-lite-java-core/issues/1540) _replicate REST API with one-shot returns immediately.
- [__#1549__](https://github.com/couchbase/couchbase-lite-java-core/issues/1549) 1.4-12 ConnectionError: ('Connection aborted.', error(54, 'Connection reset by peer')) during doc add
- [__#1550__](https://github.com/couchbase/couchbase-lite-java-core/issues/1550) Test Failure: testAndroid2MLimit
- [__#1551__](https://github.com/couchbase/couchbase-lite-java-core/issues/1551) Test failure: testMultipleLiveQueries
- [__#1552__](https://github.com/couchbase/couchbase-lite-java-core/issues/1552) P2P fails between android and macosx
- [__#1553__](https://github.com/couchbase/couchbase-lite-java-core/issues/1553) Test Failure: testGetDocumentWithLargeJSON
- [__#1557__](https://github.com/couchbase/couchbase-lite-java-core/issues/1557) List not syncing during test fest (Need to reproduce).
- [__#1558__](https://github.com/couchbase/couchbase-lite-java-core/issues/1558) Listener returning different error codes for negative tests 1.3.1 vs 1.4
- [__#1563__](https://github.com/couchbase/couchbase-lite-java-core/issues/1563) Database deletion failing with 1.4-25
- [__#1564__](https://github.com/couchbase/couchbase-lite-java-core/issues/1564) P2P sanity test failing
- [__#1575__](https://github.com/couchbase/couchbase-lite-java-core/issues/1575) SSL with allowSelfSignedSSLCertificates() method
- [__#1576__](https://github.com/couchbase/couchbase-lite-java-core/issues/1576) [Functional Test] Socket timeout when pushing docs to LiteServ
- [__#1578__](https://github.com/couchbase/couchbase-lite-java-core/issues/1578) Image attachment not sync'ing from .NET to Android
- [__#1581__](https://github.com/couchbase/couchbase-lite-java-core/issues/1581) Replication failures when running Sync Gateway in distributed index
- [__#1585__](https://github.com/couchbase/couchbase-lite-java-core/issues/1585) ForestDB + Encryption - SIGSEGV during database deletion
- [__#1588__](https://github.com/couchbase/couchbase-lite-java-core/issues/1588) Investigate test_verify_open_revs_with_revs_limit_push_conflict failure
- [__#1589__](https://github.com/couchbase/couchbase-lite-java-core/issues/1589) Investigate possible push replication issue
- [__#1590__](https://github.com/couchbase/couchbase-lite-java-core/issues/1590) Investigate failure at client.stop_replication()
- [__#1592__](https://github.com/couchbase/couchbase-lite-java-core/issues/1592) Find root cause of ConnectionError: ('Connection aborted.', error(54, 'Connection reset by peer'))
- [__#1593__](https://github.com/couchbase/couchbase-lite-java-core/issues/1593) Missing changes on changes feed (Mac <- Android) pull replication
- [__#1595__](https://github.com/couchbase/couchbase-lite-java-core/issues/1595) Database error with peer-2-peer-sanity test
- [__#1597__](https://github.com/couchbase/couchbase-lite-java-core/issues/1597) P2P - ForestDB Error: forceInsert()
- [__#1599__](https://github.com/couchbase/couchbase-lite-java-core/issues/1599) Updates not propagating to SQLite Client

__Deprecation notices__

The following features are being deprecated in Couchbase Mobile 1.4 and will be unsupported in 2.0.

- ForestDB

The following platforms are being deprecated in Couchbase Mobile 1.4 and will be unsupported in 2.0.

- Android API Level < 16 

## Where to get it

You can download this release from the [downloads page](http://www.couchbase.com/nosql-databases/downloads#couchbase-mobile).

## 1.3.1

**Enhancements**

- [**#1376**](https://github.com/couchbase/couchbase-lite-java-core/issues/1376) Implement `timeout` parameter for `_changes` REST API
- [**#1387**](https://github.com/couchbase/couchbase-lite-java-core/issues/1387) Support for _oidc_refresh response without ID token

**Bugs**

- [**#1296**](https://github.com/couchbase/couchbase-lite-java-core/issues/1296) Cordova - After putting Android app in background mode for a few hours, CB lite is unresponsive
- [**#1372**](https://github.com/couchbase/couchbase-lite-java-core/issues/1372) Router unable to route request to do_GET_DesignDocument (ForestDB)
- [**#1375**](https://github.com/couchbase/couchbase-lite-java-core/issues/1375) Reduce intermittently returns wrong results for 1.3.0-45
- [**#1379**](https://github.com/couchbase/couchbase-lite-java-core/issues/1379) MultipartDocumentReader: Attachment length cannot be parsed as Integer
- [**#1386**](https://github.com/couchbase/couchbase-lite-java-core/issues/1386) POST _replicate not create replicators when altering props beside type, target/source
- [**#1394**](https://github.com/couchbase/couchbase-lite-java-core/issues/1394) ViewsTest.testDeleteView() test failure
- [**#1399**](https://github.com/couchbase/couchbase-lite-java-core/issues/1399) Longpoll _changes on Listener does not respect timeout property

### Where to get it

You can download this release from [Couchbase.com](http://www.couchbase.com/nosql-databases/downloads#Couchbase_Mobile)

## 1.3

**Enhancements**

- [**#708**](https://github.com/couchbase/couchbase-lite-java-core/issues/708) Apache HTTP Client Removal/Deprecated in Android M.
- [**#820**](https://github.com/couchbase/couchbase-lite-java-core/issues/820) Filter out _removed revision from push replication
- [**#1054**](https://github.com/couchbase/couchbase-lite-java-core/issues/1054) Support POST /_changes in Listener
- [**#1057**](https://github.com/couchbase/couchbase-lite-java-core/issues/1057) Cbforest master branch version fails with many unit test (1.2.0-java -> master)
- [**#1097**](https://github.com/couchbase/couchbase-lite-java-core/issues/1097) After purging a doc, its rows are left behind in view indexes
- [**#1099**](https://github.com/couchbase/couchbase-lite-java-core/issues/1099) Docs in SQLite dbs never get pruned until entire db is compacted
- [**#1194**](https://github.com/couchbase/couchbase-lite-java-core/issues/1194) Fallback to GET when POST is not allowed to _changes
- [**#1207**](https://github.com/couchbase/couchbase-lite-java-core/issues/1207) TTL support
- [**#1222**](https://github.com/couchbase/couchbase-lite-java-core/issues/1222) Make SQLite one writer and one/multiple reader modes to avoid waiting connection.
- [**#1247**](https://github.com/couchbase/couchbase-lite-java-core/issues/1247) Add public API to add an existing revision (AKA new_edits=false, or -forceInsert:)
- [**#1255**](https://github.com/couchbase/couchbase-lite-java-core/issues/1255) Authenticator for OpenID Connect

**Bugs**

- [**#310**](https://github.com/couchbase/couchbase-lite-java-core/issues/310) Post on doc without data returns 404 instead of 405
- [**#667**](https://github.com/couchbase/couchbase-lite-java-core/issues/667) Using PipedInputStream and PipedOutputStream in URLConnection can cause deadlock (see issue 57 in couchbase-lite-java-listener)
- [**#880**](https://github.com/couchbase/couchbase-lite-java-core/issues/880) Query for view with map-reduce function and startkey doesn't work properly
- [**#891**](https://github.com/couchbase/couchbase-lite-java-core/issues/891) Fix failing tests (on Jenkins/VM)
- [**#952**](https://github.com/couchbase/couchbase-lite-java-core/issues/952) Views broken with concurrent update and delete
- [**#1015**](https://github.com/couchbase/couchbase-lite-java-core/issues/1015) NPE Attempt to invoke virtual method int com.couchbase.lite.Database.findMissingRevisions on a null object reference
- [**#1026**](https://github.com/couchbase/couchbase-lite-java-core/issues/1026) Change tracker stopping during replication exception
- [**#1037**](https://github.com/couchbase/couchbase-lite-java-core/issues/1037) Proxy setting on Android blocks access to Listener
- [**#1073**](https://github.com/couchbase/couchbase-lite-java-core/issues/1073) ForestDB CBL 1.2 random crash.
- [**#1090**](https://github.com/couchbase/couchbase-lite-java-core/issues/1090) Android API 10: java.lang.UnsatisfiedLinkError: nativeOpen
- [**#1091**](https://github.com/couchbase/couchbase-lite-java-core/issues/1091) ReplicationTest > testPusherBatching FAILED with CBL Java
- [**#1095**](https://github.com/couchbase/couchbase-lite-java-core/issues/1095) CBL 1.2 ForestDB random crash.
- [**#1098**](https://github.com/couchbase/couchbase-lite-java-core/issues/1098) Querying local CBLite via REST API returns all doc revisions (not just current rev)
- [**#1161**](https://github.com/couchbase/couchbase-lite-java-core/issues/1161) CBL - 1.2.0 upgrade from 1.1.0 clears device db
- [**#1176**](https://github.com/couchbase/couchbase-lite-java-core/issues/1176) ForestDB CBL 1.2  crash in endTransaction()
- [**#1177**](https://github.com/couchbase/couchbase-lite-java-core/issues/1177) ForestDB CBL 1.2 crash.
- [**#1193**](https://github.com/couchbase/couchbase-lite-java-core/issues/1193) Return 405 (Method Not Allowed) instead of 404 if Router does not support requested REST API
- [**#1196**](https://github.com/couchbase/couchbase-lite-java-core/issues/1196) Crash in ForestDB (filemgr_is_fully_resident)
- [**#1201**](https://github.com/couchbase/couchbase-lite-java-core/issues/1201) GrocerySync crashes with ForestDB
- [**#1210**](https://github.com/couchbase/couchbase-lite-java-core/issues/1210) Listener ?attachments=true to return attachment in base64
- [**#1211**](https://github.com/couchbase/couchbase-lite-java-core/issues/1211) Supports `only_conflicts` and `include_conflicts` query parameters for `_all_docs` REST API
- [**#1222**](https://github.com/couchbase/couchbase-lite-java-core/issues/1222) Make SQLite one writer and one/multiple reader modes to avoid waiting connection.
- [**#1227**](https://github.com/couchbase/couchbase-lite-java-core/issues/1227) Port: Crash when saving, conflict generated and infinite replication loop
- [**#1232**](https://github.com/couchbase/couchbase-lite-java-core/issues/1232) ManagerTest.testClose() failed with latest master branch
- [**#1235**](https://github.com/couchbase/couchbase-lite-java-core/issues/1235) BackFillTest.testPullReplWithRevsAndAtts() fails
- [**#1236**](https://github.com/couchbase/couchbase-lite-java-core/issues/1236) PullReplWithRevsAndAttsTest.testPullReplWithRevsAndAtts() fails
- [**#1241**](https://github.com/couchbase/couchbase-lite-java-core/issues/1241) Couchbase-lite-java-forestdb is not build-able on Windows
- [**#1243**](https://github.com/couchbase/couchbase-lite-java-core/issues/1243) Push replication from Android LiteServ and sync_gateway not pushing all deleted documents
- [**#1245**](https://github.com/couchbase/couchbase-lite-java-core/issues/1245) CBL Java/Android can not handle complex Accept: header value
- [**#1249**](https://github.com/couchbase/couchbase-lite-java-core/issues/1249) Purge does not update view on ForestDB Mobile
- [**#1263**](https://github.com/couchbase/couchbase-lite-java-core/issues/1263) Deleting a db takes over 1 min.
- [**#1264**](https://github.com/couchbase/couchbase-lite-java-core/issues/1264) Querying a design document view returns deleted documents too REST API
- [**#1270**](https://github.com/couchbase/couchbase-lite-java-core/issues/1270) Forestdb Handle is being used by another thread (Note: ForestDB error code = -39)
- [**#1272**](https://github.com/couchbase/couchbase-lite-java-core/issues/1272) 400 Missing data of attachment while pushing attachments
- [**#1275**](https://github.com/couchbase/couchbase-lite-java-core/issues/1275) Very slow doc PUT's with lots of garbage collection.
- [**#1276**](https://github.com/couchbase/couchbase-lite-java-core/issues/1276) ForestDB CBL crash.
- [**#1285**](https://github.com/couchbase/couchbase-lite-java-core/issues/1285) OkHttp ConnectionPool thread leaking
- [**#1289**](https://github.com/couchbase/couchbase-lite-java-core/issues/1289) SecureTokenStore does not work with  Android M/N and there is encrypting data size limitation for API 18 - 22
- [**#1297**](https://github.com/couchbase/couchbase-lite-java-core/issues/1297) 590 Database error (Note: ForestDB error code = -39)
- [**#1299**](https://github.com/couchbase/couchbase-lite-java-core/issues/1299) Get just attachment with header 'Accept: applicatio/json'  should return {"status" : 406, "error" : "not_acceptable"}
- [**#1300**](https://github.com/couchbase/couchbase-lite-java-core/issues/1300) Compaction doesn't work with ForestDb
- [**#1301**](https://github.com/couchbase/couchbase-lite-java-core/issues/1301) ForestDB throws exception from native call (Note: ForestDB error code = -39)
- [**#1308**](https://github.com/couchbase/couchbase-lite-java-core/issues/1308) Encrypted attachments fail to sync
- [**#1315**](https://github.com/couchbase/couchbase-lite-java-core/issues/1315) Replicator shouldn't go to IDLE state if the authenticating is not done
- [**#1319**](https://github.com/couchbase/couchbase-lite-java-core/issues/1319) Autopruning failing on pull replication
- [**#1324**](https://github.com/couchbase/couchbase-lite-java-core/issues/1324) OIDC shouldn't clear refresh token after refreshing the token
- [**#1332**](https://github.com/couchbase/couchbase-lite-java-core/issues/1332) Cancelling a replication does not return a response.
- [**#1333**](https://github.com/couchbase/couchbase-lite-java-core/issues/1333) OIDC: Obtaining username with refresh-token might have issue
- [**#1339**](https://github.com/couchbase/couchbase-lite-java-core/issues/1339) Make lower initial heartbeat value for /_changes REST API
- [**#1342**](https://github.com/couchbase/couchbase-lite-java-core/issues/1342) Unit Test Failures on Jenkins
- [**#1355**](https://github.com/couchbase/couchbase-lite-java-core/issues/1355) Listener does not return response for PUT /db
- [**#1356**](https://github.com/couchbase/couchbase-lite-java-core/issues/1356) Listener does not return response for DELETE /db
- [**#1367**](https://github.com/couchbase/couchbase-lite-java-core/issues/1367) Live Query Seems broken with ForestDB

### Where to get it

You can download this release from [Couchbase.com](http://www.couchbase.com/nosql-databases/downloads#Couchbase_Mobile)
