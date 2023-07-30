# AnitomySharp

[![Build](https://github.com/chu-shen/AnitomySharp/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/chu-shen/AnitomySharp/actions/workflows/build.yml)

[中文指南](https://anitomysharp.chushen.xyz/README.zh-CN/)

>*AnitomySharp* is a C# port of [Anitomy](https://github.com/erengy/anitomy), with inspiration taken from [AnitomyJ](https://github.com/Vorror/anitomyJ), a library for parsing anime video filenames. All credit to [@erengy](https://github.com/erengy) for the actual library and logic.
>
>This fork of AnitomySharp is inspired by tabratton&senritsu, which adds more custom rules.

## Examples

The following filename...

    [BM&T] Toradora! - 07v2 - Pool Opening  (2008) [720p Hi10p FLAC] [BD] [8F59F2BA].mkv

...would be resolved into these elements:

- Release group: *BM&T*
- Anime title: *Toradora!*
- Anime year: *2008*
- Episode number: *07*
- Source: *BD*
- Release version: *2*
- Episode title: *Pool Opening*
- Video resolution: *720p*
- Video term: *Hi10p*
- Audio term: *FLAC*
- File checksum: *8F59F2BA*

Here's an example code snippet...

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

...which will output:

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
## Installation

AnitomySharp is available on [NuGet](https://www.nuget.org/packages/AnitomySharp.NET6), and can be found under the name AnitomySharp.

## Issues & Pull Requests

Welcome~