---
layout: page_v2
page_type: module
title: Module - Adpod
description: Adds functions to validate, cache, and modify long-form video bids.
module_code : adpod
display_name : Adpod
enable_download : true
sidebarType : 1
---

# Adpod Module

The adpod module enables developers to add support for a new adserver that handles `adpod` (long-form) videos, like Freewheel. The  module provides functions to validate, cache, and modify long-form video bids. 

## How to use the module:

In the user's equivalent `<name>AdServerVideo` module, import the `initAdpodHooks` function and call it from within their module. Executing the init function will initialize several key functions from the module that are designed to handle `adpod` objects (ie. adUnits, bids, etc.) as the auction proceeds. These functions will only affect `adpod` objects, other `mediaTypes` will be handled by the base Prebid code. 

```
initAdpodHooks();
```

## Optional Values
In addition to the `initAdpodHooks` function, users can import values from the Adpod module that contain the adpod specific targeting keys (as strings). These values can be used to generate the correct output (ie. targeting keys) to send to the adserver.  

`TARGETING_KEY_PB_CAT_DUR`  
This variable equates to `hb_pb_cat_dur`.

`TARGETING_KEY_CACHE_ID`  
This variable equates to `hb_cache_id`. 

## Further Reading

[Prebid.js](/dev-docs/getting-started.html)   
[Prebid Video](/prebid-video/video-overview.html)  
[Freewheel Module](/dev-docs/modules/freewheel.html)