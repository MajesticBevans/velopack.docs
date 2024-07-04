---
title: SimpleFileSource
sidebar_position: 2
sidebar_label: 🟦 SimpleFileSource
---
<!--  
  <auto-generated>   
    The contents of this file were generated by a tool.  
    Changes to this file may be list if the file is regenerated  
  </auto-generated>   
-->

# SimpleFileSource Class

**Namespace:** [Velopack.Sources](../index.md)  
**Assembly:** Velopack  
**Assembly Version:** 0.0.556+83dfef5

Retrieves available updates from a local or network\-attached disk. The directory must contain one or more valid packages, as well as a 'releases.{channel}.json' index file.

```csharp
public class SimpleFileSource : IUpdateSource
```

**Inheritance:** object → SimpleFileSource

**Implements:** [IUpdateSource](../IUpdateSource/index.md)

## Constructors

| Name                                                     | Description |
| -------------------------------------------------------- | ----------- |
| [SimpleFileSource(DirectoryInfo)](constructors/index.md) |             |

## Properties

| Name                                         | Description                                             |
| -------------------------------------------- | ------------------------------------------------------- |
| [BaseDirectory](properties/BaseDirectory.md) |  The local directory containing packages to update to.  |

## Methods

| Name                                                                                                                      | Description |
| ------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [DownloadReleaseEntry(ILogger, VelopackAsset, string, Action\<int\>, CancellationToken)](methods/DownloadReleaseEntry.md) |             |
| [GetReleaseFeed(ILogger, string, Guid?, VelopackAsset)](methods/GetReleaseFeed.md)                                        |             |

___

*Documentation generated by [MdDocs](https://github.com/ap0llo/mddocs)*