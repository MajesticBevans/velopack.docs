---
title: GitBase\<T\>
sidebar_position: 2
sidebar_label: 🟦 GitBase\<T\>
---
<!--  
  <auto-generated>   
    The contents of this file were generated by a tool.  
    Changes to this file may be list if the file is regenerated  
  </auto-generated>   
-->

# GitBase\<T\> Class

**Namespace:** [Velopack.Sources](../index.md)  
**Assembly:** Velopack  
**Assembly Version:** 0.0.556+83dfef5

Base class to provide some shared implementation between sources which download releases from a Git repository.

```csharp
public abstract class GitBase<T> : IUpdateSource
```

**Inheritance:** object → GitBase\<T\>

**Implements:** [IUpdateSource](../IUpdateSource/index.md)

## Type Parameters

`T`

## Constructors

| Name                                                                    | Description |
| ----------------------------------------------------------------------- | ----------- |
| [GitBase(string, string, bool, IFileDownloader)](constructors/index.md) |             |

## Properties

| Name                                   | Description                                                                                                                   |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [Downloader](properties/Downloader.md) | The file downloader used to perform HTTP requests.                                                                            |
| [Prerelease](properties/Prerelease.md) | If true, the latest upcoming\/prerelease release will be downloaded. If false, the latest  stable release will be downloaded. |
| [RepoUri](properties/RepoUri.md)       | The URL of the repository to download releases from.                                                                          |

## Methods

| Name                                                                                                                      | Description |
| ------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [DownloadReleaseEntry(ILogger, VelopackAsset, string, Action\<int\>, CancellationToken)](methods/DownloadReleaseEntry.md) |             |
| [GetReleaseFeed(ILogger, string, Guid?, VelopackAsset)](methods/GetReleaseFeed.md)                                        |             |

___

*Documentation generated by [MdDocs](https://github.com/ap0llo/mddocs)*