---
title: UpdateManager
sidebar_position: 2
sidebar_label: 🟦 UpdateManager
---
<!--  
  <auto-generated>   
    The contents of this file were generated by a tool.  
    Changes to this file may be list if the file is regenerated  
  </auto-generated>   
-->

# UpdateManager Class

**Namespace:** [Velopack](../index.md)  
**Assembly:** Velopack  
**Assembly Version:** 0.0.556+83dfef5

Provides functionality for checking for updates, downloading updates, and applying updates to the current application.

```csharp
public class UpdateManager
```

**Inheritance:** object → UpdateManager

## Constructors

| Name                                                                                                                                                              | Description                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| [UpdateManager(IUpdateSource, UpdateOptions, ILogger, IVelopackLocator)](constructors/index.md#updatemanageriupdatesource-updateoptions-ilogger-ivelopacklocator) | Creates a new UpdateManager instance using the specified URL or file path to the releases feed, and the specified channel name. |
| [UpdateManager(string, UpdateOptions, ILogger, IVelopackLocator)](constructors/index.md#updatemanagerstring-updateoptions-ilogger-ivelopacklocator)               | Creates a new UpdateManager instance using the specified URL or file path to the releases feed, and the specified channel name. |

## Properties

| Name                                                           | Description                                                                                                                                                                                                         |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [AppId](properties/AppId.md)                                   |  The currently installed application Id. This would be what you set when you create your release.                                                                                                                   |
| [CurrentVersion](properties/CurrentVersion.md)                 |  The currently installed app version when you created your release. Null if this is not a currently installed app.                                                                                                  |
| [IsInstalled](properties/IsInstalled.md)                       |  True if this application is currently installed, and is able to download\/check for updates.                                                                                                                       |
| [IsPortable](properties/IsPortable.md)                         |                                                                                                                                                                                                                     |
| [IsUpdatePendingRestart](properties/IsUpdatePendingRestart.md) |  True if there is a local update prepared that requires a call to [ApplyUpdatesAndRestart(VelopackAsset, string\[\])](methods/ApplyUpdatesAndRestart.md#applyupdatesandrestartvelopackasset-string) to be applied.  |

## Methods

| Name                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ApplyUpdatesAndExit()](methods/ApplyUpdatesAndExit.md#applyupdatesandexit)                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [ApplyUpdatesAndExit(VelopackAsset)](methods/ApplyUpdatesAndExit.md#applyupdatesandexitvelopackasset)                             | This will exit your app immediately, apply updates, and then optionally relaunch the app using the specified  restart arguments. If you need to save state or clean up, you should do that before calling this method.  The user may be prompted during the update, if the update requires additional frameworks to be installed etc. You can check if there are pending updates by checking [IsUpdatePendingRestart](properties/IsUpdatePendingRestart.md).                     |
| [ApplyUpdatesAndRestart(VelopackAsset, string\[\])](methods/ApplyUpdatesAndRestart.md#applyupdatesandrestartvelopackasset-string) | This will exit your app immediately, apply updates, and then optionally relaunch the app using the specified  restart arguments. If you need to save state or clean up, you should do that before calling this method.  The user may be prompted during the update, if the update requires additional frameworks to be installed etc. You can check if there are pending updates by checking [IsUpdatePendingRestart](properties/IsUpdatePendingRestart.md).                     |
| [ApplyUpdatesAndRestart(string\[\])](methods/ApplyUpdatesAndRestart.md#applyupdatesandrestartstring)                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [CheckForUpdates()](methods/CheckForUpdates.md)                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [CheckForUpdatesAsync()](methods/CheckForUpdatesAsync.md)                                                                         | Checks for updates, returning null if there are none available. If there are updates available, this method will return an  UpdateInfo object containing the latest available release, and any delta updates that can be applied if they are available.                                                                                                                                                                                                                          |
| [DownloadUpdates(UpdateInfo, Action\<int\>, bool)](methods/DownloadUpdates.md)                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [DownloadUpdatesAsync(UpdateInfo, Action\<int\>, bool, CancellationToken)](methods/DownloadUpdatesAsync.md)                       | Downloads the specified updates to the local app packages directory. If the update contains delta packages and ignoreDeltas\=false,  this method will attempt to unpack and prepare them. If there is no delta update available, or there is an error preparing delta  packages, this method will fall back to downloading the full version of the update. This function will acquire a global update lock so may fail if there is already another update operation in progress. |
| [WaitExitThenApplyUpdates(VelopackAsset, bool, bool, string\[\])](methods/WaitExitThenApplyUpdates.md)                            | This will launch the Velopack updater and tell it to wait for this program to exit gracefully. You should then clean up any state and exit your app. The updater will apply updates and then optionally restart your app. The updater will only wait for 60 seconds before giving up. You can check if there are pending updates by checking [IsUpdatePendingRestart](properties/IsUpdatePendingRestart.md).                                                                     |

___

*Documentation generated by [MdDocs](https://github.com/ap0llo/mddocs)*