<div class="github-widget" data-repo="gbdev/awesome-gbdev"></div>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script><ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-6890694312814945" data-ad-slot="5473692530" data-ad-format="auto"  data-full-width-responsive="true"></ins><script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
## ![GameboyIcon](http://i.imgur.com/ROUq7NT.gif) Awesome Game Boy Development

#### [Join us on Discord](https://discord.gg/tKGMPNr) [![Discord Badge](https://img.shields.io/badge/dynamic/json.svg?label=chat&colorB=green&suffix=%20online&query=presence_count&uri=https://discordapp.com/api/guilds/303217943234215948/widget.json)](https://discord.gg/tKGMPNr)

精选的Game Boy（彩色）开发资源，工具，文档，相关项目和开源ROM的精选列表. 受启发 [awesome](https://github.com/sindresorhus/awesome) 列出的东西.

您可以找到此列表的一个（很酷的）网络版本 [here](https://gbdev.github.io/list.html).


- [Introduction](#introduction)
  - [Disambiguation](#disambiguation)
- [Community](#community)
- [Documentation](#documentation)
  - [Misc](#misc)
  - [Opcodes](#opcodes)
  - [Game Boy Color](#game-boy-color)
  - [Hardware](#hardware)
  - [Peripherals](#peripherals)
  - [Cartridges](#cartridges)
- [Emulator Development](#emulator-development)
  - [Testing](#testing)
- [Software Development](#software-development)
  - [Assemblers](#assemblers)
  - [Compilers](#compilers)
    - [Experimental/Proof of Concepts](#experimentalproof-of-concepts)
  - [Emulators](#emulators)
  - [Tools](#tools)
    - [Engines](#engines)
    - [Development tools](#development-tools)
    - [Graphics utilities](#graphics-utilities)
    - [Hardware and ROM utilities](#hardware-and-rom-utilities)
    - [Music drivers and trackers](#music-drivers-and-trackers)
- [Programming](#programming)
  - [ASM](#asm)
    - [Sources](#sources)
    - [Timings](#timings)
    - [Boilerplates](#boilerplates)
    - [Syntax highlighting packages](#syntax-highlighting-packages)
  - [C](#c)
- [Homebrews](#homebrews)
  - [ASM](#asm-1)
  - [C](#c-1)
  - [Demos](#demos)
- [Reverse Engineering](#reverse-engineering)
  - [Game Disassemblies](#game-disassemblies)
- [Game Boy Camera](#game-boy-camera)
  - [Retrieving Images](#retrieving-images)
  - [Changing the camera's behavior](#changing-the-cameras-behavior)
  - [Post-processing](#post-processing)
- [Related projects](#related-projects)
  - [Directories](#directories)
  - [Websites](#websites)
- [About](#about)
  - [Contribute](#contribute)
  - [License](#license)
  - [Acknowledgements](#acknowledgements)
  - [Sponsors](#sponsors)

## Introduction

- [The Game Boy, a hardware autopsy](https://www.youtube.com/playlist?list=PLu3xpmdUP-GRDp8tknpXC_Y4RUQtMMqEu)
- [The Ultimate Game Boy Talk](https://media.ccc.de/v/33c3-8029-the_ultimate_game_boy_talk)


> ### Disambiguation
>
> #### Game Boy Advance
>
&gt; Game Boy Advance开发包含在另一个项目中，即 [awesome-gbadev](https://github.com/gbdev/awesome-gbadev) 列表.
 &gt; GBA，但是，*可以运行* GB / GBC游戏. 与本地硬件相比，这样做的方式略有不同：此列表的“模拟器开发”部分对此进行了介绍.
>
> #### Game Boy Color and Super Game Boy
>
&gt;此列表着重于原始的* Game Boy *（GB或DMG，1989），* Game Boy Color *（GBC或CGB）和* Super Game Boy *（SGB）是非常相似的系统，其中一些重要区别，例如：
>
&gt;-不同的硬件规格；
&gt;-特定的硬件和软件功能；
&gt;-特定寄存器；
&gt;-特定的错误，怪癖和可利用的行为.
>
>If you aim to develop your software for SGB or GBC, or you want to know how it runs on the other systems, you may want to take advantage and adapt to these differences, check the [Game Boy Color](#game-boy-color) 类别，并查找对GBC / CGB和SGB的特定引用.


## Community

- [Chat channels](https://gbdev.io/chat)
- [Forum](https://gbdev.gg8.se/forums/)

## Documentation

- [**Pan Docs**](https://gbdev.github.io/pandocs/)  -向公众提供有关Game Boy的唯一，最全面的技术参考. 由社区进行更正，更新和维护.
- [The Cycle-Accurate Game Boy Docs](https://github.com/AntonioND/giibiiadvance/blob/master/docs/TCAGBD.pdf) -AntonioND提供的精确文档，可以制作出周期精确的Game Boy模拟器.
- [Complete Technical Reference](https://gekkio.fi/files/gb-docs/gbctr.pdf) -Gekkio.
- [Game Boy Project Report](http://www.cs.columbia.edu/~sedwards/classes/2019/4840-spring/reports/GameBoy.pdf) -硬件报告 [emulator](https://github.com/kitsuneh/SVGameBoy) （在Terasic DE1-SoC板上）作为哥伦比亚大学CSEE4840嵌入式系统设计课程的最终项目而开发.

#### Opcodes

- [gb-opcodes](https://gbdev.github.io/gb-opcodes/optables/) -操作码表
- [RGBDS opcodes reference](https://rednex.github.io/rgbds/gbz80.7.html) -所有指令的参考，包括简短说明，周期和字节数以及标志修改的说明.

### Game Boy Color

- [Bootstrap ROM](https://tcrf.net/Game_Boy_Color_Bootstrap_ROM)
- [Unused Palettes](https://tcrf.net/Notes:Game_Boy_Color_Bootstrap_ROM)
- [Colorization palettes in the BIOS](https://forums.nesdev.com/viewtopic.php?p=114388&sid=c3d4ce08cfd9d9c834958d4f148750c3#p114388)
- [ROM Disassembly](https://gist.github.com/drhelius/6063265)

### Hardware

- [DMG Schematics](http://gbdev.gg8.se/wiki/articles/DMG_Schematics) -硬件原理图.
- [The Game Boy Project](http://marc.rawer.de/Gameboy/Docs/GBProject.pdf) -提供有关硬件和详细结构信息的研究，以实现三个8位双向并行端口.
- [Related custom hardware](https://github.com/Gekkio/gb-hardware) -Gekkio.
- [ESP8266 GB Dev Board](https://github.com/applefreak/esp8266-gameboy-dev-board) -由ESP8266驱动的Game Boy配件开发开发板.
- [ESP8266 GB Printer](https://github.com/applefreak/esp8266-gameboy-printer) -一种模拟GB打印机并允许您使用WiFi检索图像的设备.
- [fruttenboel](http://verhoeven272.nl/fruttenboel/Gameboy/index.html) -包含有关硬件，定制板以与控制台和其他相关项目对接的大量信息的页面.
- [Game Boy hardware database](https://gbhwdb.gekkio.fi/) -各种类型的Game Boy游戏机的数据和照片.
- [DMG-CPU-Inside](https://github.com/furrtek/DMG-CPU-Inside) -从裸照中提取的DMG-CPU-B芯片的原理图和带注释的覆盖层.

### Peripherals

- [Dan Docs](https://shonumi.github.io/dandocs.html) -模糊的Game Boy硬件文档.
- [Edge of Emulation](https://shonumi.github.io/articles.html) ，有关模拟和研究Game Boy配件的一系列文章. 也可作为 [technical documents](https://github.com/shonumi/gbe-plus/tree/master/src/docs/technical) 在GBE仿真器文档中.
  - [Mobile Adapter GB](https://shonumi.github.io/articles/art14.html) -Game Boy Color上的Internet连接和DLC.
  - [The Game Boy Printer](https://shonumi.github.io/articles/art2.html)
  - [Pocket Sonar](https://shonumi.github.io/articles/art13.html) -带有内置声纳硬件的蓝色手推车.
  - [Zok Zok Heroes](https://shonumi.github.io/articles/art8.html)  -Zok Zok Heroes的Full Changer，一种动作激活的配件.
  - [Infrared Madness](https://shonumi.github.io/articles/art11.html) -关于Game Boy Color的红外通讯.
  - [Game Boy 4-Player Adapter](https://shonumi.github.io/articles/art9.html) -DMG-07.
  - [Barcode Boy](https://shonumi.github.io/articles/art7.html) -第一个Game Boy卡扫描仪.
  - [Barcode Taisen Bardigun](https://shonumi.github.io/articles/art6.html) -90年代后期DMG-GBC条码读取器.
- [DMG-07 Technical Documentation](https://raw.githubusercontent.com/shonumi/gbe-plus/master/src/docs/technical/DMG_07.txt)
- [Game Boy Camera RE](https://github.com/AntonioND/gbcam-rev-engineer) -有关GB相机的文档以及用于通过Arduino进行逆向工程的工具.
- [Creating photo realistic images with neural networks and a Gameboy Camera](http://www.pinchofintelligence.com/photorealistic-neural-network-gameboy/)
- [The Game Boy Printer](https://shonumi.github.io/articles/art2.html) -有关打印机硬件，通信协议和游戏用于实现打印功能的常规例程的深入技术文档.
- [Ben Heck Reverse Engineers Game Boy Printer](https://www.youtube.com/watch?v=43FfJvd-YP4) （勘误表：用过的热敏纸已过期，实际上可以打印4种颜色）.
- [Arduino Game Boy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator) -使用Arduino通过Game Boy Link电缆模拟Game Boy打印机.
- [Mobile Game Boy Adapter](https://bulbapedia.bulbagarden.net/wiki/Mobile_Game_Boy_Adapter)
- [GB KISS LINK MODEM](http://nectaris.tg-16.com/GB-KISS-LINK-FAQ-hudson-gameboy-nectaris.html)

### Cartridges

- [AntonioND's docs](https://github.com/AntonioND/giibiiadvance/tree/master/docs) -更正了有关墨盒头数据的示意图和信息.
- [Gekkio's Game Boy cartridge types](http://gekkio.fi/blog/2015-02-14-mooneye-gb-gameboy-cartridge-types.html) -有关现有墨盒类型的概述.
-Gekkio的弹药筒分析：
  - [DMG-BEAN-02](http://gekkio.fi/blog/2015-05-18-mooneye-gb-cartridge-analysis-dmg-bean-02.html);
  - [MBC1](http://gekkio.fi/blog/2015-05-17-mooneye-gb-cartridge-analysis-fortress-of-fear.html);
  - [no MBC](http://gekkio.fi/blog/2015-02-28-mooneye-gb-cartridge-analysis-tetris.html).
-在Tauwasser的Wiki上引脚排列，注册描述和某些墨盒类型的VHDL代码：
  - [MBC1](https://wiki.tauwasser.eu/view/MBC1)
  - [MBC2](https://wiki.tauwasser.eu/view/MBC2)
  - [MMM01](https://wiki.tauwasser.eu/view/MMM01)
- [Game Boy Cartridges Schematics](http://www.devrs.com/gb/files/gb.html) -MBC2和MBC3类型的示意图.
- [Cartridges PCB photos](https://imgur.com/a/D5bpC)
- [MBC1+RAM+Battery cartridge Schematic](http://www.devrs.com/gb/files/mbc1.gif) -杰夫·弗罗韦恩（Jeff Frohwein）的第一幅原理图.
- [MBC1 and MBC2 cartridges circuits](http://fms.komkon.org/GameBoy/Tech/Carts.html) -以及有关这些MBC bank如何切换和控制RAM的说明.
- [GB Rom List](CartridgeList.csv) -发行的每个游戏的导航表，其中包含其墨盒的详细信息.
- [Game Boy cartridge PCB photos](http://gekkio.fi/blog/2016-03-19-game-boy-cartridge-pcb-photos.html)


#### Custom cartridges

- [Emulating a GameBoy Cartridge](https://dhole.github.io/post/gameboy_cartridge_emu_1/) -用开发板STM32F4模拟Game Boy弹药筒的功能.
- [Wolf](http://www.happydaze.se/wolf/) -带有协处理器的Game Boy弹药筒.
- [Homebrew-Gameboy-Cartridge](https://github.com/dwaq/Homebrew-Gameboy-Cartridge) -使用Atmel AT49F040作为ROM的墨盒PCB的Eagle库，原理图和电路板文件.
- [Homebrew Gameboy Color Cartridge](https://github.com/Xyl2k/Gameboy-Color-Cartridge) -EEPROM供电墨盒的电路板布局.
- [Nekocart](https://github.com/zephray/NekoCart-GB) -使用Xilinx CPLD作为MBC5的开源闪存盒（[Post](https://hackaday.io/project/41160-nekocart-cpld-gameboy-cartridge)).
- [Reiner Ziegler's Game Boy page](http://reinerziegler.de.mirrors.gg8.se/)  -商业和自制的可编程盒带和编程系统. 提供了教程，接线和原理图.
- [Gameboy-MBC5-MBC1-Hybrid](https://github.com/insidegadgets/Gameboy-MBC5-MBC1-Hybrid) -MBC5 / MBC1混合磁带的CPLD实现.

#### Misc

- [Introduction to Game Boy Hacking](http://pepijndevos.nl/sha2017/workshop.pdf) -讲习班，介绍基本的组装，调试和逆向工程.
- [GBSOUND.txt](https://github.com/bwhitman/pushpin/blob/master/src/gbsound.txt) -详细说明Game Boy声音引擎的文档.
- [gbdev FAQs](http://www.devrs.com/gb/files/faqs.html) -必须由Jeff Frohwein阅读.
- [Game Boy Bootrom](http://www.neviksti.com/DMG/DMG_ROM.asm) -评论了DMG bootrom的转储.
- [Differences between the Z80 and the gameboy's processor](http://www.z80.info/z80gboy.txt)
- [Gameboy 2BPP Graphics Format](http://www.huderlem.com/demos/gameboy2bpp.html) -有关Game Boy如何将VRAM切片数据解释为彩色像素的信息.

## Emulator Development


- [Reverse Engineering fine details of Game Boy hardware](https://www.youtube.com/watch?v=GBYwjch6oEE) -Gekkio在Disobey 2018上进行的43分钟演讲（[errata](https://gekkio.fi/blog/2018-02-05-errata-for-reverse-engineering-fine-details-of-game-boy-hardware.html)).
- [Emulation of Nintendo Game Boy](https://github.com/Baekalfen/PyBoy/blob/master/PyBoy.pdf) -从构建仿真器的角度概述Game Boy硬件.
- [DMG-01](https://rylev.github.io/DMG-01/public/book/)  -Rust中的教育性Gameboy模拟器和一本解释其发展的随书.  *[Oh Boy! Creating a Game Boy Emulator in Rust](https://media.ccc.de/v/rustfest-rome-3-gameboy-emulator)-在Rust Fest 18上对此进行了演讲.
- [Building a Game Boy emulator in JavaScript](http://imrannazar.com/gameboy-Emulation-in-JavaScript) -分步教程.
- [Writing a Game Boy emulator, Cinoop](https://cturt.github.io/cinoop.html)
- [0dmg](https://jeremybanks.github.io/0dmg/2018/05/23/getting-started.html) -通过构建部分Game Boy模拟器来学习Rust.
- [RealBoy Emulator](https://realboyemulator.wordpress.com/posts/) -有关RealBoy Emulator设计和实现的一系列文章.
- [Codeslinger](http://www.codeslinger.co.uk/pages/projects/gameboy.html) -另一系列的文章记录了模拟器的构建.
- [Why did I spend 1.5 months creating a Gameboy emulator?](http://blog.rekawek.eu/2017/02/09/coffee-gb/) -博客文章.
- [binjgb rewind](https://binji.github.io/2017/12/31/binjgb-rewind.html) -实施*倒带功能.
- [binjgb on the web](https://binji.github.io/2017/02/26/binjgb-on-the-web-part-1.html) -将binjgb仿真器移植到Web Assembly. [(Part 2)](https://binji.github.io/2017/02/27/binjgb-on-the-web-part-2.html)
- [binjgb debugging hangs](https://binji.github.io/2017/05/03/debugging-hangs.html) -对仿真怪癖的调查.
- [Decoding Gameboy Z80 opcodes](https://gb-archive.github.io/salvage/decoding_gbz80_opcodes/Decoding%20Gamboy%20Z80%20Opcodes.html) -如何对Game Boy指令进行算法解码（与编写一条巨大的switch-case语句相对）.
- [Porting a GO Game Boy emulator to WebAssembly](https://djhworld.github.io/post/2018/09/21/i-ported-my-gameboy-color-emulator-to-webassembly/)
- [About swotGB](https://mitxela.com/projects/swotgb/about) -有关使用JavaScript开发Game Boy模拟器的说明.
- [List of open source emulators](EMULATORS.md)

### Testing

- [Blargg's test roms](http://gbdev.gg8.se/files/roms/blargg-gb-tests/)
- [Gekkio's test roms](https://gekkio.fi/files/mooneye-gb/latest/)
- [SameSuite](https://github.com/LIJI32/SameSuite)
- [Mealybug Tearoom Tests](https://github.com/mattcurrie/mealybug-tearoom-tests)
- [GB Accuracy Tests](http://tasvideos.org/EmulatorResources/GBAccuracyTests.html)
- [144p Test Suite](https://github.com/pinobatch/240p-test-mini/tree/master/gameboy) -Artemio Urbina的240p测试套件移植到Game Boy.
- [MBC3 RTC test ROM](https://github.com/aaaaaa123456789/rtc3test)
- [dmg-acid2](https://github.com/mattcurrie/dmg-acid2) 和 [cgb-acid2](https://github.com/mattcurrie/cgb-acid2) -基本的PPU渲染测试.

## Software Development

The [To C Or Not To C](https://gist.github.com/ISSOtm/4f4d335c3fd258ad0dfc7d4d615409fd) 文章概述了Game Boy的功能，讨论了可用开发工具的优缺点，并提供了编写更高效代码的技巧.

### Assemblers

- [RGBDS](https://github.com/gbdev/rgbds) -汇编程序和链接程序包. [Documentation](https://rgbds.gbdev.io/docs/).
- [ASMotor](https://github.com/csoren/asmotor)  -针对Game Boy等其他CPU的汇编器引擎和开发系统. 由原始RGBDS作者编写. [Documentation](https://github.com/asmotor/asmotor/tree/develop#further-reading).
- [wla-dx](https://github.com/vhelin/wla-dx) -另一个GB-Z80 / Z80 / ...多平台交叉汇编程序包. [Documentation](http://www.villehelin.com/wla.txt).

### Compilers

- [GBDK](http://gbdk.sourceforge.net/)  -一套可以在** C **中进行开发的工具. 包括一组最常见要求的库，并生成就绪的ROM文件. 上次更新时间为2001年. [Documentation](http://gbdk.sourceforge.net/doc/gbdk-doc.pdf).
  - [GBDK-2020](https://github.com/Zal0/gbdk-2020/)  -具有更新的SDCC工具链（支持ROM库），错误修复，文档和其他改进的现代化GBDK. 支持Windows，Linux和macOS.
  - [gbdk-osx](https://github.com/x43x61x69/gbdk-osx) -为macOS上的最新编译器修补了GBDK 2.96a.
  - [gbdk-n](https://github.com/rotmoset/gbdk-n)  -旨在更新gbdk库以使其与新版本的SDCC兼容，并为构建rom提供帮助. 不支持ROM库，因此将ROM大小限制为32K.
- [Turbo Rascal Syntax Error](https://lemonspawn.com/turbo-rascal-syntax-error-expected-but-begin/) -完整的套件（IDE，编译器，编程语言，资源编辑器），用于为8/16位系列的计算机（包括Game Boy和Game Boy Color）开发游戏/演示.

#### Experimental/Proof of Concepts

- [RGBDS-Live](https://daid.github.io/rgbds-live/) -浏览器内编码环境，可试用RGBDS.
- [Wiz](https://github.com/wiz-lang/wiz) -一种高级汇编语言，用于在复古控制台平台（Game Boy，NES，Atari 2600等）上编写自制程序.
- [gbforth](https://github.com/ams-hackers/gbforth) -基于Forth的Game Boy开发套件.
- [gbasm-rs](https://gitlab.com/BonsaiDen/gbasm-rs) -为Game Boy z80汇编代码使用的基于Rust的编译器.
- [gbasm](https://github.com/BonsaiDen/gbasm) -用于Game Boy z80汇编代码的基于JavaScript的编译器.
- [tniASM](http://www.tni.nl/products/tniasm.html) -宏汇编器.
- [Assembler](https://github.com/ulrikdamm/Assembler) -用Swift编写的汇编器.
- [llvm-gbz80](https://github.com/Bevinsky/llvm-gbz80) / [clang-gbz80](https://github.com/Bevinsky/clang-gbz80) -GBZ80 CPU的Clang / LLVM端口（类似于已弃用的端口） [euclio/llvm-gbz80](https://github.com/euclio/llvm-gbz80)).
- [gbdk-go](https://github.com/pokemium/gbdk-go)  -编译器将Go程序转换为C代码. 输出的C代码由GBDK内置到GB ROM中.

### Emulators

- [BGB](https://bgb.bircd.org/)  -强大的仿真器和调试器. 提供准确的硬件仿真.
- [SameBoy](https://github.com/LIJI32/SameBoy) -精确的仿真器，具有各种强大的调试功能.
- [Mooneye GB](https://github.com/Gekkio/mooneye-gb) -Rust中的研究项目和仿真器.
- [mGBA](https://github.com/mgba-emu/mgba) -现代化的跨平台GBA模拟器，该模拟器还运行GB / GBC游戏.
- [Binjgb](https://github.com/binji/binjgb)  -通过大多数测试的5Kloc模拟器.  *倒带功能. 使用WebAssembly在浏览器中运行.
- [Gambatte](https://github.com/sinamas/gambatte) -跨平台和准确的模拟器.
- [MetroBoy](https://github.com/aappleby/MetroBoy) -整个Game Boy的可播放的电路级仿真.
- [gbe-plus](https://github.com/shonumi/gbe-plus) -最近重写的仿真器，它在保留晦涩的附件（例如IR链接，移动网络GB，条形码男孩，GB打印机，本地和在线GB串行链接电缆等）上付出了巨大的努力.
- [Emulicious](https://emulicious.net/) - Provides accurate emulation and includes powerful tools such as a profiler and source-level debugging for ASM and C via a [VS Code debug adapter](https://marketplace.visualstudio.com/items?itemName=emulicious.emulicious-debugger).

[Complete list of open source emulators](EMULATORS.md)

### Tools

#### Engines

- [ZGB](https://github.com/Zal0/ZGB) -一个为原始Game Boy创建游戏的小引擎（扩展了gbdk，更多信息 [here](http://zalods.blogspot.com/2017/01/zgb-little-engine-for-game-boy.html)).
- [Retr0 GB](https://bitbucket.org/HellSuffering/retr0-gb/) -用于创建游戏的引擎（扩展了GBDK）.

#### Development tools

- [GBExtended](http://www.tensi.eu/thomas/programming/gameboy/gbextended.html) -扩展gbdk的C库.
- [gbdk-lib-extension](https://github.com/ProGM/gbdk-lib-extension) -迈克尔·霍普（Michael Hope）提供的有关Game Boy Development Kit的一小部分资源和工具.
- [Dot Matrix Game Editor](http://www.dotmatrixgame.com/) - An IDE for Game Boy programming in a C-like language called GBL, with many other features like tile and map extraction, WLA-DX assembly, and more.
- [mgbdis](https://github.com/mattcurrie/mgbdis) -具有RGBDS兼容输出的Game Boy ROM拆装器.
- [ROM Header Utility](http://catskull.net/GB-Logo-Generator/) -用于检查和修改ROM​​标头数据（包括徽标）的在线工具.
- [romusage](https://github.com/bbbbbr/romusage)  -命令行工具，用于从.map，.noi或ihx文件估计Game Boy ROM的使用（可用空间）. 与GBDK-2020和RGBDS一起使用.
- [awake](https://github.com/devdri/awake) -Game Boy反编译器.
- [Game Boy Text Tools](https://github.com/raphaklaus/gameboy-text-tools) -用Node.js编写的用于文本操作和Game Boy ROM的翻译工具集.

#### Graphics utilities

- [Game Boy Tile Data Generator](https://github.com/chrisantonellis/gbtdg) -HTML5 / JS Web应用程序，它将位图图像转换为适合在基于图块的图形应用程序（特别是GB）中使用的十六进制数据.
- [Harry Mulder's GB Development](http://www.devrs.com/gb/hmgd/intro.html) -Game Boy Tile Designer（GBTD）和Game Boy Map Builder（GBMB）工具的一些来源和主页.
- [GBTiles](https://github.com/bashaus/gbtiles) -将使用Harry Mulder的Tile Designer（GBTD）创建的.GBR文件和使用Harry Mulder的Map Builder（GBMB）创建的.GBM文件转换为与Game Boy和GBDK一起使用的不同格式.
- [bmp2cgb](https://github.com/gitendo/bmp2cgb) -用于Game Boy Color开发的图形转换器，提供实时调色板调整.
- [png2gb](https://github.com/LuckyLights/png2gb) -CLI工具，可将图像文件转换为游戏男孩.c数组.
- [GB-convert](https://github.com/exezin/gb-convert) -Game Boy磁贴转换和地图编辑器工具（转换为装配体）.
- [brewtool](http://make.vg/brewtool/) -原始编辑器/转换器工具的集合，用于使资产与自制ROM开发一起使用.
- [vtGBte](https://github.com/paul-arutyunov/vtGBte) -简约的ncurses磁贴编辑器.
- [tpp1](https://github.com/TwitchPlaysPokemon/tpp1) -自定义GB / GBC内存/硬件映射器的定义和规范，作为MBC的功能超集.
- [libstdgb](https://github.com/delwink/libstdgb) -有用的Game Boy操作（SDCC）的AC库.
- [Tilemap GB](https://github.com/bbbbbr/gimp-tilemap-gb) -GIMP图像编辑器插件，用于导入和导出GBMB和GBTD磁贴图和磁贴集（作为位图图像或.GBM / .GBR文件）.
- [Tilemap Helper](https://github.com/bbbbbr/gimp-tilemap-helper) -GIMP图像编辑器插件，用于优化图块地图和图块集.
- [Tilemap Studio](https://github.com/Rangi42/tilemap-studio)  -Game Boy，Color，Advance和SNES项目的图块编辑器. 用C ++和FLTK编写. 
- [Superfamiconv](https://github.com/Optiroc/SuperFamiconv) -灵活且可组合的图块图形转换器，支持超级任天堂，Game Boy，Game Boy Color，Game Boy Advance，Mega Drive和PC Engine格式.

#### Hardware and ROM utilities

- [cart-dumper](https://github.com/Palmr/cart-dumper) -游戏男孩墨盒翻斗ROM.
- [gbcamextract](https://github.com/jkbenaim/gbcamextract) -从“游戏男孩相机”保存中提取照片.
- [Game Boy LCD sniffing](https://github.com/svendahlstrand/game-boy-lcd-sniffing) -使用逻辑分析仪嗅探游戏男孩的LCD.
- [swapdump](https://github.com/sanqui/swapdump) -Game Boy Flashcarts的诊断实用程序.
- [Gameboy-LinkUp](https://github.com/JustinLloyd/Gameboy-LinkUp) -Game Boy LinkUp串行电缆网络项目.

#### Music drivers and trackers

- [DevSound](https://github.com/DevEd2/DevSound) -声音驱动程序可嵌入到自制软件中，支持脉冲宽度控制，琶音和多种波形.
- [Carillon Player](http://gbdev.gg8.se/files/musictools/Aleksi%20Eeben/Carillon%20Editor.zip) -音乐引擎.
- [GBT PLAYER](https://github.com/AntonioND/gbt-player) -音乐播放器库和转换器套件.
- [mmlgb](https://github.com/SimonLarsen/mmlgb) -Nintendo Game Boy的MML解析器和GBDK声音驱动程序.
- [XPMCK](https://github.com/bazzinotti/XPMCK) -基于MML的音乐编译器，支持Game Boy和Game Boy Color.
- [SoundSystem](https://github.com/BlitterObjectBob/GBSoundSystem) -GameBoy Tracker（又名Paragon 5音乐播放器）的现代化音频驱动程序.
- [hUGETracker](https://github.com/SuperDisk/hUGETracker) -基于OpenMPT的音乐跟踪器，专注于易用性，紧凑的输出以及在自制游戏中的可嵌入性.

## Programming

使用以下内容中所述的开发工具链为Game Boy开发软件的指南，教程和工具. [Software Development](#software-development) 章节.

### ASM

- **[gb asm tutorial](https://eldred.fr/gb-asm-tutorial)**-分步教程，建立一些ROM并附带其解释.
- [ASMSchool](http://gameboy.mongenel.com/asmschool.html) -Duo的一组有关GB / GBC汇编中的编码和反汇编的课程.
- [hardware.inc](https://github.com/tobiasvl/hardware.inc) -标准包含文件，其中包含用于RGBDS项目的Game Boy硬件定义.
- [Assembly tutorial by David Pello](https://gb-archive.github.io/salvage/tutorial_de_ensamblador/tutorial_de_ensamblador_la_decadence.html)  -学习如何为gb生成有效的asm代码的好文档. 对许多重要主题的简要说明. 许多带有注释源代码的示例.
- [assemblydigest](https://github.com/assemblydigest/gameboy) -探索Game Boy编程技术：
  - [Making an Empty Game Boy ROM (in Wiz)](http://assemblydigest.tumblr.com/post/77203696711/tutorial-making-an-empty-game-boy-rom-in-wiz)
  - [Making Art for the Game Boy](http://assemblydigest.tumblr.com/post/77404621743/tutorial-making-art-for-the-game-boy)
- [Beginner's Guide to Reverse Engineering GB](http://web.archive.org/web/20150511145100/http://www.bennvenn.com/Beginners_Guide_To_Reverse_Engineering.htm) -有关拆卸和逆向工程的一些入门技巧.
- [FlappyBoy: Making a simple Game Boy Game](http://voidptr.io/blog/2017/01/21/GameBoy.html)
- [Super Game Boy development](https://imanoleasgames.blogspot.no/2016/12/games-aside-1-super-game-boy.html) -逐步教程，以实现“超级游戏男孩”功能（框架和调色板）.
- [GameBoy programming tutorial: Hello World!](https://peterwynroberts.wordpress.com/2014/05/11/gameboy-programming-tutorial-hello-world/) -分步教程.
- [DMGreport](https://github.com/lancekindle/DMGreport) -汇编中的游戏编程教程.
- [OAM DMA tutorial](https://exez.in/gameboy-dma) -如何在装配中使用OAM DMA的示例.
- [Game Boy Assembly Programming for the Modern Game Developer](https://github.com/ahrnbom/gbapfomgd) -有关在汇编中制作Game Boy游戏的电子书.

#### Sources

代码片段，效果，概念证明以及通常不完整的游戏.

- [dev'rs ASM section](http://www.devrs.com/gb/asmcode.php) -许多有效的演示和资源.
- [EmmaEwert's experiments](https://github.com/EmmaEwert/gameboy)  -原型程序的集合，大部分只是在玩玩. 其中包括日光效果，透明度和天气效果.
- [DeadCScroll](https://github.com/BlitterObjectBob/DeadCScroll) -有关如何使屏幕摆动以及其他“光栅效果”的详细教程

#### Timings

- [Nitty Gritty Gameboy Cycle Timing](http://blog.kevtris.org/blogfiles/Nitty%20Gritty%20Gameboy%20VRAM%20Timing.txt)
- [Mode3 Sprite Timing](https://www.reddit.com/r/EmuDev/comments/59pawp/gb_mode3_sprite_timing/)
- [GameBoy Color DMA-Transfers v0.0.1](http://gameboy.mongenel.com/dmg/gbc_dma_transfers.txt)
- [STAT interrupt timings](http://gameboy.mongenel.com/dmg/istat98.txt)
- [Video Timing](https://github.com/jdeblese/gbcpu/wiki/Video-Timing)

#### Boilerplates and libraries

- [gb-template](https://github.com/exezin/gb-template) -具有基本功能的模板，例如游戏手柄输入，DMA传输和地图/平铺数据加载.
- [rgbds-template](https://github.com/nezticle/rgbds-template) -使用RGBDS的Game Boy的基本hello-world示例.
- [Game Boy Assembly Language Primer](http://www.devrs.com/gb/files/galp.zip) -具有内存定义，复制例程和IBM字体tilemap的简单模板代码.
- [bootstrap.gb](https://github.com/yenatch/bootstrap.gb) -一个示例Game Boy项目.
- [Gameboy Boilerplate](https://github.com/junebug12851/GameboyBoilerplateProj) -Boilerplate项目，可更快地进入游戏的实际汇编代码.
- [GingerBread](https://github.com/ahrnbom/gingerbread)  -用于制作自己的Game Boy游戏的软件库. 它可以与书一起使用 [Game Boy Assembly Programming for the Modern Game Developer](https://github.com/ahrnbom/gbapfomgd) 它也可以作为文档使用.
- [gb-vwf](https://github.com/ISSOtm/gb-vwf) -可以打印可变宽度文本的库，并带有一个演示.
- [gb-boilerplate](https://github.com/ISSOtm/gb-boilerplate) -用于启动Game Boy项目的模板，为基础结构提供Makefile.
- [gb-starter-kit](https://github.com/ISSOtm/gb-starter-kit) -对上述内容的扩展，包括基本库代码，也可以更快上手.

#### Syntax highlighting packages

- [Atom language package for RGBASM](https://atom.io/packages/language-rgbasm) -RGBDS汇编的Atom语法突出显示.
- [gbz80-highlight](https://github.com/ISSOtm/gbz80-highlight) -用于RGBDS汇编的Notepad +-和gedit语法高亮文件.
- [Vim syntax file for the Game Boy assembler RGBASM](http://www.vim.org/scripts/script.php?script_id=819) -RGBDS汇编的Vim语法突出显示.
- [Vim syntax file for RGBDS](https://github.com/Leandros/dotfiles/blob/master/.vim/syntax/rgbds.vim) -另一个用于RGBDS汇编的Vim语法突出显示文件.
- [sublime-rgbds](https://packagecontrol.io/packages/RGBDS) -用于RGBDS的Sublime Text 3软件包，包括语法突出显示和一些完成摘要.
- [Z80 Assembly support for Visual Studio Code](https://github.com/Imanolea/z80asm-vscode)
- [rgbds-vscode](https://github.com/DonaldHays/rgbds-vscode) -RGBDS GBZ80组件的Visual Studio代码语言扩展.
- [rgbds-mode](https://github.com/japanoise/rgbds-mode) -用于RGBDS组装的Emacs主要模式.

### C

- [8-Bit Wonderland](https://github.com/gb-archive/salvage/blob/master/misc/8bit_wonderland.pdf) -关于Game Boy的工作原理以及如何开始为其开发有效代码的引人入胜的入门文档.
- [Grooves Game Boy Programming](https://github.com/gbdk-salvage/grooves-game-boy-programming) -有关在Game Boy游戏中实现各种游戏机制的完整课程.
- [How to Write a Simple Side Scrolling Game](http://pastebin.com/F3tHLj68) -旧的（但仍然有用）教程.
- [Just another simple tutorial](http://pastebin.com/gzT47MPJ)
- [GBDK Tutorial](https://refreshgames.co.uk/2016/04/18/gameboy-tutorial-rom/) -入门GBDK的游戏演示相当少.
- [GBDK Sprite](http://gbdev.gg8.se/wiki/articles/GBDK_Sprite_Tutorial) -提出了用于显示和设置多个精灵的工作流.
- [GBDK Color](http://gbdev.gg8.se/wiki/articles/GBDK_Color_Tutorial) -通过向精灵，背景和窗口图层添加颜色，扩展了您对Game Boy基本拼写的知识.
- [GBDK Joypad](http://gbdev.gg8.se/wiki/articles/GBDK_Joypad_Tutorial) -详细介绍了将手柄与GBDK配合使用的方法.
- [Game Boy home of Flavor](http://www.personal.triticom.com/~erm/GameBoy/) -一些完整的游戏和资源.
- [GBDK Configuring and Programming Tutorial](https://videlais.com/2016/07/03/programming-game-boy-games-using-gbdk-part-1-configuring-programming-and-compiling/) -配置GBDK，使用图块，碰撞精灵，GBTD，GBMB，内存管理和ROM Banking.
- [Simplified GBDK examples](https://github.com/mrombout/gbdk_playground)
- [GBDK Programming Video Tutorials](https://www.youtube.com/playlist?list=PLeEj4c2zF7PaFv5MPYhNAkBGrkx4iPGJo) -一系列视频教程，向初学者介绍GBDK编程.

## Homebrews

完整和开源的游戏.

- [Homebrew Hub](https://gbhh.avivace.com) -为Game Boy制作的每一种非官方的自制软件都可以在线玩（也可以通过移动/触摸）：社区领导尝试收集，存档和保存由该社区制作的Game Boy（Color）的所有非官方游戏，自制软件，演示，补丁，hackrom通过多年的热情工作.

### ASM

- [Tuff](https://github.com/BonsaiDen/Tuff.gb)
- [2048-gb](https://github.com/Sanqui/2048-gb)
- [Snake](https://bitbucket.org/Sanqui/snake/src/?at=master)
- [PlantBoy](https://github.com/siObyte/PlantBoy)
- [Lazerpong](https://github.com/huderlem/lazerpong)
- [Geometrix](https://github.com/AntonioND/geometrix)
- [µCity](https://github.com/AntonioND/ucity)
- [Carazu](https://github.com/mholtkamp/carazu)
- [Snake-gb](https://github.com/DonaldHays/snake-gb)
- [GB303](https://github.com/furrtek/GB303) -用于任天堂Game Boy的基于GB303波形表的TB-303风格合成器.
- [Sushi](https://github.com/JustSid/Sushi)
- [Flappy-boy-asm](https://github.com/bitnenfer/flappy-boy-asm)
- [kupman](https://github.com/dubvulture/gbdev) 和其他一些项目.
- [Adjustris](https://github.com/tbsp/Adjustris)
- [exeman](https://github.com/exezin/exeman/)
- [Aevilia](https://github.com/ISSOtm/Aevilia-GB)
- [GBSlides](https://github.com/Kartones/gameboy) -一个简单的类似Game Boy Powerpoint的幻灯片查看器.
- [Pokered-gbc](https://github.com/dannye/pokered-gbc) -完全通过GBC支持对PokémonRed进行了重新制作.
- [ToyToy](https://github.com/tslanina/Retro-GameBoyColor-ToyToy)
- [StefaN](https://github.com/tslanina/Retro-GameBoyColor-StefaN) -Fourway Breakout克隆.
- [Galaxia](https://github.com/tslanina/Retro-GameBoyColor-Galaxia)
- [desgb](https://github.com/sanqui/desgb) -DES加密.
- [superhappyfunbubbletime](https://github.com/l0k1/superhappyfunbubbletime)
- [minesweepGB](https://github.com/lancekindle/minesweepGB)
- [Libbet and the Magic Floor](https://github.com/pinobatch/libbet)
- [waveform-gb](https://github.com/dannye/waveform-gb)  -程序可视化波浪通道使用的波形. 波形可以自由编辑，并且波形的回放会立即更新.
- [vectroid.gb](https://gitlab.com/BonsaiDen/vectroid.gb) -用gbasm开发.

### C

- [FlappyBoy](https://github.com/bitnenfer/FlappyBoy)
- [flappybird-gameboy](https://github.com/pashutk/flappybird-gameboy)
- [fbgb](https://github.com/gb-archive/fbgb)
- [Novascape](http://ludumdare.com/compo/ludum-dare-34/?action=preview&uid=6823)
- [Squishy the Turtle](https://github.com/cppchriscpp/SquishyTheTurtle)
- [Quadratino](https://github.com/avivace/quadratino)
- [Doctor How](https://github.com/elfgames/doctorhow)
- [Super Princess' 2092 Exodus](https://github.com/Zal0/gbjam2016)
- [GBsnake](https://github.com/brovador/GBsnake)
- [gb-mines](https://github.com/andreasjhkarlsson/gb-mines)
- [oranges](http://www.atari2600land.com/gameboy/oranges.html)
- [red hot princess carnage](https://github.com/Imanolea/bitbitjam3_red_hot_princess_carnage)
- [loderunner](http://www.tensi.eu/thomas/programming/gameboy/loderunner.html)
- [Hives](https://refreshgames.co.uk/2017/04/24/ludum-dare-38-entry-hives/)
- [Bubble Factory](https://github.com/DonaldHays/bubblefactory) -*香草-SDCC（无gbdk）.
- [GBC Atari Boxing](https://github.com/rubfi/gbc-atari-boxing) -游戏男孩（彩色）的Atari 2600拳击副本.
- [GB raycaster, Vision-8](https://github.com/haroldo-ok/really-old-stuff/tree/master/gameboy) -和其他一些项目.
- [Tobu Tobu Girl](https://github.com/SimonLarsen/tobutobugirl) -游戏男孩的街机平台游戏.
- [Burly Bear vs. The Mean Foxes](http://sebastianmihai.com/main.php?t=18&) ([GBC](http://sebastianmihai.com/main.php?t=55&n=Gameboy-Color-development-Burly-Bear-vs-The-Mean-Foxes-GBC-version) 港口）
- [PostBot](https://github.com/MasterIV/PostBot)
- [Guns & Riders](https://github.com/kanfor/gunsridersgameboy)
- [Dino's Offline Adventure](https://github.com/gingemonster/DinosOfflineAdventure) -Google Chrome离线游戏的克隆版本.
- [dino-gb](https://github.com/rnegron/dino-gb) -Chrome游戏的另一个副本.
- [Evoland.gb](https://github.com/flozz/evoland.gb) -Evoland一级港口.
- [Petris](https://github.com/bbbbbr/Petris) -身材匀称的宠物的益智游戏，适用于Game Boy Color（[itch.io](https://bbbbbr.itch.io/petris)).
- [Infinity](https://github.com/gb-archive/infinity-gbc)  -由Affinix Software开发的RPG，主要是在1999年至2001年之间开发的.该游戏从未找到发行商，并最终被取消了. 最近发布了完整的源代码，开发工具和工作流程.

### Demos

- [Back to Color](https://github.com/AntonioND/back-to-color)
- [beach-gbc](https://github.com/vegard/beach-gbc)
- [CUTE DEMO](https://github.com/mills32/CUTE_DEMO)
- [`10 PRINT` Game Boy](https://github.com/svendahlstrand/10-print-game-boy)
- [Roboto Demo](https://github.com/naavis/roboto-demo)
- [matrix-rain-gb](https://github.com/wtjones/matrix-rain-gb) -汇编程序中的矩阵数字雨效果.
- [GBVideoPlayer](https://github.com/LIJI32/GBVideoPlayer) -一个技术演示，演示了如何破解Game Boy LCD控制器以使Game Boy Color可以播放彩色全动态视频以及音乐.
- [GBVideoPlayer2](https://github.com/LIJI32/GBVideoPlayer2) -以上演示的第二次迭代，提高了分辨率，添加了“立体声PCM音频”，并引入了视频压缩*.

## Reverse Engineering

- [Reverse engineering Kirby's Dreamland 2](http://ecc-comp.blogspot.it/2016/03/reverse-engineering-kirbys-dreamland-2.html)
- [pokemontools](https://github.com/pret/pokemon-reverse-engineering-tools) -一个python模块，可为各种神奇宝贝游戏提供各种逆向工程组件.
- [Reverse Engineering a Gameboy ROM with radare2](https://www.megabeets.net/reverse-engineering-a-gameboy-rom-with-radare2) -使用radare2对Game Boy ROM挑战进行逆向工程的演练.
- [Disassembling Link's Awakening](http://kemenaran.winosx.com/posts/category-disassembling-links-awakening/) -一系列有关拆卸Link&#39;s Awakening DX的博客文章.
- [Reverse Engineering the GameBoy Tetris](https://github.com/h3nnn4n/Reverse-Engineering-the-GameBoy-Tetris)
- [DMA hijacking](https://github.com/avivace/awesome-gbdev/blob/master/articles/dma_hijacking.md) -一种简单的技术，允许您在大多数GB / SGB / CGB游戏中运行自定义代码，前提是您具有ACE漏洞利用功能.

### Game Disassemblies

- [Pokémon Red/Blue](https://github.com/pret/pokered)
- [Pokémon Crystal](https://github.com/pret/pokecrystal)
- [Pokémon Yellow](https://github.com/pret/pokeyellow)
- [Pokémon Gold and Silver](https://github.com/pret/pokegold)
- [Pokémon Pinball](https://github.com/pret/pokepinball)
- [Pokémon TCG](https://github.com/pret/poketcg)
- [pokegold-spaceworld](https://github.com/pret/pokegold-spaceworld) -《神奇宝贝》金银奖1997年太空世界演示.
- [Link's Awakening DX](https://github.com/mojobojo/LADX-Disassembly)
- [Oracle of Ages](https://github.com/drenn1/ages-disasm)
- [Tetris](https://github.com/osnr/tetris) -基于Jeff Frohwein的原始分解.
- [FX Hammer](https://github.com/DevEd2/FXHammer-Disasm)
- [Harvest Moon 3](https://github.com/sanqui/hm3)

## Game Boy Camera

### Retrieving images

游戏男孩打印机仿真（例如，从相机中检索图像）：

- [Arduino Gameboy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator) -通过游戏机链接电缆模拟游戏机打印机. 
- [ESP8266 Game Boy Printer](https://github.com/applefreak/esp8266-gameboy-printer) -一种模仿Gameboy打印机的设备，可让您使用由ESP8266供电的WiFi检索图像.
- [WiFi GBP Emulator](https://github.com/HerrZatacke/wifi-gbp-emulator) -GameBoy打印机仿真器，可通过WiFi连接提供接收到的数据.
- [Game Boy WiFi Printer - D1 Mini Shield](https://github.com/cristofercruz/gbp-esp-shield-pcb) -Game Boy打印机接口护板，用于D1 mini / mini Pro ESP8266板. 
- [Game Boy Printer Sniffer](https://github.com/mofosyne/GameboyPrinterSniffer) -游戏男孩和打印机之间的嗅探数据包通信.

### Changing the camera's behavior

改善和/或控制相机质量和行为的方法：

- [Game Boy Camera Canon EF Lens Mount](http://ekeler.com/game-boy-camera-canon-ef-mount)
- [Game Boy Camera to Canon Lens mount](https://www.thingiverse.com/thing:4337362) -基于上述内容.
- [game-boy-camera-frame-replacer](https://github.com/cristofercruz/game-boy-camera-frame-replacer) -操纵相机的ROM以包含自定义帧

### Post processing

- [Game Boy Printer Paper Simulation](https://github.com/mofosyne/GameboyPrinterPaperSimulation) -生成数字印刷图像的印刷图像.
- [Game Boy Printer Web](https://github.com/HerrZatacke/gb-printer-web) -适用于Game Boy相机的Gallery应用：从导出或墨盒转储中导入图片，并选择调色板.
- [lbcam](https://lbcam.xyz/) -用网络摄像头模拟Game Boy Camera.

## Related projects

- [ArduinoBoy](https://github.com/trash80/Arduinoboy) -从Arduino到Game Boy的串行通信（MIDI），用于音乐应用程序，例如LittleSoundDJ，Nanoloop和mGB.
- [papiGB](https://github.com/diegovalverde/papiGB) -从头开始Game Boy Classic的全功能FPGA实现.
- [fpgaboy](https://github.com/trun/fpgaboy) -在FPGA上实现任天堂的Game Boy控制台.
- [Piglet](https://github.com/danShumway/Piglet)  -由LUA驱动的AI，可通过实验来玩经典的Game Boy彩色游戏. 在积极发展中.
- [Gatesboy](https://web.archive.org/web/*/http://www.gatesboy.com/) -非游戏用途的应用程序开发.
- [Ostrich](https://github.com/PumpMagic/ostrich) -用Swift编写的Game Boy音响系统玩家.
- [mGB](https://github.com/trash80/mGB) -Game Boy盒带程序，使Game Boy可以充当受MIDI支持的完整声音模块.
- [GBVisualizer](https://github.com/LIJI32/GBVisualizer) -演示使用两个未公开记录的Game Boy Color寄存器，分别称为PCM12（FF76）和PCM34（FF77），可用于读取4个APU通道的当前PCM幅度.
- [ArduinoGameBoy](https://github.com/drhelius/arduinogameboy) -基于Arduino的Game Boy弹药筒读取器和写入器.
- [gameboy-brainfuck](https://github.com/bitnenfer/gameboy-brainfuck) -Brainf * ck口译员.
- [gbfk](https://github.com/elseyf/gbfk) -Brainf * ck解释器，带有输入.
- [gb-save-states](https://github.com/mattcurrie/gb-save-states) -修补程序，用于在原始硬件上播放时为Game Boy游戏添加保存状态支持.
- [gbcpu](https://github.com/jdeblese/gbcpu) -实现Game Boy指令集和功能的CPU和外围设备.
- [Digitized Speech in Game Boy Games](https://youtube.com/watch?v=1lzHfLYzyRM)
- [Sniffing Game Boy serial traffic with an STM32F4](https://dhole.github.io/post/gameboy_serial_1/)
- [Virtual Game Boy Printer with an STM32F4](https://dhole.github.io/post/gameboy_serial_2/)
- [Printing on the Game Boy Printer using an STM32F4](https://dhole.github.io/post/gameboy_serial_3/)
- [Programming Game Boy Chinese cartridges with an STM32F4](https://dhole.github.io/post/gameboy_cartridge_rw_1/)
- [Pokemon Pocket Computer:](https://tilde.town/~minerobber/techwriteups/pokemonpc.html) -它是什么以及如何使用它制作作弊代码.
- [Booting the Game Boy with a custom logo](https://dhole.github.io/post/gameboy_custom_logo/) -绕过Nintendo徽标检查.
 -在2017年制作Game Boy游戏：“ Sheep It！” 事后[part 1](https://www.gamasutra.com/blogs/DoctorLudos/20171207/311143/), [part 2](https://www.gamasutra.com/blogs/DoctorLudos/20180213/314554/))
- [Nintendo's fake logos](http://fuji.drillspirits.net/?post=87) -每个墨盒都必须显示真实徽标，才能被认为是有效的并且可以运行，但是很显然，有些公司设法利用了支票系统.
- [liblsdj](https://github.com/stijnfrishert/liblsdj) -用于与LSDj保存格式（.sav），歌曲文件（.lsdsng）等交互的实用程序库.
- [lsdpatch](https://github.com/jkotlinski/lsdpatch) -用于修改LSDj ROM映像上的样本，字体和调色板的工具.
- [Game Boy video effects](https://github.com/ChaosCabbage/crazy-gameboy-video-experiments) -使用STAT中断进行有趣的视频操作的一些小实验.
- [gbos](https://github.com/ekimekim/gbos) -Game Boy的基本操作系统.
- [Work Master OS](https://translate.google.com/translate?hl=&sl=ru&tl=en&u=https%3A%2F%2Fweb.archive.org%2Fweb%2F20081226145726%2Fhttp%3A%2F%2Fworkmaster.ru%2Findex.php%3Fp%3D8&sandbox=1) -俄罗斯多任务操作系统.
- [Game Boy Link Cable Breakout Board](https://github.com/Palmr/gb-link-cable)
- [GBCartFlasher firmware](https://github.com/Tauwasser/GBCartFlasher)
- [VerilogBoy](https://github.com/zephray/VerilogBoy/) -Game Boy兼容控制台Verilog RTL实现.
- [GBCamcorder](https://github.com/furrtek/GBCamcorder) -使用GameBoy相机卡盒的Lo-Fi便携式录像机.
- [GBCartRead](https://github.com/insidegadgets/GBCartRead) -从/向GameBoy弹药筒读取ROM，读取RAM或写入RAM.
- [GBxCart-RW](https://github.com/insidegadgets/GBxCart-RW) -一种用于读取游戏ROM，保存游戏并通过USB从PC上保存GB，GBC和GBA购物车的设备.
- [GB Studio](https://www.gbstudio.dev/) -简单，无需知识的可视化脚本拖放游戏创建者.
- [Dumping the Super Game Boy Boot ROM](http://www.its.caltech.edu/~costis/sgb_hack/)

### Directories

- [Archive of related files](http://gbdev.gg8.se/files/)
- [The Game Boy Archive](https://github.com/gb-archive)  -与Game Boy相关的软件，硬件和资料库. 旨在反映和保留过去三十年来的零碎旧捐款.
- [The Game Boy Archive - Salvage](https://github.com/gb-archive/salvage) -软件，旧文章，常见问题解答和各种文档的历史存档.

### Websites

- [devrs.com/gb](http://devrs.com/gb) -场景的故乡：示例，源代码，完整的文档，指南，教程和各种工具.
- [pdroms.de](http://pdroms.de/news/gameboy/) -游戏男孩发布.
- [Handheld Underground](http://hhug.me) -未经许可的游戏，有关hboyboy模拟器之家Game Boy的博客文章.


## About

### Contribute

看一眼 [Contribution Guidelines](CONTRIBUTING.md).

### License

根据** GPLv3 **许可.
See [LICENSE](LICENSE) 想要查询更多的信息.

### Acknowledgements

谢谢 [every](https://github.com/avivace/awesome-gbdev/graphs/contributors) 该项目的贡献者，Jeff Frohwein，Pascal Felber，KOOPa，Pan of Anthrox，GABY，Marat Fayzullin，Paul Robson，BOWSER，neviksti，Martin“ nocash” Korth，Nitro2k01，Duo，Chris Antonellis，Michael Hope，当心，Jonathan“ Lord梦” Gevaryahu，Carsten Sorense，SindreAamås，Otaku No Zoku，GeeBee.

### Sponsors

特别感谢我们的朋友 [DigitalOcean](https://www.digitalocean.com/)，赞助我们Game Boy Development社区（[announcement](https://twitter.com/avivace4/status/992188011990409216)).
