---
title: "Android Google Play Device Is Uncertified Issue"
date: 2022-07-05T05:53:30Z
---

## Android 安装GMS 问题

### google play 启动时 device is uncertified

```.diff
From 8165c1ed18161583f1db561899201d5f983494bd Mon Sep 17 00:00:00 2001
From: ldh <ldh@quanyuntech.com>
Date: Wed, 13 Apr 2022 17:35:19 +0800
Subject: [PATCH] gms is ok

Change-Id: I27b7192aac9b8f4dbc03b2461fe9ccdead78ba25
---
 init/property_service.cpp | 11 ++++++-----
 1 file changed, 6 insertions(+), 5 deletions(-)

diff --git a/init/property_service.cpp b/init/property_service.cpp
index a89504e59..d16ff90b9 100644
--- a/init/property_service.cpp
+++ b/init/property_service.cpp
@@ -847,11 +847,12 @@ static void property_derive_build_fingerprint() {
     }
 
     const std::string UNKNOWN = "unknown";
-    build_fingerprint = GetProperty("ro.product.brand", UNKNOWN);
-    build_fingerprint += '/';
-    build_fingerprint += GetProperty("ro.product.name", UNKNOWN);
-    build_fingerprint += '/';
-    build_fingerprint += GetProperty("ro.product.device", UNKNOWN);
+    //build_fingerprint = GetProperty("ro.product.brand", UNKNOWN);
+    //build_fingerprint += '/';
+    //build_fingerprint += GetProperty("ro.product.name", UNKNOWN);
+    //build_fingerprint += '/';
+    //build_fingerprint += GetProperty("ro.product.device", UNKNOWN);
+    build_fingerprint = "Droidlogic/franklin/franklin";
     build_fingerprint += ':';
     build_fingerprint += GetProperty("ro.build.version.release", UNKNOWN);
     build_fingerprint += '/';
-- 
2.25.1

```

### 移除其他的问题

移除不需要的应用
