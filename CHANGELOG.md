# Changelog

## [0.5.1](https://github.com/chu-shen/AnitomySharp/compare/v0.5.0...v0.5.1) (2024-05-13)


### Bug Fixes

* update version ([1cf3f20](https://github.com/chu-shen/AnitomySharp/commit/1cf3f20792c0bb67c45ccf016da7ab4027470e4c))

## [0.5.0](https://github.com/chu-shen/AnitomySharp/compare/v0.4.0...v0.5.0) (2024-05-13)


### Features

* `SearchForSymbolWithEpisode`: check keyword in PeekEntries when match episode number ([46a0ed2](https://github.com/chu-shen/AnitomySharp/commit/46a0ed2607b3d324b82a731b85237e9421b9257d))
* add new episode rule to match `OtherToken[Disc 01]` ([be12b5a](https://github.com/chu-shen/AnitomySharp/commit/be12b5ac87e93f9224229aee20e08a08ba9dd558))
* add new rule to match episode number with bracket e.g. `[13 (341)]` ([3d7373c](https://github.com/chu-shen/AnitomySharp/commit/3d7373c032be3407abfebd14d13b2569977175ee))
* check anime title: shoule not be number ([97af21e](https://github.com/chu-shen/AnitomySharp/commit/97af21e383429b9ee5603002ca3e8c8f6c124d3b))


### Bug Fixes

* fix the rule of anime year ([83e4686](https://github.com/chu-shen/AnitomySharp/commit/83e4686d21e6b082a2ca409b69ab4d0d26bb9c7b))
* properly handle full width digits & check if tokens are within range ([e8659ee](https://github.com/chu-shen/AnitomySharp/commit/e8659ee54f5a20875c4f01420c8c0207c6ce979f))


### Reverts

* check if tokens are within range ([9ee8216](https://github.com/chu-shen/AnitomySharp/commit/9ee82163ce768545d2dae071569f23de5414ed34))

## [0.3.0](https://github.com/chu-shen/AnitomySharp/compare/0.2.0...v0.3.0) (2023-08-03)


### Features

* add new episode rule to match `OtherToken[Hint05]` ([c268840](https://github.com/chu-shen/AnitomySharp/commit/c2688405fc6d21079a475ed275bf9160cf4cf2e1))
* parse `animeType episode` e.g. OVA 3 ([f1ff55b](https://github.com/chu-shen/AnitomySharp/commit/f1ff55b9e4a7dbaa3d1353918e08fa76d2720653))


### Bug Fixes

* remove empty check of ElementEpisodeNumber ([220b038](https://github.com/chu-shen/AnitomySharp/commit/220b0384751f23f759da91c94d2120fddf14c1e3))
* 修改为处理后的年份值 ([e8645d3](https://github.com/chu-shen/AnitomySharp/commit/e8645d34875c13827503ee8954354dd117d65964))
* 元素字典的比较器忽略大小写 ([bd9da46](https://github.com/chu-shen/AnitomySharp/commit/bd9da46286bd4bd570f536a7f7e0f866c0e41333))

## [0.3.5](https://github.com/chu-shen/AnitomySharp/compare/v0.3.4...v0.3.5) (2023-07-30)


### Bug Fixes

* update ([7fd1112](https://github.com/chu-shen/AnitomySharp/commit/7fd111296d51ce6dc3d54fd9bebc99478d527115))

## 0.3.4 (2023-07-30)


### Bug Fixes

* add keyword ([c98b2b5](https://github.com/chu-shen/AnitomySharp/commit/c98b2b582c0f711449bd0f430f3bf71be0438a9d))
