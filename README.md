# 关于

这将创建一个包含最新可用 Windows 系统的 ISO 文件，来自 [Unified Update Platform (UUP)](https://docs.microsoft.com/en-us/windows/deployment/update/windows-update-overview)。这把 [UUP dump](https://git.uupdump.net/uup-dump) 项目封装成了一个单一命令。

GitHub Actions 运行完成后，您将获得两种版本的最终 ISO 镜像。

1. 发布时将 .iso 文件拆分为多个部分（因为 GitHub 不允许在发布包中包含超过 2GB 的文件）。
此外，针对每次发布，都会为各种系统和架构创建相应的软件包；这些包中包含一个现成的脚本，用于下载拆分后的 ISO 所有部分并合并生成完整的 ISO 文件。
2. 构建产物（Artifacts）——提供单个 zip 压缩包，但下载时需要登录网站。

# 直接在 Windows x64 或 arm64 （最低 21H2）上运行

## 这支持以下内容：
Windows Builds:
* `windows-10`：Windows 10 22H2
* `windows-11 old`：Windows 11 23H2
* `windows-11`：Windows 11 24H2
* `windows-11 beta`：Windows 11 24H2 BETA
* `windows-11 new`：Windows 11 25H2
* `windows-11 dev`：Windows 11 25H2 BETA
* `windows-11 26h1`：Windows 11 26H1 <details><summary>详细信息</summary>针对搭载特定新款芯片（如 Snapdragon X2）的 2026 年新款设备，旨在实现硬件创新——不适用于现有 PC 或常规企业部署。</details>

* `windows-11 26h2`: Windows 11 Build 26300 系列
* `windows-dev`：Windows 11 Build 26340 系列
* `windows-canary`：Windows 11 Build 29000 系列


架构:
* `x64`
* `arm64`


版本:
* `home`
* `pro`
* `multi`：Home + Pro


语言:
* `ar-sa`：阿拉伯语（沙特阿拉伯）
* `bg-bg`：保加利亚语（保加利亚）
* `cs-cz`：捷克语（捷克共和国）
* `da-dk`：丹麦语（丹麦）
* `de-de`：德语（德国）
* `el-gr`：希腊语（希腊）
* `en-gb`：英语（英国）
* `en-us`：英语（美国）
* `es-es`：西班牙语（西班牙）
* `es-mx`：西班牙语（墨西哥）
* `et-ee`：爱沙尼亚语（爱沙尼亚）
* `fi-fi`：芬兰语（芬兰）
* `fr-ca`：法语（加拿大）
* `fr-fr`：法语（法国）
* `he-il`：希伯来语（以色列）
* `hr-hr`：克罗地亚语（克罗地亚）
* `hu-hu`：匈牙利语（匈牙利）
* `it-it`：意大利语（意大利）
* `ja-jp`：日语（日本）
* `ko-kr`：韩语（韩国）
* `lt-lt`：立陶宛语（立陶宛）
* `lv-lv`：拉脱维亚语（拉脱维亚）
* `nb-no`：挪威语（书面挪威语/Bokmål）（挪威）
* `nl-nl`：荷兰语（荷兰）
* `pl-pl`：波兰语（波兰）
* `pt-br`：葡萄牙语（巴西）
* `pt-pt`：葡萄牙语（葡萄牙）
* `ro-ro`：罗马尼亚语（罗马尼亚）
* `ru-ru`：俄语（俄罗斯）
* `sk-sk`：斯洛伐克语（斯洛伐克）
* `sl-si`：斯洛文尼亚语（斯洛文尼亚）
* `sr-latn-rs`：塞尔维亚语（拉丁字母，塞尔维亚）
* `sv-se`：瑞典语（瑞典）
* `th-th`：泰语（泰国）
* `tr-tr`：土耳其语（土耳其）
* `uk-ua`：乌克兰语（乌克兰）
* `zh-cn`：简体中文（中国）
* `zh-tw`：繁体中文（台湾）


其他选项：
* `esd`：使用 ESD 压缩
* `drivers`：从 Drivers 文件夹添加驱动程序
* `netfx3`：添加 .NET Framework 3.5
* `revision`：修订号


## 相关工具

* [Rufus](https://github.com/pbatard/rufus)
* [Fido](https://github.com/pbatard/Fido)
* [windows-evaluation-isos-scraper](https://github.com/rgl/windows-evaluation-isos-scraper)

## 参考

* [UUP dump home](https://uupdump.net)
* [UUP dump source code](https://git.uupdump.net/uup-dump)
* [Unified Update Platform (UUP)](https://docs.microsoft.com/en-us/windows/deployment/update/windows-update-overview)
