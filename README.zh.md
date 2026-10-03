<p align="center">
  <img alt="VoxSpica" src="images/voxspica_en.png" width="620">
</p>

<h1 align="center">VoxSpica</h1>

<p align="center">
  <b>Windows 语音转文字软件，声音不会离开你的电脑。</b><br>
  <sub>语音留在本地。无需账号，无需订阅，无需云端。</sub>
</p>

<p align="center">
  <a href="https://github.com/alex37529/voxspica/releases"><img alt="下载" src="https://img.shields.io/badge/下载-releases-2C7BE0?style=for-the-badge"></a>
  <a href="docs/USER-GUIDE.md"><img alt="使用指南" src="https://img.shields.io/badge/使用指南-0B1620?style=for-the-badge"></a>
  <a href="https://voxspica.4crytobot.xyz"><img alt="网站" src="https://img.shields.io/badge/网站-voxspica.4crytobot.xyz-0B1620?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-0B1620?style=flat-square">
  <img alt="许可证" src="https://img.shields.io/badge/许可证-proprietary-2C7BE0?style=flat-square">
  <img alt="界面语言" src="https://img.shields.io/badge/界面-9%20种语言-0B1620?style=flat-square">
  <img alt="识别语言" src="https://img.shields.io/badge/识别-33%20种语言-0B1620?style=flat-square">
  <img alt="引擎" src="https://img.shields.io/badge/ASR-VOSK%20(Kaldi)-0B1620?style=flat-square">
</p>

<p align="center">
  <sub><a href="README.md">English</a> · <a href="README.de.md">Deutsch</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a> · <a href="README.it.md">Italiano</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh.md">简体中文</a></sub>
</p>

---

## 这是什么

VoxSpica 在 Windows 上把语音转成文字，任何东西都不会离开电脑。识别引擎是
[VOSK](https://alphacephei.com/vosk/)——Kaldi 的桌面版本，开源，运行在你的
CPU 上。不需要显卡，不需要网络，没有遥测。

两种用法：

- **实时听写**：对着麦克风说话，文字随说随出。
- **文件转写**：系统能播放的都可以——mp3、m4a、wav，以及装了
  [ffmpeg](https://ffmpeg.org/) 后的其他格式。

每次识别都会存进本地数据库，之后可以搜索。

## 为什么离线

你可能用过的听写服务，会把你的音频送到别人的服务器。对它们来说这是合理的
设计，对一个用来记录你刚说出口的话的工具来说却不是——而那往往是一份私密
文档、一个客户的名字，或者一个你还没决定要不要发表的想法。

这里的答案是结构上的，不是承诺：模型在你的磁盘上，数据库在你的磁盘上，
程序里没有任何一处会去开网络连接。

<p align="center">
  <img alt="选择界面语言" src="images/voxspica_interface_language.png" width="820">
  <br>
  <sub>界面有九种语言，每一种都用自己的语言写出来。</sub>
</p>

## 界面

<table>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="管理识别模型" src="images/voxspica_models.png"><br>
  <sub><b>模型</b>——所有语言、各自的规格，以及每个模型要占多大。</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="选择麦克风" src="images/voxspica_device.png"><br>
  <sub><b>设备</b>——选择麦克风，附带它真实的采样率。</sub>
</td>
</tr>
<tr>
<td width="50%" align="center" valign="top">
  <img alt="识别历史" src="images/voxspica_history.png"><br>
  <sub><b>历史</b>——每条识别都能搜索、删除、复制。</sub>
</td>
<td width="50%" align="center" valign="top">
  <img alt="选择界面语言" src="images/voxspica_interface_language.png"><br>
  <sub><b>界面</b>——随时切换界面语言。</sub>
</td>
</tr>
</table>

## 获取

<table>
<tr>
<th align="left" width="50%">分语言安装包</th>
<th align="left" width="50%">便携版压缩包</th>
</tr>
<tr>
<td valign="top">

七个安装包，每种界面语言一个。每个都自带该语言的现成识别模型，所以第一次
启动完全不需要联网。选你的语言，链接在下面。

</td>
<td valign="top">

一个 zip，里面只有一个 <code>VoxSpica.exe</code>。不安装任何东西，不往系统里
写任何东西，文件夹可以放在 U 盘里带走。界面语言和模型都在第一次运行时选择。

便携版见 [Releases](https://github.com/alex37529/voxspica/releases)。

</td>
</tr>
</table>

### Scoop

如果你已经在用 [Scoop](https://scoop.sh)：

```powershell
scoop bucket add voxspica https://github.com/alex37529/voxspica-scoop
scoop install voxspica
```

它安装的是便携版，并把 `voxspica` 加进 PATH。清单的校验和取自该版本
release 自带的 `SHA256SUMS.txt`，所以 `scoop update` 会自己拿到新版本。

### 七个安装包

基础地址：<https://voxspica.4crytobot.xyz/downloads>

- <img src="https://flagcdn.com/16x12/gb.png" width="16" alt="GB"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-en-setup.exe"><code>VoxSpica-0.1.6-en-setup.exe</code></a> — English, 119.3 MB
- <img src="https://flagcdn.com/16x12/ru.png" width="16" alt="RU"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-ru-setup.exe"><code>VoxSpica-0.1.6-ru-setup.exe</code></a> — Русский, 124.3 MB
- <img src="https://flagcdn.com/16x12/de.png" width="16" alt="DE"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-de-setup.exe"><code>VoxSpica-0.1.6-de-setup.exe</code></a> — Deutsch, 124.3 MB
- <img src="https://flagcdn.com/16x12/fr.png" width="16" alt="FR"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-fr-setup.exe"><code>VoxSpica-0.1.6-fr-setup.exe</code></a> — Français, 120.6 MB
- <img src="https://flagcdn.com/16x12/es.png" width="16" alt="ES"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-es-setup.exe"><code>VoxSpica-0.1.6-es-setup.exe</code></a> — Español, 117.8 MB
- <img src="https://flagcdn.com/16x12/it.png" width="16" alt="IT"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-it-setup.exe"><code>VoxSpica-0.1.6-it-setup.exe</code></a> — Italiano, 127.7 MB
- <img src="https://flagcdn.com/16x12/cn.png" width="16" alt="CN"> <a href="https://voxspica.4crytobot.xyz/downloads/VoxSpica-0.1.6-zh-setup.exe"><code>VoxSpica-0.1.6-zh-setup.exe</code></a> — 简体中文, 122.0 MB

这份列表写的是某一个版本，出了新版本就会替换。便携版压缩包故意不放进来：它在
Releases 里，而且当你要的界面语言不在上面这份列表里时，它才是对的选择。旗帜
图片由 [flagcdn.com](https://flagcdn.com) 提供，表示的是语言而不是国家：英文
用 🇬🇧 而不是 🇺🇸，因为界面语言代码是 `en` 而不是 `en-US`，没有哪个安装包带
美国界面。如果 flagcdn 打不开，下面的链接照样能用，只是图片不显示。

> **Windows 会弹出警告。** 编译产物没有做代码签名，SmartScreen 会提示未知
> 发布者。点 *更多信息* → *仍要运行*。详见
> [它做不到什么](#它做不到什么)。

## 第一次运行

1. 启动程序。第一次运行时它会问界面语言。
2. 选**识别语言**——也就是你**要说的**那个语言。它和界面语言是两回事，互相
   独立。
3. 下载对应模型。**小模型**约 50 MB，够用来打草稿；**大模型**更准，需要大约
   8 GB 内存，而且每次开机后第一次加载要从磁盘读 60 到 90 秒。
4. 选一个麦克风，按下录制，开始说话。

[使用指南](docs/USER-GUIDE.md)逐屏讲了一遍，包括模型找不到时该怎么办、
小模型和大模型的区别。

## 语言

**界面**有九种：白俄罗斯语、德语、英语、西班牙语、法语、意大利语、俄语、
乌克兰语、简体中文。

**识别**支持 33 种。完整清单和对应模型见
[docs/LANGUAGES.md](docs/LANGUAGES.md)。识别语言和界面语言互不绑定——你可以
用英语界面识别乌克兰语。

## 命令行

它不只是一个窗口。它能做的每一件事都能在命令行里做，写脚本或者绑到热键上
时用的就是这个：

```powershell
VoxSpica.exe mic --lang zh --size small      # 听写，输出到 stdout
VoxSpica.exe file meeting.mp3 --lang en-us   # 转写文件
VoxSpica.exe devices                         # 列出麦克风
VoxSpica.exe download --lang zh --size small
VoxSpica.exe list                            # 语言和它们的模型
VoxSpica.exe history --search "meeting"      # 之前识别过什么
```

## 它做不到什么

直说，因为这部分通常都是后来才发现。

- **没有代码签名。** 每次安装 Windows 都会弹 SmartScreen 警告。
- **没有逗号。** VOSK 输出的词不带标点。VoxSpica 会还原大小写，并在句末加
  句号，但不做语法分析就无法正确断句——任何简单规则都会把「你好吗」变成
  「你好，吗」。
- **只有 Windows x64。** 没有 macOS 和 Linux 版本。
- **模型要单独下。** 除了分语言安装包，程序本身不带任何模型，而模型从 50 MB
  到 1.8 GB 不等。分语言安装包是例外：每个都自带一个。

## 关于这个仓库

这里**只放发布版本**。源代码不公开，也没有镜像到这里——这个仓库里不存在任何
源代码。`vX.Y.Z` 标签指向的是引入这个文件的那个很小的公开提交，不是应用
代码。每个 release 附带的文件是编译好的二进制。

网站：<https://voxspica.4crytobot.xyz>

## 许可证

专有软件，免费使用，见 [LICENSE](LICENSE)。识别由
[VOSK](https://alphacephei.com/vosk/)（Apache-2.0）完成；识别模型由
Alpha Cephei 同样以 Apache-2.0 发布。
