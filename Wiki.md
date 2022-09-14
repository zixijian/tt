# TINTIN++中文手册

> 日拱一卒，功不唐捐。  
技术交流 QQ 群：951665549。

# 导航

|[ 总览 ](#总览)
|[ 快速上手 ](#快速上手)
|[ 关于 ](#关于)|  
|[ Action ](#action)
|[ Alias ](#alias)
|[ All ](#all)|  
|[ Bell ](#bell)
|[ Break ](#break)
|[ Buffer ](#buffer)
|[ Button ](#button)|  
|[ Case ](#case)
|[ Cat ](#cat)
|[ Characters ](#characters)
|[ Chat ](#chat)|  
|[ Class ](#class) 
|[ Colors ](#colors)
|[ Cr ](#cr)|  
|[ Commands](#commands) 
|[ Config ](#config) 
|[ Continue ](#continue)|  
|[ Coordinates ](#coordinates)
|[ Cursor ](#cursor)|  
|[ Daemon ](#daemon)|  
|[ Debug ](#debug)
|[ Default ](#default)
|[ Delay ](#delay)
|[ Draw ](#draw)|  
|[ Echo ](#echo)
|[ Else ](#else)
|[ Edit](#edit)
|[ Editing ](#editing)|  
|[ Elseif ](#elseif)
|[ End ](#end)
|[ Escape Codes ](#escape-codes)
|[ Event ](#event)|  
|[ Forall ](#forall)
|[ Foreach ](#foreach)
|[ Format ](#format)
|[ Function ](#function)|  
|[ Gag ](#gag)
|[ GMCP ](#gmcp)
|[ Greeting ](#greeting)
|[ Grep ](#Grep)|  
|[ Help ](#help)
|[ Highlight ](#highlight)
|[ History](#history)|  
|[ If ](#if)
|[ Ignore ](#ignore)
|[ Index ](#快速上手)
|[ Info ](#info)|  
|[ Keypad ](#keypad)
|[ Kill ](#kill)|  
|[ Line ](#line)
|[ List ](#list)
|[ Lists ](#lists)
|[ Local ](#local)
|[ Log ](#log)
|[ Loop ](#loop)|  
|[ Macro ](#macro)
|[ Map ](#map)
|[ Mapping ](#map)
|[ Math ](#math)|  
|[ Mathematics ](#mathematics) 
|[ Message ](#message)|  
|[ Metric System ](#metric-system)
|[ Mouse ](#mouse)
|[ MSDP ](#msdp)
|[ MSLP ](#mslp)|  
|[ Nop ](#nop)|   
|[ Parse ](#parse)
|[ Path ](#path)
|[ Pathdir ](#pathdir)|  
|[ PCRE ](#pcre)
|[ Port ](#port)
|[ Prompt ](#prompt)|  
|[ Read ](#read)
|[ Regexp ](#regexp)
|[ Repeat ](#repeat)|  
|[ Replace ](#replace)
|[ Return ](#return)
|[ Run ](#run)|  
|[ Scan ](#scan)
|[ Screen ](#screen)
|[ Screen Reader ](#screen-reader)|  
|[ Script ](#script) 
|[ Send ](#send)
|[ Session ](#session)
|[ Session Name ](#session-name)|  
|[ Showme ](#showme)
|[ Snoop ](#snoop)
|[ Speedwalk ](#speedwalk)
|[ Split ](#split)|  
|[ SSL ](#ssl)
|[ Statements](#statements)
|[ Substitute ](#substitute)|  
|[ Suspend ](#suspend)
|[ Switch ](#switch)
|[ System ](#system)|  
|[ Tab ](#tab)
|[ Textin ](#textin)
|[ Ticker ](#ticker)
|[ Time ](#time)|  
|[ Variable ](#variable)|  
|[ While ](#while)
|[ WildCards ](#wildcards)
|[ Write ](#write)|  
|[ Zap ](#zap)|  
***

# 总览

## 关于 TinTin++ Mud 客户端

TinTin++ (或称 tt++) 是 `Free(自由)` Mud 客户端。

适用于 Android,iOS,Linux,macOS,Windows 等平台。  

具有高级自动程序、脚本语言和 VT100 接口。  

WinTin++ Windows 桌面程序适用于不使用 Cygwin 的用户。

Windows 还可以使用 WSL 来体验原汁原味的 Linux TinTin++。

--WinTin++（使用 PuTTY 派生的 mintty 终端）  
--Cygwin（Windows 的 Linux/Unix 模拟器）  
--WSL（Windows 10 以上的 Linux 子系统）  

## 关于 TinTin++ 手册

手册中描述了大多数 TinTin++ 命令，如果需要帮助，您可能需要先浏览一下。  

TinTin++ 还提供内部帮助文件，可通过 `#help` 命令访问。  

有多个 Mud 客户端使用 tt++ 脚本语言，因此您可能已经熟悉使用另一个 Mud 客户端的一些命令。  

对于错误报告、问题、请求和建议，您可以访问 [「Github 论坛」](https://github.com/scandum/tintin/discussions)或[「Discord 频道」](https://discord.gg/gv7a37n)。

## 安装 TinTin++ Mud 客户端

[「安装说明」](https://tintin.mudhalla.net/install.php)介绍如何在多个操作系统上安装 TinTin++。  

TinTin++ 源代码可在[「下载部分」](https://tintin.mudhalla.net/download.php)获得，并可在大多数 Linux/Unix 系统以及 Cygwin 上编译。  

通过使用自制软件包安装程序，在 macOS 上安装非常容易。  

WinTin++ Windows 桌面程序可作为安装程序使用。  

要在[「安卓」](https://tintin.mudhalla.net/android.php)或 ChromeOS 上运行客户端，需要 Termux（一个安卓终端模拟器和 Linux 环境，它也在 Chromebook 和 Kindle Fire 平板电脑上运行）。  

要在 iPhone 和 iPad 上运行客户端，需要 iSH（相当于 iOS 上的 Termux）。 
 
也可以在 macOS、Linux、Unix 计算机上运行 ssh 守护程序，无论您使用 ssh 客户端还是 web 浏览器，都可以远程访问脚本和客户端。

## TinTin++ 特性

虽然 TinTin++ 主要用作 Mud 客户端，但它也可以用作 Unix shell 命令语言、多路复用程序、自动程序。  

大多数控制台程序 (比如 bash) 都可以从 TinTin++ 内部启动，并且允许您创建高亮显示、进行替换、设置触发器、计时器、别名，或者是将文本转移到不同的子窗口、将多个流合并为一个等等。  
这允许您修改大多数控制台应用程序的外观、界面和行为。

TinTin++ 支持的协议有 MCCP (Mud 客户端压缩协议) 、MMCP (Mud 主聊天协议) 、Xterm 256色、真彩色和 Muds 使用的大多数 TELNET 选项。  

TinTin++ 适用于大多数屏幕阅读器，其可访问的非图形命令界面让那些使用屏幕阅读器的视力障碍人士轻松使用。

作为一门编程语言，TinTin 有如下特性：  
* 支持 PCRE 的触发器、别名、gag（文本消除）、高亮、替换、按键宏、定时器、延迟响应、事件
* 支持关联数组（类比其他语言的 table 或者 map）
* 丰富的文本格式化功能
* 可搜索的滚动缓冲区
* 64 位浮点逻辑运算和算术表达式
* 自动画地图并可通过 VT100 来显示地图
* 多路会话支持
* 加载和解析任何文件
* 执行命令行脚本
* 通过 ssh/sftp 等客户端来运行命令行程序
* 全面控制 TinTin++ 的脚本语言
* 切分屏幕以区分客户端输入和 MUD 输出
* 用 VT100 控制字符来绘制状态条
* 基于滚动缓冲区的 tab 补全

TinTin++ 具有快速而强大的基于 JIT(即时编译) 实现的内置脚本引擎。

# 快速上手

接下来介绍了一些 TinTin++ 的常用命令，指引您快速上手。  

其他命令可以在本页面各个详细介绍部分找到，也可以通过 `#help <指令>` 查看。

## 启动及结束

启动 TinTin++ 的语法是：

> ./tt++ <配置文件名>

您应该了解一下相对路径和绝对路径的相关知识。
```
示例：
cd ~/tt && screen tt++ init.tt
```

请记住：启动 TinTin++ 时定义的所有触发器、别名、替换等都是由所有会话继承的。

退出 TinTin++ 可以键入 `#end`，或者在空行上按组合键 ctrl-d。

对于 WinTin++ 用户，会在选择文本时自动复制，使用 shift-insert 进行粘贴。

```
TinTin++ 启动时可附加下列参数：

用法：tt++ [option] [file]

-a 设定程序开始事件的参数。  
-e 执行给定命令。 
-g 打开用户启动界面。  
-G 不要显示问候信息。  
-h 显示此帮助。  
-H nohup 兼容模式。  
-M 矩阵数字雨。  
-r 读给定文件。  
-R 重连到到后台守护进程。  
-s 启用屏幕阅读模式。  
-t 设置给定标题。  
-T 不设置默认标题。  
-v 启用详细信息模式。  
-V 显示版本信息。
```

## 程序的基本特性

首先，我将解释一些非常基本和重要的功能:

所有 TinTin++ 命令都以 `#` 开头(可以用 `#config` 来改变)。  

```
示例：
#help   
--#help 是客户端命令，不会发送到服务端。
```

TinTin++ 的所有命令可以缩写。  

```
示例：
#he   
--#he 等效于 #help。
```

所有命令都可以用 `;` 分隔。

```
示例：
w;u;look;say dzp我要买药！   
--递归执行这四条命令。
```

有三种方法可以转义符号 `;` 。
```
示例: \say Hello ;) 
用符号'\'开头的行不会被 TinTin++ 解析。

示例: say Hello \;)
不解析'\'后面的字符。

示例: #config verbatim off 
除非以 '#' 开头，所有语句都会被原样整行发送。
```

## 连接至 MUDs 服务端

> 命令: #session {会话名} {网址或 ip} {端口}  
示例: #session pku mud.pkuxkx.com 8080

可以在上面示例的末尾添加 `;用户名;密码;` 来实现自动登录。

您可以拥有多个会话，可以键入 `#<会话名称>` 在多个会话之间切换。

默认会话是 `#gts`，可以向其他会话发送指令：`#gts #echo hi`。

您可以通过键入: `#session` 来获得所有会话列表。  

```
--当前活动会话标记为 (active)。    
--Snooped 会话标记为 (snooped)。  
--MCCP 会话 (MUDs 客户端压缩协议) 标记为 (mccp)。
```

## 分屏

> 命令: #split

`#Split(分屏)` 命令将创建一个独立的输入和输出区域。

使用 `#prompt` 命令，您可以捕获提示并将其放在拆分行上。  

要取消拆分界面，您可以使用 `#unsplit` 将终端设置恢复为默认设置。

## 别名

> 命令: #alias  
语法: #alias {name} {commands}

`#Alias(别名)` 命令的语法几乎和 `csh` 中的别名一样。  

使用 `#alias` 命令定义别名。  

变量 %0，%1..%9 包含别名命令的参数，如下所示:  

%0 变量包含所有参数。  
%1 变量包含第 1 个参数。  
....  
%9 变量包含第 9个参数。  

```
示例: #alias nice helo Mr %1
--如果别右侧没有定义的变量，那么别名指令后面的所有参数都将附加到命令字符串中。
```

```
示例:  #alias ff cast 'fireball'
--'ff dzp' 等效于: cast 'fireball' dzp
```

如果希望别名执行更多命令，则必须使用大括号。

例如: `#alias ws {wake;stand}`。

要删除别名，请使用 `#unalias` 命令。

TinTin++ 不检查递归别名！您可以通过转义整行或者使用 `#send` 命令来避免递归。

```
示例: #alias put \put %1 in %2

示例: #send put %1 in %2
```

## 触发器

> 命令: #action  
语法: #action {action-text} {commands}

使用此命令定义当屏幕上出现特定文本时要执行的触发。  

在 `action-text` 中，有 99 个变量可以用作匹配。  

这些变量是 %1，%2...%9，%10...%99。  

```
示例:
#action {你受伤了} {buy yao;eat yao}

#action {%1想要杀了你。} {kill %1}

#action {%1告诉你'%2'} {tell dzp %1告诉我'%2'}
--转发消息给 dzp。

#action {%1告诉你%2} {#bell }
--当你得到一个通知时终端发出嘟嘟声和振动提醒。
```

如果键入 “#ignore action on”，  
您可以让 TinTin++ 忽略触发器。

通过键入 “#debug action on”，  
您可以看到 TinTin++ 在触发器执行时的命令。

您可以使用 `#unaction` 命令删除触发器。

## 高亮显示

> 命令: #highlight (记住你可以缩写命令：#high)  
语法: #high {text} {color}

这个命令有点像 `#action`。  
这个命令的目的是用你提供的颜色包装 MUDs 中的文本。  
此命令是 `#substitute` 命令的简化版本。

```
示例:
#high {通脉药} {light yellow}
--为词语"脉药标"记亮黄色。

#high {%1通脉药%2} {light yellow} 
--给包含词语"通脉药"的整行标记亮黄色。
```

可以使用 `#unhigh` 删除高亮显示。

## 快速行走

如果您键入仅由字母和数字以及 `e 、 s 、 w 、 n 、 u 、 d` 组成的命令，则此命令可以解释为一系列移动命令。

```
示例: 
ssw2n 
--相当于南、南、西、北、北
```

如果您在键入一些仅由这些字母组成的命令时遇到问题，请键入大写字母。  

例如：当使用检查新闻命令 news，或输入 new 作为你的名字时。

您必须在设置中启用快速行走才能使用本功能。

指令：`#config speedwalk on/off`。

## 定时器

> 命令: #ticker {name} {命令} {秒}

北大侠客行 MUDs 上每 15 分钟就可以使用 fullme 命令。  
如果你使用 fullme 验证并输入正确验证文本，五百万经验以内你会获得双倍内力精力并恢复状态，所有任务会获得完整奖励，五百万经验后长时间不使用 fullme 会被判定为机器人。  
所以这种情况经常使用 fullme 是非常好的，TinTin++ 可以帮助你做到这一点。

**注意：** fullme 会导致年龄增加。

```
#ticker {tick} {#delay 1 {#show 现在可以使用 fullme 命令了}} {900}

这将创建一个名为 {tick} 的定时器，
定时器会在 900 秒后输出提示信息，
并在每个 900 秒定时循环时间点再次输出该提示。
```

你可以用 `#untick` 删除定时器。

## 命令文件

当您使用 TinTin++ 读取命令文件时，它会解析文件中的所有文本。  

你可以使用命令文件来保存别名/触发器，登录到一个 MUDs (账户、密码等)。  

基本上各种命令都可以加载。

您可以使用文本编辑器 (强烈建议) 制作命令文件。

也可以使用 `#write` 命令将所有当前定义的内容列表写入文件。

```
#read <文件名>
--读取并执行文件。

#write <文件名>
--将当前会话已知的所有触发/别名/替换等写入文件。
```

## 重复命令

> 语法:#number <指令>  
--可以重复一个命令

```
例子:
#5 eat yao
--如果你受伤了，多吃药可以快速恢复伤势。

#10 {buy yao;eat yao}
--重复这两个命令 10 次。
```

## 历史回溯

TinTin++ 具有 `csh` 历史回溯特性的有限子集，可以通过上下箭头来选择输入过的内容。

!  -- 重复最后一个命令。  
!cast -- 重复以 cast 开头的最后一个命令。  
Ctrl-r -- 组合键进入反向历史搜索模式。  

## 路径记录

如果使用了 `#path new` 命令，TinTin++ 会跟踪你的移动轨迹。  

也就是说，每当你键入 北/南/东/西/上/下 等移动命令时，TinTin++ 会自动将该方向和它的相反方向加入队列 (路径)。  

要正常使用该功能，必须预先定义[「路径方向」](#pathdir)。

```
Path 的子命令:

#path new 
--启动路径记录，重置队列。
#path end 
--停止路径记录。
#path map 
--显示路径。
#path ins {forward} {backward} 
--将命令插入队列。
#path del 
--删除路径中的最后一步。
#path save {f|b} {变量} 
--将路径保存到给定的变量。
#path load {alias} 
--将路径别名加载到路径队列中。
#path walk {forward|backward} 
--按照队列路径向前或向后走 1 步。
#path run <n>
--在已加载路径的情况下，每 n 秒执行一个路径指令。
#path stop
--停止记录路径，行走时则停止行走。
```

```
示例：
#act {这个方向没有出路} {#path del}  
--上面的触发可以有效地帮助记录路径。

游戏中的例子:  
你想要快速的完成任务后返回，  
键入: #path new  
然后行走并杀掉任务目标后，  
键入: #path save backward tmp;$tmp 
在限制每秒指令数的服务器加载路径并缓慢行走：  
键入：#path load $tmp;#path run 1

还可以建立别名，这可以节省不少时间。
```

## 地图命令

TinTin++ 有一个强大的高度可配置的自动地图绘制器。

每当您键入 `n/ne/e/se/s/sw/w/nw/n/u/d`， tt++ 尝试跟踪您的移动轨迹。

地图命令：

> #map create  
--创建地图。

> #map goto 1  
--转到地图中默认创建的第一个房间。

> #map map  
--显示地图。

> #map undo  
--撤消上次对地图的更改。

> #map write <filename>  
--将地图保存到文件中。

> #map read <filename>  
--从文件加载地图。

还有许多其他的地图命令选项。`#help map` 将介绍所有关于 `#map` 命令的信息。  

但我会给出一组将让大多数人开始的命令。  

```
#map create
#split 12 1
#map flag unicode on
#map flag vt on
#map goto 1
```

这些命令将在屏幕顶部创建一个 12 行 vt100 分割部分来显示使用 unicode 字符绘制的地图。

```
示例：
#action {这个方向没有出路。} {#map undo}
```

当你四处移动时，地图会自动创建。

## 帮助

> 命令: #help <指令>

`#Help(帮助)` 命令是你最忠实的朋友，它包含所有可用 TinTin 命令的最新信息。 
 
如果你在没有参数的情况下键入 `#help`，你会看到所有的命令列表，其中大部分在快速上手部分没有描述，因为这里只涵盖了开始的基本知识，也可以通过下面更详细的手册部分进行学习和了解。

***
**享受 MUDs 带来的乐趣吧！**
***

# Action

> 语法：#action {文本} {命令} {优先级}

`#Action(触发器)` 命令可用于用一个或多个命令响应服务器发送的特定消息。  

从文本消息中替换 %1-%99 个变量，并可以在触发器的命令部分使用。  

优先级部分是可选的，用来确定触发的优先级，默认为 5。

```
%1-%99 个变量针对当前设置触发器有效，
触发器中套嵌的触发器应使用 %%1-%%99，
若不想保存匹配到的内容，使用 %!*。
示例：
#action {%!*bli bla%1} {
  #showme %1;
  #action {%%1bla bli%*} {
     #showme %%1 %%2;
  };
};
使用如下命令测试：
#show bla bli bla blo;#show blb bla bli blc
```

__注意：%0 永远不应用于触发器（会导致所有内容被响应）。__

如果消息以 `~` 开头必定匹配颜色代码。  

为了触发颜色，您可以启用 `#config {convert meta} on` 来显示元字符。  

```
示例: 
#action {~^\e[1;37m%1} 
{#showme {--用粗体白色显示: %1}}
```

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

```
示例: 
#action {%1告诉你'%2'} {tell %1 我暂时不在.}
```

`#showme` 命令可以被触发器响应，如果你不想被触发器响应：  

使用：`#line ignore #showme {text}`。

触发器按字母顺序排序，一次只能触发一个。  

要更改触发顺序，您可以为触发器分配优先级。

优先级默认为 5，数字越小，优先级越高，可以是浮点数字。

```
若要使一行输出触发两次，
可以使用 #sub 替换一个触发到 #func 中。

示例：
#action {aaa} {#showme {RECEIVED AAA}}
#action {bbb} {#showme {RECEIVED BBB}}
#showme {zzzzz aaa zzzzz bbb zzzz}
RECEIVED AAA
#function echo {#showme {%0};#return}
#sub {aaa} {aaa@echo{RECEIVED AAA}}
#showme {zzzzz aaa zzzzz bbb zzzz}
RECEIVED AAA
RECEIVED AAA
```

要删除以 `%*` 为消息的触发器，请使用：

```
#unaction {%%*}
或
#unaction {\%*}
```

或者，您可以将触发封装在分类 `#class` 中，然后在不再需要触发器时清除该分类。

注: 您可以使用 `#unaction` 命令删除触发器。  

另可参见: [Gag](#gag)， [Highlight](#highlight)，[Prompt](#prompt)， [Substitute](#substitude)。

# Alias

> 语法：#alias {名称} {命令} {优先级}

`#Alias` 别名命令可用于缩短长时间或经常使用的命令。  

当使用别名时，%1-%99 变量从参数中被替换，表示第 1 到 99 个单词，这些单词可以在别名的命令部分使用。  

优先级部分是可选的，并用来确定别名的优先级，默认为 5。

如果使用 %0，它将包含所有参数，如果命令部分只存在一个单词，则变量会自动附加到末尾。

```
示例: 
#alias {k} {kill %1;kick}
输入 “k dzp” 将会下手杀死 dzp，紧接着做表情 kick(对着空气踢了一脚)。
```

您可以使用别名的“名称”部分中的变量创建更复杂的别名，该部分将覆盖默认变量处理。

```
示例: 
#alias {k %1 with %2} {
  wield %2;attack %1;
  slash %1 with %2;
  whirl %2;
  strike %1 with %2
}

使用上面的别名，你可以用键入如下内容: 
k blue smurf with battle axe
```

若要定义与所有用户输入内容相匹配的别名，请使用 `%*` 作为名称。

```
示例: 
#alias {%*} {#showme You Wrote:%0}
```

别名按字母顺序排序，一次只能触发一个别名。  

要更改顺序，您可以为别名分配优先级。

优先级默认为 5，数字越小，优先级越高，可以是浮点数字。

注: 您可以使用 `#unalias` 命令删除别名。

要删除以 %* 为名称的别名，请使用：  

```
#unalias {%%*} 
或 
#unalias {\%*}。
```
或者，您可以将别名封装在分类 `#class` 中，然后在不再需要别名时清除该类。

另可参见: [Cursor](#cursor)， [History](#history)，[Keypad](#keypad)， [Macro](#macro)， [Speedwalk](#speedwalk)，[Tab](#tab)。

# All

> 语法: #all {commands}

如果您在一个终端中有多个会话，您可以使用 `#all` 在所有会话 (不包括启动会话) 中执行命令。

```
示例: 
#all quit
--会在所有会话中执行 quit。
```

另可参见: [Port](#port)，[Run](#run)，[Session](#session)，[Session Name](#session-name)，[Snoop](#snoop)，[SSL](#ssl)，[Zap](#zap)。

# Bell

> 语法：#bell {flash|focus|margin|ring|volume} {argument}

没有参数的 `#bell` 命令会响起终端铃声。

注：手机使用 `#bell` 可以使手机振动并发出嘟嘟声。

```
示例: 
#action {bubba tells you} {#bell}
```

如果你不看屏幕，并且你不想错过与 bubba 的对话，这可能会很有用。  
或者，您可以使用 `#system` 播放声音文件。  

一些终端将允许您使用 VT100 操作系统命令来更改终端的标题，该标题可以用作视觉警报。  
```
示例:
#action {bubba tells you}
{
    #screen save title;
    #screen set title 新消息！;
    #bell ring;
    #delay 10 #screen load title
}
```
上面的示例将保存窗口标题，并将标题更改为 “新消息！”，振起响铃，然后在 10 秒钟后重置窗口标题。

振铃响起时，可以将终端设置为弹出到前台。
```
示例：
#bell focus on;#bell ring;#bell focus off
```

还可以在一些终端上调整响铃音量。  
```
示例:
#loop {1} {8} {cnt} {
  #line substitute variable;
  #delay {$cnt} {
    #showme Volume $cnt: #bell volume $cnt;
    #bell
  };
};
```
另可参见: [Screen](#screen)。

# Break

> 语法: #break

#Break 中断命令可用于中断 `#foreach、#loop、#parse、#switch、#while` 命令。  

当脚本执行到 `#break` 时，TinTin 将跳到命令的末尾并继续执行。  

```
示例:
#math cnt 0;
#while {1}
{
  #math cnt $cnt + 1;
  #if {$cnt == 20}
  {
    #break;
  };
};
```

另可参见: [Continue](#continue)，[Foreach](#foreach)，[List](#list)， [Loop](#loop)，[Parse](#parse)，[Repeat](#repeat)，[Return](#return)，[While](#while)。

# Buffer

> 语法：#buffer {home|up|down|end|find|get|lock|clear|jump|refresh|write|info}

`#Buffer` 缓冲区命令有各种操作终端回滚缓冲区的选项。

可以使用 `#config buffer_size <size>` 配置回滚缓冲区的大小，  
大小必须是 100、1000、10000、100000 或者 1000000 行。

在滚动回滚缓冲区时传入的文本不显示，  
可以使用 `#config scroll_lock off` 禁用滚动锁定。

当收到手动输入时，滚动锁定会自动禁用，随后，`#buffer {up|down}` 只能在宏或鼠标事件中工作。

> #buffer {clear} {[lower bound]} {[upper bound]}

如果没有参数，这将清除整个回滚缓冲区。否则它将清除给定的范围。  
正数是从回滚缓冲区开头计量的，负数从末尾开始。

> #buffer {jump} {\<location>}

将缓冲区移动到给定位置。  
正数从回滚缓冲区的开头移动，负数从末尾开始。

> #buffer {refresh}

将缓冲区标记为需要刷新，仅在垂直分割模式有用。

> #buffer {home}

将您移动到回滚缓冲区的顶部并显示该页。启用滚动锁定模式。在 `#macro` 中很有用。

> #buffer {up} [lines]

将回滚缓冲区向上移动一页并显示该页。启用滚动锁定模式。在 `#macro` 中很有用。  
你可以使用 `#buffer {up} {1}` 将回滚缓冲区向上移动 1 行。

> #buffer {down} [lines]

将回滚缓冲区向下移动一页并显示该页。启用滚动锁定模式。在 `#macro` 中很有用。  
如果提供了一个行数，它将向下滚动给定的行数。

> #buffer {end}

将您移动到回滚缓冲区的末尾并显示该页。禁用滚动锁定模式。在 `#macro` 中很有用。

> #buffer {find} {[number]} {\<string>} {[variable]}

将缓冲区移动到可以包含正则表达式的给定字符串。  
或者，您可以提供要跳过的匹配数，允许您在缓冲区中进一步跳转。  
正数从缓冲区开头搜索，负数从尾部开始。  
如果你提供一个变量，位置将会被储存，不发生跳转。

> #buffer {get} {\<variable>} {\<lower bound>} {[upper bound]}

允许您将回滚缓冲区中的一行或几行 (包括颜色代码) 存储到变量中。  
下限和上限必须在 1 到缓冲区大小之间。  
如果省略上限，则将给定行存储为标准变量。  
如果给定上限，两个边界之间的线将存储为列表。

> #buffer {lock} {on|off}

切换回滚缓冲区锁定状态。  
当锁定时，不会显示新传入的文本，任何命令都将禁用锁定。  
通过多个缓冲区命令将重新启用锁定。  
解锁时，它会将您移动到回滚缓冲区的末尾并显示该页。

> #buffer {write} {\<filename>}

将回滚缓冲区写入给定文件名。  
想要写入不带颜色编码的文本，请设置 `#config log plain`。

> #buffer {info} {[save]} {[variable]}

显示回滚缓冲区信息，并可以选择将信息写入到变量。

```
示例: 
#macro {(press ctrl-v)(press F1)} {#buffer end}

示例：
#macro {\e[F} {#buffer end}

注：在终端中按下 ctrl-v，随后按下的按键会转换为键码，可以用在 #macro 中。

示例:
#act {^[Exits: %1]}
{
    #loop 2 20 loop
    {
        #buffer get name $loop;
        #if {"$name" == "\e[1;33m%*"}
        {
            #var roomname &1;
            #break
        }
    }
}
--当退出时，循环浏览缓冲区的最后 20 行，寻找粗体黄色 (\e[1;33m) 的房间名称。当地图绘制时，知道你所在房间的名称可能会很有用。
```

另可参见: [Echo](#echo)，[Grep](#grep)，[Showme](#showme)。

# Button

> 语法：#button {square} {commands} {priority}

`#Button` 按钮命令可用于当在指定的空间区域内收到鼠标单击动作时响应一个或多个命令。  

鼠标单击的坐标存储在 %0-%3 中，可以用于按钮的命令部分。

空间部分应存在两个坐标，定义左上角和右下角，使用行、列、行、列语法。  
空间参数应该用空格、分号或括号。

默认情况下，该按钮设置为响应鼠标点击动作，要响应其他按钮动作，你必须添加第 5 个参数到定义按钮类型的空间。  

您可以启用 `#info button on` 查看发生的按钮事件及其类型。

优先级部分是可选的，默认为 5。

您必须启用 `#config {mouse tracking} on` 才能使按钮工作。

此命令不会绘制可见按钮，如果需要您必须单独执行此操作。

```
例如: 
#button {1;1;2;2} {#showme 你点击了左上角.}
```
按钮按字母顺序排序，一次只会触发一个按钮。  
要更改顺序，您可以分配优先级，默认 5，较低的数字表示更高的优先级。  
优先级可以是浮点数。

注：要查看按钮点击触发器，请使用 `#info button on`。  

注：您可以使用 `#unbutton` 命令删除按钮。

另可参见：[Delay](#delay)，[Event](#event)，[Ticker](#ticker)。

# Case

> 语法: #case {条件} {参数}

必须在 `#switch` 命令中使用 `#case` 命令。  

当 case 命令的条件参数与 switch 命令的条件参数匹配时，执行 case 的主体。

当比较字符串时，`switch` 和 `case` 写参数必须用引号包围。

```
示例:
#function {reverse_direction}
{
     #switch {"%1"}
     {
          #case {"north"} {#return south};
          #case {"east"}  {#return west};
          #case {"south"} {#return north};
          #case {"west"}  {#return east};
          #case {"up"}    {#return down};
          #case {"down"}  {#return up}
     }
}
```

这个函数返回相反的方向。`@reverse_direction{north}` 将返回 `south`。

另可参见: [Default](#default)， [Else](#else)，[Elseif](#elseif)，[If](#if)，[Switch](#switch)，[Regex](#regex)。

# Cat

> 语法：#cat {variable} {argument}

`#Cat` 命令将参数连接到给定变量。

另可参见: [Format](#format)，[Function](#function)，[Local](#local), [Math](#math)，[Replace](#replace)，[Script](#script)，[Variable](#variable)。

# Characters

TinTin++ 定义了以下特殊字符:

`#` Hashtag 是启动命令的默认字符，下面会称为命令字符或 tintin 字符。   
加载命令文件时，命令字符设置为文件中的第一个字符。  
可以使用 `#config` 重新定义该字符。

`;` 分号作为命令分离器可用于分开两个命令。多个命令可以串在一起。  
读取脚本文件时忽略尾随分号是一个常见的错误。

`{}` 花括号 (又名大括号) 用于分隔多个单词、命令、参数、嵌套命令和嵌套变量。  
大括号不容易被转义，并且必须总是成对使用。

`" "` 引号字符用于 `#math、#if、#switch、#case` 命令中的字符串。  
建议使用额外一组大括号 `{}` 来定义字符串。

`!` 感叹号用于重复命令，请参阅 `#help history`。  
可以使用 `#config` 重新定义该字符。

`\` 发送到服务器时以反斜杠开头的输入行是原样发送的。  
可以使用 `#config` 重新定义该字符。

另可参见：[Colors](#colors)，[Escape codes](#escape-codes)，[Mathematics](#mathematics)，[PCRE](#pcre)。

# Chat

> 语法: #chat {命令} {参数}

`#Chat` 命令用于创建与其他 mud 客户端的点对点连接，通常用于聊天和发送文件。  
这是一个分散的聊天系统，要连接到其他用户，你必须与他们交换 ip 地址和端口号。

> #chat {initialize|init} {port}

聊天初始化启动您的聊天服务器。  
端口号是可选的，默认情况下，4050 用作您的端口。  
使用此命令后，其他人可以使用您的 ip 地址和端口号连接到您的聊天服务器，您也可以反过来连接到其他人。

> #chat {uninitialize}

卸载聊天端口。

> #chat {name} {your name}

默认情况下，你的聊天名字被设置为 TinTin，但是如果已经有人使用了该名字，大多数服务器都会拒绝你连接， 所以你要做的第一件事就是改变你的聊天名称。聊天名字可以包含颜色代码。tt++ 聊天服务器不接受一些名字，比如 “all” 这个名字和超过 20 个字符的名字。

> #chat {call} {ip address} {port}

`#chat call` 聊天呼叫用于连接到另一个聊天服务器。如果省略端口参数，则使用默认端口 (4050)。

> #chat {color} {color names}

默认聊天颜色为粗体红色，您可以使用 `#chat color` 命令来更改此颜色，例如: `#chat color bold yellow` 粗体黄色，或者使用 256 颜色代码: `#chat color <cde>`。

> #chat {message} {buddy|all} {text}

这是用于通信的主要命令。如果您使用 `#chat message all`，则该消息被标记为公共消息，并发送给您连接的每个人。

> #chat {emote} {user|all} {text}

这个命令的工作方式与 `#chat message` 除了在外观上完全一样，它所做的只是在消息前面加上你的名字。

> #chat {paste} {user|all} {text}

此命令允许粘贴，将连续快速跟随的输入附加到消息中。请记住，大多数 mud 客户端不会正确接收超过 40 行的消息。

> #chat {reply} {text}

`#chat reply` 聊天回复，回复你收到私人信息的最后一个人。

> #chat {send} {user|all} {text}

此命令向另一个人发送原始数据字符串，这需要了解聊天协议[「Mud Master Chat Protocol」](https://tintin.sourceforge.io/manual/chatprotocol.php)才能使用。

> #chat dnd

DND 代表 “不打扰”，此命令切换 DND 状态。启用后，所有新的传入连接都会自动关闭。

> #chat {ip} {address}

此命令设置默认情况下未设置的 ip地址，并在连接到另一个 mud 客户端时发送。TinTin++ 忽视了其他 mud 客户端报告的知识产权，只需获取套接字地址，但是其他 mud 客户端可能需要设置它。

> #chat {who}

`#chat who` 显示你联系的所有人。第一列显示连接的参考号，当向某人发送消息时，可以使用该参考号而不是连接的名称。第二列显示连接的名称。第三列显示为连接设置的标志，(P)rivate，(I)gnore，(S)erve，(F)orward (from|to) user，下一列列显示 ip 、端口和 mud 客户端名称。

> #chat {info}

此命令显示您的姓名、 ip地址、端口、下载目录、回复和 DND 状态。

> #chat {ignore} {user}

这个命令将忽视给定的用户，他们不会被告知你忽视了他们，或者不再接收他们的消息。

> #chat {private} {user|all}

此命令将禁用对给定连接工作的窥视和请求命令。

> #chat {public} {user|all}

此命令与私有命令相反，允许窥视和请求命令为给定连接工作。默认情况下，新连接是公共的。

> #chat {peek} {user}

此命令显示给定用户的公共连接。

> #chat {request} {user}

此命令将获取给定用户的公共连接，如果您还没有连接到它们，则自动连接到它们。

> #chat {ping} {user}

此命令显示 ping 到达并以毫秒为单位发回给您所需的时间。

> #chat {zap} {user|all}

此命令关闭与给定用户的连接。

> #chat {forward} {user}

此命令将所有聊天消息作为 snoop 数据转发给给定用户。为了避免无限循环，当从该用户接收 snoop 数据时，转发给用户将被禁用。

> #chat {forwardall} {user}

此命令将保存到回滚缓冲区中的所有内容作为 snoop 数据转发给给定用户。

> #chat {serve} {user}

此命令将使您将所有公共聊天消息转发给给定用户，并将该用户的所有公共聊天消息转发给您所连接的每个人。为了避免无限循环，消息作为私人消息被转发。

> #chat {group} {user} {name}

此命令允许您将给定用户分配给组。您可以将组名与表情、消息和发送命令一起使用。如果你在没有参数的情况下使用 `#chat group`，它的行为会像 `#chat who` 一样，显示所有用户的列表和他们的组名。

> #chat {sendfile} {user} {filename}

此命令允许您向给定用户发送文件，他们必须在传输开始前接受该文件。

> #chat {accept} {buddy} {boost}

在用户提供发送文件后接受文件传输。速率是可选的，必须是介于 1-1000 之间的值。

> #chat {decline} {user}

在用户提供发送文件后拒绝文件传输。

> #chat {cancel} {user}

启动文件传输后取消文件传输。

> #chat {filestat} {user}

显示当前正在进行的文件传输的信息。

> #chat {download} {directory}

此命令设置新的下载目录。

有关更多信息，请参见描述 `#chat` 使用的基础协议 MMCP 规范：[「MMCP Specification」](https://tintin.sourceforge.io/manual/chatprotocol.php)。

另可参见：[Port](#port)。

# Class

> 语法: #class {name} {open|close|read filename|write filename|kill}

`#Class` 命令可以方便的管理和封装成组的列表。

注： `Class` 在其他语言中通常被称为类，在 `tt++` 中称为分类或分组更适合。

> #class {\<classname>} {open}

{Open} 选项将类标记为开始，并自动将以前打开的类标记为结束 (如果有)，之后创建的所有触发器和变量都将被分配给这个类，直到被标记结束。

> #class {\<classname>} {close}

{Close} 选项将当前打开的类标记为结束，并打开最后一个标记为开始的类 (如果有)。

> #class {\<classname>} {read} {\<filename>}

{Read} 选项将类标记为开始，读取给定文件，并在读取后将类标记为结束。

> #class {\<classname>} {write} {\<filename>}

{Write} 选项将给定类的所有触发（#action、#var...）写入文件。  
此选项可以通过将变量分配给属于特定类来存储数据。

> #class {\<classname>} {kill}

{Kill} 选项将删除给定的类。

> #class {\<name>} {clear}

{Clear} 选项将删除与给定类关联的所有触发（#action、#var...）。

> #class {\<name>} {list}

{List} 选项将列出与给定类关联的所有触发（#action、#var...）。

> #class {\<name>} {load}

{Load} 选项将从内存加载已保存的类副本。

> #class {\<name>} {save}

{Save} 选项将将把给定类的所有触发（#action、#var...）保存到内存中。

> #class {\<name>} {assign} {\<argument>}

将在给定类打开的情况下执行参数。

> #class {\<name>} {size} {\<variable>}

将类的大小存储在变量中。

```
示例：
#class extra kill;#class extra read extra.tin
--删除 “extra” 类
--读取 “extra.tin” 文件
--加载的所有触发（#action、#var...）都将分配给新的 “extra” 类。
```

另请参见: [Debug](#debug)，[Ignore](#ignore)，[Info](#info)，[Kill](#kill)，[Message](#message)。

# Colors

* **ANSI Colors**

> 语法: \<abc>  
-- a, b, c 是参数

参数 'a': VT100 code
```
0 - 重置所有参数为默认
1 - 粗体
2 - 暗色
4 - 下划线
5 - 闪烁
7 - 反色
8 - 跳过
```
参数 'b':  前景色Foreground color

参数 'c':  背景色Background color

```
0 - Black  黑色  5 - Magenta 品红色
1 - Red    红色  6 - Cyan    青色
2 - Green  绿色  7 - White   白色
3 - Yellow 黄色  8 - Skip    跳过
4 - Blue   蓝色  9 - Default 默认
```

* **Xterm 256 Colors**

对于 xterm 256 色支持：

对于 RGB 前景色使用 `<aaa> 到 <fff>`  
对于 RGB 背景色使用 `<AAA> 到 <FFF>`  

对于灰度前景色，使用 `<g00> 到 <g23>`  
对于灰度背景色，使用 `<G00> 到 <G23>`  

```
示例:
#showme <034>T<025>i<016>n<007>T<043>i<052>n<061>+<070>+<088>

示例:
#showme <fca> orange <cfa> lime <caf> indigo <acf> azure <fac> crimson

示例：
#show <acf>Azure    <afc>Jade     <caf>Violet
#show <cfa>Lime     <fac>Pink     <fca>Orange
```

在 TinTin++ 中执行示例，以查看实际结果。

* **Truecolor**

对于 12 位 truecolor 真彩色：

前景色使用 `<F000> 到 <FFFF>`  
背景色使用 `<B000> 到 <BFFF>`  

第一个字符表示 F (前景) 或 B (背景)，接下来的三个字符是十六进制 RGB 值。  

这允许 4096 种不同的颜色。

**注：请记住，并非所有终端都支持 truecolor 真彩色**。

对于 24 位 truecolor 真彩色：  

前景色使用 `<F000000> 到 <FFFFFFF>`  
背景色使用 `<B000000> 到 <BFFFFFF>`  

如果颜色代码超出您配置的颜色模式，它将会降级到最接近的匹配项。

另可参见: [Escape Codes](#escape-codes)， [Mathematics](#mathematics)，[PCRE](#pcre)。

# Commands

> 语法: #commands {regex}

如果没有参数，此命令将显示所有命令，否则将显示与缩写匹配的所有命令。

## Command 语法

所有 TinTin++ 命令都以 “#” 开头，可以使用 `#config {TINTIN CHAR}` 更改。

键入时，所有 tintin 命令都可以缩写。  

例如：`#variable` 可以缩写为 `#var`。

可以使用 `#<session name>` 激活会话，也可以使用 `#<session name> {commands}` 在不激活会话的情况下执行命令。

`#<number> {commands}` 可用于执行给定命令 “number” 次。

您可以通过将命令封装在一组大括号中，并用分号分隔每个命令来执行几个命令。  

例如，显示 “hello” 和 “world” 4 次:
```
示例:
#4 {#showme Hello;#showme World}
```

## Commands Seperator

如果你想发送文字 “;”，你可以使用 `\;` 来发送。  

要按原样发送整行内容，使用 `\` 开头。

```
示例: \Hello ;) 
-- tintin 不解析以 “\” 开头的行。
示例: say Hello \;) 
-- '\'不解析后面的字符。
示例: #config verbatim on 
-- 除非以 “#” 开头，否则所有内容都是按原样整行发送的。
示例: #line substitute secure {say Hello ;)} 
-- 自动排除特殊字符。
```

```
来自dzp@pkuxkx的释义：

比如你要告诉别人一个路径，
chat n;w;s;e 这样是不行的，
这样你就会走路。
你可以 chat n\;w\;s\;e，
也可以 chat {n;w;s;e}。
\ 的意思就是不再解析。
{} 的意思就是延迟解析。
```

## Carriage Return

当您发出命令时，系统会自动添加换行/回车。要更改此行为，请以 “\” 结尾。

```
示例: 
#showme hi\
#send look\
```

## Command Files

可以将命令放在文件中，这些文件被称为命令文件。  

您可以使用读取(read)、会话(session)、端口(port)、运行(run)和 (ssl) 命令读取命令文件。

您可以使用 `tt++ <filename>` 启动 TinTin++，以在启动时加载命令文件。

如果使用会话命令提供文件名，则只有当会话成功连接到主机时，命令文件才会被读取。

默认的命令字符是 `#` 。TinTin++ 将命令字符设置为命令文件中找到的第一个字符。

如果您想在读取文件时看到更多信息，请使用: `#config {verbose} {on}`。

请记住，文件中使用的每个开口大括号 {必须与闭合大括号} 相匹配。  

如果不这样做会失败，您将收到错误消息，并且文件不会加载。

您可以保存使用 `#write` 命令创建的触发器、变量和设置。  

请记住，并非所有设置都已保存。  

您可以使用 `#event {PROGRAM START}` 或 `#event {SESSION CREATED}` 来添加初始化命令，并用 `#Write` 保存。

另可参见：[Help](#help)，[Info](#info)，[Statements](#statements)。

# Config

> 语法: #config {option} {argument}

如果您配置了全局会话 (启动时看到的会话），所有启动的会话都将继承这些设置。

如果你不喜欢默认设置，建议使用配置文件启动。

当 `TinTin++` 启动时，它将生成一个配置文件，可以用 `#config` 命令修改它。 
 
键入没有参数的 `#config` 将显示当前配置，这些配置可以用 `#write` 命令写入文件方便以后加载。

***
默认情况下不启用以下配置选项:

> #CONFIG {CHILD LOCK}   {ON|OFF}

启用或禁用命令输入。

> #config {CONVERT META} {ON|OFF}

对于键盘输入和服务器输出，此选项使元字符可见。对于调试、创建宏和创建颜色触发器很有用。

> #config {DEBUG TELNET} {ON|OFF}

此选项将显示大多数 `telnet 子选项协商`。创建 `telnet` 事件时很有用。

> #config {INHERITANCE} {ON|OFF}

会话触发继承开关。

> #config {LOG LEVEL} {LOW|HIGH}

日志级别 LOW 是原始日志，只记录和服务器的交互。  

日志级别 HIGH 是 buffer 日志，记录屏幕上的内容，默认值为高。

> #config {MCCP} {ON|OFF}

默认情况下启用，可用于开关 `MCCP` 支持。

***
以下配置选项需要进一步说明:

> #config {COLOR PATCH} {ON|OFF}

此选项用于修复某些 muds 上的分屏模式下的颜色代码。  

默认情况下，它是关闭的，启用时可能会影响颜色触发器。

> #config {PACKET PATCH} {ON|OFF}

如果您的 mud 没有使用 MCCP，将数据包补丁设置为 0.5 到 1.0 之间的值将有助于处理损坏的数据包。

如果这导致在显示提示之前出现小延迟，您可以使用 `#split` 并使用 `#prompt` 命令将提示放在拆分行上来解决这个问题。

一些 MUDs 允许启用 EOR 或 GA，这也可以消除延迟。

***

可用的设置选项：  

选项          | 参数                        | 释义 
 :---        | ---:                        | :--- 
AUTO TAB     |                         5000| TAB 自动补全行数
BUFFER SIZE  |                        10000| 缓冲区存储大小 
CHARSET      |                        GBK-1| 编码设置
COLOR MODE   |                         TRUE| 颜色代码模式
COLOR PATCH  |                      ON\|OFF| 颜色修正模式
COMMAND COLOR|                     \e[0;37m| 命令颜色
COMMAND ECHO |                      ON\|OFF| 分屏模式指令显示
CONNECT RETRY|                          0.0| 会话重连间隔时间
HISTORY SIZE |                         1000| 命令历史存储大小
LOG MODE     |                          RAW| 日志文件数据格式
LOG LEVEL    |                    LOW\|HIGH| 日志等级
MOUSE        |                      ON\|OFF| 鼠标事件
PACKET PATCH |                         0.80| 修补损坏数据包时间
RANDOM SEED  |                         AUTO| 随机数种子
REPEAT CHAR  |                            !| 重复指令符号
REPEAT ENTER |                      ON\|OFF| 重复发送最后一个指令
SCREEN READER|                      ON\|OFF| 屏幕阅读器模式
SCROLL LOCK  |                      ON\|OFF| 卷轴锁定
SPEEDWALK    |                      ON\|OFF| 快速行走
TAB WIDTH    |                            8| TAB 占用空格数
TELNET       |                      ON\|OFF| TELNET 支持
TINTIN CHAR  |                            #| 命令字符
VERBATIM     |                      ON\|OFF| 解析键盘输入
VERBATIM CHAR|                          \\ | 解析字符
VERBOSE      |                      ON\|OFF| 静默读取脚本
WORDWRAP     |                      ON\|OFF| 包装服务器输出

```
参数补充说明：

颜色模式：
#CONFIG {COLOR MODE} <ON|OFF|ANSI|256|TRUE>

日志格式：
#CONFIG LOG <HTML|PLAIN|RAW>

随机数种子：
#SYNTAX: #CONFIG {RANDOM SEED} <AUTO|NUMBER>

编码：
#CONFIG {CHARSET} <AUTO|ASCII|BIG-5|BIG5TOUTF8|CP1251TOUTF8|CP949|CP949TOUTF8|FANSI|GBK-1|GBK1TOUTF8|ISO1TOUTF8|ISO2TOUTF8|KOI8TOUTF8|UTF-8>

卷轴锁定：
#CONFIG {SCROLL LOCK} {ON|OFF}
参数 ON 在滚动时看不到服务器输出，
参数 OFF 在滚动时可以看到服务器输出。
```

注：要查看每个选项的具体语法，请键入任意与参数完全不匹配的字符。

```
例如：
#config {mouse} 担子炮最牛逼！炮爷救我！
#SYNTAX: #CONFIG {MOUSE} <ON|OFF|DEBUG|INFO|PIXELS>
```

另可参见：[Class](#class)，[Line](#line)。

# Continue

> 命令: #continue

`#Continue(继续)` 可以用于 `#foreach`、`#loop`、`#parse`、`#switch`、`#while`。  

当发现 `#continue` 时，TinTin++ 将移动到循环的末尾，并继续执行。

这可能会反复执行命令。


```
示例:
#loop 1 10 cnt
{
  #if {$cnt % 2 == 0}
  {
    #continue
  };
  say $cnt
}
--此处将 $cnt 做整数模运算求余数。
```
另可参见: [Break](#break), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

# Coordinates

当 `0,0` 坐标位于左上角时，TinTin++ 使用 y,x / rows,cols 记法。  
此时 `1,1` 表示左上角，`-1,-1` 表示右下角。  
此类参数由 `#showme` 使用。

当 `0,0` 坐标位于左下角时，TinTin++ 使用 x,y / cols,rows 记法。  
此类参数由 `#map jump` 使用。

定义空间坐标时，通过使用四个坐标指定空间的左上角和空间的右下角。

绝大多数的 tintin 命令使用 `row,col` 记法，主要是因为这种记法是 "VT100 标准" 在终端仿真使用的。

注：此处可参考笛卡尔坐标系相关资料。

***

* Squares

`Squares(正方形)` 参数采用 2 个坐标。

第一个坐标定义左上角，第二个坐标定义右下角。

终端的左上角定义为 1,1，右下角为 -1,-1。

此类参数由 `#draw`、`#button` 和 `#map offset` 使用。

* Panes

`Pane(窗格)` 参数采用 4 个尺寸值，即: 顶部窗格、底部窗格，左窗格，右窗格。  

当提供负值时是用最大尺寸减去该值。

此类参数由 `#split` 命令使用。

* Ranges

`Range(范围)` 参数采用 2 个值，称为上限和下限。

上限 (第一个值) 定义范围开头，下限 (第二个值) 定义范围结束。

第一个索引范围定义为 1。当提供负值时最后一个索引定义为 -1。

此类参数由 `#buffer` 和 `#variable` 使用。

***

另可参见：[Characters](#characters)，[Colors](#colors)，[Escape](#escape)，[Mathematics](#mathematics) ，[PCRE](#pcre)。

# Cr

> 命令: #cr

此命令向会话发送回车符。在 `#alias` 需要返回额外的回车符时很有用。

如果启用了 `REPEAT ENTER` ，并且在不重复最后一个命令的情况下需要输入时很有用。

此命令已过时，可以选择在没有参数的情况下使用 `#send`，或者使用命令分隔符 `;` 插入回车符。

如果你想在 DikuMUD 服务器上发送多个返回，最好使用 `#send {\n \n}` (空格是有意的)，因为许多 DikuMUD 服务器将连续的返回视为一次返回。

```
示例: 
#ticker {idle} {#send} {300}
--这将每 300 秒 (5 分钟) 向 mud 发送一次回车符来保持在线状态。
```

另可参见: [Bell](#bell)，[Forall](#forall)。

# Cursor

> 语法: #cursor {option} {argument}

键入不带参数的 `#cursor` 时，将显示所有可用的光标选项和它们的默认绑定、介绍。

`#Cursor` 命令的主要目标是为 `#macro` 添加可定制的输入编辑，其工作的主要方式是基于光标位置进行的操作。

可用选项如下：

选项 | 绑定 | 释义
:--- | :--- |:---
BACKSPACE         | \b      | 退格删除
BRACE             |         | 插入大括号
BACKWARD          | \cb     | 前移光标
CLEAR             | \cc     | 清除输入行
CLEAR LEFT        | \cu     | 从光标左侧清除
CLEAR RIGHT       | \ck     | 从光标右侧清除
CONVERT META      | \cv     | 转换下一个字符为元字符
CTRL DELETE       | \cd     | 删除一个字符,在空行上退出
DELETE            | \e3~    | 删除光标处的字符
DELETE WORD LEFT  | \cw     | 向前删除到空格
DELETE WORD RIGHT | \e3;5~  | 向后删除到空格
DOWN              | \eB     | 下移光标
END               | \ce     | 移动光标到输入行尾部
ENTER             |         | 执行输入行
FLAG              |         | 设置输入行状态
FORWARD           | \cf     | 后移光标
GET               |         | 复制输入行到变量
HISTORY NEXT      | \cn     | 选择下一个历史命令
HISTORY PREV      | \cp     | 选择上一个历史命令
HISTORY SEARCH    | \cr     | 搜索历史命令
HOME              | \ca     | 移动光标到输入行首
NEXT WORD         | \ef     | 移动光标到下一个单词
MACRO             |         | 宏缓冲区
PAGE              |         | 翻页
PASTE BUFFER      | \cy     | 粘贴以前删除的输入文本
POSITION          |         | 移动光标位置到指定列
PREV WORD         | \eb     | 移动光标到前一个单词
REDRAW INPUT      | \cl     | 重绘输入行
SET               |         | 复制给定字符串到输入行
SOFT ENTER        | \e[13;2u| 在编辑模式新建行
SUSPEND           | \cz     | 挂起程序，用 fg 返回
TAB               |         | 自动补全
UP                | \eA     | 上移光标

注：请键入 `#cursor <子选项>` 查看子选项的语法。

许多光标命令仅在以下情况才能正常工作在 `#macro` 或 `#event` 中。

* #cursor flag

选项 | 释义
:---|:---
EOL         |行结束符  
ECHO        |开关回显标记  
INSERT      |切换插入\|替换  
OVERTYPE    |改写模式  

```
设置换行符的格式：
#CURSOR {FLAG} {EOL} {CR|LF|CRLF|CRNUL|OFF}
```
* #cursor macro

选项 | 释义
:---|:---
PRESERVE    |不从宏输入缓冲区中擦除宏
RESET       |擦除宏输入缓冲区  

* #cursor tab

选项 | 释义
:---|:---
CASELESS    |使自动补全不区分大小写  
COMPLETE    |使自动补全在编辑时工作  
DICTIONARY  |在字典上执行自动补全  
SCROLLBACK  |在回滚缓冲区执行自动补全  
BACKWARD    |指定自动补全向后  
FORWARD     |指定自动补全向前  

大多数选项可以/必须一次性设定。

```
示例: 
#macro {\e\e[3~} {#cursor clear right}
--当按下 alt-delete 时，光标右侧的所有输入都被清除，默认情况下，该输入被设置为 ctrl-k。
```

另可参见: [Alias](#alias)，[History](#history)，[Keypad](#keybord)， [Macro](#macro)，[Speedwalk](#speedwalk)，[Tab](#tab)。

# Daemon

> 语法：#daemon {attach|detach|kill|list} [name]

`#Daemon` 提供类似于 `screen` 和 `tmux` 的守护进程功能。  

- #daemon attach [name]  
`attach` 重连选项将尝试找到一个守护中的 tintin 实例，并且接管控制权。Name 参数是可选的。  
- #daemon detach [name]  
`detach` 分离选项将守护 tintin 进程，将其变成后台进程。Name 参数是可选的，如果您有几个守护中的 tt++ 实例正在运行，可以用来区分它们。  
- #daemon kill [name]  
杀死所有或具有匹配名称的守护进程。  
- #daemon list [name]  
列出所有或具有匹配名称的守护进程。

另可参见：[Script](#script)，[System](#system)，[Run](#run)。


# Debug

> 语法: #debug {listname} {on|off|log}

打开或关闭对列表的调试。

没有给出参数时，将显示当前设置，以及可以调试的列表名称。

可调试列表如下：
*  ACTIONS
*  ALIASES
*  BUTTONS
*  CLASSES
*  COMMANDS
*  CONFIGS
*  DELAYS
*  EVENTS
*  FUNCTIONS
*  GAGS
*  HIGHLIGHTS
*  MACROS
*  PATHS
*  PATHDIRS
*  PROMPTS
*  SUBSTITUTES
*  TABS
*  TICKERS
*  VARIABLES

```
示例: 
#debug action on
--当 action 被触发时，将会得到调试信息。

#debug {listname} {log}   
--将调试信息静默写入日志文件，您必须为这项工作按顺序记录。
```

并非每个列表都有调试支持。

另可参见: [Class](#class)，[Ignore](#ignore)，[Info](info)，[Kill](#kill)，[Message](#message)。

# Default

> 语法: #default {commands}

只能在 `#switch` 命令中使用 `#default(默认)` 命令。

当没有 `#case` 命令的条件参数与 `#switch` 命令的条件参数相匹配时，将会执行 `default(默认)` 命令。

```
示例:
#switch {1d4}
{
  #case 1 cackle;
  #case 2 smile;
  #default giggle
}
```

另可参见: [Case](#case)，[Default](#default)，[Else](#else)，[Elseif](#elseif)，[If](#if)，[Switch](#switch)，[Regex](#regex)。

# Delay

> 语法：#delay {second} {command}

> 语法：#delay {name} {command} {second}

`#Delay(延迟执行)` 命令允许您在执行给定命令之前让 tintin 等待给定的秒数。

允许纳秒级浮点精度，延迟执行命令将在 0.01 秒间隔内动作。

命名后的延迟执行被视为一次性定时器，请参见 `#help ticker`。

为延迟执行命名可以更容易地使用 `#undelay` 命令，注意这会改变语法。

请记住，如果命名使用数字，那么具有相同数字名称的延迟执行不会被覆写。

```
示例：
#delay {1} {#show 第二};#show 第一
--这将先输出"第一"，然后输出"第二"。

示例: 
#delay {600} {#showme 检查通脉情况}
--这将在 600 秒后通知您检查通脉情况。

示例: 
#delay {checkdz} {#showme 检查通脉情况} {600}
--与上面相同，只是为延迟执行命名。
```

与 zmud 的 `#wa` 指令不同，使用多个 `#delay` 需要注意其套嵌关系。

```
示例：
#delay {1} {
  #show 1;
  #delay {1} {
    #show 2;
    #delay {1} {
      #show 3;
    };
  };
};
```

另可参见: [Event](#event)，[Ticker](#ticker)。

# Draw

> 语法：#draw [line color] [options] \<type> \<square> {text}

`Draw(绘制)` 命令允许您在屏幕上绘制各种类型的线条和形状。

当您在没有参数的情况下键入 `#draw` 时提供常见的选项和类型和简要说明。

空间参数 `<square>` 应该存在两个坐标定义左上角和右下角，使用 `row, col, row, col` 语法。

空间参数 `<square>` 可以是负数，在这种情况下坐标从屏幕的另一侧计算。

在这种情况下，在一个 80 列宽度的屏幕上绘制 `#draw box 1 60 10 70` 等效于 `#draw box 1 -21 10 -11`。

但是在不同宽度的屏幕上，盒子会被绘制在不同的位置。

您可以使用颜色代码或颜色名称为选项添加前缀来给线条和形状上色。

您可以进一步为该选项添加以下前缀:

前缀|说明
:-|:- 
ASCII|将在 ASCII 模式下绘制。
BALIGN|将文本底部对齐。
BLANKED|将绘制空白线条和角。
BOLD|将用粗体字母绘制文本。
BOTTOM|如果可能的话，将在底部绘制。
BUMPED|将在绘制之前输入一个enter。
CIRCLED|将绕着角。
CONVERT|将使用元转换绘制文本。
CROSSED|将越过角。
CURSIVE|将用花体字母绘制文本。
FAT|将使用胖字母绘制文本。
FILLED|将填满圆圈和菱形。
FOREGROUND|即使会话未激活也会绘制。
GRID|将表格绘制为网格。
HORIZONTAL|如果可能的话，将水平绘制。
HUGE|将用巨大的字母绘制文本。
JEWELED|将在角绘制菱形。
JOINTED|将绘制角。
LALIGN|将左对齐文本。
LEFT|如果可能的话，将在左侧绘制。
NUMBERED|将绘制编号，主要用于调试。
PRUNED|将修剪角。
RIGHT|如果可能的话，将在右侧绘制。
ROUNDED|将绕过角。
SANSSERIF|将用无衬线字母绘制文本。
SCALED|将使正方形适合文本大小。
SCROLL|将在滚动区域中绘制。
SHADOWED|将给大文本加阴影。
TALIGN|将大文本顶部对齐。
TEED|将在角绘制T型。
TRACED|将追踪大文本。
TOP|如果可能的话，将在顶部绘制。
TUBED|将绘制管而不是线。
UALIGN|将打开并重新包装文本。
UNICODE|将在 unicode 模式下绘制。
VERTICAL|如果可能的话，将垂直绘制。

有以下几种类型可用：

* __[HORIZONTAL] BAR {\<MIN>;\<MAX>;[COLOR]}__  
绘制一个条，使用两个 256 颜色代码进行颜色渐变。

* __[BOXED|FOREGROUND] BUFFER__  
绘制回滚缓冲区。

* __[BOXED] MAP__  
绘制地图。

* __[ASCII|UNICODE|HUGE] BOX {[TEXT1]} {[TEXT2]}__  
绘制一个盒子。

* __[BLANKED|CIRCLED|CROSSED|JEWELED|ROUNDED|TEED|PRUNED] CORNER__  
绘制一个角。

* __[BLANKED|HORIZONTAL|NUMBERED|TUBED|VERTICAL] LINE {[TEXT]}__  
绘制线条。

* __RAIN {\<VARIABLE\>} {[SPAWN]} {[FADE]} {[LEGEND]}__  
绘制数字雨。

* __[JOINTED|TOP|LEFT|BOTTOM|RIGHT] SIDE__  
绘制一个盒子的一个或多个边。

* __[GRID] TABLE {[LIST1]} {[LIST2]}__  
绘制一个表格。

* __[HUGE] TILE {[TEXT1]} {[TEXT2]}__  
绘制一块瓷砖。

所有绘图类型都采用可选的文本参数，只要定义了足够大的有效空间。

文本自动进行文字包装，可以使用 `CALIGN`、`LALIGN`、`RALIGN`、`UALIGN` 等选项定制。

```
示例：
#draw Blue box 1 1 3 20 {Hello world!}
```

另可参见：[Buffer](#buffer)，[Echo](#echo)，[Grep](#grep)，[Showme](#showme)。

# Echo

> 语法: #echo {format} {argument1} {argument2} {etc}

`#Echo(显示)` 在屏幕上显示带有格式选项的文本，请使用 `#help format` 查看更多信息。

与 `#showme` 命令不同，`#echo` 命令不会触发 `#action`。

与 `#showme` 命令一样，您可以将 {format} 参数拆分为两个大括号参数，第二个参数是行号。

有关更多信息，请参见 [Format](#format) 和 [Prompt](#prompt) 的帮助文件。

```
示例: 
#echo {The current date is %t.} {%Y-%m-%d %H:%M:%S}
#echo {[%38s][%-38s]} {Hello World} {Hello World}
#echo {{this is %s on the top row} {1}} {printed}

示例：
#echo {%c%h} {light green} {【逍遥行】}
--这将用亮绿色显示被 # 填充满的标题。
##############【逍遥行】##############
```
另可参见: [Buffer](#buffer)，[Grep](#grep)，[Showme](#showme)。

# Edit

> 语法：#edit {option} [argument]

`#Edit(编辑)` 命令可用于将默认行编辑器转换为文本编辑器。

* #edit create \<arguments>  
创建编辑器，使用提供的参数进行初始化。
* #edit load \<variable>  
创建编辑器，使用提供的列表变量进行初始化。
* #edit read \<filename>  
创建编辑器，使用提供的文件初始化。
* #edit resume  
挂起后恢复编辑。
* #edit save \<variable>  
将编辑器保存到指定的变量。
* #edit suspend  
挂起编辑，类似于按回车键，但不触发事件。
* #edit write \<filename>  
将编辑器内容写入文件。

```
示例：
#edit create {bli}{bla}{blo}
```

另可参见：[Cursor](#cursor)，[Macro](#macro)。

# Editing

下表展示了默认快捷键绑定功能。

快捷键           | 功能
:---            | :---
alt b           | 光标移到单词左侧
alt f           | 光标移到单词右侧
ctrl a          | 光标移到开头
ctrl b          | 光标向后
ctrl c          | 清除行
ctrl d          | 删除或退出
ctrl e          | 光标移到尾部
ctrl f          | 光标向前
ctrl g          | null
ctrl h          | backspace
ctrl i          | tab
ctrl j          | enter
ctrl k          | 向光标右删除
ctrl l          | 重绘输入行
ctrl m          | enter
ctrl n          | 选择下一条历史命令
ctrl o          | null
ctrl p          | 选择上一条历史命令
ctrl q          | null
ctrl r          | 进入反向历史搜索
ctrl s          | null
ctrl t          | 锁定回滚缓冲区
ctrl u          | 向光标左侧删除
ctrl v          | 转换元字符
ctrl w          | 向单词左侧删除
ctrl x          | null
ctrl y          | 粘贴
ctrl z          | 挂起
arrow left      | 光标向左
arrow right     | 光标向右
arrow up        | 上一个输入行
arrow down      | 下一个输入行
ctrl arrow left | 光标移到单词左侧
ctrl arrow right| 光标移到单词右侧
backspace       | backspace
alt backspace   | 向左清除
ctrl backspace  | 清除行
delete          | 删除
ctrl delete     | 向单词右侧删除
end             | 光标移到尾部
ctrl end        | 回滚缓冲区尾部
enter           | enter
shift-enter     | soft enter
home            | 光标移到开头
ctrl home       | 回滚缓冲区开头
page up         | 回滚缓冲区向上翻页
page down       | 回滚缓冲区向下翻页
tab             | 向后补全单词
shift-tab       | 向前补全单词

另可参见：[Cursor](#cursor)，[Edit](#edit)，[Macro](#macro)。

# Else

> 语法: #else {commands}

`#Else(否则)` 语句应该跟随 `#IF` 或 `#ELSEIF` 语句使用，并且只有在前面的 `#IF` 或 `#ELSEIF` 语句为 `false` 时才被调用。

```
示例:
#if {1d2 == 1} {
  smile
};
#else {
  cry
};
```
另可参见: [Case](#case)，[Default](#default)，[Elseif](#elseif)，[If](#if)，[Switch](#switch)，[Regex](#regex)。

# Elseif

> 语法: #elseif {conditional} {commands}

`#Elseif` 语句应该跟随 `#IF` 或 `#ELSEIF` 语句使用，并且仅在语句为 `true` 且前面的 `#IF` 和 `#ELSEIF` 语句为 `false` 时才调用。

```
示例: 
#if {1d3 == 1} {
  smirk
};
#elseif {1d2 == 1} {
  snicker
};
#else {
  laugh
};
```

另可参见: [Case](#case)，[Default](#default)，[Else](#else)，[If](#if)，[Switch](#switch)，[Regex](#regex)。

# End

> 语法: #end {message}

终止 TinTin 程序并返回 shell。  

通常：结束当前会话可使用 ctrl-d。  
清除已输入的内容可使用 ctrl-c。

消息在 tintin 终止前立即打印。  
如果消息是 `#end {\}`，tintin 将被无声地终止。

另可参见: [Zap](#zap)。

# Escape Codes

TinTin 中的 escape 字符是反斜杠: `\`，可以与几个字符组合使用来创建 escape 代码。

字符  |释义
:-   |:-
\a   |会在终端发出嘟嘟声。
\c   |将发送 ctrl-a 的控制字符 \ca。
\e   |将开始一个 escape 序列。
\f   |将发送换页。
\n   |将发送换行。
\r   |将发送回车符。
\t   |将发送水平制表符。
\x   |将打印十六进制 8 位符号，如\xFF。
\x7B |将发送 “{” 字符。
\x7D |将发送 “}” 字符。
\u   |打印 16位 unicode 字符，如：\uFFFD。
\u{} |打印 8-21位 unicode 字符，如：\u{2AF21}。
\U   |打印 21位 unicode 字符，如：\U02AF21。
\v   |打印垂直制表符。
\\\  |将打印单个 \ 。

当使用 `#showme`、`#send` 或 `#line` 时，以 `\` 结尾的行将停止 tintin 追加换行符。

要在触发器或别名中转义参数，请使用 `%%0 %%1 %%2`等。

```
来自dzp@pkuxkx的释义：

每多一层套嵌关系加一个%，防止参数被吃。

例如：
#act {%*的个人档案}{
  #var myname %1;
  #act {你是一位%*岁的%*婚%*性人类}{
    #var myage @ctd{%%1};
    #var mygender %%3
  }
}

内部实现示例：
#kill action
#OK: #ACTION LIST CLEARED.
#action 
####### ACTIONS ###########
#action {^test %1} {#action {^hello %%1} {say %1: hello %%1}}
#OK. {^test %1} NOW TRIGGERS {#action {^hello %%1} {say %1: hello %%1}} @ {5}.
#action 
####### ACTIONS ###########
#ACTION {^test %1}={#action {^hello %%1} {say %1: hello %%1}} @ {5}
#showme test dzp
test dzp
#action 
####### ACTIONS ###########
#ACTION {^hello %1}={say dzp: hello %1} @ {5}
#ACTION {^test %1}={#action {^hello %%1} {say %1: hello %%1}} @ {5}
#showme hello xgg
CMD: say dzp: hello xgg
hello xgg
你说道：「dzp: hello xgg」
```

另可参见: [Characters](#characters)，[Colors](#colors)，[Coordinates](#coordinates)，[Mathematics](#mathematics)，[PCRE](#pcre)。

# Event

> 语法：#event {event type} {commands}

`#Event(事件)` 命令允许为预定的客户端事件创建触发器。

使用没有参数的 `#event` 将列出大多数可用的事件，及其简要描述。

使用 `#event %*` 将显示所有已定义的事件。

使用 `#info {events} {on}` 查看事件抛出信息。

事件如同一般触发器一样需要区分大小写和事件名称，必须全部使用大写字母来定义。

每种事件类型只能定义一个事件。

要启用鼠标事件，请使用 `#config mouse_trace on`。  

要查看鼠标事件，使使用 `#config mouse_trace info`。

***

下面展示了一些事件的详细参数。

## CATCH EVENTS

`CATCH <EVENT>`  
一些事件可以用 `CATCH` 为前缀来中断默认行为。

## CLASS EVENTS

`CLASS ACTIVATED [CLASS]`  
`CLASS_CLEAR [CLASS]`  
`CLASS CREATED [CLASS]`  
`CLASS DEACTIVATED [CLASS]`  
`CLASS DESTROYED [CLASS]`  
`CLASS_LOAD [CLASS]`  

%0 class name

## GAG EVENTS

`GAG <EVENT>`  
一些事件可以用 `GAG` 为前缀来消除默认系统消息显示。

## INPUT EVENTS

`EDIT STARTED`  `EDIT FINISHED`  
%0 name  %1 lines %2 size %3 data

`RECEIVED KEYPRESS` `PROCESSED KEYPRESS`  
%0 character  %1 unicode index  %2 edit row  %3 edit column

`RECEIVED INPUT [NAME]`  
%0 raw text

`RECEIVED INPUT CHARACTER`  
%0 character  %1 unicode index  %2 size  %3 width

`SEND OUTPUT`  
%0 raw text %1 size

`SENT OUTPUT`  
%0 raw text %1 size

## MAP EVENTS

`END OF PATH`  `END OF RUN` `MAP UPDATED VTMAP`  
这些事件没有额外的参数。

`MAP CREATE EXIT` `MAP DELETE EXIT`  
%0 vnum  %1 exit name  %2 exit cmd  %3 exit vnum

`MAP CREATE ROOM`  `MAP DELETE ROOM`  
%0 vnum  %1 name

`MAP CREATE ROOM`  `MAP DELETE ROOM`  
%0 vnum

`MAP ENTER ROOM [VNUM]`  
%0 new vnum  %1 old vnum %2 direction

`MAP EXIT ROOM [VNUM]`  
%0 old vnum  %1 new vnum %2 direction

`MAP FOLLOW MAP`  
%0 old vnum  %1 new vnum  %2 exit name

`MAP REGION <MOUSE>`  `MAP ROOM <MOUSE>`  
%0 row  %1 col  %2 -row  %3 -col  %5 vnum  %6 info

## MOUSE EVENTS

鼠标行为                 | 释义
:---                    |:----
DOUBLE-CLICKED \<MOUSE> | 双击鼠标
LONG-CLICKED \<MOUSE>   | 长点鼠标
MOVED \<MOUSE>          | 移动鼠标 
PRESSED \<MOUSE>        | 按下的鼠标
SHORT-CLICKED \<MOUSE>  | 短点鼠标
RELEASED \<MOUSE>       | 释放鼠标
SCROLLED \<MOUSE>       | 滚动鼠标
TRIPLE-CLICKED \<MOUSE> | 点击三次鼠标

鼠标事件参数：%0 row %1 col %2 -row %3 -col %4 word %5 line。

`MAP <MOUSE EVENT>`  
鼠标事件可以以 `MAP` 为前缀，仅当事件发生在 VT100 地图区域内才会触发。

`SWIPED [DIR]`  
%0 dir  %1 button  %2 row  %3 col  %4 -row  %5 -col  
%6 row  %7 col  %8 -row  %9 -col %10 rows %11 cols

## OUTPUT EVENTS

`BUFFER UPDATE`  `DISPLAY UPDATE`  
这些事件没有额外的参数。

`RECEIVED LINE`        
%0 raw text %1 plain text  

`RECEIVED OUTPUT`  
%0 raw text  

`RECEIVED PROMPT`  
%0 raw text %1 plain text  

## PORT EVENTS

`CHAT MESSAGE`  `PORT MESSAGE`  
%0 raw text  %1 plain text

`PORT CONNECTION`  
%0 name %1 ip %2 port

`PORT DISCONNECTION`  
%0 name %1 ip %2 port

`PORT LOG MESSAGE`  
%0 name %1 ip %2 port %3 data %4 plain data

`PORT RECEIVED MESSAGE`
%0 name %1 ip %2 port %3 data %4 plain data

## SCAN EVENTS

`SCAN CSV HEADER`  
`SCAN CSV LINE`  
`SCAN TSV HEADER`
`SCAN TSV LINE`  

%0 all args %1 arg1 %2 arg3 .. %99 arg99

## SCREEN EVENTS

`SCREEN FOCUS`  
%0 focus (0 or 1)

`SCREEN LOCATION`  
%0 rows %1 cols  %2 height %3 width

`SCREEN MOUSE LOCATION`  
%0 row  %1 col  %2 -row  %3 -col  %4 pix row  %5 pix col  
%6 -pix row  %7 -pix col  %8 location

`SCREEN RESIZE`  
%0 rows %1 cols %2 height %3 width

`SCREEN SPLIT`  
%0 top row %1 top col %2 bot row %3 bot col

`SCREEN UNSPLIT`  
%0 top row %1 top col %2 bot row %3 bot col

## SESSION EVENTS

`SESSION ACTIVATED`  
%0 name

`SESSION CONNECTED`  
%0 name %1 host %2 ip %3 port %4 file

`SESSION CREATED`  
%0 name %1 host %2 ip %3 port %4 file

`SESSION DEACTIVATED`
%0 name

`SESSION DISCONNECTED`  
%0 name %1 host %2 ip %3 port

`SESSION TIMED OUT`  
%0 name %1 host %2 ip %3 port

## SYSTEM EVENTS

`DAEMON ATTACHED`
%0 file %1 pid

`DAEMON DETACHED`  
%0 file %1 pid

`PROGRAM START`  
%0 startup arguments

`PROGRAM TERMINATION`  
%0 goodbye message

`READ ERROR`  
%0 filename %1 error message

`READ FILE`  
%0 filename

`WRITE ERROR`  
%0 filename %1 error message

`WRITE FILE`  
%0 filename

`SYSTEM CRASH`  
%0 message

`SYSTEM ERROR`  
%0 name %1 system msg %2 error %3 error msg

`UNKNOWN COMMAND`  
%0 raw text

`SIGUSR`  
%0 signal

## TELNET EVENTS

`IAC <EVENT>`  
可使用 `#config telnet info` 来查看 IAC TELNET 事件信息。

IAC 事件                  | 参数
:---                     |:---
`IAC SB GMCP [MODULE]`   |%0 module    %1 data  %2 plain data
`IAC SB MSSP`            |%0 variable  %1 data
`IAC SB MSDP`            |%0 variable  %1 data  %2 plain data
`IAC SB MSDP [VAR]`      |%0 variable  %1 data  %2 plain data
`IAC SB NEW-ENVIRON`     |%0 variable  %1 data  %2 plain data
`IAC SB ZMP <VAR>`       |%0 variable  %1 data
`IAC SB <VAR>`           |%0 variable  %1 raw data  %2 plain data

## TIME EVENTS

`DATE <MONTH-DAY OF MONTH> [HOUR:MINUTE]`  
`DAY [DAY OF MONTH]`  
`HOUR [HOUR]`  
`MONTH [DAY OF MONTH]`  
`TIME <HOUR:MINUTE>[:SECOND]`  
`WEEK [DAY OF WEEK]`  
`YEAR [YEAR]`  

%0 year  %1 month  %2 day of week  %3 day of month  %4 hour %5 minute  %6 second

## VARIABLE EVENTS

`VARIABLE UPDATE <VAR>`  
%0 name %1 new value %2 path

`VARIABLE UPDATED <VAR>`  
%0 name %1 new value %2 path

## VT100 EVENTS

`VT100 SCROLL REGION`  
%0 top row %1 bot row %2 rows %3 cols %4 wrap

***

要查看所有事件触发器，请使用 `#info event on`。

这样就可以得到一些有用的信息，来消除一些事件信息的显示。

```
示例：
#event {SESSION CONNECTED} {#read mychar.tin}
```

注：您可以使用 `#unevent` 命令删除事件。

***

下面是一些事件的详细说明：

**Chronological Events**  

所有按时间顺序排列的事件设置以下参数:  
%0-year 使用 4 位数字填充，  
%1-month 使用 2 个零填充数字，  
%2-week 使用 2 个零填充数字，  
%3-day 在 month 中使用 2 个零填充数字，   
%4-hour 使用 2 个零填充数字，  
%5-minute 使用 2 个零填充数字，  
%6-second 使用 2 个零填充数字。

**DATE <MONTH-DAY> [HOUR:MINUTE]**

在给定的日期和时间触发事件。  
必须提供日期，时间是可选的。  
如果没有时间，它会在午夜触发。

```
示例: 
#event {DATE 12-31 23:59}
{#showme 再过一分钟新年就要到来了!}
```

**DAY [DAY]**

触发每月的每一天或某一天。

**HOUR [HOUR]**

在一天中的每小时或给定时间触发。

**MINUTE [MINUTE]**

在一小时的每一分钟或每一分钟触发。

**MONTH [MONTH]**

每月开始或午夜给定月份触发。

**SECOND [SECOND]**

在一分钟的每一秒或每一秒触发一次。

**TIME \<HOUR:MINUTE\>**

在给定时间触发。

**WEEK [WEEK]**

在每周开始时或午夜给定的一周触发。

**YEAR [YEAR]**

在每年的开始或午夜的某一年触发。

**CHAT MESSAGE**

收到 `#chat` 消息时触发。  

%0 包含原始数据，%1 包含修改后的数据。

**END OF PATH**

当使用 `#path walk` 到达路径末端时，此事件触发一次。

**IAC**

此事件触发所有 `telnet negotiations`。  

使用 `#config {debug telnet} {on}` 查看 telnet 事件发生时的正确名称。  

如果为通常由 mud 客户端 (如 IAC SB TTYPE) 处理的 `telnet negotiations`创建 telnet 事件，则只执行该事件，自动响应将被阻止。

**IAC [DO|DON'T|WILL|DON'T] [OPTION]**

当触发 `DO, DON'T, WILL or WON't` 选项时，这将阻止 TinTin 自动处理该选项，你必须自己处理。

**IAC SB GMCP <MODULE> IAC SE**

GMCP (通用 Mud 通信协议) 上触发此事件。  

%0 参数包含模块名称，%1 参数包含 JSON 数据。  

JSON 数据被转换为 TinTin 的内部变量系统，因此可以使用 `#variable {gmcp [%0]}{%1}` 直接存储数据。  

原始 JSON 数据存储在 %2 参数中。

**IAC SB MSDP [VARIABLE]**

此事件触发 [MSDP](https://tintin.sourceforge.io/scripts/msdp.php) (Mud Server 数据协议) 子协商。  

%0 参数包含变量的名称，%1 参数包含变量的值。  

值转换为 TinTin 的内部变量系统，因此可以使用 `#variable {msdp [%0]} {%1}` 直接存储数据。

**IAC [DO|DON'T|WILL|DON'T] MSP**

此事件在 [MSP](https://tintin.sourceforge.io/scripts/msp.php) (MUD 声音协议) 子协商上触发。

**IAC SB MSSP [VARIABLE]**

此事件在 MSSP (Mud 服务器状态协议) 子协商上触发。  

%0 参数包含变量的名称，%1 参数包含变量的值。  

如果变量作为数组发送，则为每个索引生成名称/值事件。

**IAC [DO|DON'T|WILL|DON'T] MXP**

MXP (Mud 扩展协议) 子协商上触发此事件。

**IAC SB NEW-ENVIRON <IS|INFO|SEND> [VAR|USR]**

此事件触发新环境子协商。  

根据协商类型，您必须将发送、是或信息附加到事件名称，如使用 `#config {debug telnet} {on}` 时所示。  

%0 参数包含变量的名称，%1 参数包含变量的值。

**IAC SB ZMP**

ZMP 子协商上触发此事件。  

根据 ZMP 包，您必须将包附加到事件名称，如使用 `#config {debug telnet} {on}` 时所示。  

%0 参数包含 ZMP 包数据。

**IAC SB**

任何未定义的子协商都会触发此事件。  

一些 telnet 选项将被命名，其他选项将是一个数字，如使用 `#config {debug telnet} {on}` 时所示。  

%0 参数将包含子协商内的数据。

**MAP ENTER MAP**

进入地图时触发。%0 包含新的 vnum。

**MAP ENTER ROOM [VNUM]**

在自动映射程序中进入新房间后，此事件立即触发。房间号是 vnum。  

%0 参数包含房间的 vnum，%1 包含分区房间的 vnum。

**MAP EXIT MAP**

退出地图时触发。%0 包含旧 vnum。

**MAP EXIT ROOM [VNUM]**

此事件在退出自动映射程序中的当前房间之前立即触发。房间号是 vnum。  

%0 参数包含房间的 vnum，%1 包含目标房间的 vnum。

**PORT CONNECTION**

当进行新的套接字连接时，此事件会触发。  

%0 包含套接字号，%1 ip 地址，%2 端口号 (对于传入连接，设置为 0)。

**PORT DISCONNECTION**

当套接字断开时，此事件触发。  

%0 包含套接字号，%1 ip 地址，%2 端口号 (对于传入连接，设置为 0)。

**PORT MESSAGE**

当套接字发送数据时，这甚至会触发。  

%0 包含套接字号，%1 ip 地址，%2 端口号 (对于传入连接，设置为 0)，%3 包含剥离的数据, %4 包含原始数据。

**PROGRAM START**

这个事件在 TinTin++ 的启动过程结束时触发。  

%0 包含客户端名称，%1 包含客户端版本。

**PROGRAM TERMINATION**

此事件在启动会话中 TinTin++ 终止进程结束时触发。

**RECEIVED INPUT**

此事件在输入键盘输入后，但在执行之前触发。%0 参数包含原始输入。

**RECEIVED LINE**

当接收到新输出时，多行输出被分解成单行输出。  

在执行任何触发器之前，此事件会触发来自服务器的每一行输出。  

%0 参数包含原始行，%1 参数包含纯行，去掉所有颜色代码，始终包含单行。

**RECEIVED OUTPUT**

在将输出分成单行之前，当接收到新输出时触发。  

%0 包含可以包含多行的原始输出。

**SCREEN RESIZE**

当程序启动时，每当屏幕调整大小时，此事件都会触发一次。  

%0 包含屏幕宽度，%1 包含屏幕高度。

**SEND OUTPUT**

此事件在命令行发送到服务器后立即触发。%0 参数包含原始命令行。

**SESSION CREATED**

创建会话时触发。  

%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字 ip 地址，%3 参数包含端口号。

**SESSION ACTIVATED**

激活会话时触发。%0 参数包含会话名称。

**SESSION CONNECTED**

会话连接到服务器后，此事件立即触发。  

%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字 ip 地址，%3 参数包含端口号。

**SESSION DEACTIVATED**

停用会话时触发。%0 参数包含会话名称。

**SESSION DISCONNECTED**

会话与服务器断开连接后，此事件立即触发。  

%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字 ip 地址，%3 参数包含端口号。

**SESSION TIMED OUT**

当会话无法连接时，此事件会触发。  

%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字 ip 地址，%3 参数包含端口号。

**VARIABLE UPDATE \<VARIABLE\>**

当创建或更新变量时，此事件会触发。  

%0 参数包含变量名，%1 参数包含变量值。

**VT100 [CPR|DA|DECID|DSR|ENQ]**

当接收到终端识别码时，这些事件会触发。  

它们记录不良，很少使用，通常可以忽略。

***

另可参见: [Button](#button)，[Delay](#delay)，[Ticker](#ticker)。

# Forall

> #forall 已经过时。  
#foreach 替代使用。

```
来自 xgg@pkuxkx 的提示：
这个命令在新版本中已被移除，
使用 #foreach 代替，
旧版本逍遥行路径显示列表时用的到，
现在已用 #foreach 重写。
```
另可参见: [Foreach](#foreach)，[Bell](#bell)，[Cr](#cr)。

# Foreach

> 语法：#foreach {list} {variable} {commands}

`#Foreach(遍历数组)` 命令就像一个简化的循环。  

列表中的每个项目将在执行时存储在变量中，并可以在命令部分中使用。

所提供列表中的项目必须使用分号 `;` 分隔，或者用大括号将它们括起来。

```
示例: 
#foreach {Bob;Jim;Tom} {name} {say Hello $name!}
#foreach {{Bob}{Jim}{Tom}} {name} {say Hello $name!}
--相当于：hello Bob!hello Jim!hello Tom!
```

要使用 foreach 命令循环遍历列表 (或嵌套变量) 中的所有项目，请使用 `$<list>[%*]`，新版本中请用 `*<list>[]`。

另可参见: [Break](#break)，[Continue](#continue)，[List](#list)， [Loop](#loop)，[Parse](#parse)，[Repeat](#repeat)，[Return](#return)，[While](#while)。

# Format

> 语法：#format {variable} {format} {argument1} {argument2} {etc}

`Format(格式化)` 允许您像 `C` 中的 `sprintf` 函数一样将字符串存储在给定的变量中。

此命令有一些增强和限制，并且最多可以给出 30 个参数。

如果在 `alias` 或 `action` 中使用 `#format`，则必须将 `%1` 转义为
`%+1s` 或 `%%1s` 或 `%\1s`，来确保 `%1` 不会被触发替换。

格式	|参数	|描述
:- |:- |:-
%+9s	|String 	|前方插入9个空格
%-9s	|String 	|后方插入9个空格
%.8s	|String 	|最多打印8个字符
%a	 |Number	 |打印对应的 ascii 字符
%c	 |String |使用高亮颜色
%d  |Number |用整数格式打印一个数字
%f  |String  |使用浮点格式打印数字
%g  |Number	 |对数字执行千位分组。
%h	 |String |将参数转换为标题
%l  |String |将参数小写
%m  |String |进行数学运算
%n	 |String |第一个字母大写
%p  |String |剥离前导和尾随空格
%r  |Reverse |翻转参数(hiya = ayih)
%s  |String |普通字符串参数
%t	 |String |在参数中使用[ strftime ](http://www.manpagez.com/man/3/strftime/)格式创建时间戳
%u	 |String |将整个参数大写
%w	 |String |以列表形式包装参数，可选 {{string} {width}} 语法
%x  |hex |打印相应的字符集字符
%A	 |Char |打印对应的 ascii 值
%D  |hex |将十六进制转换为十进制
%H	 |String |打印参数的 64 位散列值
%L	 |String |打印参数的长度
%M  |Number |将数字转换为公制
%S  |String |存储拼写错误的数量
%T	 |Epochtime	|打印自epoch以来的秒数
%U	 |Epochtime	|打印自epoch以来的微秒数
%X  |dec |将十进制转换为十六进制

```
来自 dzp@pkuxkx 的释义：
epoch 就是 E 纪元，也称为 Unix 纪元。
也就是自格林威治时间（GMT+0） 1970 年 1 月 1 日 00:00:00 以来的秒数。
所谓的「时间戳」，就是这个东西。
有时候也叫 timestamp。
```
```
示例:
#alias {time}
{
        #format line {%cThe time is: %t} {light green} {%Y-%m-%d %T};
        #showme {$line}
}
--使用高亮绿色

示例：
#format {test} {%%} 
--一个 % 字符

示例：
#echo {%c%h} {light green} {【逍遥行】};
--这将用亮绿色显示被 # 填充满的标题。
##############【逍遥行】##############
```

另可参见: [Cat](#cat)，[Echo](#echo)，[Function](#function)，[Local](#local)，[Math](#math)，[Replace](#replace)，[Script](#script)，[Time](#time)，[Variable](#variable)。

# Function

> 语法: #function {name} {operation}

`Function(函数)` 命令允许你在文本中执行一个脚本，然后用该函数执行完后生成的文本替换该函数调用。

函数命令是别名和变量之间的交叉。

除了可以传递参数之外，函数就像变量一样使用。  

请注意，应使用 `#return` 结束函数，或设置 {result} 变量。

函数的名称必须只存在字母、数字、下划线，函数名称的第一个字符必须始终是字母。

要使用函数，请在函数名称前使用 `@` 字符。

> 语法: `@<functionname> {<arguments>}` 

参数存储在 %0 到 %99 中，%0 保存所有参数，%1 第一个, %2 第二个等。  

参数通过大括号或分号来分隔。

可以通过添加其他 `@` 符号来转义函数。

```
示例：
#function test #return 42;#showme @@test{}
```
```
示例：
#function {rnd} {#math {result} {1 d (%2 - %1 + 1) + %1 - 1}}
#show 100-200中的随机数字: @rnd{100;200}

示例：
#function gettime {#format result %t %H:%M}
#show 当前时间：@gettime{}
```
```
示例:
#function {time}
{
	#if {"%0" == ""}
	{
		#format {epoch} {%T}
	};
	#else
	{
		#var epoch %0
	};
	#format {time} {%t} {{%T}{$epoch}};
	#return $time
}
#showme The time is @time{}
```

上面函数的 `#if` 部分将检查是否传递了参数，  
如果传递了，参数 (假设是时间戳) 存储在 $epoch 中,   
如果不是，则使用 `#format {epoch} %T` 检索自 1970 年以来的当前秒数。  
下一个 $epoch 用于将当前时间存储在 $result 中。  
使用: `#showme @time{}` 将显示当前时间。


可以在函数中的任何地方使用 `#return` 命令。  

但是当执行到 `#return` 命令时，函数调用就结束了。  

您可以在任何触发器中使用 `#return` 提前结束命令执行。

注: 您可以使用 `#unfunction` 命令删除函数。

另可参见: [Format](#format)，[Local](#local)，[Math](#math)，[Replace](#replace)，[Script](#script)，[Variable](#variable)。

# Gag

> 语法: #gag {string}

在屏幕上消除任何包含字符串的行的显示。

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

```
示例: 
#gag {%iTwinkie chats}
```
如果 Twinkie 是一个讨厌的人，这个 gag 会阻止他的聊天被显示出来。  

一开始的 %i 使得 gag 具有关联性，所以如果 Twinkie 以 TWINKIE 的身份登录，gag 仍然有效。

```
来自 xgg@pkuxkx 的注释：

有时使用 #gag 会出现大量">"符号，
这时候可以使用：
#gag {^> $}
并且有时会出现大量空行：
#gag {^$}
在这种情况下要显示空行：
#line ignore #showme {}
```

可以使用 `gag events` 来消除一些系统消息的显示。

注: 您可以使用 `#ungag` 命令删除文本消除。

另可参见: [Action](#action)，[Event](#event)，[Highlight](#highlight)，[Prompt](#prompt)，[Substitute](#substitute)。

# GMCP

MUD 服务器通常希望向 MUD 客户端发送不一定需要显示的附加数据，以及需要一种方法来识别支持带外数据的客户端。

GMCP 的历史始于使用 `TELNET code 200` 的 Achaea TELNET Client Protocol  (ATCP)，该协议于 2008 年由 cMUD 实现。

但是，ATCP只允许发送纯文本。

MSDP (Mud 服务器数据协议) 于2009年开发，提供了一种定义无类型变量、数组、表和命令的标准化方法。

2010 年 IRE 推出 mudstandards.org 尝试更新 ATCP 协议。

这产生了使用 `TELNET code 201` 的 ATCP2 概念协议，后来被重命名为 GMCP。

GMCP 使用 JSON 语法定义类型化数据。

2011 年 mudstandards.org 失效。

此处提供了 GMCP 协议和 GMCP over MSDP 的技术描述。

除了发送结构化数据之外，MSDP over GMCP 还提供标准化的事件处理。

通过 GMCP over MSDP 的服务器将能够同时使用 MSDP 和 JSON 标准来定义结构化数据，并以任何一种格式执行 MSDP 事件处理。

GMCP 实现为 Telnet 选项：[RFC854](https://tintin.mudhalla.net/rfc/rfc854)、[RFC855](https://tintin.mudhalla.net/rfc/rfc855)。

服务器和客户端像协商任何其他 telnet 选项一样协商 GMCP 的使用。

一旦就选项的使用达成一致，就使用选项子协商在服务器和客户端之间交换信息。

**服务端命令**

* IAC WILL GMCP  
--表明服务器想开启 GMCP。

* IAC WONT GMCP  
--表明服务器想关闭 GMCP。

**客户端命令**

* IAC DO GMCP  
--表明客户端接受 GMCP 子协商。

* IAC DONT GMCP  
--表明客户端拒绝 GMCP 子协商。

**握手协议**

当客户端连接到启用 GMCP 的服务器时，服务器应发送 `IAC WILL GMCP`。

客户端应该用 `IAC DO GMCP` 或 `IAC DONT GMCP` 来回应。

一旦服务器收到 `IAC DO GMCP`，客户端和服务器都可以发送 GMCP 子协商。

客户端不应发起协商，如果发生这种情况，服务器应遵守状态更改。

为了避免触发循环，服务器不应响应来自客户端的协商，除非它正确实现了 [RFC1143](https://tintin.mudhalla.net/rfc/rfc1143.html) 中的 Q 方法。

更多信息请查看 [「GMCP 协议」](https://tintin.sourceforge.io/protocols/gmcp)。

要查看 Telnet 协商信息，请使用：`#config telnet info`。

要查看 Telnet 事件，请查看[「Event」](#event) TELNET EVENTS 相关条目。

```
北大侠客行 GMCP 协商

/* ====== 说明 ======

需要在游戏中打开接收 gmcp 频道。

在游戏中输入 gmcp 查看：

GMCP 频道收听汇总：
BUFF(Buff)         〖开〗
移动信息(Move)      〖开〗
战斗相关(Combat)    〖开〗
人物状态(Status)    〖开〗

你接收 GMCP 信息的格式为 raw。
你可以用 gmcp <channel> on/off 开关 GMCP 频道。

需要在连接服务器之前加载握手事件。
*/

#class gmcp open;

#nop 定义字符;
#var TELNET[IAC]  \xFF;
#var TELNET[DONT] \xFE;
#var TELNET[DO]   \xFD;
#var TELNET[WONT] \xFC;
#var TELNET[WILL] \xFB;
#var TELNET[SB]   \xFA;
#var TELNET[SE]   \xF0;
#var TELNET[GMCP] \xC9;

#nop GMCP 握手事件;
#EVENT {IAC WILL GMCP} {
  #send {$TELNET[IAC]$TELNET[DO]$TELNET[GMCP]\};
};

#nop GMCP 调试;

#config {debug telnet} {on};

#eve {IAC SB GMCP} {
  #echo {%c%h} {light green} {【GMCP 事件：%0】};
  #echo {<139>参数0:<099>%0};
  #echo {<139>参数1:<099>%1};
  #echo {<139>参数2:<099>%2};
  #echo {<139>参数3:<099>%3};
  #echo {<139>参数4:<099>%4};
  #echo {<139>参数5:<099>%5};
  #echo {%c%h} {light green};
};

/* ======= 数据示例 ============

RCVD IAC SB GMCP
IAC SB GMCP GMCP.Status IAC SE
#########【GMCP 事件：GMCP.Status】#########
参数0:GMCP.Status
参数1:{qi}{497}{food}{218}{water}{259}{jing}{397}
参数2:GMCP.Status {"qi":497,"food":218,"water":259,"jing":397}
参数3:有
参数4: northwest、north 和 east
参数5:
###########################################

RCVD IAC SB GMCP
IAC SB GMCP GMCP.Move IAC SE
##########【GMCP 事件：GMCP.Move】#########
参数0:GMCP.Move
参数1:{1}{{result}{true}{dir}{{1}{south}{2}{north}{3}{east}{4}{west}}{short}{西大街}}
参数2:GMCP.Move [{"result":"true","dir":["south","north","east","west"],"short":"西大街"}]
参数3:有
参数4: northwest、north 和 east
参数5:
###########################################

*/

#class gmcp close;
```

另可参见：[MSDP](#msdp)，[MSLP](#mslp)。

# Greeting

> 语法: #help greeting

将简单明了地向您显示每次启动客户端时显示的问候消息 (其中包含客户端版本号)。

如果您希望看到它，并且它在缓冲区中不再可用，则很有用。

这实际上不是一个命令，因为你只能通过 `#help greeting` 访问它。

# Grep

> 语法:#grep [page] {search string}

此命令在回滚缓冲区中搜索匹配的行。  

显示的匹配数量等于您的屏幕尺寸。

页码是可选的，你可以使用页码进一步搜索。

使用通配符以获得更好的搜索结果。

注意搜索字符串区分大小写，可以使用 `%i` 禁用。

默认情况下，grep 从回滚缓冲区的末尾搜索到开头，这可以通过使用负号来逆转。

```
示例: 
#grep Bubba tells you
--这将展示所有 Bubba 告诉你的一些事情。
```

另可参见: [Buffer](#buffer)，[Echo](#echo)，[Showme](#showme)。

# Help

> 语法: #help {subject}

没有参数 `#help` 将列出所有可用的帮助主题。

**注：Help 命令比在线手册更新。**

使用 `#help %*` 将显示所有帮助条目。

```
示例: 
#help alias
--将显示 #alias 的帮助文件。
```

要创建一个包含所有内部帮助主题的文件: 

```
#buffer clear;
#help %*;
#buffer write help.txt
```

# Highlight

> 语法: #highlight {string} {color names} {priority}

`#Highlight(高亮显示)` 命令用于突出显示文本字符串。

可用的颜色选项有：

* reset  
--重置颜色到默认状态

* light  
--使用 ansi 十六色中的亮色，{light \<color>}

* dark  
--使用 ansi 十六色中的暗色，{dark \<color>}

* underscore  
--添加下划线

* blink  
--文本闪烁

* reverse  
--反转前景色和背景色

* b  
--使下一种颜色成为背景色

可用的颜色名称有：

颜色代码 | 颜色     |颜色代码  | 颜色
:-      |:-       |:-       |:-
\<F06B> | azure   | \<F08F> | Azure
\<F00B> | blue    | \<F00F> | Blue
\<F0BB> | cyan    | \<F0FF> | Cyan
\<F000> | ebony   | \<F666> | Ebony
\<F0B0> | green   | \<F0F0> | Green
\<F0B6> | jade    | \<F0F8> | Jade
\<F6B0> | lime    | \<F8F0> | Lime
\<FB0B> | magenta | \<FF0F> | Magenta
\<FB60> | orange  | \<FF80> | Orange
\<FB06> | pink    | \<FF08> | Pink
\<FB00> | red     | \<FF00> | Red
\<F888> | silver  | \<FDDD> | Silver
\<F860> | tan     | \<FDB0> | Tan
\<F60B> | violet  | \<F80F> | Violet
\<FBBB> | white   | \<FFFF> | White
\<FBB0> | yellow  | \<FFF0> | Yellow

`%1-%99` 变量可用作与任何变量匹配的 “通配符”文本。

`%0` 变量绝对不能用于 `#highlight`。

如果 `<string>` 参数以 `^` 开头，那么只有该文本位于行首时才会被高亮显示。

除了颜色名称，还可以使用颜色代码：[「color codes」](#colors)。

```
示例：
#high {Valgar} {reverse blink}
--每次出现"Valgar"都会使用闪烁着的颜色反转来突出显示。

示例：
#high {^You %1} {bold cyan}
--任何以"You"开头的行都用粗体青色表示。

示例：
#high {Bubba} {red underscore b green}
--使用红色下划线文本在绿色背景上高亮显示"Bubba"。

示例: 
#high {^{你|你的}%*} {light cyan}
--这将用亮青色突出显示以 “你” 和 “你的” 开头的行。

示例: 
#high {%* tells you '%*'} {<ace>}
--使用"<ace>"蓝色来为匹配的行着色。
```

注：有关触发器的更多信息，请参见 `#help action`。

注：有关更高级的颜色替换，请参见 `#help substitute`。

注：此命令仅适用于 `ANSI/VT100` 终端或仿真器。

注: 您可以使用 `#unhighlight` 命令删除高亮显示。

另可参见: [Action](#action)，[Gag](#gag)，[Prompt](#prompt)， [Substitute](#substitute)。

# History

> 语法：#history {delete}        
--删除最后一个命令。

> 语法：#history {insert} {command}  
--插入一个命令。

> 语法：#history {list}      
-- 显示整个历史命令记录。

> 语法：#history {read} {filename}  
--从文件读取历史命令。  
--使用[ Event ](#event)可以在会话打开时执行此操作。

> 语法：#history {write} {filename}  
--将历史命令写入文件。  
--使用[ Event ](#event)可以在会话关闭时执行此操作。

没有参数，将显示所有可用选项。

默认情况下，所有命令都会保存到历史命令列表。

历史命令列表保存在 `~/.tintin/history.txt` 文件中。

你可以使用 `#config {REPEAT CHAR} {<character>}` 设置重复历史指令字符。

默认情况下，重复历史指令字符被设置为 `!`。

你可以用 `!` 重复最后一个命令。

或者`!<文本>` 重复以给定文本开头的最后一个命令。

您可以使用 `#config {REPEAT ENTER} {ON}` 重复最后一个命令（当您在空行上按回车键时）。

每个会话都会记住最后 1000 个唯一命令，这可以用 [config](#config) 命令来更改。

您也可以通过按 `ctrl-r`（或者通过发出 `#cursor {history search}`）进入反向历史命令搜索模式，这与 ctrl-p (上一个) 和 ctrl-n (下一个) 一起工作。

TinTin++ 默认尝试绑定上箭头和下箭头键以滚动浏览历史命令列表。

您也可以自己用 `#macro` 绑定 `#cursor {history prev}` 和 `#cursor {history next}` 来滚动浏览历史命令列表。许多 `#cursor` 命令仅在与 `#macro` 绑定时才能正常工作。

每个会话都有自己的历史列表，从启动会话继承而来。

使用 `#kill` 或 `#kill histories` 将清除历史命令列表。

启动/退出 tintin 时，启动会话将尝试自动加载/保存命令历史记录。

```
来自 xgg@pkuxkx 的说明：
这里的 ~/.tintin 目录在当前登录终端的默认用户目录中
```

另可参见: [Alias](#alias)，[Cursor](#cursor)，[Keypad](#keypad)， [Macro](#macro)，[Speedwalk](#speedwalk)，[Tab](#tab)。

# If

> 语法: #if {condition} {commands if true}  
> 语法: #if {condition} {true} {false}
> 
`If(如果)` 命令是自 TinTin Ⅲ 版本添加以来最强大的命令之一。

它的工作原理类似于其他语言中的 `if` 语句，并且基于 `C` 处理其条件语句。

当遇到 `#if` 命令时，如果条件语句求值结果为 `TRUE` (任何非零结果)，则执行命令。

`If` 语句仅在读取时求值，所以你必须将 `if` 语句套嵌另一个语句中 (最有可能是 `#action`)。

条件语句的求值与 `#math` 命令一样，但仅使用结果来确定是否执行命令而不存储。

要处理 `if` 语句为 `false` 的情况，可以通过 `#else` 命令。

```
示例：
#action {%0 gives you %1 gold coins.} {
  #if {%1 > 5000} {
    thank %0;
  };
};
--如果有人给你 5000 个金币，感谢他们。

示例：
#alias {k} {
  #if {"%0" == ""} {
    kill $target;
  };
  #else {
    kill %0;
  };
};
```

注：使用 `#else`、`#elseif` 时，前面的 `;` 不能省略。

条件语句使用 `c` 风格的数学或正则表达式。

字符串必须用引号 `" "` 包围。

当使用 `==` 或 `!=` 比较字符串时，左边是原始字符串，右边是正则表达式。

当使用 `<`  `>` 或 `<=`  `>=` 时，会执行基本的字符串比较。

有关更多信息，请参见 [Mathexp](#mathematics) 和 [Regexp](#regex) 上的帮助文件。

```
来自 man@pkuxkx 的疑惑：

为什么 "#if {$a==好的}" 不行，
因为字符串必须用引号包围。
示例：
#if {"$a"=="好的"}
```

另可参见: [Case](#case)，[Default](#default)，[Else](#else)，[Elseif](#elseif)，[Switch](#switch)，[Regex](#regex)，[While](#while)。

# Ignore

> 语法: #ignore {listname} {on|off}

`#Ignore(忽略)` 命令将打开或关闭列表。

如果没有参数，将显示当前设置，以及您可以忽略的列表名称。

```
示例: 
#ignore actions off
--暂时忽略所有触发器，触发器将不再被触发。
```

并非每个列表都可以忽略。

忽略时，以下列表类型的行为没有变化: `classes`，`commands`，`configurations`，`paths`，`pathdirs`。

另可参见: [Class](#class)，[Debug](#debug)，[Info](#info)，[Kill](#kill)，[Message](#message)。

# Info

> 语法: #info {listname} {LIST|ON|OFF|SAVE}

如果没有参数信息，则显示每个 tintin 列表的设置。

可用的列表有：

* ACTIONS      
* ALIASES      
* BUTTONS      
* CLASSES      
* COMMANDS     
* CONFIGS      
* DELAYS       
* EVENTS       
* FUNCTIONS    
* GAGS         
* HIGHLIGHTS   
* MACROS       
* PATHS        
* PATHDIRS     
* PROMPTS      
* SUBSTITUTES  
* TABS         
* TICKERS      
* VARIABLES    

通过提供列表的名称和列表选项，将显示所有与该列表关联的触发器/变量。

使用 `SAVE` 选项时，这些数据将写入 `$info` 变量。

可用的 `#info` 参数还有：

参数      | 行为
:---     | :---
arguments| 将显示匹配的触发参数。
big5toutf| 将显示 big5 到 utf8 的转换表。
cpu      | 将显示 tt 的 cpu 使用信息。
environ  | 将显示环境变量。
input    | 将显示输入行信息。
matches  | 将显示匹配的命令参数。
mccp     | 将显示数据压缩信息
memory   | 将显示有关内存堆栈的信息。
stack    | 将显示低级调试堆栈。
session  | 将显示会话的信息。
sessions | 将显示所有会话的信息。
system   | 将显示一些系统信息。
tokenizer| 将显示有关脚本堆栈的信息。
unicode  | 将显示有关给定字符的信息。

另可参见: [Class](#class)，[Debug](#debug)，[Ignore](#ignore)，[Kill](#kill)，[Message](#message)。

# Keypad

当 TinTin++ 启动时，它会向终端发送 `\e=` 以启用终端的应用小键盘模式。  

使用 `#showme {\e>}` 可以禁用该模式。

```
三种小键盘方案：

**Configuration A**
+-----+-----+-----+-----+
|Num  |/    |*    |-    |
+-----+-----+-----+-----+
|7    |8    |9    |     |
+-----+-----+-----+     |
|4    |5    |6    |+    |
+-----+-----+-----+-----+
|1    |2    |3    |     |
+-----+-----+-----+     |
|0          |.    |Enter|
+-----+-----+-----+-----+

**Configuration B**
+-----+-----+-----+-----+
|Num  |/    |*    |-    |
+-----+-----+-----+-----+
|Home |Up   |PgUp |     |
+-----+-----+-----+     |
|Left |Centr|Right|+    |
+-----+-----+-----+-----+
|End  |Down |PgDn |     |
+-----+-----+-----+     |
|Ins        |Del  |Enter|
+-----+-----+-----+-----+

**Configuration C**
+-----+-----+-----+-----+
|Num  |nkp/ |nkp* |nkp- |
+-----+-----+-----+-----+
|nkp7 |nkp8 |nkp9 |     |
+-----+-----+-----+     |
|nkp4 |nkp5 |nkp6 |nkp+ |
+-----+-----+-----+-----+
|nkp1 |nkp2 |nkp3 |     |
+-----+-----+-----+     |
|nkp0       |nkp. |nkpEn|
+-----+-----+-----+-----+
```

禁用小键盘模式后：配置 A (`numlock on`)，配置 B (`numlock off`)。  
启用小键盘模式后：配置 C。

## 支持小键盘模式的终端

Linux Console, PuTTY, Eterm, aterm。

## 不支持小键盘模式的终端

RXVT on Cygwin, Windows Console, Gnome Terminal, Konsole。

## 特殊终端

RXVT 需要关闭 numlock 才能启用配置 C。

Xterm 可能需要在 `ctrl-leftclick` 菜单中禁用 `Alt/NumLock` 修饰符`(num-lock)`。

或编辑 `~/.Xresources` 并添加 `XTerm*VT100.numLock:false`。

macOS 终端要求在终端-> 窗口设置-> 仿真中启用 `strict vt100 keypad behavior`。

另可参见: [Alias](#alias)，[Cursor](#cursor)，[History](#history)， [Macro](#macro)，[Speedwalk](#speedwalk)，[Tab](#tab)。

# Kill

> 语法: #kill {list} {pattern}

如果没有参数，`#kill` 命令将清除所有列表。

不退出 tintin 重新加载命令文件时很有用。

```
示例：
#nop 重载配置;
#alias {reload} {
    #kill;
    #read main.tt;
};
```

使用一个参数，可以清除特定列表。

```
示例: #kill alias
```

使用两个参数，所选列表中的所有匹配触发将被移除。

```
示例: #kill alias %*test*
```

另可参见: [Class](#class)，[Debug](#debug)，[Ignore](#ignore)，[Info](#info)，[Message](#message)。

# Line

> 语法: #line {option} {argument}

`#Line(行)` 命令提供各种基于行的操作。  

## 更改参数的子命令

**#line strip {argument}**

该参数是在删除了所有 VT100 和 ANSI 颜色代码后执行的。

**#line substitute {options} {argument}**

使用提供的替换执行参数。

有效的选项有:

* arguments(参数)  
--替换所有参数  
* braces(大括号)  
--替换所有大括号  
* variables(变量)  
--替换所有变量  
* vunctions(功能)  
--替换所有功能  
* colors(颜色)  
--替换所有 TinTin 颜色代码  
* escapes(转义)  
--替代所有转义字符  
* secure(安全)  
--避开所有大括号、变量、函数和命令分隔符  

## 更改行的执行方式的子命令

**#line background \<argument\>**

防止新会话激活。

**#line capture \<variable\> \<argument\>**

参数被执行并输出存储在变量中。

**#line convert \<argument\>**

参数使用转义的元字符执行。

**#line debug \<argument\>**

参数在调试模式下执行。

**#line local {argument}**

参数执行所有新的和间接创建的是局部变量。

**#line msdp \<argument\>**

从第一个左花括号开始把 tintin 数据结构转换成 msdp 的 telnet 序列，tintin table 会转换成 msdp table，分号分隔的值则会被转换成 msdp 数组。

**#line multishot \<number\> \<argument\>**

参数在 multishot 模式下执行，所有创建的触发器只会触发给定的次数。

**#line oneshot \<argument\>**

参数在 oneshot 模式下执行，所有创建的触发器只触发一次。

**#line logmode \<option\> \<argument\>**

参数使用提供的 logmode 执行，可用模式有: html、plain、raw。

**#line {log} {\<filename>} {[text]}**

`#Line log` 将给定的文本记录到给定的文件名中。  

如果没有给出文本参数，则显示的下一行将被记录到给定的文件中。  

如果文本参数中使用了任何 TinTin++ 颜色代码，它们将被翻译为 ANSI 颜色代码。

根据 `#config {LOG MODE}` 设置，日志记录格式将是 HTML、RAW、PLAIN。

**#line {logverbatim} {\<filename>} {[text]}**

工作方式与 `#line log` 一样，只是文本参数中的颜色代码、变量和函数不会被替换。

**#line {gag}**

当被调用时，显示的下一行将被消除。

当触发器在显示其触发的行之前触发时，使用 `#line gag` 将导致触发行不显示。

**#line {ignore} {argument}**

参数在没有检查任何触发器的情况下执行。

如果你想在不触发任何触发器的情况下使用 `#showme` 来避免循环触发，这很有用。

**#line {quiet} {argument}**

在静默大多数系统消息的情况下执行参数。

**#line verbatim \<argument\>**

参数逐字执行，禁止变量和函数替换。

**#line verbose {argument}**

参数在大多数系统消息启用的情况下执行。

当执行 `#line log` 并以 html 格式记录时，使用 `"\c< \c> \c& \c"` 来转义 `< > & "`。

```
示例:
#var ignore_list {{Bubba}{1}{Pamela}{1}};

#act {%1 tells you '%2'}
{
	#if {&ignore_list[%1]}
	{
		#line gag
	}
	{
		#line logverbatim tells.log
	}
}

将所有 tells 记录到 tells.log 文件中，
除非发件人在忽略列表中，否则 tell 内容不会显示。
```

另可参见：[Class](#class)，[Config](#config)。

# List

> 语法：#list {variable} {option} {argument}

指令|描述
:-|:-
#list {var} {add} {item}|将 {item} 添加到列表中
#list {var} {clear}|清空给定列表
#list {var} {collapse} {separator}|将列表转换为变量
#list {var} {create} {item}|使用 {item} 创建列表
#list {var} {delete} {index} {amount}|删除位于 {index} 的项目,{amount} 是可选的。
#list {var} {explode}{separator}|将变量转换为列表
#list {var} {indexate}|索引排序列表
#list {var} {insert} {index} {string}|在给定索引处插入 {string}
#list {var} {filter} {keep} {remove}|保留/删除正则表达式进行过滤
#list {var} {find} {regex} {variable}|返回找到的索引
#list {var} {get} {index} {variable}|将 {item} 复制到 {variable}
#list {var} {numerate}|将表转换为列表
#list {var} {order} {string}|按数字顺序插入 {item}
#list {var} {shuffle}|重新排序列表
#list {var} {set} {index} {string}|更改 {index} 处的项目
#list {var} {simplify} {variable}|将列表转换为简单列表
#list {var} {size} {variable}|将列表大小复制到 {variable}
#list {var} {sort} {string}|按字母顺序插入 {item}
#list {var} {tokenize} {string}|创建字符列表

关于列表的类型，请参见：[Lists](#lists)。

索引应该在 `+1` 和列表大小（&list）之间。

你也可以给出负值，在这种情况下 `-1` 等于列表中的最后一项，`-2` 为倒数第二个，依次类推。

插入项目（item）时，正索引将在给定索引处插入，而负索引将附加到列表尾部。

添加和创建选项也允许使用多个项目，最好是用分号分隔。

对于空列表或不存在的列表，返回长度为 0。

您可以使用 `$var[+1]` 直接访问列表变量中的元素,例如：`$var[+2]`，`$var[-1]` 等。

另可参见：[Break](#break)，[Continue](#continue)，[Foreach](#foreach)，[Loop](#loop)，[Parse](#parse)，[Repeat](#repeat)，[Return](#return)，[While](#while).

# Lists

TinTin 有几种不同类型的列表。

为了正确解释列表，在讨论更复杂的类型之前，首先解释最基本的变量类型。

- Basic variable（基本变量）  
--标准 key = value 变量。  
- Simple list（简单列表）  
--包含分号分隔字段的字符串。`{a;b;c}`。可以保存为变量。  
- Brace list（大括号列表）  
--用大括号分隔字段的字符串。`{a}{b}{c}`。由于表也使用大括号，大括号列表不能存储为变量，因此必须将它们存储为简单列表。  
- Table（表）  
--将此视为嵌套在另一个变量中的变量。或者作为包含在另一个变量中的变量。  
- List（列表）  
--使用整数作为索引的 `table(表)`。也称为 `数组(array)`。`#list` 是将 `table(表)` 用作数组的实用程序命令。  

## Simple Variables

```
示例:
#variable {simple} {Hello World!}  
#showme $simple
```

要查看 `"simple"` 变量是否存在，您可以使用 `&simple`，如果变量不存在，它将显示 0，如果变量存在，它将显示变量的索引。

如果你有多个变量，它们按字母顺序和数字排序。

虽然对于简单变量来说，这并不完全相关，但是第一个变量有索引 1，第二个变量索引 2，等等。

变量名必须以字母开头，并且只存在字母、数字和下划线。

如果您需要使用非标准变量名，可以使用大括号。

```
示例:
#variable {:)} {Happy!};
#showme ${:)}
```

可以使用它们的索引访问变量。

虽然主要对于对 `table(表)` 有用，但是简单变量也可以这样做。

第一个变量使用 `+1`，第二个变量使用 `+2`，等等。

最后一个变量使用 `-1`，倒数第二个变量使用 `-2`，等等。

```
示例: 
#showme 第一个变量是: ${+1}
```

## Removing Variables

要删除变量，请使用 `#unvariable` 或 `#unvar` (每个命令都可以缩写)。

可以使用 `#unvar {var 1} {var 2} {etc}` 同时删除多个变量。

变量对于每个会话都是唯一的，因此，如果您有多个会话，从一个会话中删除变量不会将其从其他会话中删除。

如果删除一个 `table variable(表变量)`，则该表中包含的所有变量也将被删除。

## Simple Lists

简单列表是包含分号分隔字段的字符串。

可以将命令作为简单列表输入，例如：`#showme {a};#showme {b}` 将作为两个命令执行。

有几个命令以简单列表作为输入，这些命令是：

* `#foreach`
* `#line substitute`
* `#path load`
* `#list create`
* `#highlight`

## Brace Lists

大括号列表是用大括号分隔字段的字符串。

大多数命令的参数都采用大括号列表，例如: `#session {x} {mud.com} {1234} {mud.tin}`。`#session` 命令接受四个参数，第四个参数 (命令文件) 是可选的。

将简单列表作为输入的命令也将接受括号列表，请记住，您必须将括号列表嵌入额外的括号集中，例如：`#path load {{n}{s}{w}}` 与 `#path load {n;s;w}` 相同。

不能将大括号列表存储为变量，因为 TinTin++ 会将它们与 `table(表)` 混淆。

您可以使用: `#list {bracelist} {create} {{a}{b}{c}}` 将大括号列表转换为表变量，这在内部看起来如下: `{{1}{a}{2}{b}{3}{c}}`。  

然后，您可以使用: `#list {bracelist} {simplify} {simplelist}` 将此表转换为简单列表，该列表将在 `$simplelist` 变量中存储。

在 TinTin++ 中，大括号很难被转义。使用 `\{` 或 `\}` 将不起作用。

这是由于几个因素造成的，主要是为了向后兼容性。

要转义大括号，您必须使用 `\x7B` 和 `\x7D` 等十六进制符号来定义大括号。

有关转义选项的列表，请参见 `#help escape`，帮助文件还将提醒您如何转义大括号。

## Tables

表是存储在变量中的 `key`/`value` 键值对。

创建和访问表有几种方法：

```
示例:
#variable {friendlist}{
   {dzp}{dzp@hotmail.com}         
   {xgg}{xgg@gmail.com}
}
```
这将创建一个包含两个条目的好友列表，键是好友的名称，值是好友的电子邮件地址。

您可以使用: `#showme {$friendlist[dzp]}` 看到 dzp 的电子邮件地址。

您也可以将此表定义如下:

```
示例:
#variable {friendlist[dzp]} {dzp@hotmail.com}
#variable {friendlist[xgg]} {xgg@gmail.com}
```

这将创建与以前使用的单行声明完全相同的表。

要查看表使用中的第一个键: `*friendlist[+1]`，  
请查看表使用中的第一个值: `$friendlist[+1]`，  
要查看表的大小：`&friendlist[]`，  
要打印所有朋友的括号列表： `*friendlist[%*]`，  
打印名称以字母 “a” 开头的所有朋友: `*freindlist[a%*]`，  
类似地，查看名称以字母 “b” 结尾的所有朋友：`&friendlist[%*b]`。

有关正则表达式选项的简要概述，请参见 `#help regexp`。

虽然 TinTin++ 支持 PCRE (与 perl 兼容的正则表达式)，但它将它们嵌入了自己的正则表达式语法中，该语法更简单、侵入性更小, 同时仍然允许那些需要 PCRE 的人充分发挥 PCRE 的力量。

```
示例: #unvariable {friendlist[xgg]}
```

这将从好友列表中删除 {xgg}。

要删除您将使用的整个friendlist: `#unvariable {friendlist}`。

```
示例: 
#variable {friendlist} {
   {dzp} {
      {email}{dzp@hotmail.com} {phone}{123456}
   }
}
```

集合的数量是没有限制的，只需增加更多的大括号。

要在此示例中查看 dzp 的电子邮件: `#showme {$friendlist[dzp][email]}`。

```
注意：
新版本中使用 $var[] 将会展开整个变量，
这可能导致 crash，
应使用 ${var[]}。

来自dzp@pkuxkx的高级数据结构示例:

#var {JMapData-rooms} {
{26} {{id}{26}{name}{客店}{links}{up;west}{area}{扬州}{center}{45}{map}{客店二楼〓北大街-----客店}{desc}{这是一家价钱低廉的客栈，生意非常兴隆。外地游客多选择这里落脚，你可以在这里打听到各地的风土人情。店小二里里外外忙得团团转，接待着南腔北调的客人。客店的主人从不露面，他究竟是谁，有各种各样的猜测。墙上挂着一个牌子(paizi)。}{cost}{0}{exits}{{142}{q;u}{27}{q;w}}{objs}{{天神随从}{tianshen suicong}{店小二}{xiao er}{彭波}{peng bo}{扬州的客店留言板}{26}{酉鸡}{zodiac animal}}}}

打印26号room的全部数据：
#showme ${JMapData-rooms[26]}
#精简代码长度
#var room {${JMapData-rooms[26]}}
打印26号room的第一层键：
#showme ${room[]}
打印26号room的id：
#showme ${room[id]}
打印26号room的出口：
#showme ${room[exits][]}
打印26号room的出口个数：
#showme &{room[exits][]}
打印26号room的第一个出口的键：
#showme *{room[exits][+1]}
打印26号room的最后一个出口的值：
#showme ${room[exits][-1]}

高级数据结构可大幅度简化代码。
```

## Lists

表按数值排序，数值异常的按字母顺序排序。

如果你想自己确定排序顺序，你可以使用 `#list` 命令来帮助你将表用作数组。

```
示例: 
#action {%1 chats %2} {#list chats add {%0}}
```

每次收到聊天时，它都会被添加到 “chats” 列表变量的末尾。  

如果你输入 `#variable chats`，这看起来像：  

```
#variable {chats}
{
  {1}{xgg chats Hi}
  {2}{dzp chats Hi xgg}
  {3}{xgg chats Bye}
  {4}{dzp chats xgg bye}
}
```

`#List` 命令是在表实现之前编写的，因此 `get`、`set`、`size` 选项是多余的。

## Parsing

有多种方法来解析列表和表。

* #loop

`#loop` 采用两个数字参数，递增或递减第一个数字，直到它与第二个数字匹配。

loop 计数器的值存储在提供的变量中。

* #foreach

`#foreach` 首先采用简单列表或大括号列表参数。

foreach 将遍历列表中的每个项目并将值存储提供的变量中。

* #while

`#while` 将对第一个参数执行 `if` 检查。

如果结果为 true，它将执行第二个参数中的命令。

然后它再次对第一个参数执行 `if` 检查。

它将继续重复，直到 if 检查返回 0 或循环被控制流命令中断。

特别注意要避免死循环。

* #\<number> 

将执行提供的参数 'number' 次。

示例：`#4 {#show beep! \a}`。

这里有一些例子：

```
示例：
#list friends create {bob;bubba;zorro}
--内部看起来像 {{1}{bob}{2}{bubba}{3}{zorro}}
```

列表可以通过各种方式进行解析：

```
示例：
#foreach {$friends[%*]} {name} {#show $name}

示例：
#foreach {*friends[%*]} {i} {#show $friends[$i]}

示例：
#loop {1} {&friends[]} {i} {#show $friends[+$i]}

示例：
#math i 1;
#while {&friends[+$i]} {
  #show $friends[+$i];
  #math i $i + 1;
}

示例：
#math i 1;
#&friends[] {#show $friends[+$i];#math i $i + 1}
```

以上五个示例中的每一个都执行相同的任务：打印好友列表中的三个名字。

如果你想更好地了解幕后发生的事情，  
执行脚本时，您可以使用 `#debug all on`，  
停止观察调试信息使用 `#debug all off`。

## List Tables

`List tables` 数组表也称为数据库，并且 `list` 命令有多个选项操纵它们。

为了使这些选项正常工作，所有表都需要具有相同的 `key`。

这是一个示例数组表：

```
#var {friendlist} {
   {1}{{name}{bob} {age}{54}}
   {2}{{name}{bubba} {age}{21}}
   {3}{{name}{pamela} {age}{36}}
}
```

要按年龄对列表表进行排序，您可以使用：

`#list friendlist indexate age`  
`#list friendlist order`  

要删除名称以 “b” 开头的所有人，您可以使用：

`#list friendlist indexate name`  
`#list friendlist filter {} {b%*}`  

筛选器选项仅支持正则表达式。

要为筛选器使用数学表达式，你可以向后循环遍历列表:

```
#loop &friendlist[] 1 index {
   #if {$friendlist[+$index][age] < 30} {
      #list friendlist delete $index
   }
}
```

要将项目添加到数组表中，有两个选项:

`#list friendlist add {{{name}{hobo} {age}{42}}}`  
`#list friendlist insert -1 {{name}{hobo} {age}{42}}`  

## Optimization

TinTin++ 表在 100 个项目下时速度非常快。

一旦表的长度超过 10000 个项目，插入和删除文件开头或中间的项目时可能会出现性能问题。

如果从文件中加载一个大型表，确保它被排序是很重要的，当使用 `#write` 保存一个表时，它会自动排序。

如果您注意到大型表的性能问题，创建 `hash table(哈希表)` 相对容易。

```
示例:
#alias {sethash}
{
	#format hash %H %1;
	#math hash1 $hash % 100;
	#math hash2 $hash / 100 % 100;
	#var hashtable[$hash1][$hash2][%1] %2
}

#function {gethash}
{
	#format hash %H %1;
	#math hash1 $hash % 100;
	#math hash2 $hash / 100 % 100;
	#return $hashtable[$hash1][$hash2][%1]
}

#alias {test}
{
	sethash bli hey;
	sethash bla hi;
	sethash blo hello;
	#showme The value of bla is: @gethash{bla}
}
```

以上脚本将快速存储和检索超过 100 万个项目。遍历哈希表也相对容易。

```
示例:
#alias {showhash}
{
	#foreach {*hashtable[%*]} {hash1}
	{
		#foreach {*hashtable[$hash1][%*]} {hash2}
		{
			#echo {%-20s = %s} {hashtable[$hash1][$hash2]} {$hashtable[$hash1][$hash2]}
		}
	}
}
```

## The list command

> 语法: #list {\<variable>} {\<option>} {\<arguments>}

TinTin++ 中的列表是具有数字索引的表 (又名关联数组)。

`#List` 命令通过在删除或插入项目时自动重新编号项目来更容易模拟数组行为。

当 list 命令需要索引时，应该提供 1 到列表大小之间的值。

也可以给出负值，在这种情况下，-1 等于列表中的最后一项，-2 等于倒数第二项等。

您可以使用索引直接显示列表中的项目，例如: `$var[+1] 、$var[+2] 、$var[-1]` 等。

要使用 [foreach](#foreach) 命令循环遍历列表中的所有项目，请使用 `$<list>[%*]`。

***

**#list {\<list>} {add} {\<argument1>} {\<argument2>} {...}**

#List add 将为提供的每个参数向给定列表添加一个项目。

**#list {\<list>} {clear}**

#List clear 将清空给定的列表变量。

该命令相当于: `#variable {<variable>} {}`。

**#list {\<list>} {create} {\<argument1>} {\<argument2>} {...}**

#List create 将清除给定的列表，并为提供的每个参数添加一个项目。

**#list {\<list>} {delete} {\<index>} {[number]**

#List delete 将删除给定索引处的项目。  

Number 参数是要删除的项数，如果省略，索引第 1 项将被删除。

**#list {\<list>} {find} {\<argument>} {\<variable>}**

#List find 允许搜索与提供的参数匹配的项目。  

如果找不到匹配项，则将目标变量设置为 0，否则将变量设置为包含匹配项的索引。

**#list {\<list>} {get} {\<indext>} {\<variable>}**

#List get 将在提供的索引中检索列表的项目。  

如果索引不存在，则目标变量设置为 0，否则目标变量设置为包含找到的索引的值。

或者，您可以使用 `$list [<index>]` 使用表的接口检索值。

**#list {\<list>} {insert} {\<index>} {\<argument>}**

#List insert 将在给定索引处插入项目。

如果索引是正数，则在给定索引处创建项目。

如果索引是负数，则在下一个索引处创建项目。

因此，使用 -1 将在列表的末尾附加一个新项，使用 +1 将在列表的开头添加一个新项。

**#list {\<list>} {set} {\<index>} {\<argument>}**

#List set 将提供的索引的值更改为给定的参数。  

或者，您可以使用：`#variable {<list>[<index>]} {<argument>}` 使用表的接口更改值。

**#list {\<list>} {simplify} {\<variable>}**

#List simplify 将表保存为用分号分隔到的简单列表。

**#list {\<list>} {size} {\<variable>}**

#List size 将检索列表中的项目数，并将其存储在提供的目标变量中。  

或者，您可以使用: `&list[]` 使用表的接口检索列表中的项目数。

**#list {\<list>} {sort} {\<argument>}**

#List sort 将按字母顺序插入提供的参数。

**#list {\<list>} {tokenize} {\<argument>}**

#List tokenize 使用列表标记将把给定的参数变成一个字符列表。 

`{haha}` 将成为 `{{1}{h}{2}{a}{3}{h}{4}{a}}`。

如果你想执行低级文本处理，这很有用。

***

另可参见: [Break](#break)，[Continue](#continue)，[Foreach](#foreach)，[Loop](#loop)，[Parse](#parse)，[Repeat](#repeat)， [Return](#return)，[While](#while)。

# Local

> 语法: #local {variable name} {text to fill variable}

`#Local` 命令设置局部变量。

与常规变量不同，局部变量只会在创建它的事件持续时间内留在内存中。

它们的访问方式与常规变量相同。

将信息存储到变量的命令将使用局部变量 (如果存在)。

避免在函数中将结果变量设置为局部变量，因为这可能会导致特殊的行为。

```
示例: 
#alias {swap} {
   #local x %0;
   #replace x {e} {u};
   #showme $x
}
```

注：您可以使用 `#unlocal` 命令删除局部变量。

另可参见: [Format](#format)，[Function](#function)，[Math](#math)， [Replace](#replace)，[Script](#script)，[Variable](#variable)。

# Log

> 语法：#log {option} {argument}

`#Log` 命令将回滚缓冲区中接收到的所有数据记录到指定的文件中。

使用 `#config` 命令，您可以指定用于日志文件的数据类型。

这些类型是: 

* raw  
--原始 (也打印转义代码)

* plain  
--普通 (带转义代码)

* html  
--超文本标记语言 (将转义颜色代码转换为 html 颜色代码)。

***

可用的选项有：

* #log append \<filename>

开始记录到给定文件，如果该文件已经存在，它将不会被覆盖，数据将被附加到末尾。

* #log move \<filename_1> \<filename_2>

将 filename_1 重命名为 filename_2。这可以是任何文件，不需要是日志文件。

* #log overwrite \<filename>

开始记录到给定文件，如果该文件已经存在，它将被覆盖。

* #log off

停止记录。

* #log remove \<filename>

删除文件。这可以是任何文件，不需要是日志文件。

* #log timestamp \<format>

设置时，时间戳将被添加到记录到文件的每一行。

该格式将使用 `strftime` 格式化为日期，参见 `#help time` 中所述。

***

```
示例: 
#log o mylog.txt
```

这将把所有的 mud 输出写入 mylog.txt。

如果您使用 `#showme` 命令，它也将被记录到文件中，除非是您在启用 `#split` 的情况下显示在滚动区域之外的内容。

您可以使用 `#line log` 命令将单个行记录到日志文件中。

```
示例: 
#act {~%1 chats '%2'} {
   #line log comms.txt %1 chats '%2'
}
```

注: 您可以使用 `#buffer write` 命令将整个回滚缓冲区保存到文件中。

```
示例: 
#alias savebuffer {
    #format date %t %F;
    #buffer write log_$date.txt
}
```

注：您还可以使用 `#history write` 将命令历史记录保存到文件中。

另可参见: [Read](#read)，[Scan](#scan)，[Textin](#textin)，[Time](#time)，[Write](#write)。

# Loop

> 语法: #loop {\<start>} {\<finish>} {\<variable>} {commands}

`Loop(循环)` 命令的工作方式类似于 C 语言的简化 `for` 循环， \<start> 和 \<finish> 参数应该是数字。

该命令将递增或递减 1 (取决于数字顺序)，直到达到第 2 个数字。

循环计数器的值将存储在变量中，可以在命令部分使用。

```
示例：
#loop 1 3 cnt {say $cnt}
--这等于：say 1;say 2;say 3

示例：
#loop 1 3 loop {get all $loop.corpse}
--这等于：get all 1.corpse;get all 2.corpse;get all 3.corpse

示例：
#loop 3 1 cnt {drop $cnt\.key}
--这等于：drop 3.key;drop 2.key;drop 1.key
```

另可参见: [Break](#beak)，[Continue](#continue)，[Foreach](#foreach)， [List](#list)，[Parse](#parse)，[Repeat](#repeat)，[Return](#return)，[While](#while)。

# Macro

> 语法: #macro {key sequence} {commands}

`#Macro(宏)` 命令使 tintin 可以响应按键。

按下按键时发送给终端的按键码可能会因操作系统和终端而异。

要了解发送详情，您可以启用 `CONVERT META` 配置选项。  

您也可以通过组合键 `ctrl-v` 为下一次按键动作启用 `CONVERT META`。

如果您只希望一个按键码被触发，在输入行开头为按键码添加前缀 `^`。

```
示例: 
#macro {(press ctrl-v)(press F1)} {#show \e[2J;#buffer lock}
--当您按下 F1 时，清除屏幕并锁定窗口，可以用作老板键。

示例：
#macro {\eOM} {#cursor enter}
--使小键盘的回车键在键盘模式下作为回车键工作。

示例：
#macro {^nn} {north}
--在空行上按两次 n 执行 north。
```

默认情况下，tintin 模拟 bash 输入编辑。  

可以使用与 `#cursor` 命令相结合的宏来改变 TinTin 的输入编辑行为。

注：并非所有终端都能正确初始化小键盘按键码，如果是这种情况，您仍然可以使用小键盘，但是需要替换方向键为 ctrl-b、f、p、n。

注: 您可以使用 `#unmacro` 命令删除宏。

另可参见: [Alias](#alias)，[Cursor](#cursor)，[History](#history)， [Keypad](#keypad)，[Speedwalk](#speedwalk)，[Tab](#tab)。

# Map

> 语法: #map {option} {argument}

`#Map(地图)` 是自动绘图特性的主要命令。

TinTin++ 有一个功能强大的自动地图绘制器，它使用类似于 Diku MUDs 的房间系统，这意味着奇怪的地图布局和奇怪的出口配置不是一个重大问题。

mapper 提供了改进的可视化地图工具。

有关基本路径跟踪，请参见路径命令：[Path](#path)。

使用不带参数的 `#map`，查看可用选项及其简单介绍。

选项      | 介绍
:---      | :---
AT        | 在给定区域执行命令
CENTER    | 设置地图显示中心
COLOR     | 设置给定区域颜色
CREATE    | 创建初始化的地图
DEBUG     | 调试信息
DELETE    | 删除给定方向的房间
DESTROY   | 摧毁区域或地图
DIG       | 在给定方向创建新房间
ENTRANCE  | 改变给定出口的入口
EXIT      | 改变给定出口
EXITFLAG  | 改变给定出的的标签
EXPLORE   | 保存探测到的路径到 #path
FIND      | 保存寻找到到位路径到 #path
FLAG      | 改变地图标志
GET       | 获取各种房间相关值
GLOBAL    | 设置全局出口
GOTO      | 移动到给定房间
INFO      | 显示地图和房间信息
INSERT    | 在给定方向插入一个房间
JUMP      | 移动到给定坐标
LANDMARK  | 设置全局房间地标
LEAVE     | 离开地图
LEGEND    | 操纵地图图例
LINK      | 在给定方向连接房间
LIST      | 列出匹配房间
MAP       | 显示地图
MOVE      | 移动到给定方向
NAME      |（过时）改为使用 SET ROOMNAME
OFFSET    | 设置 vt 地图的偏移量
READ      | 读取地图文件
RESIZE    | 调整地图房间号范围的大小
RETURN    | 返回最后一个已知房间
ROOMFLAG  | 改变房间标志
RUN       | 保存找到的路径到 #path 并执行
SET       | 设置多种房间相关的值
SYNC      | 读取地图文件且不覆写
TERRAIN   | 创建地形类型
TRAVEL    | 保存探寻到的路径到 #path 并执行
UNDO      | 取消最后一个地图指令
UNINSERT  | 在给定方向取消插入房间
UNLANDMARK| 移除地标
UNLINK    | 移除给定出口
UNTERRAIN | 移除地形类型
UPDATE    | 标记 vt map 为自动更新
VNUM      | 改变房间号为给定数字
WRITE     | 保存地图到给定文件

***

以下是关于 `#map` 选项的相关介绍：

**#map at \<exit|vnum> \<command>**

在给定出口或房间号执行命令。

如果位置不存在，则不执行命令。

如果你想遍历所有房间号并访问所有房间来执行某种操作，这将非常有用。

**#map center \<x> \<y> \<z>**

设置地图查看器的显示中心，默认值为0。

**#map color \<field> [value]**

> 语法: #MAP COLOR {AVOID|BACKGROUND|EXIT|FOG|HIDE|INVIS|PATH|ROOM|USER} {COLOR CODE}

为给定地图字段设置颜色。

使用 `#map color reset` 将颜色恢复为默认值。

要将背景设置为蓝色，您可以使用 `#map color background <884>`。  

要将房间颜色设置为暗红色，您可以使用 `#map color room <218>`。

**#map create {size}**

此命令创建初始地图和第一个房间。

默认情况下，地图大小为 50000。

可以使用 `#map resize` 命令随时更改地图大小。  

如果你玩的是使用 MSDP 或 GMCP 提供房间号码的 MUDs，你必须将它增加到报告的最高房间号码。

增加地图的大小不会降低性能。

**#map destroy {area|world} \<name>**

删除地图或给定区域。

**#map delete {exit|vnum}**

删除给定出口或房间号的房间。

**#map dig {exit|vnum} {new|vnum}**

为给定出口名称创建出口。

如果没有给出有效的出口名称或未找到现有房间则创建新房间。

对于传送点（驿站）的连接以及其他可替代的两点间移动方式很有用。

如果提供了 “new” 参数，则忽略所有出口房间并创建新房间。

如果房间号是第二个参数，将创建一个出口，引导到给定的房间号。如果房间号不存在，则创建新房间。

* `#map dig {vnum}`   
--将使用给定的房间号创建一个新房间，除非已经存在具有该房间号的房间。

* `#map dig {exit}`   
--将在给定方向创建一个新的出口。如果一个房间占据了这个空间，出口将与那个房间相连，否则将创建一个新的房间。

* `#map dig {exit} {new}`   
--将在给定方向创建一个新的出口，将始终创建一个新的房间。

* `#map dig {exit} {vnum}`   
--将在给定方向创建一个新的出口，该出口指向具有给定房间号的房间。如果这个房间不存在，将创建一个带有这个房间号的新房间。

**#map entrance \<exit> [option] [arg]**

设置给定出口的入口数据。您必须指定一个有效的双向出口。

**#map exit \<exit> \<option> <arg>**

设置出口数据。

如果你想自动打开关闭的门，使用: `#map exit {e} {command} {open door;e}`。  

当使用 `#map run` 时，它将执行 {open door;e} 而不是 {e}。

如果你有一个不寻常的出口，你可以给它一个方向。

例如：`#map exit {enter portal} direction {s}`。

也接受类似于 `#pathdir` 提供的数字方向。

这允许 mapper 显示位于门户之外的房间，尽管你必须注意没有通往南方的实际出口。

查看可用选项列表使用：`#map exit <exit>`。

保存出口数据使用：`#map exit <eixt> save`。

* `#map exit {exit} {NAME} {argument}`  
--将设置移动命令。如果名称设置为 “and”，并且键入 “and”，这将使您跟随出口。实际执行的移动命令可以用 `#map exit {exit} {command}` 设置。名称和命令通常是相同的。

* `#map exit {exit} {COMMAND} {argument}`  
--将设置发送到服务器的移动命令。例如 {open door;n}

* `#map exit {exit} {DIRECTION} {argument}`  
--将设置出口的方向。这可以是与 `#PATHDIR` 命令使用的数字参数相同的数字参数。

* `#map exit {exit} {FLAG} {argument}`  
--将设置标志。这一定是个数字，使用 `#map exitflag` 设置出口标志更容易。

* `#map exit {exit} {GET} {variable}`  
--将出口数据保存到给定变量中。

* `#map exit {exit} {SET} {argument}`  
--将出口数据设置为给定的参数。参数可以是表。

* `#map exit {exit} {SAVE} {variable}`  
--将出口相关信息 (commands/direction/flags/name/vnum) 等保存到给定变量中。

* `#map exit {exit} {VNUM} {argument}`  
--将出口房间号设置为给定的参数。这是出口通向的房间的索引号。

**#map exitflag {exit} {AVOID|BLOCK|HIDE|INVIS} {ON|OFF}**

设置出口标志。

有关更多信息，请参阅 `#map roomflag`。

* `#map exitflag {exit}`  
--将显示出口标志的状态。

* `#map exitflag {exit} {HIDE}`  
--启用后，此出口之外的房间将不会显示在地图上。用于隐藏重叠区域。

* `#map exitflag {exit} {AVOID}`  
--启用时，在搜索到给定描述的路径时，mapper 不会使用出口。

**#map explore {exit}**

mapper 将探索给定的出口，直到到达交叉路口或死胡同。

路径存储在 `#path` 中，随后可以与 `#walk` 一起使用。

对于走过漫长的路径特别有用。

**#map find \<name> \<exits> \<desc> \<area> \<note> \<terrain> \<flag>**

搜索给定的房间名称。

如果找到，将计算从当前位置到目的地的最短路径。

路径存储在 `#path` 中，并可以与各种 `#path` 命令一起使用。

如果 `#map flag nofollow` 被设置，将存储出口命令而不是出口名称。

如果提供了 \<exit>，则必须匹配所有出口。

如果提供了 \<roomdesc>，\<roomarea>，\<roomnote>，\<roomterrain>，\<roomflag> ，将找到与这些参数更加匹配的房间。

这些搜索选项也可用于： `at`，`delete`，`goto`，`link`，`list`，`run`。

`delete` 和 `dig` 命令只接受房间号。

该位置可以存在多个参数，其中第一个参数应该是房间名称或房间号。

如果你想进一步缩小范围，你可以使用以下键/值对:
```
第二、三个大括号必须匹配
#map find {location} {roomname} {argument}
--房间名必须匹配参数

#map find {location} {roomexits} {argument} 
--房间出口必须匹配参数，例如：{n;e;u}.

#map find {location} {roomdesc} {argument}
--房间描述必须匹配参数

#map find {location} {roomarea} {argument}
--房间区域必须匹配参数

#map find {location} {roomnote} {argument}
--房间注释必须匹配参数

#map find {location} {roomterrain} {argument}
--房间地形必须匹配参数

#map find {location} {roomflag} {number}
--房间标志必须匹配参数
```

例如，可以使用几个键/值对来找到房间：

```
示例: 
#map find {A small clearing} {roomexits} {n;e;s;w} {roomarea} {The holy grove} {roomterrain} {Forest}
```

**#map flag asciigraphics**

默认情况下启用此标志，并绘制一张宽敞的地图，显示 NE SE SW NW 出口、单向出口、上下出口和房间符号。

禁用时，它将默认为地图图例，该图例使用紧凑的 UTF-8 框绘图字符。

**#map flag asciivnums**

显示房间号。用于编辑或调试地图。

**#map flag mudfont**

这是一种不太受支持的实验显示模式。它需要特殊的字体和 `#map legend` 的正确配置。

**#map flag nofollow**

启用时，当您输入移动命令时，地图不会尝试跟随。

使用 `#PATHDIR` 定义移动命令。对于 MSDP 和 GMCP 地图自动绘制脚本很有用。

当您使用 `#map find` 时，nofollow 模式将存储出口命令而不是出口名称到路径。

**#map flag static**

启用时，当进入未绘制的方向时，不再自动创建新房间。

当你完成地图绘制并经常意外撞到墙壁时，这很有用。

**#map flag vtgraphics**

启用某些终端上的 vt line 绘制。

**#map flag vtmap**

启用时，地图会显示在顶部分割区中。

这需要一个支持 VT100 的终端，并使用 `#split` 分割屏幕。

创建一个 16 行高的屏幕顶部分割区域: `#split 16 1`。

**#map get {option} {variable} [vnum]**

此命令允许您将地图信息存储到变量中。

如果没有提供房间号使用当前房间。使用 “all” 选项会将所有值存储到表变量。

```
可用选项有: 
WORLDFLAGS,
WORLDSIZE, 
ROOMVNUM, 
ROOMAREA, 
ROOMCOLOR, 
ROOMDATA, 
ROOMDESC, 
ROOMEXITS, 
ROOMFLAGS, 
ROOMNAME, 
ROOMNOTE, 
ROOMSYMBOL, 
ROOMTERRAIN, 
ROOMWEIGHT.
```

**#map get roomexits \<variable>**

将所有房间出口存储为变量。

**#map global \<room vnum>**

为包含全局出口房间的设置房间号，例如名为 “recall” 的出口。

一些 mud 中输入 "recall" 会返回初始地点/复活点/传送点。

```
示例:
#map goto {984} dig
#map global 984
#map link recall 26
#map link gohome 116
```
这将创建 984 号房间，然后将 984 号房间设置为全局房间，然后将出口链接到 26 号房间。

每当您输入 “recall”，您的地图位置将更改为 26 号房间。

如果您输入 "gohome" 则更改到 116 号房间。

因此，基本上 984 号房间将成为一个特别的房间。它不应该是 mud 的实际房间。

房间可以包含多个出口，以防万一可以设置多个类似 recall 的命令。

**#map goto \<room vnum> [dig]**

转到给定的房间号，dig 参数如果不存在，将创建一个新房间。

创建地图时，您不会自动进入地图。

默认情况下，创建了房间号 (vnum) 1，因此您可以使用 `#map goto 1` 转到它。

一旦您进入地图，当您四处走动时，新房间会使用 `#pathdir` 命令定义移动命令。

默认情况下，n, ne, e, se, s, sw, w, nw, u, d 被定义。

**#map goto \<name> \<exits> \<desc> \<area> \<note> \<terrain>**

转到给定的房间名称，如果你提供出口则这些必须匹配。

**#map info [save]**

提供有关您所在的地图和房间的信息。

如果给定 `save` 参数，地图数据被保存到 `info[map]` 变量中。

**#map insert \<direction> [roomflag]**

这将在提供的方向插入一个新房间。最有用的是插入空房间。

如果你想同时设置多个房间标志，你必须用半冒号将它们分开。

```
示例: 
#map insert {e} {void;hide}
```

`insert` 命令对于添加名为 void 的间隔房间很有用。

房间经常重叠，通过增加房间空间，你可以延伸出出口，也可以使用空房间来对齐房间。

例如: `#map insert north void`。

一旦创建了空房间，你就不能进入空房间，所以你必须在相邻的房间中使用 `#map info` 来找到房间号, 然后使用 `#map goto {vnum}` 访问。

也可以隐藏整个区域，直到你输入它，为了做到这一点，你可以设置隐藏标志。

例如：`#map insert north {void;hide}`。

**#map jump {x} {y} {z}**

跳转到给定坐标。

此命令类似于 `#map goto`，只是您提供了相对于当前所在房间的坐标。

**#map landmark \<name> \<vnum> [description] [size]**

创建别名以定位所提供的房间号。描述是可选的，应该简短。

大小决定从多少个房间的距离到地标可见。

**#map leave**

让你离开地图。地图仍然存在，但是您的移动命令将不再被跟踪。

当进入迷宫时很有用。

你可以使用 `#map return` 返回最后的已知房间。

如果使用 `#map read`，返回点将设置为保存地图时所在的房间。


**#map legend**

> #map legend \<legend> [symbols|reset]  
> #map legend \<legend> \<index> [symbol]

有几个图例和子图例可用于绘制适合个人喜好和字符集的地图。

使用 `#map legend all` 查看当前定义的图例。

使用 `#map legend <legend> <reset>` 重置默认图例。

使用 `#map legend <legend> <character list>` 创建自定义图例。

自定义图例会自动保存，使用 `#map read` 和 `#map write` 加载。

图例包含对用于显示地图的绘图字符的引用。

紧凑显示模式使用前 16 个字符。

它只显示值 N E S W 出口值为 n=1 e=2 s=4 w=8。

0 指数是指没有出口的房间。

第一个指数是指有一个出口通向北方的房间。

第二个指数是一个房间，有一个出口通向东方。

第三个指数是一个出口朝北向东的房间，等等。

位于索引 1+4+8=13 的房间，出口通向北、南、西。

索引应该是 ASCII 字符的 32 到 254 之间的数字，或者 UTF-8 字符的 hex 序列。

如果 `#config` 字符集设置为 UTF-8，TinTin++ 将自动用 UTF-8 框绘图字符初始化新创建的地图。

仅部分使用了指数 16 至 31。

在紧凑模式下，索引 16 用于当前位置。

在 `MUDFONT` 模式下，当前位置使用索引 17 和 18。

指数 32 95 用于 `MUDFONT` 显示模式。

指数 32 到 63 显示 NW W SW S 出口值为 n=1 nw=2 w=4 sw=8 s=16。

指数 64 到 95 显示 NE E SE S 出口值为 n=1 ne=2 e=4 se=8 s=16。

默认情况下，MUDFONT 字符映射到从 U+E000 开始的第一个 Unicode 专用区域。

在 Windows 上，这将在下面下载的两个 EUDC (最终用户定义字符) 文件一起使用。

[EUDC.EUF](https://tintin.sourceforge.io/download/EUDC.EUF) 和 [EUDC.TTE](https://tintin.sourceforge.io/download/EUDC.TTE)

必须使用 7zip 或类似的实用程序将这些文件复制到 `C:/Windows/Fonts` 目录中。  

您不能使用 Windows 自带的复制例程复制文件，因为它会尝试安装字体，这不是您想要的。

要修改 EUDC 文件，必须启动私有字符编辑器程序。默认情况下应该安装它。

进行更改后，您已经使用文件-> 字体链接-> 所有字体的链接来完成更改。

EUDC 文件是概念功能。

**#map link {direction} \<room name> {both}**

此命令将在指向给定位置的给定方向创建单向出口。

如果方向是有效的路径目录，您可以提供 {both} 作为第三个参数来创建双向出口。

**#map list \<name> \<exits> \<desc> \<area> \<note> \<terrain>**

这个命令列出了所有匹配的房间和它们的距离。

您可以使用`#map list {<location>} {variable} {<variablename>}` 将列表存储在变量中。

支持以下搜索关键词：

关键词 | 行为
:---   | :---
{distance}   \<arg>| 将列出给定距离内的房间。
{roomarea}   \<arg>| 将列出匹配区域名称的房间。
{roomdesc}   \<arg>| 将列出与描述匹配的房间。
{roomexits}  \<arg>| 将列出具有相同房间出口的房间。使用 * 作为出口以忽略没有路径值的出口。
{roomflag}   \<arg>| 将列出带有匹配房间标志的房间。
{roomid}     \<arg>| 将列出具有相同id名的房间。
{roomname}   \<arg>| 将列出与房间名称匹配的房间。
{roomnote}   \<arg>| 将列出房间与匹配的房间说明。
{roomterrain}\<arg>| 将列出与房间地形相匹配的房间。
{variable}   \<arg>| 将输出保存到给定的变量。

**#map map \<rows> \<cols> \<append|overwrite|list|variable> \<name>**

显示给定高度和宽度的地图图形。

所有参数都是可选的。

如果 {rows} 或 {cols} 设置为 {} 或 {0}，它们将使用滚动窗口大小作为默认值。

如果 {rows} 或 {cols} 为负数，则该数字为从滚动窗口大小中减去。

`#map map {<x>x<y>}` 向屏幕显示具有给定空间大小的地图。

`#map map {<x>x<y>} {filename}` 将 map 显示写入给定的文件名。

`#map map {<x>x<y>} {filename} {a}` 将 map 显示写入文件，附加到现有文件中。

`#map map {<x>x<y>} {variable} {v}` 将地图显示保存到给定变量。

要查看地图，您可以使用 `#map`。

然而，必须不断键入 `#map` 是令人讨厌的。

可以使用 `#split` 显示 vt100 地图。  

执行:   

```
#split 16 1   
#map flag vtmap 
```
第一个命令将顶部分割线设置为 16，底部分割线设置为 1。

如果您想要更小或更大的地图显示，可以使用 10 、 13 、 19 、 22 等, 尽管对于默认显示设置，更改需要是 3 的倍数。

如果要在屏幕的其他位置显示地图，使用如下内容：

```
#split 0 1 0 -80
#map offset 1 81 -4 -1
```

这将在屏幕右侧显示地图，如果屏幕足够宽。

如果你不需要显示对角线出口，更喜欢更紧凑的外观，你可以使用 `#map flag AsciiGraphics off`。

这将启用使用 UTF-8 框绘图字符的标准显示，结果可能会因使用的字体而异。

如果您的终端支持UTF-8，您还可以使用 `#Map flag unicode` 试一试。

如果你想在不同的终端中显示地图，打开一个新的终端，启动 tt++，然后输入:   
`#port init mapper 4051 `

在你的 MUDs 终端中，输入:   
`#ses mapper localhost 4051`

这将地图程序会话连接到您在另一个终端窗口中初始化的端口。  

接下来，在 MUD 会话中定义以下事件:   

```
#EVENT {MAP ENTER ROOM} {
  #map map 80x24 mapvar v;
  #mapper #line sub {secure;var} #send {$mapvar}
}
```

**#map map \<rows> \<cols> draw \<square>**

显示给定高度和宽度的地图图形。

空间参数由 4 个数字组成，构成空间的左上角和右下角。

如果使用 {append|overwrite}，地图将写入指定的文件名必须作为第四个参数给出。

如果使用 {list|variable}，则地图将保存到指定的变量名称。


**#map move \<direction>**

这与实际移动命令相同，更新地图上的位置并创建新房间。

当你跟踪某人并希望地图跟随时，这很有用。

当然，您必须使用 `#map move` 创建触发器才能正常工作。

**#map offset \<row> \<col> \<row> \<col>**

将 vtmap 的偏移量定义为空间。没有参数它默认为整个顶部分割区域。

**#map read {filename}**

将加载给定的文件名。

您可以使用 `#map goto` 进入地图，也可以使用 `#map return`，它会将您带回保存地图的房间。

**#map resize {size}**

调整地图大小，设置最大房间数。

**#map return**

离开地图或加载地图后，返回到最后一个已知的房间。

**#map roomflag \<flags> \<get|on|off>**

* #map roomflag avoid  
设置后，`#map find` 将避免穿过该房间的路线。避免关闭的门、陷阱和攻击性怪物很有用。

* #map roomflag block  
设置后，自动地图将阻止移动进入或通过房间。对死亡陷阱有用。
 
* #map roomflag hide  
设置后，`#map` 将不会在这个房间之外显示地图。当地图绘制重叠的区域或不一致构建的区域时，除非使用空房间，否则您也需要此标志来防止自动链接。

* #map roomflag invis  
设置后，房间将使用 INVIS 颜色着色。

* #map roomflag leave  
当你带着这个标志进入房间时，你会自动离开地图。当设置在带有随机出口的迷宫入口处时很有用。

* #map roomflag noglobal  
这标志着一个房间不允许全局返回，就像阻碍返回的 norecall 房间。

* #map roomflag void  
当设置房间时，房间变成了一个间隔房间，可以用来连接重叠的区域。一个空房间应该只有两个出口。当你进入一个空房间时，你会被移动到间隔房间，直到你进入一个非空房间。要访问空房间，必须使用 `#map goto` 或 `#map jump`。

* #map roomflag static  
设置时，当四处走动时，房间将不再自动链接。用于绘制迷宫。

**#map run \<room name> {delay}**

找到到给定位置的最短路径，并执行到达那里的移动命令。

{delay} 是可选的，且必须使用大括号。

您可以以浮点精度提供秒为单位的延迟，例如: `#map run {dark alley} {0.5}`

除了房间名称还可以提供出口列表，以便更精确匹配。

**#map set {option} {value}**

为您当前的房间设置一个地图信息值。

```
可用选项有: 
ROOMVNUM, 
ROOMAREA, 
ROOMCOLOR, 
ROOMDATA, 
ROOMDESC, 
ROOMEXITS, 
ROOMFLAGS, 
ROOMNAME, 
ROOMNOTE, 
ROOMSYMBOL, 
ROOMTERRAIN, 
ROOMWEIGHT.
```

可以使用 `#map set roomname {name}` 设置房间名称。

您必须手动执行此操作，或者创建触发器手动设置房间名称。

设置房间名称后，您可以使用 `#map goto` 作为访问房间名称的命令。

如果有两个同名的房间，`#map goto` 会去附近的房间。

如果你总是想去同一个房间，你应该记住房间号码。

您可以通过提供额外的参数来进一步缩小匹配范围。

```
例如: 
#map goto {武庙} {n;w} {roomarea} {扬州}
```
您可以使用 `#map set roomweight {value}` 设置房间权重。

默认情况下，权重设置为 1.0，表示穿过房间的难度。

如果你有一个湖泊作为替代路线，并且穿越水房比普通房间慢 4 倍，那么你可以将湖房的权重设置为 4.0 。

如果湖宽 3 个房间，总权重是 12。如果绕着湖泊散步的权重小于 12 ，穿越湖泊权重大于 12 ，mapper 将沿着湖走一条路线。

```
来自一位不愿扬名大佬的注释:

tt 的 map 信息本身就记录了周边房间号，
还能设置权重，
通过权重很容易就能实现河两边分两次遍历，
不需要额外的代码。

一个 NPC 只给一个大概范围，
可能在河这边也可能在对岸，
没有权重控制，简单广度优先的话，
会来来回回的坐船。
渡口到对岸权重 999 即可。

权重用来计算 GPS 路径也很有用，
能做马车不坐船，能穿洞不坐车，
不同门派不同需求，
score 捕获了信息，自动修改权重即可。
```

可以使用 `#map set roomsymbol {value}` 设置房间符号。

符号应该是可以上色的一、二、三个字符。

例如，你可以用 “S” 标记商店，并根据商店的类型对 “S” 进行着色。

**#map sync \<filename>**

类似于 `#map read`，只是不会卸载当前地图或者覆盖。

**#map terrain \<name> \<symbol> [flag]**

设置地形符号和标志。

**#map terrain \<name> \<symbol> [DENSE|SPARSE|SCANT]**

确定符号密度，省略默认值。

**#map terrain \<name> \<symbol> [NARROW|WIDE|VAST]**

确定符号扩展范围，省略默认值。

**#map terrain \<name> \<symbol> [FADEIN|FADEOUT]**

确定符号扩散密度，省略默认值。

**#map terrain \<name> \<symbol> [DOUBLE]**

您使用两个字符作为符号。

**#map travel {exit} {delay}**

对于穿越长道路很有用。

该命令将沿着给定的出口移动，并将继续移动，直到到达死胡同或交叉路口。

延迟是可选的浮点数字，在每个移动命令之间添加延迟。

使用 `#path stop` 停止延迟移动。

**#map undo**

将撤消您最后一个移动行为。

如果这个命令创建了一个房间或链接，它将被删除。

如果这个命令涉及移动，它会将你移回上一个房间。

如果你走进一个不存在的方向，那就很有用了。

如果你想在地图上而不是在 MUDs 上四处移动，使用: `#map move {direction}`。

要手动删除房间，使用: `#map delete {direction}`。

您可以手动创建房间：`#map dig {direction}`。

**#map uninsert {exit}**

这个命令与 `#map insert` 完全相反。

它将删除出口通向的房间，并将出口连接到被删除房间之外的房间。

**#map unlandmark \<name>**

移除地标。

**#map unlink \<direction> [both]**

将移除出口，这不是双向的，所以你可以适当地显示无出口房间和迷宫。

如果您同时使用这两个参数，则将删除双向出口。

**#map unterrain \<name>**

移除地形。

**#map update [now]**

将 vtmap 设置为在接下来的 0.1 秒内更新，或者使用 `now` 立即更新。

**#map {vnum} {number}**

将房间号更改为给定的数字。

**#map {vnum} {low} {high}**

改变房间号。

如果提供了一个范围，则选择该范围内的第一个可用房间。

低和高是一个数字范围。

如果最低数量不可用，则在找到可用的房间号之前，房间号会递增。

如果最高号码不可用，命令将失败。

**#map {write} {filename} [force]**

将地图保存到给定的文件名。

建议偶尔创建备份，因为很容易混淆 `#map write` 和 `#write`。

如果要将地图保存到 .tin 为后缀的文件，您必须提供 {force} 参数。

**#help map**

`#help map` 为您提供关于可用地图选项的其他信息。

请记住输入部分命令可能会为您提供有用的语法建议或概述。

***

另可参见: [Path](#path)，[Pathdir](#pathdir)，[Speedwalk](#speedwalk)。

# Math

> 语法: #math {variable} {expression}

`#Math` 允许您执行数学计算，并将结果存储在给定变量中。

数学计算遵循类似 C 的优先级，如下所示，在列表的顶部具有最高优先级。

运算符 | 优先级 | 功能
:-   | :- | :-
!    |  0 | 逻辑非
~    |  0 | 按位非
d    |  1 | 整数随机骰子
\*   |  2 | 整数乘
\**  |  2 | 整数幂
/    |  2 | 整数除
//   |  2 | 整数开平方根or立方根
%    |  2 | 整数模
\+   |  3 | 整数加
\-   |  3 | 整数减
<<   |  4 | 左移位
\>>  |  4 | 右移位
..   |  4 | 整数范围
\>   |  5 | 逻辑大于
\>=  |  5 | 逻辑大于等于
<    |  5 | 逻辑小于
<=   |  5 | 逻辑小于等于
==   |  6 | 逻辑等值 (可以使用正则表达式)
===  |  6 | 逻辑等值 (不可以使用正则表达式)
!=   |  6 | 逻辑非等值 (可以使用正则表达式)
!==  |  6 | 逻辑非等值 (不可以使用正则表达式)
 &   |  7 | 按位与
 ^   |  8 | 按位亦或
 \|  |  9 | 按位或
&&   | 10 | 逻辑与
^^   | 11 | 逻辑亦或
\|\| | 12 | 逻辑或
?    | 13 | 逻辑三元 if (未完成的代码)
:    | 14 | 逻辑三元 else

True 是任何非零数字，False 是零。

括号 `()` 有最高优先级，因此始终首先计算 `()` 内部。

字符串必须用 `" "` 包围且包含在 `{}` 中，并使用正则表达式 `==` 和 `!=`，在 `<=` 和 `>=` 的情况下，比较字母顺序。

`#if` 和 `#switch` 命令使用 `#math`。

有多个命令接受整数输入也允许数学运算。

浮点精度支持使用小数点 `.` 。

```
示例：
#math {heals} {$mana / 40}
--将变量 #mana 的值除以 40 并存储结果到 $heals。

示例：
#action {^You receive %0 experience} {updatexp %0}
#alias updatexp {#math {xpneed} {$xpneed - %0}
--变量 $xpnewd 存储了升到下一级所需的经验值，每次击杀后修改还需要多少经验值。

示例：
#action {%0 tells %1} {
  #if {{%0} == {Bubba} && $afk} {
    reply I'm away, my friend.
  }
}
--当你暂时离开时，它只会回复你的朋友。
```

```
示例: 
#math sumvar {(1 + 1) * 10}
--这个基本操作将在 sumvar 中存储结果 (20)。
```

如果计算包含浮点数字，结果将以与精度最高的参数相同的精度存储为浮点数字。

```
示例: 
#math var {1.0 / 4}
--将结果 (即 0.2) 存储在 var 中。使用 1.00/4 将存储 0.25。
```

```
示例: 
#math var 2d6
--d 代表骰子，2d6 相当于投掷两个 6 面骰子。  
```

如果你需要 1 到 100 之间的随机数，你可以使用 1d100。

如果你需要 0 到 9 之间的随机数，你可以使用 1d10-1。

```
来自xgg@pkuxkx的注释：

一个骰子只能从 1 开始，
所以当范围不是从 1 开始时，需要对数值进行差值运算。

示例：
#function {rnd} {#math {result} {1 d (%2 - %1 + 1) + %1 - 1}};
#showme 从100-200范围抽取随机数: @rnd{100;200}
```

注: 其他运算符的行为或多或少与预期的相同。

另可参见: [Cat](#cat)，[Format](#format)，[Function](#function)，[Local](#local)，[Mathematics](#mathematics)，[Replace](#replace)，[Script](#script)，[Variable](#variable)。

# Mathematics

数学表达式用于数学计算和 boolean if 检查。

TinTin++ 支持全套 C 操作和一些额外的操作。

以下是用于数值运算的运算符的优先级列表。

运算符 | 优先级 | 功能
:-   | :- | :-
!    |  0 | 逻辑非
~    |  0 | 按位非
d    |  1 | 整数随机骰子
\*   |  2 | 整数乘
\**  |  2 | 整数幂
/    |  2 | 整数除
//   |  2 | 整数开平方根or立方根
%    |  2 | 整数模
\+   |  3 | 整数加
\-   |  3 | 整数减
<<   |  4 | 左移位
\>>  |  4 | 右移位
..   |  4 | 整数范围
\>   |  5 | 逻辑大于
\>=  |  5 | 逻辑大于等于
<    |  5 | 逻辑小于
<=   |  5 | 逻辑小于等于
==   |  6 | 逻辑等值 (可以使用正则表达式)
===  |  6 | 逻辑等值 (不可以使用正则表达式)
!=   |  6 | 逻辑非等值 (可以使用正则表达式)
!==  |  6 | 逻辑非等值 (不可以使用正则表达式)
 &   |  7 | 按位与
 ^   |  8 | 按位亦或
 \|  |  9 | 按位或
&&   | 10 | 逻辑与
^^   | 11 | 逻辑亦或
\|\| | 12 | 逻辑或
?    | 13 | 逻辑三元 if (未完成的代码)
:    | 14 | 逻辑三元 else

可以使用括号忽略运算符优先级。

例如：`(1+1)*2` 等于 4，而 `1+1*2` 等于 3。

这些运算符中的一些也可以用于字符串。

字符串必须用双引号 `" "` 括起来。

运算符	| 优先级	| 功能
:-    | :- | :-
\>    | 4 | 字母顺序大于
\>=   | 4 | 字母顺序大于等于
\<	   | 4 | 字母顺序小于
\<=	  | 4 | 字母顺序小于等于
\==   | 5 | 字母顺序等值(可以使用正则表达式)
\!=   | 5	| 字母顺序非等值(可以使用正则表达式)
\===  | 5 | 字母顺序等值
\!==  | 5	| 字母顺序非等值

运算符 `>` `>=` `<` `<=` 执行基本的字符串比较。

`==` `!=` 运算符执行正则表达式，左边的参数是字符串，右边的参数是正则表达式。

例如：`"bla"=="%*a"` 将评估为 1 (true)。

另可参见: [Math](#math)，[PCRE](#pcre)，[Regexp](#regexp)。

# Message

> 语法: #message {listname} {on|off}

没有参数将显示所有您可以切换消息状态的列表。

您可以使用 `ON` 或 `OFF` 作为参数更改消息状态。

例如: `#message variable off`

当执行的变量被创建或删除时不再创建消息。

只有在正确使用 `#variable`、`#unvariable` 命令或以详细模式执行命令时，才会显示消息。

`#config {verbose} {on}` 将导致在使用 `#read` 读取脚本文件时显示消息。

`#line {verbose} {argument}` 将导致参数在详细模式下执行，显示所有消息。

`#line {quiet} {argument}` 将导致在静默模式下执行参数，不会显示任何消息。

另可参见: [Class](#class)，[Debug](#debug)，[Ignore](#ignore)，[Info](#info)，[Kill](#kill)。

# Metric System

名称         | 符号 | 因数
:-           | :-  | :-
百万 million | M | 1000000
千   kilo    | K | 1000
毫   milli   | m | 0.001
微   macro   | u | 0.000001

另可参见：[Echo](#echo)，[Format](#format)，[Math](#math)。

# Mouse

要启用 xterm 鼠标跟踪，请使用 `#CONFIG MOUSE ON`。

要在鼠标事件发生时查看它们，请使用 `#CONFIG MOUSE INFO`。

这些信息可用于 `#event` 创建鼠标事件和 `#button` 创建带有按钮命令的按钮。

可以使用 `#draw` 在屏幕上绘制可视按钮和弹出窗口。

输入框允许创建用于输入处理的命名事件，可以使用 `#screen inputregion` 更改和重命名。

可以使用 MSLP 协议创建链接，该协议将生成链接单击时的特定事件。

另可参见：[Button](#button)，[Draw](#draw)，[Event](#event)，[MSLP](#mslp)。

# MSDP

MSDP（Mud 服务器数据协议） 是 `#port` 功能的一部分。

请参阅 `#help event` 附加文档，所有 MSDP 事件都可以作为常规事件。

可以访问[「MSDP 协议」](https://tintin.sourceforge.io/protocols/msdp) 查询可用的 MSDP 事件。

MUD 服务器通常希望向 MUD 客户端发送不一定需要显示的附加数据，以及需要一种方法来识别支持带外数据的客户端。

MSDP 协议旨在通过为 MUD 服务器提供透明且直接的带外协议来解决这些问题，以将变量及其值发送给 MUD 客户端（针对有问题的 MUD 可以是通用的和特定的）。使用通用变量将允许通用客户端接口脚本适用于所有 MSDP MUDs。

MSDP 实现为 Telnet 选项：[RFC854](https://tintin.mudhalla.net/rfc/rfc854)、[RFC855](https://tintin.mudhalla.net/rfc/rfc855)。

服务器和客户端像协商任何其他 telnet 选项一样协商 MSDP 的使用。

一旦就选项的使用达成一致，就使用选项子协商在服务器和客户端之间交换信息。

**服务端命令**

* IAC WILL MSDP  
--表明服务器想开启 MSDP。

* IAC WONT MSDP  
--表明服务器想关闭 MSDP。

**客户端命令**

* IAC DO MSDP  
--表明客户端接受 MSDP 子协商。

* IAC DONT MSDP  
--表明客户端拒绝 MSDP 子协商。

**握手协议**

当客户端连接到启用 MSDP 的服务器时，服务器应发送 `IAC WILL MSDP`。

客户端应该用 `IAC DO MSDP` 或 `IAC DONT MSDP` 来回应。

一旦服务器收到 `IAC DO MSDP`，客户端和服务器都可以发送 MSDP 子协商。

客户端不应发起协商，如果发生这种情况，服务器应遵守状态更改。

为了避免触发循环，服务器不应响应来自客户端的协商，除非它正确实现了 [RFC1143](https://tintin.mudhalla.net/rfc/rfc1143.html) 中的 Q 方法。

更多信息请查看 [「MSDP 协议」](https://tintin.sourceforge.io/protocols/msdp)。

另可参见：[Event](#event)，[Port](#port)，[GMCP](#gmcp)。

# MSLP

MSLP（Mud 服务器链接协议）需要启用 `#config mouse on`，并创建适当的链接事件。

最简单的链接可以通过使用 `\e[4m` 和 `\e[24m` 标签。

```
示例：
#substitute {\b{n|e|s|w|u|d}\b} {\e[4m%1\e[24m}
```

这将显示 “n，e，w” 为带有下划线的 “<ins>n</ins>，<ins>e</ins>，<ins>w</ins>”。

当点击时，将触发 `PRESSED LINK MOUSE BUTTON ONE` 事件，其中 %4 将保存链接命令，%6 将保链接名称，在简单链接的情况下将为空。

```
示例：
#event {PRESSED LINK MOUSE BUTTON ONE} {#send {%4}}
```

请记住，如果你改变 `PRESS` 为 `DOUBLE-CLICKED` ，仅当在点击时文本没有滚动才有效。

如果要创建复杂链接，请使用 OSC 代码。

```
示例：
#sub {\bsmurf\b} {\e]68;1;;say I hate smurfs!\a\e[4m%0\e[24m}
```

如果您具有以上示例的链接事件，%4 参数将包含 'say I hate smurfs!'。

```
示例：
#sub {\bgoblin\b} {\e]68;1;SEND;kill goblin\a\e[4m%0\e[24m}
```

注意以上示例 `;;` 已被替换为 `;SEND;`，这将命名链接。这还将生成命名事件。

```
示例：
#event {PRESSED LINK SEND MOUSE BUTTON ONE} {#send {%4}}
```

通过命名链接，你可以更好地组织事务来替代通过同一事件干所有事。

请记住，服务器同样允许使用 `\e]68;1;\a`，这使各种安全措施到位。

要创建安全链接，这些链接在服务器发送时会被过滤掉，您需要使用 `#\e]68;2;\a`，然后它们会触发安全链接事件。

```
示例：
#sub {%* tells %*} {\e]68;2;EXEC;#cursor set tell %1 \a\e[4m%0\e[24m}
#event {PRESSED SECURE LINK EXEC MOUSE BUTTON ONE} {%4}
--这将使您在单击 tells 时开始回复。
```

```
来自 xgg@pkuxkx 的示例：
鼠标事件点击带有下划线的方向自动发送移动指令

#nop 开启鼠标模式;
#config mouse on;

#nop 开启鼠标点击事件，点击即发送带有下划线标签的内容;
#event {PRESSED LINK MOUSE BUTTON ONE} {#send {%4}};

#nop 匹配方向替换为带有下划线标签的可点击链接;
#action  {^    这里{唯一|明显}的{出口|方向}{有|是}%*。$} {
  #local {dir_all} {%3};
  #replace {dir_all} {{\w+}} {<139>\e[4m&1\e[24m<099>};
  #line ignore #show {    这里%1的%2%3$dir_all。};
  #line gag;
}
```

请参阅 `#help event` 附加文档，所有 MSLP 事件都可以作为常规事件使用。

可以访问[「MSLP 协议」](https://tintin.mudhalla.net/protocols/mslp) 查询可用的 MSLP 事件。

另可参见：[Event](#event)，[Port](#port)。

# Nop

> 语法: #nop {whatever}

`#Nop` 是 “no operation” 的简称，有助于在脚本中留下注释。

任何 `#nop` 后面到分号 `;` 之前的文本都会被忽略。

不应将 `{}` 符号放到注释内容里面，除非是一对闭合的大括号。

注：通过使用大括号，您可以在脚本文件中注释掉多行代码。每一行仍需 `;` 结尾。

```
示例: 
#act {&} {#nop}
```

一些 MUDs 允许你使用 “&” 来分离命令，同时仍然允许玩家在 “say” 或 “tell” 中使用它。

这将允许一些狡猾的玩家在没有保护的情况下滥用你的触发器。

因此，如果消息包含 “&” 字符，则不会触发易受攻击的操作，因为一次只允许触发 1 个操作。

要注释掉整个触发，尤其是包含大量内容的可以使用 `/* test */`。

注：`/* */` 只能写在行首位置，且不能插入 `{}` 中。

```
示例：

#nop 这是我的脚本文件开头;

#nop {
  bli;
  bla;
  blo;
};

/*
脚本文件 written by xgg
2022.9.11 
*/
```

如果想忽略事件触发消息，你可以在命令部分使用 `#nop` 或 `#0`。

```
示例：
#event {GAG SESSION ACTIVATED} {#0};
```

另可参见：[Read](#read)。

# Parse

> 语法: #parse {string} {variable} {commands}

`#Parse` 命令就像一个简化的循环。

Parse 将遍历访问给定字符串的每个字符，该字符存储在给定变量中，并可以在命令部分使用。

```
示例: 
#parse {hello} {character} {say $character!}
--这等于：say h!;say e!;say l!;say l!;say o!
```

虽然很少使用，但是 parse 仍然相当实用，比如使用 `.` 快速行走。

```
示例:
#alias {.%0}
{
        #var cnt {};

        #parse {%0} {char}
        {
                #if {"$char" >= "0" && "$char" <= "9"}
                {
                        #var cnt $cnt$char
                };
                #elseif {"$cnt" == ""}
                {                     
                        $char
                };
                #else
                {    
                        #loop $cnt 1 cnt
                        {
                                $char
                        };
                        #var cnt {}
                }
        }
}
```

还可以作出一些有趣的功能，比如给每个字符随机上色。

```
来自 xgg@pkuxkx 的示例：

#function bc0 {
   #local color_r {};
   #parse %1 char {
     #math a {1d9-1};
     #math b {1d9};
     #math c {1d9};
     #local ccolor {<$a$b$c>};
     #local color_r {$color_r$ccolor$char};
   };
   #return $color_r;
};
#echo {@bc0{「大慈大悲入凡尘，普度苍生怜世人」}};

--上述示例还用到了循环变量拼接，这也是相当实用的技巧。
```

另可参见: [Break](#break)，[Continue](#continue)，[Foreach](#foreach)，[List](#list)，[Loop](#loop)，[Repeat](#repeat)，[Return](#return)，[While](#while)。

# Path

> 语法: #path {option} {argument}

`#Path` 命令是一种可以快速简单地记录您的移动的方法，并创建一个命令列表，以便从一个位置移动到另一个位置并返回。

要使用更高级的地图程序，请查看 [「Map」](#map) 命令。

使用没有参数的 `#path` ，将列出可用选项及其介绍：

选项    | 说明
:---    | :---
create  | 将会清除路径并开始记录新路径。
delete  | 移除最后的移动。
describe| 描述路径信息和当前位置。
destroy | 将会清除路径并开停止记录路径。
get     | 将得到长度或位置。
goto    | 转到开始、结束或给定位置索引。
insert  | 添加给定参数到路径。
load    | 加载指定变量作为新路径。
map     | 显示地图和当前位置。
move    | 向前或向后移动位置。如果给出了一个数字,通过给定的步数改变位置。
run     | 执行或延迟执行当前路径 (以秒为单位) 。
save    | 保存路径到变量，必须指定方向 'forward' 或 'backward'。
start   | 开始记录路径。
stop    | 停止记录路径，行走时则停止行走。
undo    | 撤销上一步。
swap    | 切换向前和向后路径。
unzip   | 加载给定的快速行走作为新路径。
walk    | 向前或向后走一步。
zip     | 把路径变成快速行走。

***

以下是部分选项的详细说明：

**#path {new|create}**

此命令启动路径跟踪模式。

如果输入移动命令 (用 `#pathdir` 列出)，它将被添加到路径中。

**#path {end}**

使用 `#path new` 启动路径跟踪后，您可以使用 `#path end` 停止。

这不会删除创建的路径，尽管再次键入 `#path new` 会。

**#path {map}**

此命令用列表显示到目前为止创建的路径和当前位置。

**#path {ins} {forward command} {backward command}**

有时当你移动时需要打开门，使用这个选项可以将命令插入你正在创建的路径中。

当创建从 A 到 B 的路径时，也会自动创建从 B 到 A 的向后路径。

因此，第二个参数是为向后路径插入的命令。

```
示例: 
#path ins {unlock n;open n} {unlock s;open s}
```

没有简单的方法在路径的开头插入。

您可以使用 `#path save`，更新变量，然后使用 `#path load`。

或者使用 `#path swap`，`#path insert`，然后再次使用 `#path swap`。

**#path {del}**

移除路径中的最后一个移动，这在撞墙时十分有用。

```
示例: 
#act {这个方向没有出路} {#path del}
```

**#path {save} {forward|backward} {variable}**

此命令将创建的路径保存到提供的变量中，您必须指定是向前还是向后保存路径。

你可以用 f 和 b。

如果使用: `#path save f A2B`，您可以使用: `$A2B` 执行保存的路径。

```
示例: 
#path new;n;n;n;e;e;e;
#path save f A2B;
$A2B
```

**#path {load} {variable}**

此命令将加载任何给定的变量作为路径，并且不需要与移动相关。

**#path {run} {delay}**

要使此命令工作，您必须创建或加载了路径。

执行时，路径中的所有命令都会被删除并立即执行，延迟参数是可选的，每个命令执行将延迟给定的时间。

例如: `#path run 0.5`。

**#path {start}**

开始记录路径。

**#path {stop}**

停止记录路径，行走时则停止行走，路径没有被删除，可以继续行走。

**#path {walk} {forward|backward}**

要使此命令工作，您必须创建或加载了路径。

执行时，路径队列中的下一个命令将被删除并执行。

如果到达路径的末尾，将触发到达路径末尾的特定事件。

```
示例: 
#tick {slowwalk} {#walk f} {0.5};
#event {END OF PATH} {#untick slowwalk}
```

***

另可参见: [Map](#map)，[Pathdir](#pathdir)。

# Pathdir

> 语法: #pathdir {dir} {reversed dir} {coord}

默认情况下，TinTin 设置了最常用的移动命令，这意味着你通常不必费心路径方向。

`#path` 和 `#map` 命令使用路径方向。

第一个参数是方向，第二个参数是相反的方向。

north 的反方向是 south 等。

第三个参数是空间坐标。

一般来说，每个基数方向都应该有一个唯一的值，该值是 2 的幂。

例如：'n' 1，'e' 2，'s' 4，'w' '8'，'u' 16，'d' 32。

复合方向除外，复合方向的值应为每个组件方向的值之和。

例如，如果 “n” 值是 1，“w” 是 8，那么你 “nw” 的值是 9 (1+8)。

`#map` 功能工作需要此值。

示例: `#pathdir {eu} {wd} {18}`。

在上面的例子中，18 是 2(e) 和 16(u)的总和。

当你键入 `eu` 时，一旦设置，地图程序就知道你在向东上方移动。

请记住，您还必须设置反方向 {wd} {eu} {40} 路径才能正常工作。

注意: 您可以使用 `#unpathdir` 命令删除路径方向。

如果你的 MUDs 没有使用 ne se sw nw (默认设置)，你可以使用 `#unpath ne se sw nw` 来移除它们。


```
来自 xgg@pkuxkx 的说明：
自定义命令只能是 1-63 之间的值。
比如：enter，out。

#PATHDIR         {n}  {s}  {1}
#PATHDIR         {e}  {w}  {2}
#PATHDIR         {s}  {n}  {4}
#PATHDIR         {w}  {e}  {8}
#PATHDIR         {u}  {d}  {16}
#PATHDIR         {d}  {u}  {32}
#PATHDIR         {ne} {sw} {3}
#PATHDIR         {se} {nw} {6}
#PATHDIR         {nw} {se} {9}
#PATHDIR         {sw} {ne} {12}
#PATHDIR         {nu} {sd} {17}
#PATHDIR         {eu} {wd} {18}
#PATHDIR         {su} {nd} {20}
#PATHDIR         {wu} {ed} {24}
#PATHDIR         {nd} {su} {33}
#PATHDIR         {ed} {wu} {34}
#PATHDIR         {sd} {nu} {36}
#PATHDIR         {wd} {eu} {40}
#nop 自定义命令范围 1-63;
#PATHDIR         {out} {enter} {61}
#PATHDIR         {enter} {out} {62}
```

另可参见: [Map](#map)，[Path](#path)。

# PCRE

Regular Expressions、Regex 或 Regexp 是定义搜索模式的字符序列。

自从 1980 年以后，就有了编写正则表达式的不同语法，其中使用最广泛的是 POSIX 语法和类似但更高级的 Perl 标准。

TinTin++ 支持被称为 PCRE (Perl 兼容正则表达式) 的 Perl 标准。

正则表达式是 TinTin++ 的一个组成部分，但是请记住，TinTin 不允许直接使用正则表达式, 相反，它使用更简单的中间语法，当需要时，它仍然允许更复杂的表达式。

以下命令利用正则表达式: action, alias, elseif, gag, grep, highlight, if, kill, local, math, prompt, regexp, replace, substitute, switch, variable, while。

其他几个命令以次要的方式使用正则表达式。

幸运的是，基础知识非常容易学习。

**TinTin++ Regular Expression**

正则表达式有以下支持。

```
^ 匹配行首。
$ 匹配行尾。
\ 转义字符。

%1-%99 匹配任意文本并保存在相应索引中。
%0 匹配所有文本。
{ } 嵌入与 perl 兼容的正则表达式，存储匹配项。
%!{ } 嵌入与 perl 兼容的正则表达式，不存储匹配项。
[ ] . + | ( ) ? * 等符号除非在大括号内使用，否则被视为普通文本。
请记住，除非使用 %!{}，否则 {} 会自动替换为 ()。
```

正则  | 描述                          | POSIX
:---  |:---                           |:---
\%d   | 匹配零到任意量的数字          | ([0-9]*?)
\%D   | 匹配零到任意数量的非数字      | ([^0-9]*?)
\%i   | 匹配不区分大小写              | (?i)
\%I   | 匹配区分大小写(默认)          | (?-i)
\%s   | 匹配零到任意数量的空格        |  ([\r\n\t ]*?)
\%S   | 匹配零到任意数量的非空格      |  ([^\r\n\t ]*?)
\%w   |  匹配零到任意数量的单词字符   | ([A-Za-z0-9_]*?)
\%W   |  匹配零到任意数量的非单词字符 | ([^A-Za-z0-9_]*?)
\%?   | 匹配 0 个或 1 个字符          | (.??)
\%.   | 匹配一个字符                  | (.)
\%+   | 匹配一个到与任意数量的字符    | (.+?)
\%\*  | 匹配零到任意数量的字符        | (.*?)

要匹配 4 个空格：`%+4s`。

要匹配 2-5 个数字：`%+2..5d`。

要匹配 0 到任意个字母：`%+0..w`。

**Variables**

如果在触发器中使用 %1 执行匹配，则匹配到的字符串存储在 %1 变量中，该变量可用于触发器主体部分。

```
示例：
#act {%1 says 'Tickle me'} {tickle %1}
```

如果使用 %2，则匹配存储在 %2 中，以此类推。

如果使用未编号的匹配，如 %* 或  %S，则在最后使用的索引处递增 1。

```
示例：
#act {%3 says '%*'} {
  #if {"%4" == "Tickle me"} {
     tickle %3
  }
}
```

最大变量索引为 99。

如果以 %* 在开头触发，匹配项将存储在 %1 中。

在触发器主体部分永远不应使用 %0，%0 包含匹配的字符串的所有部分。

要防止存储匹配项，请使用 %!* 、 %!w 等。

**Perl Compatible Regular Expressions**

您可以使用大括号 `{}` 嵌入 PCRE (Perl 兼容正则表达式)，除非使用 `%!{}`，否则这些大括号将被 `()` 替换。

或者，您可以使用 `|` 字符在 PCRE 中分离替代方案。

```
示例: 
#act {%* scratches {his|her|its} butt.} {
  mutter Someone should wash %2 hands..
}

示例：
#action  {^    这里{唯一|明显}的{出口|方向}{有|是}%*。$} {
  #local {dir_all} {%4};
  #replace {dir_all} {{\w+}} {<139>\e[4m&1\e[24m<099>};
  #line ignore #show {    这里%1的%2%3$dir_all。};
  #line gag;
}
--上述示例可以为方向加上可点击的下划线标签和颜色，详情查看 #help mslp。
```

**Brackets**

您可以使用方括号 `[]` 对 PCRE 中的替代方案和范围进行分组。

```
示例: 
#act {%* says 'Who is number {[1-9]}} {
   say $number[%2] is number %2
}
```

只有当有人提供 1 到 9 之间的数字时，该示例才会触发。

任何其他字符都不会导致触发器触发。

```
示例: 
#act {%* says 'Set password to {[^0-9]*}$} {
 say The password must contain at least one number, not for security reasons, but just to annoy you.
} {4}
```

当 `^` 字符在方括号内使用时，它会创建反向搜索，除了 0 到 9 之间的数字之外，[^0-9] 会匹配每个字符。

**Quantification**

匹配后放置的量化限定词指定允许匹配发生的频率。

```
? 重复零次或一次。
* 重复零次或多次。
+ 重复一次或多次。

{n} 准确的重复次数，并且必须是一个数字。
{n,} 至少重复 n 次，并且必须是一个数字。
{n,o} 重复 n 到 o 次，n 和 o 必须是一个数字。
```
```
示例: 
#act {%* says 'Who is number {[1-9][0-9]{0,2}} {
   Say $number[%2] is number %2
}
```

仅当有人提供 1 到 999 之间的数字时，示例才会触发。

**Paranthesis**

TinTin 正则表达式自动添加圆括号 `()`，例如 `%*` 在 PCRE 中转换为 `(.*？)`，除非在行首或行尾找到 `%*`，这种情况下会转换为 `(.*)`。

PCRE 中的圆括号导致执行优先级发生类似于数学表达式的变化，但圆括号也会存储匹配项到变量中。

当嵌套多组圆括号时，每个嵌套都按照外观顺序分配自己的数值变量。

```
示例：
#act {%* chats '{Mu(ha)+}'} {chat %2ha!}
--如果有人说 Muha，你会说 Muhaha，如果有人说 Muhaha，你会说 Muhahaha。
```

**Lazy vs Greedy**

默认的正则表达式匹配是贪婪的，这意味着 `{.*}` 将捕获尽可能多的文本。

通过附加 `?` 在正则表达式后面，它变得懒惰，意味着 `{.*？}` 将尽可能少地捕捉文本。

```
示例: 
#regex {bli bla blo} {^{.*} {.*}$} {#showme Arg1=(&1) Arg2=(&2)}
--这将显示：Arg1=(bli bla) Arg2=(blo)。

示例: 
#regex {bli bla blo} {^{.*?} {.*?}$} {#showme Arg1=(&1) Arg2=(&2)}
--这将显示：Arg1=(bli) Arg2=(bla blo)。
```

**Escape Codes**

PCRE 支持以下转义代码。


PCRE |描述                       |POSIX
:-   |:-                         |:-
\\A  | 匹配行首                  | ^ 
\\b  | 匹配单词边界              | (^|\r|\n|\t| |$) 
\\B  | 匹配非单词边界            | [^\r\n\t ] 
\\c  | 插入控制字符              | \c 
\\d  | 匹配数字                  | [0-9] 
\\D  | 匹配非数字                | [^0-9] 
\\e  | 插入转义字符              | \e 
\\f  | 插入表单输入字符          | \f 
\\n  | 插入表单换行字符          | \n 
\\r  | 插入回车字符              | \r 
\\s  | 匹配空格                  | [\r\n\t ] 
\\S  | 匹配非空格                | [^\r\n\t ] 
\\t  | 插入 tab 字符             | \t 
\\w  | 匹配字母、数字和下划线    | [A-Za-z0-9_] 
\\w+ | 匹配字母                  | [A-Za-z]
\\W  | 匹配非字母、数字和下划线  | [^A-Za-z0-9_] 
\\x  | 插入十六进制字符          | \x 
\\Z  | 匹配字符串结束            | $
\\Q  | 开始引用                  | /
\\E  | 结束引用                  | /


`\s` 匹配一个空格，`\s+` 匹配一个或多个空格，`\s+{4}` 匹配四个空格。

```
示例：
#sub {\b{north|east|west|south|enter|out}\b} {\e[4m%1\e[24m}
--替换方向为带有下划线标签的链接，使用 \b 避免 out 和 south 重复替换。

示例：
#var {str1} {>    ))))))))))))))))=\\\x7B}
#var {str2} {))))))))=\\\x7B}
#regex {$str1} {{\Q$str2\E}} {#sh OK} {#sh NO}
--使用 \Q..\E 表示原样匹配，不转义。

示例：
#nop 北侠房间匹配;
#var s_nation {?:[ ]+\[大(宋|元|理|夏)国\]|};
#var s_terrain {?:[ ]+\[(城市|城内|门派|野外|阴间|(\S+)势力范围)\]|};
#var s_save {?:[ ]+\[(存盘点)\]|};
#var s_store {?:[ ]+\[(玩家储物柜)\]|};
#var s_group {?:[ ]+\[(\S+)\]|};
#var s_node {?:[ ]+★|};
#var s_path {?:[ ]+((/\w).+)|};
#var SUF {%s-%s{$s_nation}{$s_terrain}{$s_save}{$s_store}{$s_group}{$s_node}{$s_path}%s};
--使用分离组合方案将更好地控制匹配结果。
```

**Color triggers**

为了使文本触发器更容易匹配，(Actions, Gags, Highlights, Prompts, and Substitutes）的颜色代码会被删除。

如果要创建颜色触发器，必须在触发的开头使用 `~`。

使用 `#config {convert meta} on` 使转义代码可见。

```
示例: 
#action {~\e[1;37m%1} {#var roomname %1}
--如果房间名称是 MUDs 上唯一一行亮白色的，将 %1 保存为房间名称。
```

***

这里涵盖了正则表达式的基础知识。

阅读 [「PCRE 手册」](https://www.pcre.org/original/doc/html/pcre.html) 获得更多关于 PCRE 的信息。

在 Linux 和 macOS 下，使用 `man pcresyntax` 查看更多 PCRE 语法。

另可参见: [Colors](#colors)，[Escape Codes](#escape-codes)，[Mathematics](#mathematics)，[Regexp](#regexp)。

# Port

> 语法: #port {command} {argument}

`#Port(端口)` 命令用于创建与其他 mud 客户端 (包括您自己的客户端) 的对等连接，通常用于更新状态窗口。

如果你想让别人从另一台机器上连接，你必须交换 ip 地址和端口号。

您可以使用 `#session` 命令连接到端口。

***

以下是 `#port` 命令的详细说明：

**#port {init} {name} {port} {file}**

`#port init` 启动您的端口。文件参数是可选的。

该命令创建具有给定名称的新会话，该会话接受给定端口的传入套接字连接。

**#port {call} {address} {port}**

创建低级远程套接字连接。

**#port {color} {color names}**

设置端口消息的颜色，必须是有效的颜色名称或颜色代码。

**#port {dnd}**

切换请勿打扰模式，拒绝新的 socket 连接。

**#port {group} {name} {group}**

分配一个 socket 组。目前没用，但在未来的更新中可能会变得有用。

**#port {ignore} {name}**

忽略套接字连接。

**#port {info}**

显示有关端口的一些非常基本的信息。

**#port {name} {name}**

更改套接字连接的名称。

**#port {prefix} {text}**

更改端口消息的前缀。

**#port {send} {name|all} {text}**

向 socket 连接发送文本。

**#port {uninit}**

取消初始化端口会话。

**#port {who}**

显示所有套接字连接。

**#port {zap}**

关闭 socket 连接。

***

`#port` 命令与 `#chat` 非常相似，只是它创建了一个专用于在给定端口接收套接字连接的新会话，并没有内置通信协议支持。

您还可以使用 0 作为端口号初始化以创建虚拟会话。

例如：`#port init test 0`。

```
示例:
#event {PORT CONNECTION}
{
    #if {"%1" != "127.0.0.1"}
    {
        #port send {%0} {<118>Sorry, only accepting connections from local host.<088>};
        #port zap {%0}
    }
}
--此示例将事件设置为仅允许从本地主机连接的 IP。
```

```
示例:
#nop 在新终端里启动 tt++ 并执行：
#port init commwindow 4052
#port prefix {}

#nop 在你的终端开启另一个 tt++ 会话并执行：
#gts #ses comms localhost 4052
#act {~%* chats '%*'} {#comms #send {%0}}
#showme <128>Bubba chats 'Testing if this works'
--此示例设置显示聊天的通信窗口。
```

创建新会话时，它将成为活动会话，通过使用 #gts (启动会话)，活动会话在执行命令后返回到原始会话。

如果没有生效可能是您有一个名为 “mud” 的会话，该会话执行 `#gts {argument}`。

因为 `#gts` 是一个未知的命令 ，TinTin 检查 “gts” 是否是会话名称，因为这是它暂时启动 gts 并执行参数的情况, 执行参数后，TinTin 重新启动调用会话，在这种情况下，会话名为 “mud”。

另可参见: [All](#all)，[Chat](#chat)，[Run](#run)，[Session](#session)，[Session Name](#session-name)，[Snoop](#snoop)，[SSL](#ssl)，[Zap](#zap)。

# Prompt

> 语法: #prompt {text} {new text} {row #} {col #}

`#Prompt(提示)` 是 [split](#split) 分割窗口模式的一项特性功能。

它将从服务器捕捉行并显示在分割屏幕后的状态条上。  

你可以使用和 [substitute](#substitute) 命令相同的方式来定义 {text}  和 {new text}。

行号 raw 是可选且实用的参数，有助于非标准屏幕拆分模式的显示。  

正行号从顶部绘制 #raw 行，而负行号从底部绘制 #raw 行。

没有参数时 `#prompt` 将写入默认的分割行，即输入行上面的一行，通常位于 `raw -2`。

列号 col 是可选的参数，可用于设置列索引。  

正列号从左部绘制 #col 列，而负列号从右部绘制 #col 列。

如果列参数为空，tintin 将在打印行的开头前先把行的内容清空。

```
打印前清空行：
#prompt {bla} {bli} {-1}
打印前不清空行：
#prompt {bla} {bli} {-1} {1}
```

[showme](#showme) 和 [echo](#echo) 命令也可以使用 raw、col 参数，因此使用 `#show` 和 `#echo` 命令在也可以在分割窗口上显示文本。

注: 有关拆分窗口模式的更多信息，请参阅 `#help split`。

注: 有关替换文本的更多信息，请参见 `#help substitute`。

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

```
示例: 
#prompt {[%1/%2hp]} {[<078>%1/%2hp]}
--这将在状态条中打印匹配的行，将颜色设置为暗淡的白色。
```

注：`#prompt` 有一定的局限性，比如一行只能显示一个字段，不能自主更新等，可以通过使用 `#list`、`#echo` 等写插件来解决这些问题，请参见技术交流群内示例文件。

注: 您可以使用 `#unprompt` 命令删除提示。

另可参见: [Action](#action)，[Gag](#gag)，[Highlight](#highlight)，[Substitute](#substitute)。

# Read

> 语法: #read {filename}

将命令文件读取到内存中。

命令文件将与当前加载的命令合并，重复的命令将被覆盖。

如果使用大括号 `{` 和 `}`，则可以对一个命令使用多行。

但是，这意味着您必须始终将每个 `{` 与 `}` 匹配，否则 `#read` 会失败。

您可以使用 `/* text */` 注释掉多行内容。

```
示例：
#read autolevel.tin
```

这将在你制作的命令文件中读取包含 aliasses 、action 、tickers 等，以参与一些淘气的全自动升级。

TinTin++ 将命令字符设置为命令文件中找到的第一个字符，默认情况下命令字符设置为 `#`。

如果您想在读取文件时看到更多信息，请使用: `#config {verbose} {on}`。

请记住，文件中使用的每个开口大括号 `{` 必须与闭合大括号 `}` 相匹配。

如果不这样做，您将收到错误消息，并且文件不会加载。

另可参见: [Log](#log)，[Scan](#scan)，[Textin](#textin)，[Write](#write)。

# Regexp

> 语法: #regexp {string} {expression} {true} {false}

`#Regex` 命令 (正则表达式的缩写) 用于将给定字符串与给定正则表达式进行比较。

正则表达式可以包含转义，并且如果要匹配单个 `\` 字符您应该使用 `\\`。

变量存储在 &1 到 &99 中，&0 保存整个匹配的子字符串。

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

正则表达式有以下支持。

```
^ 匹配行首。
$ 匹配行尾。
\ 转义字符。

%1-%99 匹配任意文本并保存在相应索引中。
%0 匹配所有文本。
{ } 嵌入与 perl 兼容的正则表达式，存储匹配项。
%!{ } 嵌入与 perl 兼容的正则表达式，不存储匹配项。
[ ] . + | ( ) ? * 等符号除非在大括号内使用，否则被视为普通文本。
请记住，除非使用 %!{}，否则 {} 会自动替换为 ()。
```

以下(懒惰)匹配项在 %1-%99 + 1 处可用：

参数|说明
:-|:-
%d|匹配零到任意数量的数字
%D|匹配零到任意数量的非数字
%s|匹配零到任意数量的空格
%S|匹配零到任意数量的非空格
%w|匹配零到任意数量的字母
%W|匹配零到任意数量的非字母

实验性 (可能发生变化) 的匹配项有:

参数|说明
:-|:-
%a|匹配零到任意数量的除换行符以外的字符
%A|匹配零到任意数量的换行符
%p|匹配零到任意数量的可打印字符
%P|匹配零到任意数量的不可打印字符
%u|匹配零到任意数量的 unicode 字符
%U|匹配零到任意数量的非 unicode 字符

如果要匹配 1 个数字，请使用 `%+1d`。

如果要匹配 4 个空格，请使用 `%+4s`。

如果要匹配 3-5 个空格，请使用 `%+3..5s`。

如果要匹配 0 到任意个字母，请使用 `%+0..w`，以此类推。

参数|说明
:-|:-
%+|匹配一到任意数量的字符
%?|匹配零到一个字符
%.|匹配一个字符
%*|匹配零到任意数量的字符
%i|匹配时不区分大小写
%I|匹配时区分大小写(默认)

匹配项将自动存储到 %1 和 %99 之间的值。从 %1 开始，每个正则表达式递增 1。

如果您使用 %15 作为正则表达式，下一个未编号的正则表达式将是 %16。

要防止存储匹配项，请使用 %!*、%!w 等。

```
示例: 
#regex {Hello World} {%* World} {#showme Matched &1 World} {#showme no match}

示例: 
#regexp {bli bla blo} {bli {.*} blo} {#showme &1}
```  
```
来自 xgg@pkuxkx 的示例：

在北侠中抓取闲聊频道id时，
#act {^【闲聊】%!*(%1 ||} {
  #var lastid %1
};
正常用了一段时间后发现会被表情污染：
【闲聊】...(@_@)。(xgg || pure dzp)
此时变量抓取错误，
$lastid = {@_@)。(xgg}

指定匹配类型字母即可解决冲突。
#act {^【闲聊】%!*(%w ||} {
  #var lastid %1
};
```

注：就像别名或函数一样，`#regex` 有自己的范围。

另可参见: [PCRE](#pcre)，[Replace](#replace)。

# Repeat

> 语法: #[number] {commands}

`#repeat` 命令是实现重复相同命令最简单的方法。

```
示例：
#10 buy bread
--这将使你执行 “by bread” 10 次。
```

另可参见: [Break](#break)，[Continue](#continue)，[Foreach](#foreach)，[List](#list)，[Loop](#loop)，[Parse](#parse)，[Return](#return)，[While](#while)。

# Replace

> 语法: #replace {variable} {oldtext} {newtext}

搜索给定变量，并将每次出现的 'oldtext' 替换为 'newtext'。

变量存储在 &1 到 &99中，&0 保存整个匹配子字符串。

'oldtext' 参数是正则表达式。

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

如果将 'newtext' 留空，则将删除 'oldtext'。

```
示例: 
#var {test} {bli bla blo};
#replace {test} {bl} {tr}
--将变量 test 从 “bli bla blo” 更改为 “tri tra tro”。

示例：
#function rnd #math result 1d9;
#replace test {%.} {@rnd{}}
```

如果你想替换一个 `\` 字符，需要输入 `\\`。

```
示例：
#var {test} {aa\cc};#rep {test} {\\} {bb};#var test
#VARIABLE {test} {aabbcc}
```

另可参见: [Cat](#cat)，[Format](#format)，[Function](#function)，[Local](#local)，[Math](#math)，[PCRE](#pcre)，[Script](#script)，[Variable](#variable)。

# Return

> 语法: #return {text}

可以使用 return 命令从正在执行的触发器中断开。

在 #function 函数中，您可以使用 #return 和参数来断开函数并设置结果变量。

另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat) and [While](#while).

# Run

> 语法: #run {session name} {shell commands} {file}

Run 命令以交互方式运行 shell 命令或控制台应用程序。当应用程序终止时，会话也会像正常会话一样终止。

无论是 ssh 、 telnet 、 python 、 php 、 perl 还是 ruby，您都可以运行任何 shell 命令。

默认情况下，#run 命令将使您处于字符模式，这意味着每个按键都直接传输到应用程序。按下 enter 键后，可以输入 tintin 命令。要禁用字符模式，请按 enter 键并输入: #cursor echo on。
```
示例: 
#run myserver ssh myname@myserver.com
```

这将创建到具有完整 tintin 脚本功能的 * nix 服务器的 ssh 会话。
```
示例: 
#run python python;
#act {^cmd %1} {%1};
print "cmd #showme <118>Hello World!"
```
这将启动一个 python shell，创建一个触发器来执行 “cmd” 前面的任何文本，并打印一条红色的线。

注意: 您也可以使用 #script 和 #system 命令执行 shell 命令。

另可参见: [All](#all), [Port](#port), [Session](#session), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

# Scan

> 语法: #scan {abort|read}

Scan 命令读取文件名并将其发送到屏幕上，就好像它是MUDs输出一样。这对于将 ansi 文件转换为 html 和读取日志文件非常有用。

包括接收到的行事件在内的操作和其他触发器将在每一行触发，并且可以通过发出: #scan abort 来中止扫描。

另可参见: [Log](#log), [Read](#read), [Scan](#scan), [Textin](#textin) and [Write](#write).

# Screen

> 语法：#screen {option} {argument}

Screen 屏幕命令提供了各种屏幕操作命令和实用程序。

指令|效果
:-|:-
#screen blur|将终端移动到堆栈的后面。
#screen clear [all\|scroll region\|square] \<args>|当清屏时提供 4 个参数，定义顶部、左角、底部、右角。
#screen focus|将终端移动到堆栈的前面。
#screen fullscreen [on\|off]|在没有参数的情况下使用时切换全屏模式。
#screen get \<option> \<var>|获取各种屏幕选项并将其保存到 \<var>。使用 #screen 无需参数即可查看所有可用选项。
#screen info|调试信息。
#screen input \<square>|设置输入区域。
#screen load \<both\|label\|title>|重新加载保存的标题、标签或两者。
#screen minimize \<on\|off>|打开时最小化，关闭时恢复。
#screen maximize [on\|off]|打开时最大化，关闭时恢复。
#screen move \<height> \<width>|将终端的左上角移动到像素坐标。
#screen raise \<event>|这将引发几个带有 %1 和 %2 参数的屏幕事件。
#screen refresh|终端dependant，可能什么也不做。
#screen rescale \<height> \<width>|将屏幕调整到给定的高度和宽度 (以像素为单位)。
#screen resize \<rows> \<cols>|将屏幕调整为给定的高度和宽度 (以字符为单位)。
#screen save \<both\|label\|title>|保存标题、标签或两者。
#screen scroll \<square>|设置滚动区域，更改拆分设置。
#screen set \<both\|label\|title>|设置标题、标签或两者。标题只在 Windows 上有效。

另可参见：[Bell](#bell).

# Screen Reader

> 语法：#config {SCREEN READER} {ON|OFF}

屏幕阅读器模式通过使用 `#config screen on` 启用。屏幕阅读器模式的主要目的是向服务器报告屏幕阅读器正在使用 [MTTS 标准](http://tintin.sourceforge.net/protocols/mtts)。  

启用屏幕阅读器模式后，TinTin++ 将尝试删除可能可视的元素。

另可参见：[Config](#config).

# Script

> 语法: #script {variable} {shell commands}

脚本命令允许您在 shell 中执行命令。这些命令的输出将作为列表存储在给定变量中。可以使用 script 命令执行 Lua 、 PHP 、 Perl 、 Python 、 Tcl 和 Ruby 脚本。
```
示例: 
#script {result} {lua -e 'print("Hello TinTin++")'

示例: 
#script {result} {ruby -e 'print "Hello TinTin++"'}

示例: 
#script {result} {python -c 'print "Hello TinTin++"'}

示例: 
#script {result} {php -r 'echo "Hello TinTin++"'}

示例: 
#script {result} {tcl -c 'puts "Hello TinTin++"'}

示例: 
#script {path} {pwd}
```

如果没有给出变量参数，脚本输出将被视为 tintin 输入，允许您使用 #showme 和 #send 命令来处理脚本的输出。请记住，您也可以执行脚本文件。

如果给定变量参数，脚本的输出将作为列表存储在变量中。使用 $variable[1] 、 $variable[2] 等查看列表。
```
示例: 
#script {OS} {uname -s};
#showme My OS is: $OS[1]
```
注意: 您也可以使用 #run 和 #system 命令来执行 shell 命令。

另可参见: [Format](#format), [Function](#function), [Local](#local), [Math](#)math, [Replace](#replace) and [Variable](#variable).

# Send

> 语法: #send {text}

直接将文本发送到 MUD，如果你想从转义代码开始，这很有用。

#send 将自动附加换行符，您可以用 \ 结束换行，以防止这种情况发生。

另可参见：[Textin](#textin).

# Session

> 语法: #session {name} {address} {port} {file}

将以给定的名称开始会话，连接到指定的地址和端口，加载可选文件。
```
示例: 
#ses pku mud.pkuxkx.com 8080
```
当然，如果你真的想去某个地方，你必须填写其他东西。Mud 连接器提供了大量可搜索的 muds 列表。

其他选项是 #session + 和 - 转到下一个或上一个会话。只有当你正在多次播放时，这才有效。`#session <number>` 激活对应于给定号码的 session。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

# Session name

> 语法: #[sessionname] {commands}

您可以使用 #session 命令创建多个会话。默认情况下，只有一个会话处于活动状态，这意味着您输入的命令在活动会话中执行，当所有会话接收输出时，只显示发送到活动会话的输出。

当您使用 #session 命令创建会话时，您必须指定会话名称，在没有参数的情况下使用时，可以使用带有 hashtag 的会话名称来激活会话。如果给定参数，该会话将作为命令执行该参数，则不会激活会话。
```
示例: 
#ses one mymud.com 23;
#ses two mymud.com 23;
#one;
#two wiggle
```
这将创建两个会话，最后创建的会话 (在本例中为两个) 将被激活。使用 #one 激活会话 1。使用 #two wiggle，wiggle social 将由会话 2 执行，会话 1 将保持活动。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session](#session), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

# Showme

> 语法: #show {string} {row} {col}

show 命令将字符串显示到终端，不会发送到服务器，可用于状态、警告等。 
 
show 命令显示的消息可以被触发，并且可以用于调试操作、替换等。由于变量也被替换，这也可以用于显示信息。

如果你想避免 `#show` 显示的信息被触发，  
可以使用：`#line ignore #show {<string>}`.

```
示例：
#tick {TICK} {#delay 50 #show 10秒后警告!!!} {60}

示例: 
#showme $bla
如果定义了变量 “bla”，这将显示 bla 设置为的任何内容。
```

行号和列号是可选的，  
工作方式与 [#prompt](#prompt) 命令相同。

另可参见: [Buffer](#buffer), [Echo](#echo) and [Grep](#grep).

# Snoop

> 语法: #snoop {sessionname}

此命令将切换会话的 snoop 状态。即使会话在后台，窥探会话也会显示其服务器输出。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session](#session), [Session Name](#session-name), [SSL](#ssl) and [Zap](#zap).

# Speedwalk

Speedwalking 允许您键入不以分号分隔的多个方向，现在它允许您用数字为方向加前缀，以表示前进该方向的次数。您可以使用 #config 打开/关闭它。

> 示例: 2s5w3s3w2nw

如果没有打开快速行走，你需要输入:<br> s;s;w;w;w;w;w;s;s;s;w;w;w;n;n;w

如果你想使用.2s5w3s3w2w 来执行快速行走，你可以尝试下面的脚本。
```
示例:
#alias {.%0}
{
        #local cnt {};
        #local char {};

        #parse {%0} {char}
        {
                #if {"$char" >= "0" && "$char" <= "9"}
                {
                        #var cnt $cnt$char
                };
                #elseif {"$cnt" == ""}
                {
                        $char
                };
                #else
                {
                        #loop $cnt 1 cnt
                        {
                                $char
                        };
                        #var cnt {}
                }
        }
}
```
另可参见: [Alias](#alias), [Cursor](#cursor), [History](#history), [Keypad](#keypad), [Macro](#macro) and [Tab](#tab).

# Split

> 语法: #split {top bar} {bottom bar} {left bar} {right bar} {input bar}

此选项要求您的终端支持VT100仿真。

split 命令允许创建顶部状态栏，左右状态条，滚动区域，底部状态栏和输入行。 

屏幕分割区域如下表所示：  
<table>
 <tr >
	    <td align="center"colspan="3">顶部状态栏</td>
	</tr>
 <tr >
	    <td align="center">左部状态条</td>
	    <td align="center">滚动区域</td>
	    <td align="center">右部状态条</td>
	</tr>
 <tr >
	    <td align="center"colspan="3">底部状态栏</td>
	</tr>
 <tr >
	    <td align="center"colspan="3">输入条</td>
	</tr>
</table>

默认情况下，底部状态栏填充有破折号 ---，破折号线条也被称为分割线。滚动区域也被称为主屏幕，所有传入文本默认显示在这里。

如果您在没有参数的情况下使用 `#split`，它将设置顶部状态栏高度为0 行，底部状态栏为 1 行。

如果将 `#split` 与一个参数一起使用，它将设置顶部状态栏的高度到给定的行数，底部状态栏将为 1 行。

如果使用两个参数，则第一个参数是顶部状态栏的高度，第二个参数是底部状态栏的高度。

第三和第四个参数是可选的，默认为 0。

第五个参数是可选的，它用来设置输入栏的尺寸，它的默认值为 1。

可以使用负参数，在这种情况下，状态栏宽度被定义为滚动区域的最小宽度。

```
示例: #split 0 0
这将只分割出滚动区域和输入行。
非常适合极简主义者。

示例: #split 1 1 0 -80
这将分割出单独一行顶部状态栏和底部状态栏。
左栏的宽度为0，而右栏的宽度为可变宽度。
例如：如果屏幕列宽是100，80列将用于滚动区域，留下一个右栏宽度为20列。
```

注意：您可以使用[ #promt ](#prompt)及 `#show {line} {row}` 命令在分割区域中显示文本。  
注意: 您可以使用 #unsplit 命令关闭分割模式。

如果您使用的是 #map 命令，您可以通过使用: #map flag vtmap 在顶部分割部分显示自动地图。
```
示例: 
#map create;
#map goto 1;
#split 16 1;
#map flag vtmap;
#parse eewssdeeeunnweewssdeeeunwesnewnssdeeeunnsewsnwesdwwwunw tmp #map move $tmp
```

# SSL

> 语法: #ssl {name} {address} {port} {file}

将以给定的名称开始会话，连接到指定的地址和端口，加载可选的文件名。

> 示例: 
#ssl pku mud.pkuxkx.com 8080

除了将 ssl (安全套接字层) 添加到会话之外，#SSL 命令类似于 #session。为了 SSL 工作，需要安装 GnuTLS。


另可参见: [All](#all), [Port](#port), [Run](#run), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

# Statements

TinTin++ 理解以下声明。

#break  
#case {value} {true}  
#continue  
#default {commands}   
#else {commands}  
#elseif {expression} {true}  
#foreach {list} {variable} {commands}  
#if {expression} {true}  
#loop {min} {max} {variable} {commands}  
#parse {string} {variable} {commands}  
#return {value}  
#switch {expression} {commands}  
#while {expression} {commands}  

另可参见：[Commands](#commands),[Help](#help) and [Info](#info).

# Substitute

> 语法: #substitute {message} {newmessage} {priority}

#Substitute 命令允许您更改MUDs输出。%1-99 变量从消息中被替换，可以在替换的新消息部分使用。消息部分不应使用 %0 变量。优先级部分是可选的，并确定替代部分的优先级，默认为 5。

有关正则匹配的信息，请参见正则表达式 [「PCRE」](#pcre) 一节。

您可以在新消息部分添加TinTin颜色代码来更改消息的颜色，默认情况下，删除所有以前的MUDs消息颜色代码。有关更多信息，请参见颜色[Colors](#colors)。
```
示例: 
#substitute {%1 tells you '%2'} {
   <128>%1 <138>tells you '<128>%2<138>'
}
```
添加这个替换，并告诉自己看到结果。

注意: 您可以使用 #unsubstitute 命令删除替换。

另可参见: [Action](#action), [Gag](#gag), [Highlight](#highlight) and [Prompt](#prompt).

# Suspend

> 语法: #suspend

这将在后台放置TinTin++，您将返回到 shell。按 ctrl-z 会做同样的事情。你可以通过键入 fg 来返回TinTin++。

# Switch

> 语法: #switch {condition} {arguments}

#Switch 命令的工作方式类似于其他语言中的 switch 语句。当遇到 #switch 命令时，它的主体被解析，找到的每个 #case 命令将与 switch 的条件参数进行比较，如果有匹配，则执行。如果找到 #default 命令并且没有匹配 #case 语句，则执行 #default 命令的参数。

#Break 命令可用于从switch中断开，但不像在 C 中那样需要，因为每个switch只能执行一个 #case 命令。
```
示例: 
#switch {1d4} {
   #case 1 cackle;
   #case 2 smile;
   #default giggle
}
```
另可参见: [Case](#case), [Default](#default), [Else](#else), [Elseif](#elseif), [If](#if) and [Regex](#regex).

# System

> 语法: #system {commands}

系统命令允许您在 shell 中执行命令。

> 示例: #system ls

如果你忘记了你想阅读的文件的确切名称或顺序，这很有用。

注意: 您也可以使用 #script 和 #run 命令来执行 shell 命令。

另可参见: [Script](#script) and [Run](#run).

# Tab

> 语法: #tab {completionword}

Tab 命令将完成 word 添加到选项卡完成列表中。按下 “tab” 键时，TinTin将在您的 tab 列表中搜索最佳匹配。对于长命令很有用。

如果您在没有定义标签的情况下单击标签，tintin 将使用 scrollback buffer 查找匹配项。

> 示例: #tab muhahaha

键入 mu，然后按 tab，会出现这个邪恶的命令。

注意: 您可以使用 “untab” 命令删除标签。

另可参见: [Alias](#alias), [Cursor](#curse), [History](#history), [Keypad](#keypad), [Macro](#macro) and [Speedwalk](#speedwalk).

# Textin

> 语法: #textin {filename} {delay}

这将在文件中读取，并将每一行发送到MUDs。Tintin 不会解析文本。将脚本文件转储到 mud 的注释编辑器或类似的命令中很有用。请记住，如果您一次发送太多数据，大多数 muds 都会关闭您的连接。使用可选的延迟参数在每个命令之间添加一个小延迟。

> 示例: #textin desc1.txt 0.2

会在 olc 编辑器中加载 desc1 的数据。

另可参见: [Log](#log), [Read](#read), [Scan](#scan) and [Write](#write).

# Ticker

> 语法: #ticker {name} {commands} {interval}

名称部分可以是任何你想要的，取消只需要 unticker 命令。每隔 x 秒执行一次命令，这在间隔部分中指定。

> 示例: #ticker {autosave} {save} {300}

这将使 TinTin 每 300 秒执行一次save命令。

注意: 您可以使用 #untic 命令删除定时器。

另可参见: [Delay](#delay) and [Event](#event).

# Time

> 语法：#format {variable} {%t} {argument}

#format 命令的 %t 参数使 strftime() 打印日期。

默认情况下，使用的时间戳是当前时间，如果要打印过去或将来的日期，请使用:

> 指令：#format {variable} {%t} {{argument} {{epoch time}}

当前时间戳是使用 #format {time} {%T} 获得的。

使用 %t 时，参数应包含 strftime 格式说明符。输出值可能因您的本地化设置而异。

参数|说明
:-|:-
%a|星期几的缩写名称(周一...周日)
%A|星期几的全名(周一...周日)
%b|月份的缩写名称 (1月..12月)
%B|月份的全名(1月...12月)
%C|2位数字 世纪。(19...20)
%d|2位数字 月份中的天。(0...31)
%H|2位数字 24 小时制。(00...23)
%I|2位数字 12 小时制。(01...12)
%j|3 位数 一年中的第几天。 (001...366)
%m|2位数字 年份中的月份 (01...12)
%M|2位数字 小时中的分钟 (00...59)
%p|缩写 12 小时制 (AM...PM)
%P|缩写 12 小时制 (am...pm)
%S|2位数字 分钟中的秒 (00...59)
%u|1位数字 星期几 (1...7)
%U|2位数字 一年中的下周日 (00...53)
%w|1位数字 一周中的第几天 (0...6)
%W|2位数字 一年中的下周一 (00...53)
%y|2位数字 年份(70...38)
%Y|4位数字 年份(1970...2038)
%z|5位时区偏移量(-1200...+1400)
%Z|时区的缩写名称

```
获取当前年月日：
#format foo {%t} {%Y-%m-%d}
#OK. VARIABLE {foo} HAS BEEN SET TO {2020-04-07}.
```

另可参见：[Echo](#echo),[Event](#event) and [Format](#format).

# Variable

> 语法: #variable {name} {string}

变量不同于 %0-99 个参数，因为您可以将完整单词指定为变量，除非它们被更改，否则它们会保留在完整会话的内存中。它们可以保存在 coms 文件中，如果您同时运行两个或多个会话，则可以将它们设置为不同的值。变量对于每个会话都是全局的，可以通过在变量名之前添加 $ 来访问。  

```
示例:
#alias {target} {#var target %0}
#alias {x} {cast 'acid blast' $target}
```  
变量的名称必须只存在字母、数字、下划线，变量名称的第一个字符必须始终是字母。如果不满足这些要求，请不要惊慌，只需将变量封装在大括号中。  

```
示例: #variable {cool website!} {http://tintin.sourceforge.net} 
chat I was on ${cool website!} yesterday!
```  
可以使用括号嵌套变量，使变量的行为类似于关联数组。  

```
示例: 
#var hp[self] 34;
#var hp[target] 46
```  
使用 `$variable[+1]` 可以看到变量的第一个嵌套的值，使用 `$variable[-1]` 可以看到最后一个嵌套的值。使用 `$variable[-2]` 将报告倒数第二个值，依此类推。

您可以使用 `*variable[+1]` 看到变量第一个嵌套的键，查看所有键使用 `*variable[]` 或 `*variable[%*]`。

查看变量使用 `&variable` 的嵌套索引。查看变量索引总数使用 `&variable[]`。

注意: 不存在变量的嵌套索引为 0，因此您可以使用 `#if {&{variable}}` 检查变量是否存在。

注意: 您可以使用 #unvariable 命令删除变量（对套嵌中的变量也适用）。

```
来自蓝日的疑问：
#var mylist {
	{a} {str1}
	{b} {str2}
	{c}	{str3}
};
如何删除{c} {str3}这对键值？

答：
#unvar mylist[c]
```

另可参见: [Format](#format), [Function](#function), [Local](#local), [Math](#math), [List](#list), [Replace](#replace) and [Script](#script).

# While

> 语法: #while {variable} {commands}

While 命令的工作方式类似于 c 中的 while 命令。一旦条件等于 0，while 循环将停止。

```
示例:
#list var create a b c d
#while {\&var[]} {#showme $var[+1];#unvar var[+1]}
```
另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat) and [Return](#return).

# Wildcards

在 TinTin++ 中，所有的通配符/globs 都是由正则表达式处理的。许多命令以某种形式或方式支持通配符。
```
示例: #alias {a%*}
显示以 “a” 开头的所有别名。
示例: #help {A%*}
显示以 “A” 开头的所有别名。
示例: #kill action %*Bubba%*
删除包含单词 Bubba 的所有act。
示例: #grep ^Bubba %*
显示所有以 Bubba 开头的 scrollback buffer 中的行。
示例: #showme ${map_%*}
显示以 map_ 开头的所有变量
```
另可参见: [PCRE](#pcre).

# Write

> 语法: #write {filename}

这个命令会将你所有的TinTin列表写入文件。

> 示例: #write bla.tin

会把你的TinTin别名、触发器等写给 bla.tin。
```
来自dzp@pkuxkx的注释：

单独 #write 变量、别名等出来，
可以写到一个单独的 class 里，
使用下列命令保存：
#class {<classname>} {write} {<filename>}。
```
另可参见: [Log](#log), [Read](#read), [Scan](#scan) and [Textin](#textin).

# Zap

> 语法: #zap {session}

如果没有参数，这将关闭当前活动会话。  
如果没有活动会话，它将关闭 TinTin++。  
如果提供会话名称，它将关闭给定的会话。

通常可使用组合键 ctrl-d 关闭会话。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session](#session), [Session Name](#session-name), [Snoop](#snoop) and [SSL](#ssl).

# 关于
***
**文档来自[「TinTin++ 官网」](https://tintin.sourceforge.io/)**  

**翻译者：xgg@pkuxkx**  
**贡献者：dzp@pkuxkx**  

**继续阅读:[ 返回导航 ](#导航)**
***