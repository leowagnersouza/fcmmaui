# fcmmaui
This repository implements push notifications that works on iOS, using .NET MAUI, .NET7 and Plugin.Firebase

## Quick intro

This repo is based on the popular Cedric Gabrang article, that you can read [here](https://cedricgabrang.medium.com/firebase-push-notifications-in-net-maui-ios-2f4388bf1ac).

The are two diferences: 

 1. The article is based on .NET6, and this repo uses .NET7;
 2. The article uses Plugin.Firebase 1.2.0 and this repo uses the version 2.0.4;

## Motivation

If you follow the Cedric's article step by step, using the newest platform version, it won't work.

If you follow the setup documentation of the plugin with the new version, it also won't work, at least at the time I wrote this file.

To make it work, I had to copy some small parts of the official docs into de Cedric's code, so if you are facing the same problem, you may find this useful. 

## Know issues

Notifications don't work on iOS simulator, you will need a physical device.

Also, at this moment, is not possible to deploy or debug a app that uses push notification using a Windows machine.

If you try you will face the "long file name error", that is less documented, but fatal.

You may face error messages like this:

    Could not find a part of the path 'C:\Nuget\xamarin.firebase.ios.cloudfirestore\8.10.0.1\lib\net6.0-ios15.4\Firebase.CloudFirestore.resources\grpcpp.xcframework\ios-arm64_i386_x86_64-simulator\grpcpp.framework\PrivateHeaders\src\core\ext\filters\client_channel\lb_policy\grpclb\client_load_reporting_filter.h'

##### **Remember, you will only encounter this error if:**
-   is using a Windows machine to develop;
-   is trying to debug with a physical iPhone;
-   is using the "Firebase.iOS.Core" package above version 8.10.0.0 ;

Currently, the only work around is to use a Mac for development.

You can find more info [here].(https://github.com/xamarin/GoogleApisForiOSComponents/issues/555): 

## Stuck?

If you have the choice, try to use a push notification service that offers a native .NET SDK, therefore you will not need another dependency, like Firebase.plugin.

Some choices, that offer a good free layer:

 - Azure Notification Service
 - OneSignal
 - Amazon Simple Notification System

## Need help or some quick fix in your app?

Drop me a line:
 - leowsouza@outlook.com.br
 - https://www.linkedin.com/in/lwsouza/

```
