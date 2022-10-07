# AnitomySharp

[中文指南](https://anitomysharp.chushen.xyz/README.zh-CN/)

>*AnitomySharp* is a C# port of [Anitomy](https://github.com/erengy/anitomy), with inspiration taken from [AnitomyJ](https://github.com/Vorror/anitomyJ), a library for parsing anime video filenames. All credit to [@erengy](https://github.com/erengy) for the actual library and logic.

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
AnitomySharp is available on NuGet, and can be found under the name AnitomySharp.


## Issues & Pull Requests

For the most part, AnitomyJ aims to be an exact Java replica of the original Anitomy. To make porting upstream changes easier most of the logic + file structure remain similar to their c++ counterparts. So, for the time being, I won't be accepting pull requests/issues that change the core parsing logic. I suggest opening an issue with the original Anitomy project and when it's fixed I'll merge it downstream.

That being said if the output of AnitomyJ and Anitomy differ in *any way* please open an issue.

## FAQ

- Why didn't you write a C# wrapper since *Anitomy* is in C++?

    I could have, but the main motivation behind this project was to expose myself to C# and how it was different from Java, so I figured the best way to do that would be to port the library instead of making a wrapper.
