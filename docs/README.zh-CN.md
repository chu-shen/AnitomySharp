# AnitomySharp

## 示例

现有如下文件：

    [BM&T] Toradora! - 07v2 - Pool Opening  (2008) [720p Hi10p FLAC] [BD] [8F59F2BA].mkv

此文件将被 AnitomySharp 提取出如下元素:

- 发布组: *BM&T*
- 动画名: *Toradora!*
- 集数: *07*
- 发布版本: *2*
- 本集标题: *Pool Opening*
- 动画年份: *2008*
- 视频分辨率: *720p*
- 视频专用术语: *Hi10p*
- 音频专用术语: *FLAC*
- 来源: *BD*
- 文件校验码: *8F59F2BA*
- 文件扩展名: *mkv*

使用示例代码段如下：

```csharp
using System;
using static AnitomySharp.AnitomySharp;

namespace anitomytest
{
  class Program
  {
    public static void Main(string[] args)
    {
      const string filename = "[BM&T] Toradora! - 07v2 - Pool Opening  (2008) [720p Hi10p FLAC] [BD] [8F59F2BA].mkv";
      var results = Parse(filename);
      results.ForEach(x => Console.WriteLine(x.Category + ": " + x.Value));
    }
  }
}
```

该代码段将输出如下结果:

```
ElementFileExtension: mkv
ElementFileName: [BM&T] Toradora! - 07v2 - Pool Opening  (2008) [720p Hi10p FLAC] [BD] [8F59F2BA]
ElementVideoResolution: 720p
ElementVideoTerm: Hi10p
ElementAudioTerm: FLAC
ElementSource: BD
ElementFileChecksum: 8F59F2BA
ElementAnimeYear: 2008
ElementEpisodeNumber: 07
ElementReleaseVersion: 2
ElementAnimeTitle: Toradora!
ElementReleaseGroup: BM&T
ElementEpisodeTitle: Pool Opening
```

详细原理请查阅[设计文档](design.md)

## 安装

NuGet提供[Anitomy及其相关版本](https://www.nuget.org/packages?q=Anitomy)的历史版本下载

最新版本请关注本项目[Releases](https://github.com/chu-shen/AnitomySharp/releases)

## Issues & Pull Requests

欢迎提交新规则、问题、功能……

## 用例

- 在 jellyfin 中使用[bangumi插件](https://github.com/kookxiang/jellyfin-plugin-bangumi)解析文件名、集数、文件类型

- 在 jellyfin 中使用[anilist插件](https://github.com/chu-shen/jellyfin-plugin-anilist-with-filter)解析文件名

## 致谢

本项目基于[tabratton](https://github.com/tabratton/AnitomySharp)与[senritsu](https://github.com/senritsu/AnitomySharp)编写的 AnitomySharp ，在其基础上完善，使其在中文环境下也能使用

>*AnitomySharp* is a C# port of [Anitomy](https://github.com/erengy/anitomy), with inspiration taken from [AnitomyJ](https://github.com/Vorror/anitomyJ), a library for parsing anime video filenames. All credit to [@erengy](https://github.com/erengy) for the actual library and logic.