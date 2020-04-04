# TINTIN++中文手册

# 导航

|[ 总览 ](#总览)
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
|[ Daemon ](#daemon)
|[ Debug ](#debug)
|[ Default ](#default)
|[ Delay ](#delay)
|[ Draw ](#draw)|  
|[ Echo ](#echo)
|[ Elseif ](#elseif)
|[ End ](#end)|  
|[ Escape Codes ](#escape-codes)
|[ Event ](#event)|  
|[ Forall ](#forall)
|[ Foreach ](#foreach)
|[ Format ](#format)
|[ Function ](#function)|  
|[ Gag ](#gag)
|[ Greeting ](#greeting)
|[ Grep ](#Grep)|  
|[ Help ](#help)
|[ Highlight ](#highlight)
|[ History](#history)|  
|[ If ](#if)
|[ Ignore ](#ignore)
|[ Index ](#总览)
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
|[ MSDP ](#msdp)
|[ MSLP ](#mslp)|  
|[ Nop ](#nop)|   
|[ Parse ](#parse)
|[ Path ](#path)
|[ Pathdir ](#pathdir)|  
|[ PCRE ](##regular-expressions)
|[ Port ](#port)
|[ Prompt ](#prompt)|  
|[ Read ](#read)
|[ Regex ](#regex)
|[ Regular Expressions ](#regular-expressions)|  
|[ Repeat ](#repeat)
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

- **TinTin++**

这是一个MUDs游戏客户端，  
支持：    
Mac OS X,IOS,Android,Linux,Windows。

在这个页面上，  
你会发现使用  TinTin++ 的使用介绍。    
其他信息可以在各个帮助部分找到。

- **启动及结束**

启动 TinTin++ 的语法是: <br>
> ./tt++ 【配置文件名】

您可以在下面的文件部分阅读更多关于命令文件的信息。不过，记住一件事。启动 TinTin++ 时定义的所有操作、别名、替换等都是由所有会话继承的。

如果要退出 TinTin++ 可以键入“#end”，或者在空行上按组合键 ctrl-d。

对于 WinTin++ 用户，如果要使用 shift-insert 粘贴文本，则在选择时自动复制文本。

- **程序的基本特性**

首先，我将解释一些非常基本和重要的功能:

所有 TinTin++ 命令都以 “#” 开头。
<br>
(这可以用 #config 来改变)。

> 示例: #help <br>
    -- #help是客户端命令，不会发送到服务端。

键入时，TinTin++ 的所有命令可以缩写。

> 示例: #he   
    -- #he 等效于 #help。

所有命令都可以用 ';' 分隔。

> 示例: w;u;look;say dzp我要买药！ 
<br>-- 递归执行这四条命令。

有三种方法可以转义符号";"。
```
示例: \say Hello ;) 
用符号'\'开头的行不会被TinTin++解析。

示例: say Hello \;)
不解析'\'后面的字符。

示例: #config verbatim off 
除非以'#'开头，所有语句都会被原样整行发送。
```

- **连接至MUDs服务端**

命令: <br>
#session {会话名} {mud ip} {端口}

示例: <br>
#session pku mud.pkuxkx.com 8080

可以在上面示例末尾添加`;用户名;密码;`自动登录。

您可以拥有多个会话，在这种情况下，您可以在键入 `#<会话名称>` 的会话之间切换。

您可以通过键入: #session 来获得所有会话的列表。当前活动会话标记为 (active)。  snooped会话标记为 (snooped)。MCCP 会话 (MUDs客户端压缩协议) 标记为 (mccp)。

- **分屏**

命令: #split

Split 命令将创建一个独立的输入和输出区域。

使用 #prompt 命令，您可以捕获提示并将其放在拆分行上。要摆脱拆分界面，您可以使用 #unsplit 将终端设置恢复为默认设置。

- **别名**

命令: #alias

用法: #alias {name} {commands}

#alias 命令的语法几乎和 csh 中的别名一样。
使用此命令定义别名。变量 %0，%1..%9 包含别名命令的参数，如下所示:
%0 变量包含所有参数。
%1 变量包含第1 个参数。
....
%9 变量包含第九个参数。

示例: #alias nice helo Mr %1

如果别名定义右侧没有变量，别名-command 后面的任何参数都将附加到命令字符串中。

示例: 
#alias ff cast 'fireball'  
'ff dzp' 等效于: cast 'fireball' dzp

如果希望别名执行更多命令，则必须使用大括号。

示例: #alias ws {wake;stand}

要删除别名，请使用 #unalias 命令。

警告!TinTin++ 不是你的临时保姆，因此不检查递归别名!您可以通过转义整行来避免递归。

示例: #alias put \put %1 in %2

或者使用 send 命令。

示例: #send put %1 in %2

- **触发**

命令: #action

用法: #action {action-text} {commands}

使用此命令定义当屏幕上出现特定文本时要执行的操作。在 action-text 中，有 99 个变量可以用作通配符。这些变量是 %1，%2...%9，%10...%99。
```
示例:
#Action {你受伤了} {buy yao;eat yao}

#Action {%1想要杀了你。} {kill %1}

#Action {%1告诉你'%2'} {tell dzp %1告诉我'%2'}
-- 转发消息给 dzp。

#Action {告诉你} #bell 
-- 当你得到一个通知时发出嘟嘟声。
```
如果键入 “#ignore action on”，<br>
您可以让 TinTin++ 忽略触发。

通过键入 “#debug action on”，<br>
您可以看到 TinTin++ 在触发时执行的命令。

您可以使用 #unaction 命令删除操作。

- **高亮显示**

命令: #highlight (记住你可以缩写命令)

使用方法: #high {text} {color}

这个命令有点像 #action。这个命令的目的是用你提供的颜色替换MUDs中的文本。此命令是 #substitute 命令的简化版本。

```
示例:
#high {通脉药} {黄色}
-- 为词语 通脉药 上色。

#high {%1通脉药%2} {黄色} 
-- 给包含 通脉药 的行上色。
```
使用 #unhigh 删除高亮显示。

- **快速行走**

如果您键入仅由字母和数字以及 `e 、 s 、 w 、 n 、 u 、 d` 组成的命令，则此命令可以解释为一系列移动命令。

示例: ssw2n -- 南、南、西、北、北

如果您在键入一些实际上仅由这些字母组成的命令时遇到问题，请键入大写字母。例如，当检查新闻NEWS或被要求输入 NEW 作为你的名字时。

您必须启用快速行走才能使用本功能:<br>
`#config speedwalk on/off`

- **定时器**

命令: #ticker {name} {命令} {秒}

北大侠客行 MUDs 上每 15 分钟就可以 使用fullme命令。如果你在使用fullme验证并输入正确验证文本，5M经验以内你会获得双倍内力精力并恢复状态，所有任务会获得完整奖励，5M经验后长时间不使用fullme会被判定为机器人。所以经常使用是非常好的。TinTin++ 帮助你做到这一点。

**注意：** fullme会导致年龄增加。

#Ticker {tick} {#delay 1 {#show 现在可以使用fullme命令了}} {900}

这将创建一个名为 {tick} 的 定时器，该 ticker 将打印提示信息，并在900秒后下一个 tick 出现时再次打印该提示。

你可以用 #untick 删除标记。

- **命令文件**

当您命令 TinTin++ 读取命令文件时，它会解析文件中的所有文本。你可以使用命令文件来保存别名/动作，登录到一个MUDs (名称、密码等)。基本上各种命令都可以加载。

您可以使用文本编辑器 (强烈建议) 制作命令文件，也可以使用 #write 命令将所有列表写入文件。

文件命令:

#read 文件名 <br>
-- 读取并执行文件。

#Write 文件名 <br>
-- 将当前会话已知的所有操作/别名/替换写入文件。

- **重复命令**

可以重复一个命令

语法:#number 命令

例子:

#5 eat yao <br>
-- 如果你受伤了，吃药可以恢复伤势。

#10 {buy yao;eat yao} <br>
-- 重复这两个命令 10 次。

- **历史回溯**

TinTin++ 具有 csh 历史特性的有限子集。

!  -- 重复最后一个命令。 <br>
!Cast -- 重复从 cast 开始的最后一个命令。 <br>
Ctrl-r -- 进入反向历史搜索模式。

- **路径记录**

如果使用了#path new命令，TinTin++ 会跟踪你的移动。也就是说，每当你键入北/南/东/西/上/下 等移动命令时，TinTin++ 会自动将方向和它的相反方向加入队列 (路径)。
```
Path 的命令:
#path new 
-- 启动路径模式，重置队列。
#path end 
-- 停止路径模式。
#path map 
-- 显示路径。
#path ins {forward} {backward} 
-- 将命令插入队列。
#path del 
-- 删除路径中的最后一步。
#path save {f|b} {别名} 
-- 将路径保存到给定的别名。
#path load {alias} 
-- 将路径别名加载到映射队列中
#path walk {forward|backward} 
-- 按照队列路径向前或向后走 1 步。
```
#act {这个方向没有出路} {#path del}

上面的触发可以有效的帮助记录路径。

游戏中的例子:<br>
你想要快速的完成任务后返回，<br>
键入: #path new<br>
然后行走并杀掉任务目标后，<br>
键入: #path save backward tmp;$tmp<br>
还可以建立别名，这应该可以节省不少时间。

- **帮助**

命令: #help {主题}

帮助命令是你的朋友，它还包含所有可用TinTin命令的最新信息。如果你在没有参数的情况下键入 #help，你会看到各种帮助主题，其中大部分在本介绍中没有描述，因为这里只涵盖了开始的基本知识。

***
**享受MUDs带来的乐趣吧！**
***

## Action

> 语法：#action {文本} {命令} {优先级}

#action 命令可用于用一个或多个命令响应服务器发送的特定消息。从文本消息中替换%1-99个变量，并可以在操作的命令部分使用。优先级部分是可选的，并确定操作的优先级，默认为5。

__注意：%0永远不应用于触发。__

如果消息以 ~ 开头必定匹配颜色代码。为了触发颜色，您可以启用`#config {convert meta} on` 为使用颜色触发而显示元字符。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。

```
示例: 
#action {%1告诉你'%2'} {tell %1 我暂时不在.}
```
使用 tilda，您可以创建颜色触发器来捕获难以触发文本的颜色触发器，以查看使用的颜色代码:`#config {convert meta) on`。
```
示例: 
#action {~^\e[1;37m%1} 
{#showme {--用粗体白色显示: %1}}
```
Showme命令可以触发操作。<br>
如果你不想让showme被触发使用: 
```
#line ignore #showme {text}
```
操作按字母顺序排序，一次只能触发一个操作。要更改顺序，您可以分配优先级，默认为 5，数字越小，优先级越高。优先级可以是浮点数字。

要删除以 %* 为消息的操作，请使用：
```
#unaction {%%*}
或
#unaction {\%*}
```
或者，您可以将动作包装在类#class中，然后在不再需要触发动作时杀死该类。

另可参见: [Gag](#gag), [Highlight](#highlight), [Prompt](#prompt) and [Substitute](#substitude).

## Alias

> 语法：#alias {name} {命令} {优先级}

#Alias 别名命令可用于缩短长时间或经常使用的命令。当使用别名时，%1-99变量从参数中被替换，表示第1 到 99 个单词，这些单词可以在别名的命令部分使用。优先级部分是可选的，并确定别名的优先级，默认为 5。

如果使用 %0，它将包含所有参数，如果命令部分只存在一个单词，则变量会自动附加到末尾。

> 示例: #alias {k} {kill %1;kick}

输入 “k dzp” 将导致下手杀死 dzp ，紧接着做表情kick(对着空气踢了一脚)。

**注意：不要杀人不成反被杀。**

您可以使用别名的 “名称” 部分中的变量创建更复杂的别名，该部分将覆盖默认变量处理。
```
示例: 
#alias {k %1 with %2} {
  wield %2;attack %1;
  slash %1 with %2;
  whirl %2;
  strike %1 with %2
}
```
使用上面的别名，你可以用键入如下内容: 
```
k blue smurf with battle axe
```
若要具有与所有用户输入相匹配的别名，请使用 %* 作为名称。
```
示例: 
#alias {%*} {#showme You Wrote:%0}
```
别名按字母顺序排序，一次只能触发一个别名。要更改顺序，您可以分配优先级，默认为 5，数字越小，优先级越高。优先级可以是浮点数字。

注意: 您可以使用 #unalias 命令删除别名。

要删除以 %* 为名称的别名，请使用 
```
#unalias {%%*} 
或 
#unalias {\%*}。
```
或者，您可以将别名包装在类#class中，然后在不再需要别名时杀死该类。

另可参见: [Cursor](#cursor), [History](#history), [Keypad](#keypad), [Macro](#macro), [Speedwalk](#speedwalk) and [Tab](#tab).

## All

> 语法: #all {commands}

如果您在一个终端中有多个会话，您可以使用 #all 在所有会话 (不包括启动会话) 中执行命令。

> 示例: #all quit

会使所有会话quit。

另可参见: [Port](#port), [Run](#run), [Session](#session), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

## Bell

> 语法: #bell

#Bell 命令会响起终端铃声，已经过时，应该避免，而是使用 #showme {\a} 将终端报警字符发送到终端。

注意：使用手机客户端`#bell`可以使手机振动。

```
示例: 
#action {dzp tells you} 
{#showme {\a\}
```

如果你不看屏幕，如果你不想错过与dzp的对话，这可能会很有用。或者，您可以使用#system 播放声音文件。用 \ 结束 #showme 会阻止添加换行符。`#Showme {\a}` 将导致空行，而 `#showme {\a\}` 不会。

一些终端将允许您使用 VT100 操作系统命令来更改终端的标题，该标题可以用作视觉警报。
```
示例:
#action {dzp tells you}
{
    #showme{\e[22;0t\e]0;新消息\e\a\};
    #delay 10 #showme {\e[23;0t\}
}
```
上面的示例将保存窗口标题，将标题更改为 “新消息”，然后在 10 秒钟后重置窗口标题。

铃声响起时，可以将终端设置为弹出到前台。
```
示例: 
#showme {pop up alarm: \e[?1043h\a\e[?1043l}
```
可以在一些终端上调整响铃音量。

```
示例:
#loop {1} {8} {cnt}
{
  #line substitute variable
    #delay {$cnt} 
      #showme {音量 $cnt: \e[$cnt t\a}
}
```
另可参见: [Cr](#cr) and [Forall](#forall).

## Break

> 语法: #break

#break 中断命令可用于中断 `#foreach 、 #loop 、 #parse 、 #switch 和 #while `命令。当发现 #break 时，tintin将移动到命令的末尾，并从那里继续。
```
示例:
#math cnt 0;
#while {1}
{
  #math cnt $cnt + 1;
  #if {$cnt == 20}
  {
    #break
  }
}
```
另可参见: [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Buffer
```
语法: 
#buffer {home|up|down|end|find|get|lock|write|info}
```
#Buffer 缓冲区命令有各种操作 `scrollback buffer`的选项。

> #buffer {home}

将您移动到 scrollback 缓冲区的顶部并显示页面。启用滚动锁定模式。在宏中使用时最有用。

> #buffer {up}

将 scrollback 缓冲区向上移动一页并显示该页。启用滚动锁定模式。在宏中使用时最有用。

> #buffer {down}

将 scrollback 缓冲区向下移动一页并显示该页。启用滚动锁定模式。在宏中使用时最有用。

> #buffer {end}

将您移动到 scrollback 缓冲区的末尾并显示页面。禁用滚动锁定模式。在宏中使用时最有用。

> #buffer {find} {[number]} {\<string>}

将缓冲区移动到可以包含正则表达式的给定字符串。或者，您可以提供要跳过的匹配数，允许您在缓冲区中进一步跳转。

> #buffer {get} {\<variable>} {\<lower bound>} {[upper bound]}

允许您将 `scrollback buffer` 中的一行或几行 (包括颜色代码) 存储到变量中。下限和上限必须在 1 到缓冲区大小之间。如果省略上限，则将给定行存储为标准变量。如果给定上限，两个边界之间的线将存储为列表。

> #buffer {lock}

切换 scrollback 缓冲区上锁。当锁定时，不会显示新传入的文本，任何命令都将禁用锁定，通过几个缓冲区命令将重新启用锁定。解锁时，它会将您移动到 `scrollback buffer` 的末尾并显示页面。

> #buffer {write} {\<filename>}

将 scrollback 缓冲区写入给定文件名。

> #buffer {info}

显示 `scrollback buffer` 用于节省内存的共享字符串内存系统的一些统计数据。

```
示例: 
#macro {(press ctrl-v)(press F1)} {#buffer end}
```
将 ctrl-v 与 F1 键与 “将缓冲区滚动到其末尾” 命令相关联。
```
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
```
当退出时: line 出现在上部，循环浏览缓冲区的最后 20 行，寻找粗体黄色 `(\e[1;33m)` 房间名称。当地图绘制时，知道你所在房间的名称可能会很有用。

另可参见: [Echo](#echo), [Grep](#grep) and [Showme](#showme).

## Button

> 语法：#button {square} {commands} {priority}

#Button 按钮命令可用于当在指定的空间区域内收到鼠标单击动作时响应一个或多个命令。  
鼠标单击的坐标存储在 %0-%3 中，可以用于按钮的命令部分。

空间部分应存在两个坐标，定义左上角和右下角，使用行、列、行、列语法。  
空间参数应该用空格、分号或括号。

默认情况下，该按钮设置为响应鼠标点击动作，要响应其他按键，你必须定义一个5th的参数。您可以启用 `#info button on` 查看发生的按钮事件及其类型。

优先级部分是可选的，默认为 5。

您必须启用 `#config {mouse tracking} on` 才能使按钮工作。

此命令不会绘制可见按钮，如果需要您必须单独执行此操作。

```
例如: 
#button {1;1;2;2} {#showme 你点击了左上角.}
```
按钮按字母顺序排序，一次只会触发一个按钮。要更改顺序，您可以分配优先级，默认5，较低的数字表示更高的优先级。优先级可以是浮点数。

注释：要查看按钮点击触发器，请使用 `#info button on`。  
注释：您可以使用 #unbutton 命令删除按钮。

另可参见：[Delay](#delay),[Event](#event) and [Ticker](#ticker).

## Case

> 语法: #case {条件} {参数}

必须在 `switch` 命令中使用 `case` 命令。当 case 命令的条件参数与 switch 命令的条件参数匹配时，执行 case 的主体。

当比较字符串时，`switch` 和 `case` 写参数必须用引号包围。

```
示例:
#function {bar_color}
{
	switch {10 * %1 / %2}
	{
		#case  0 #return ;
		#case  1 #return ;
		#case  2 #return ;
		#case  3 #return ;
		#case  4 #return ;
		#case  5 #return ;
		#case  6 #return ;
		#case  7 #return ;
		#case  8 #return ;
		#case  9 #return ;
		#case 10 #return 
	}
}
```
如果最大健康度为 100，当前健康度为 44，您使用 `@bar_color{44;100}`，它将返回 `<fea>`。

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

这个函数返回相反的方向。<br>
`@Reverse_direction{north}`将回返`south`。

另可参见: [Default](#default), [Else](#else), [Elseif](#elseif), [If](#if), [Switch](#switch) and [Regex](#regex).

## Cat

> 语法： #cat {variable} {argument}

Cat 命令将参数连接到给定变量。

另可参见: [Format](#format), [Function](#function), [Local](#local), [Math](#math), [Replace](#replace) [Script](#script) and [Variable](#variable).

## Characters

TinTin++定义了以下特殊字符:

`#` Hashtag 是启动命令的默认字符，下面会称为命令字符或tintin字符。  
加载命令文件时，命令字符设置为文件中的第一个字符。字符也可以使用 `#config` 重新定义。

`;` 分号作为命令分离器可用于分开两个命令。多个命令可以串在一起。读取脚本文件时忽略尾随分号是一个常见的错误。

`{}` 花括号 (又名大括号) 用于分隔多个单词、命令、参数、嵌套命令和嵌套变量。大括号不容易被转义，并且必须总是成对使用。

`" "` 引号字符用于 #math，#if，#switch 和 #case 命令中的字符串。建议使用额外一组大括号 {} 来定义字符串。

`!` 感叹号用于重复命令，请参阅 #help history。  
可以使用 #config 重新定义该字符。

`\` 发送到服务器时以反斜杠开头的输入行是原样发送的。  
可以使用 #config 重新定义该字符。

另可参见：[Colors](#colors),[Escape](#escape),[Mathematics](#mathematics) and [PCRE](#pcre).

## Chat

> 语法: #chat {命令} {参数}

`#chat` 命令用于创建与其他 mud 客户端的点对点连接，通常用于聊天和发送文件。这是一个分散的聊天系统，这意味着为了连接到其他用户，你必须与他们交换 ip地址和端口号。

> #chat {initialize} {port}

聊天初始化启动您的聊天服务器。端口号是可选的，默认情况下，4050 用作您的端口。使用此命令后，其他人可以使用您的 ip地址和端口号连接到您的聊天服务器，然后您可以连接到其他人。

> #chat {name} {your name}

默认情况下，你的名字被设置为tintin，但是如果已经有人连接了tintin，大多数服务器都会拒绝你, 所以你想做的第一件事就是改变你的聊天名称。你的名字可以包括颜色代码。tt++ 聊天服务器不接受一些名字，比如 “all” 这个名字和超过 20 个字符的名字。

> #chat {call} {ip address} {port}

`#chat call` 聊天呼叫用于连接到另一个聊天服务器。如果省略端口参数，则使用默认端口 (4050)。

> #chat {color} {color names}

默认聊天颜色为粗体红色，您可以使用 `#chat color` 命令来更改此颜色，例如: `#chat color bold yellow` 粗体黄色，或者使用 256 颜色代码: `#chat color <cde>`。

> #chat {message} {user|all} {text}

这是用于通信的主命令。如果您使用 `#chat message all`，则该消息被标记为公共消息，并发送给您连接的每个人。

> #chat {emote} {user|all} {text}

这个命令的工作方式与 `#chat message` 除了在外观上完全一样，它所做的只是在消息前面加上你的名字。

> #chat {paste} {user|all} {text}

此命令允许粘贴，将连续快速跟随的输入附加到消息中。请记住，大多数 mud 客户端不会正确接收超过 40 行的消息。

> #chat {reply} {text}

`#chat reply`聊天回复，回复你收到私人信息的最后一个人。

> #chat {send} {user|all}

此命令向另一个人发送原始数据字符串，这需要了解聊天协议 [Mud Master Chat Protocol](https://tintin.sourceforge.io/manual/chatprotocol.php)才能使用。

> #chat dnd

DND 代表 “不打扰”，此命令切换 DND 状态。启用后，所有新的传入连接都会自动关闭。

> #chat {ip} {address}

此命令设置默认情况下未设置的 ip地址，并在连接到另一个 mud 客户端时发送。TinTin++ 忽略了其他 mud 客户端报告的知识产权，只需获取套接字地址，但是其他 mud 客户端可能需要设置它。

> #chat {who}

`#chat who`，显示你联系的所有人。第一列显示连接的参考号，当向某人发送消息时，可以使用该参考号而不是连接的名称。第二列显示连接的名称。第三列显示为连接设置的标志，(P)rivate，(I)gnore，(S)erve，(F)orward 到 user，以及 (f)or以下列显示 ip 、端口和 mud 客户端名称。

> #chat {info}

此命令显示您的姓名、 ip地址、端口、下载目录、回复和 DND 状态。

> #chat {ignore} {user}

这个命令将忽略给定的用户，他们不会被告知你忽略了他们，或者他们的消息不再通过。

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

此命令将保存到 scrollback 缓冲区中的所有内容作为 snoop 数据转发给给定用户。

> #chat {serve} {user}

此命令将使您将所有公共聊天消息转发给给定用户，并将该用户的所有公共聊天消息转发给您所连接的每个人。为了避免无限循环，消息作为私人消息被转发。

> #chat {group} {user} {name}

此命令允许您将给定用户分配给组。您可以将组名与表情、消息和发送命令一起使用。如果你在没有参数的情况下使用 `#chat group`，它的行为会像 `#chat who` 一样，显示所有用户的列表和他们的组名。

> #chat {sendfile} {user} {filename}

此命令允许您向给定用户发送文件，他们必须在传输开始前接受该文件。

> #chat {accept} {user}

在用户提供发送文件后接受文件传输。

> #chat {decline} {user}

在用户提供发送文件后拒绝文件传输。

> #chat {cancel} {user}

启动文件传输后取消文件传输。

> #chat {filestat} {user}

显示当前正在进行的文件传输的信息。

> #chat {downloaddir} {directory}

此命令设置新下载的目录。

有关更多信息，请参见描述 `#chat` 使用的基础协议 MMCP 规范：[MMCP Specification](https://tintin.sourceforge.io/manual/chatprotocol.php)。

## Class

> 语法: <br> 
#class {name} {open|close|read filename|write filename|kill}

Class命令可以方便的管理成组的列表。

> #class {\<classname>} {open}

{Open} 选项将打开一个类，并自动关闭以前打开的类 (如果有的话)，之后创建的所有触发器和变量都将被分配给这个类，直到它关闭。

> #class {\<classname>} {close}

{Close} 选项将关闭当前打开的类。

> #class {\<classname>} {read} {\<filename>}

{Read} 选项将打开提供的类，读取给定文件，并在读取后关闭类。

> #class {\<classname>} {write} {\<filename>}

{Write} 选项将给定类的所有触发器写入文件。此选项可以通过将变量分配给属于特定类来存储数据。

> #class {\<classname>} {kill}

{Kill} 选项将删除给定类的所有触发器。

没有启用或禁用类的选项。要禁用一个类，你必须杀死它，要启用它，你必须从文件中重新加载它。或者，您可以使用变量来打开或关闭功能，或者如果要最小化文件访问，可以使用别名来重新创建触发器。

另请参见: [Debug](#debug), [Ignore](#ignore), [Info](#info), [Kill](#kill) and [Message](#message)。

## Colors

**ANSI Colors**

> 语法: \<abc> with a, b, c 是参数

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

**Xterm 256 Colors**

对于 xterm 256 颜色支持：

对于 RGB 前景色使用 `<aaa>到<fff>`，<br>
对于 RGB 背景色使用 `<AAA>到<FFF>`。

对于灰度前景色，使用 `<g00>到<g23>`; <br>
对于灰度背景色，使用 `<G00>到<G23>`。
```
示例:
#showme <034>T<025>i<016>n<007>T<043>i<052>n<061>+<070>+<088>
```
在 TinTin++ 中执行此操作，以查看实际结果。
```
示例:
#showme <fca> orange <cfa> lime <caf> indigo <acf> azure <fac> crimson
```

在 TinTin++ 中执行此操作，要查看实际结果，您的终端必须支持 `xterm 256 color`。

**Truecolor**

对于 12 位 truecolor 真彩色，<br>
前景色使用 `<F000>到<FFFF>`，<br>
背景色使用 `<B000>到<BFFF>`。<br>
第一个字符表示 F (前景) 或 B (背景)，接下来的三个字符是十六进制 RGB 值。这允许 4096 种不同的颜色。**请记住，并非所有终端都支持 truecolor**。

对于 24 位 truecolor 前景色，使用`\e[38;2;R;G;Bm`，其中 RGB 是 0 到 255 之间的红色/绿色/蓝色强度。<br>
例如: `\e[37;2;50;100;150m`。

对于 24 位 truecolor 背景颜色，<br>
请使用 `\e[48;2;R;G;Bm`。

另可参见: [ Escape Codes ](#escape-codes), [Mathematics](#mathematics) and [Regular Expressions](#regular-expressions)

## Commands

> 语法: #commands {abbreviation}

如果没有参数，此命令将显示所有命令，否则将显示与缩写匹配的所有命令。

**Command 语法**

所有 TinTin++ 命令都以 “#” 开头，可以使用 `#config {TINTIN CHAR}` 更改。例如，键入时，可以缩写所有 tintin 命令。全名 #variable，您可以使用 #var。

可以使用 `#<session name>` 激活会话，也可以使用 `#<session name> {commands}` 在不激活会话的情况下执行命令。

`#<Number> {commands}` 可用于执行给定命令的 “number” 次。

您可以通过将命令封装在一组大括号中，并用分号分隔每个命令来执行几个命令，例如，显示您将使用的 “hello” 和 “world” 4 次:
```
示例:
#4 {#showme Hello;#showme World}
```
**Commands Seperator**

如果你想发送文字 “;”，你可以使用 `\;` 来发送。要按原样发送整行内容，您将以 `\'`开头

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
{} 的意思就是延迟解析
```

**Carriage Return**

当您发出命令时，系统会自动添加换行/回车。要更改此行为，请以 “\” 结尾。

> 示例: #showme hi\

> #send look\

**Command Files**

可以将命令放在文件中，这些文件随后被称为命令文件。您可以使用读取read、会话session、端口port、运行run和 ssl 命令读取命令文件。

您可以使用 `“tt++ <filename>”` 启动 TinTin++，以在启动时加载命令文件。如果使用会话命令提供文件名，则只有当会话成功连接到主机时，命令文件才会被读取。

默认的命令字符是 `#` 。TinTin++ 将命令字符设置为命令文件中找到的第一个字符。

如果您想在读取文件时看到更多信息，请使用: `#config {verbose} {on}`

请记住，文件中使用的每个开口大括号 {必须与闭合大括号} 相匹配。如果不这样做会失败，您将收到错误消息，并且文件不会加载。

您可以保存使用 `#write` 命令创建的触发器、变量和设置。请记住，并非所有设置都已保存。您可以使用 `#event {PROGRAM START}` 或 `#event {SESSION CREATED}` 来添加初始化命令，并用`#Write`保存。

## Config

> 语法: #config {option} {argument}

当 TinTin++ 启动时，它将生成一个配置文件，可以用 config 命令修改它。键入没有参数的 config 将显示当前配置，这些配置可以用 `#write` 命令写入文件方便以后加载。

***
默认情况下不启用以下配置选项:

> #config {CONVERT META} {ON|OFF}

对于键盘输入和服务器输出，此选项使元字符可见。对于调试、创建宏和创建颜色触发器很有用。

> #config {DEBUG TELNET} {ON|OFF}

此选项将显示大多数 telnet negotiations。创建 telnet 事件时很有用。

> #config {INHERITANCE} {ON|OFF}

设置为 OFF 时，触发器不会从启动会话继承。仍将继承配置设置。

> #config {LOG LEVEL} {LOW|HIGH}，

The low setting logs mud output before triggers,默认值为高。

> #config {MCCP} {ON|OFF}

默认情况下启用此选项，可用于关闭 MCCP 支持。对于 MCCP 支持中断的 MUDs 很有用。

***
以下配置选项需要进一步说明:

> #config {COLOR PATCH} {ON|OFF}

此选项修复了某些 muds 上的拆分模式下的颜色代码使用，最明显的是 Achaea。默认情况下，它是关闭的，启用时可能会影响颜色触发器。

> #config {PACKET PATCH} {ON|OFF}

如果您的mud没有使用 MCCP，将数据包补丁设置为 0.5 到 1.0 之间的值将有助于处理损坏的数据包。如果这导致在显示提示之前出现小延迟，您可以使用 #split 并使用 `#prompt` 命令将提示放在拆分行上来解决这个问题。一些 MUDs 允许启用 EOR 或 GA，这也将消除延迟。

## Continue

> 语法: #continue

可以使用 “继续” 命令跳过` #foreach 、 #loop 、 #parse 、 #switch 和 #while `命令中的命令。当发现 `#continue` 时，TinTin++ 将移动到循环的末尾，并像往常一样继续。
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
```
另可参见: [Break](#break), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Coordinates

当 0,0 坐标位于左上角时，TinTin++ 使用 y,x / rows,cols 表示。  
当 0,0 坐标位于左下角时，TinTin++ 使用 x,y / cols/rows 表示。

定义空间坐标时，通过使用四个坐标指定空间的左上角和空间的右下角。

绝大多数的 tintin 命令使用 row,col 表示法。

另可参见：[Characters](#characters),[Colors](#colors),[Escape](#escape),[Mathematics](#mathematics) and [PCRE](#pcre).

## Cr

> 语法: #cr

此命令向mud服务器发送回车。这是过时的，应该避免。

#Cr 如果启用了重复输入配置选项，并且在不重复最后一个命令的情况下需要输入，则很有用。

一个很好的选择是在没有参数的情况下使用 #send，或者使用命令分隔符 `;` 插入 enter。

如果你想在 DikuMUD 服务器上发送多个返回，最好使用 `#send {\n \n}` (空格是有意的)，因为许多 DikuMUD 服务器将连续的返回视为一次返回。

```
示例: 
#ticker {idle} {#send} {300}

这将每 300 秒 (5 分钟) 向mud发送一次回车，这将阻止大多数mud和网络因不活动而断开您的连接。
```

另可参见: [Bell](#bell)and [Forall](#forall).

## Cursor

> 语法: #cursor {option}

键入 #cursor 时，如果没有选项，将显示所有可用的光标选项。Cursor 命令的主要目标是使用宏添加可定制的输入编辑。
```
示例: 
#macro {\e\e[3~} {#cursor clear right}
```
当按下 alt-delete 时，光标右侧的所有输入都被清除，默认情况下，该输入被设置为 ctrl-k。

另可参见: [Alias](#alias), [History](#history), [Keypad](#keybord), [Macro](#macro), [Speedwalk](#speedwalk) and [Tab](#tab).

## Daemon

> 语法：#daemon {attach|detach|kill|list} [name]

#daemon 守护程序提供类似于 screen 和 tmux 的功能。  

- #daemon attach [name]  
attach 附加选项将尝试找到一个守护中的 tintin 实例，并且接管控制权。Name 参数是可选的。  
- #daemon detach [name]  
detach 分离选项将屏蔽tintin，将其变成后台进程。Name 参数是可选的，如果您有
几个守护中的 tt++ 实例正在运行，可以用来将它们分开。  
- #daemon kill [name]  
杀死所有或具有匹配名称的守护程序。  
- #daemon list [name]  
列出所有或具有匹配名称的守护程序。

另可参见：[Script](#script),[System](#system) and [Run](#run).


## Debug

> 语法: #debug {listname} {argument}

如果没有参数，debug 将显示您可以切换的列表。如果没有给出参数，它将切换指定的列表标志。您可以使用 ON 、 OFF 或 LOG 作为参数更具体地更改调试标志。

如果设置了日志标志，并且您正在使用 #LOG 命令记录会话，调试信息将被写入文件。

> 示例: #debug action on

当触发时，操作将生成一条消息，解析器将向您显示操作执行的具体命令。

另可参见: [Class](#class), [Ignore](#ignore), [Info](info), [Kill](#kill) and [Message](#message).

## Default

> 语法: #default {commands}

只能在 switch 命令中使用默认命令。当没有一个 case 命令的条件参数与 switch 命令的条件语句相匹配时，执行默认命令。

```
示例:
#switch {1d4}
{
  #case 1 cackle;
  #case 2 smile;
  #default giggle
}
```
另可参见: [Case](#case), [Default](#default), [Else](#else), [Elseif](#elseif), [If](#if), [Switch](#switch) and [Regex](regex).

## Delay

> 语法:#delay {秒} {命令}

> 语法:#delay {name} {命令} {秒}

延迟命令允许您在执行给定命令之前让 tintin 等待给定的秒数。秒字段以毫秒精度采用浮点数字。

根据参数的数量，delay 命令的工作方式不同。对于三个参数，#delay 具有与 #tick 命令相同的语法，允许您命名延迟。如果您使用命名延迟，并且当前正在等待具有完全相同名称的延迟，它将被删除，并且永远不会执行。使用命名延迟还可以更容易地使用 #undelay 命令。
```
示例: 
#delay {600} {#showme 检查通脉情况}
```
这将在 600 秒后通知您检查通脉情况。

```
示例: 
#delay {checkdz} {#showme 检查通脉情况} {600}
```
与上面相同，只是是使用命名延迟。

另可参见: [Event](#event) and [Ticker](#ticker).

## Draw

> 语法：#draw [color] [options] \<type> \<square> {text}

`Draw` 绘制命令允许您在屏幕上绘制各种类型的线和形状。当您在没有参数的情况下键入 #draw 时提供常见的选项和类型和简要说明。

空间参数应该存在两个坐标，定义左上角和右下角使用行、列、行、列语法。

您可以使用颜色代码或颜色名称为选项添加前缀来给线条和形状上色。

您可以进一步为该选项添加以下前缀:

前缀|说明
:-|:- 
ASCII|将在 ASCII 模式下绘制。
BLANKED|将绘制空白线条和角。
BOLD|将用粗体字母绘制文本。
BOTTOM|如果可能的话，将在底部绘制。
BUMPED|将在绘制之前输入一个enter。
CIRCLED|将绕着角。
CONVERT|将使用元转换绘制文本。
CROSSED|将越过角。
CURSIVE|将用草书字母绘制文本。
FILLED|将填满圆圈和菱形。
GRID|将表格绘制为网格。
HORIZONTAL|如果可能的话，将水平绘制。
HUGE|将用巨大的字母绘制文本。
JEWELED|将在角绘制菱形。
JOINTED|将绘制角。
LEFT|如果可能的话，将在左侧绘制。
NUMBERED|将绘制编号，主要用于调试。
PRUNED|将修剪角。
RIGHT|如果可能的话，将在右侧绘制。
ROUNDED|将绕过角。
SCROLL|将在滚动区域中绘制。
SHADOWED|将给大文本加阴影。
TEED|将在角绘制T型。
TRACED|将追踪大文本。
TOP|如果可能的话，将在顶部绘制。
TUBED|将绘制管而不是线。
UNICODE|将在 unicode 模式下绘制。
VERTICAL|如果可能的话，将垂直绘制。

有以下几种类型可用。

__[ASCII|UNICODE|HUGE] BOX {[TEXT1]} {[TEXT2]}__  
将绘制一个盒子。

__[BLANKED|CIRCLED|CROSSED|JEWELED|ROUNDED|TEED|PRUNED] CORNER__  
将绘制一个角。

__[BLANKED|HORIZONTAL|NUMBERED|TUBED|VERTICAL] LINE {[TEXT]}__  
将绘制线条。

__RAIN {\<VARIABLE\>} {[SPAWN]} {[FADE]} {[LEGEND]}__  
将绘制数字雨。

__[JOINTED|TOP|LEFT|BOTTOM|RIGHT] SIDE__  
将绘制一个盒子的一个或多个边。

__[GRID] TABLE {[LIST1]} {[LIST2]}__  
将绘制一个表格。

__[HUGE] TILE {[TEXT1]} {[TEXT2]}__  
会绘制一块瓷砖。

当已定义了足够大的有效空间，所有绘图类型都采用可选的文本参数。文本自动进行文字包装。

```
例如：
#draw Blue box 1 1 3 20 {Hello world!}
```

另可参见：[Buffer](#buffer),[Echo](#echo),[Grep](#grep) and [Showme](#showme).

## Echo

> 语法: #echo {format} {arguments}

> #echo {{format} {row}} {arguments}

Echo 在屏幕上显示文本，格式选项与 #format 命令相同。与 showme 命令不同，echo 命令不会触发操作。就像 #showme 命令一样，您可以在格式中添加第二个参数，该参数指定该行应该打印的屏幕行，与 #prompt 命令相同。

有关更多信息，请参见[Format](#format) 和 [Prompt](#prompt)的帮助文件。

```
示例: 
#echo {现在时间 %t.} {%Y-%m-%d %H:%M:%S}
```
另可参见: [Buffer](#buffer), [Grep](#grep) and [Showme](#showme).


## Else

> 语法: #else {commands}

Else 语句应该遵循 #IF 或 #ELSEIF 语句，并且只有在前面的 #if 或 #ELSEIF 为 false 时才被调用。
```
示例:
#if {1d2 == 1} {
  smile};
#else {cry}
```
另可参见: [Case](#case), [Default](#default), [Elseif](#elseif), [If](#if), [Switch](#switch) and [Regex](#regex).

## Elseif

> 语法: #elseif {commands}

Elseif 语句应该遵循 #IF 或 #ELSEIF 语句，并且仅在语句为 true 且前面的 #IF 和 #ELSEIF 语句为 false 时才调用。

```
示例: 
#if {1d3 == 1} {
  smirk};
#elseif {1d2 == 1} {
  snicker};
#else {laugh}
```

另可参见: [Case](#case), [Default](#default), [Else](#else), [If](#if), [Switch](#switch) and [Regex](#regex).

## End

> 语法: #end {message}

终止TinTin程序并返回 shell。在空行上按 ctrl-d 也会调用 #end。

消息在终止前立即打印。如果消息是 `\tintin`，将被无声地终止。

## Escape Codes

Tintin 中的 escape 字符是反斜杠: \，可以与几个字符组合使用来创建 escape 代码。

字符  |释义
:-   |:-
\a   |会在终端发出嘟嘟声
\c   |将发送 ctrl-a 的控制字符 \ca。
\e   |将开始一个escape序列。
\n   |将发送线路馈送。
\r   |将发送回车。
\t   |将发送tab。
\x   |例如\xFF将打印十六进制字符值。
\x7B |将发送 “{” 字符。
\x7D |将发送 “}” 字符。
\0   |例如\\077将打印 6 位 octal 字符值。
\\\ |将打印单个 \ 。

当使用 #showme 、 #send 或 #line 时，以 \ 结尾的行将停止 tintin 追加换行符。

要在触发或别名中转义参数，请使用 `%%0 %%1 %%2`等。
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

另可参见: [Colors](#colors), [Mathematics](#mathematics) and [Regular Expressions](#regular-expressions).

## Event

> 语法: #event {event name} {命令}

事件命令允许为预定的客户端事件创建触发器。使用没有参数的 #event 将列出大多数可能的事件，并进行简要描述。使用 `#event %*` 将显示所有定义的事件。大多数事件都会设置参数。

**Chronological Events**

所有按时间顺序排列的事件设置以下参数:<br> 
%0-year使用 4 位数字填充，%1-month使用 2 个零填充数字，%2-week使用 2 个零填充数字，%3-day在month中使用 2 个零填充数字， %4-hour，使用 2 个零填充数字，%5-minute使用 2 个零填充数字，%6-second使用 2 个零填充数字。

**DATE <MONTH-DAY> [HOUR:MINUTE]**

在给定的日期和时间触发事件。必须提供日期，时间是可选的。如果没有时间，它会在午夜触发。
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

收到 #chat 消息时触发。%0 包含原始数据，%1 包含修改后的数据。

**END OF PATH**

当使用 #path walk 到达路径末端时，此事件触发一次。

**IAC**

此事件触发所有 `telnet negotiations`。使用 `#config {debug telnet} {on}` 查看 telnet 事件发生时的正确名称。如果为通常由 mud 客户端 (如 IAC SB TTYPE) 处理的 `telnet negotiations`创建 telnet 事件，则只执行该事件，自动响应将被阻止。

**IAC [DO|DON'T|WILL|DON'T] [OPTION]**

当触发 `DO, DON'T, WILL or WON't` 选项时，这将阻止TinTin自动处理该选项，你必须自己处理。

**IAC SB GMCP <MODULE> IAC SE**

GMCP (通用 Mud 通信协议) 上触发此事件。%0 参数包含模块名称，%1 参数包含 JSON 数据。JSON 数据被转换为TinTin的内部变量系统，因此可以使用 `#variable {gmcp [%0]}{%1}` 直接存储数据。原始 JSON 数据存储在 %2 参数中。

**IAC SB MSDP [VARIABLE]**

此事件触发 [MSDP](https://tintin.sourceforge.io/scripts/msdp.php) (Mud Server 数据协议) 子协商。%0 参数包含变量的名称，%1 参数包含变量的值。值转换为TinTin的内部变量系统，因此可以使用 `#variable {msdp [%0]} {%1}` 直接存储数据。

**IAC [DO|DON'T|WILL|DON'T] MSP**

此事件在 [MSP](https://tintin.sourceforge.io/scripts/msp.php) (MUD声音协议) 子协商上触发。


**IAC SB MSSP [VARIABLE]**

此事件在 MSSP (Mud 服务器状态协议) 子协商上触发。%0 参数包含变量的名称，%1 参数包含变量的值。如果变量作为数组发送，则为每个索引生成名称/值事件。

**IAC [DO|DON'T|WILL|DON'T] MXP**

MXP (Mud 扩展协议) 子协商上触发此事件。

**IAC SB NEW-ENVIRON <IS|INFO|SEND> [VAR|USR]**

此事件触发新环境子协商。根据协商类型，您必须将发送、是或信息附加到事件名称，如使用 `#config {debug telnet} {on}` 时所示。%0 参数包含变量的名称，%1 参数包含变量的值。

**IAC SB ZMP**

ZMP 子协商上触发此事件。根据 ZMP 包，您必须将包附加到事件名称，如使用 `#config {debug telnet} {on}` 时所示。%0 参数包含 ZMP 包数据。

**IAC SB**

任何未定义的子协商都会触发此事件。一些 telnet 选项将被命名，其他选项将是一个数字，如使用 `#config {debug telnet} {on}` 时所示。%0 参数将包含子协商内的数据。

**MAP ENTER MAP**

进入地图时触发。%0 包含新的 vnum。

**MAP ENTER ROOM [VNUM]**

在自动映射程序中进入新房间后，此事件立即触发。房间号是 vnum。%0 参数包含房间的 vnum，%1 包含分区房间的 vnum。

**MAP EXIT MAP**

退出地图时触发。%0 包含旧 vnum。

**MAP EXIT ROOM [VNUM]**

此事件在退出自动映射程序中的当前房间之前立即触发。房间号是 vnum。%0 参数包含房间的 vnum，%1 包含目标房间的 vnum。

**PORT CONNECTION**

当进行新的套接字连接时，此事件会触发。%0 包含套接字号，%1 ip地址，%2 端口号 (对于传入连接，设置为 0)。

**PORT DISCONNECTION**

当套接字断开时，此事件触发。%0 包含套接字号，%1 ip地址，%2 端口号 (对于传入连接，设置为 0)。

**PORT MESSAGE**

当套接字发送数据时，这甚至会触发。%0 包含套接字号，%1 ip地址，%2 端口号 (对于传入连接，设置为 0)，%3 包含剥离的数据, %4 包含原始数据。

**PROGRAM START**

这个事件在TinTIN++ 的启动过程结束时触发。%0 包含客户端名称，%1 包含客户端版本。

**PROGRAM TERMINATION**

此事件在启动会话中TinTin++ 终止进程结束时触发。

**RECEIVED INPUT**

此事件在输入键盘输入后，但在执行之前触发。%0 参数包含原始输入。

**RECEIVED LINE**

当接收到新输出时，多行输出被分解成单行输出。在执行任何触发器之前，此事件会触发来自服务器的每一行输出。%0 参数包含原始行，%1 参数包含纯行，去掉所有颜色代码，始终包含单行。

**RECEIVED OUTPUT**

在将输出分成单行之前，当接收到新输出时触发。%0 包含可以包含多行的原始输出。

**SCREEN RESIZE**

当程序启动时，每当屏幕调整大小时，此事件都会触发一次。%0 包含屏幕宽度，%1 包含屏幕高度。

**SEND OUTPUT**

此事件在命令行发送到服务器后立即触发。% 0参数包含原始命令行。

**SESSION CREATED**

创建会话时触发。%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字ip地址，%3 参数包含端口号。

**SESSION ACTIVATED**

激活会话时触发。%0 参数包含会话名称。

**SESSION CONNECTED**

会话连接到服务器后，此事件立即触发。%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字ip地址，%3 参数包含端口号。

**SESSION DEACTIVATED**

停用会话时触发。%0 参数包含会话名称。

**SESSION DISCONNECTED**

会话与服务器断开连接后，此事件立即触发。%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字ip地址，%3 参数包含端口号。

**SESSION TIMED OUT**

当会话无法连接时，此事件会触发。%0 参数包含会话名称，%1 参数包含主机名，%2 参数包含数字ip地址，%3 参数包含端口号。

**VARIABLE UPDATE \<VARIABLE\>**

当创建或更新变量时，此事件会触发。%0 参数包含变量名，%1 参数包含变量值。

**VT100 [CPR|DA|DECID|DSR|ENQ]**

当接收到终端识别码时，这些事件会触发。它们记录不良，很少使用，通常可以忽略。

另可参见: [Delay](#delay) and [Ticker](#ticker).

## Forall

> #forall 已经过时. 

> #foreach 替代使用.

```
来自xgg@pkuxkx的提示：
这个命令在新版本中已被移除，
使用#foreach代替，
旧版本逍遥行路径显示列表时用的到，
现在已用foreach重写。
```
另可参见: [Foreach](#foreach),[Bell](#bell) and [Cr](#cr).

## Foreach

> 语法: <br>
#foreach {list} {variable} {commands}

Foreach 命令就像一个简化的循环。列表中的每个单词将在执行时存储在变量中，并可以在命令部分中使用。

所提供列表中的项目必须使用分号`;`分隔，或者用大括号将它们括起来。

```
示例: 
#foreach {Bob;Jim;Tom} {name} {say Hello $name!}

示例: 
#foreach {{Bob}{Jim}{Tom}} {name} {say Hello $name!}
```

相当于：hello，Bob!hello,jim!hello,tom!

要使用 foreach 命令循环遍历列表 (或嵌套变量) 中的所有项目，请使用 `$<list> [%*]`。

另可参见: [Break](#break), [Continue](#continue), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Format

> 语法: <br>
#format {variable} {format} {argument1} {argument2} {etc}

此命令允许您像 C 中的 sprintf 函数一样格式化文本。结果将存储在给定的变量中。格式部分可以包含文本和参数变量。在参数部分，你最多可以给出最多 20 个参数。另请参见 sprintf 上的 linux man 文件。

参数	|名字	|描述
:- |:- |:-
%+9s	|String	|前方插入9个空格
%-9s	|String	|后方插入9个空格
%.9s	|String	|最多打印9个字符
%a	  |Number	|打印对应的 ascii 字符
%c	  |Color	 |将参数转换为颜色代码
%d  |	Decimal|	用整数格式打印一个数字
%f  |	Float|	使用浮点格式打印数字
%g  |	Number	|对数字执行千分组。
%h	  |Header	|将参数转换为标题
%l  |	Lowercase	|参数小写
%m  |	Mathexp	|进行数学运算
%n	  |Name	|第一个字母大写
%p  |	String|带前导和尾随空格
%r|	Reverse|	翻转参数(看上下文)
%s|	String	|普通字符串参数
%t	|Format|	在参数中使用[strftime](http://www.manpagez.com/man/3/strftime/)格式创建时间戳。
%u	|Uppercase	|将整个参数大写
%w	|Wordwrap	|以列表形式包装参数
%A	|Char	|打印对应的 ascii 值
%C	|Columns	|打印屏幕宽度 (列)
%H	|Hash|	打印参数的 32 位散列值
%L	|Length|	打印参数的长度
%R|	Rows|	打印屏幕高度 (行)
%S|	Session|打印会话名称
%T	|Epochtime	|打印自epoch以来的秒数
%U	|Epochtime	|打印自epoch以来的微秒数

```
来自dzp@pkuxkx的释义：
epoch 就是 E 纪元，也称为 Unix 纪元。
也就是自格林威治时间（GMT+0） 1970 年 1 月 1 日 00:00:00 以来的秒数。
所谓的「时间戳」，就是这个东西。
有时候也叫 timestamp。
```
```
例如:
#alias {time}
{
        #format line {%cThe time is: %t} {light green} {%Y-%m-%d %T};
        #showme {$line}
}
```
另可参见: [Function](#function), [Local](#local), [Math](#math), [Replace](#replace), [Script](#script) and [Variable](#variable).

## Function

> 语法: #function {name} {commands}

函数命令是别名和变量之间的交叉。除了可以传递参数之外，函数就像变量一样使用。函数类似于别名，因为您可以在函数中执行命令, 函数完成后，调用函数的行将函数调用替换为 [return](#return) 命令提供的值。

函数的名称必须只存在字母、数字、下划线，函数名称的第一个字符必须始终是字母。

您可以使用函数，方法是: `@<functionname> {<arguments>}`， 参数存储在 %0 到 %99 中，%0 保存所有参数，%1 第一个, %2 第二个等。参数通过用大括号或分号来分隔。

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
函数的 if check in 将检查是否传递了参数，如果传递了，参数 (假设是时间戳) 存储在 $epoch 中, 如果不是，则使用 `#format {epoch} %T` 检索自 1970年以来的当前秒数。下一个 $epoch 用于将当前时间存储在 $result 中。使用: `#showme @time{}` 将显示当前时间。

可以在函数中的任何地方使用 #return 命令，但是当找到 #return 命令时，命令执行就结束了。您可以在任何触发器中使用 #return 提前结束命令执行。

有关其他示例，请参见脚本部分。

注释: 您可以使用 #unfunction 命令删除函数。

另可参见: [Format](#format), [Local](#local), [Math](#math), [Replace](#replace), [Script](#script) and [Variable](#variable).

## Gag

> 语法: #gag {message}

将不再显示屏蔽的消息。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。

> 示例: #gag {%iTwinkie chats}

如果 Twinkie 是一个讨厌的人，这个 gag 会阻止他的聊天被显示出来。一开始的 %i 使得 gag 案变得关联性，所以如果 Twinkie 以 TWINKIE 的身份登录，gag 仍然有效。
```
来自xgg@pkuxkx的注释：

有时使用#gag会出现大量">"符号，
这时候可以使用：
#gag {^> $}
并且有时会出现大量空行：
#gag {^$}
在这种情况下要显示空行：
#line ignore #showme {}
```
注释: 您可以使用 #ungag 命令删除 gag。

另可参见: [Action](#action), [Highlight](#highlight), [Prompt](#prompt) and [Substitute](#substitute).

## Greeting

> 语法: #help greeting

将简单明了地向您显示每次启动客户端时显示的问候消息 (其中包含客户端版本号)。如果您希望看到它，并且它在缓冲区中不再可用，则很有用。

这实际上不是一个命令，因为你只能通过 #help 访问它。

## Grep

> 语法:#grep {[页码]} {关键字}

此命令在回滚缓冲区中搜索给定关键字。页码是可选的。它将打印 1 页的对象。如果你想使用 pagenumber 1，然后使用 2 3 ..等，你可以使用 regexp 来获得更好的结果。记得搜索是区分大小写的。

> 示例: #grep tells you

这将显示包含子字符串 “tells you” 的所有接收到的MUDs输出。

另可参见: [Buffer](#buffer), [Echo](#echo) and [Showme](#showme).

## Help

> 语法: #help {subject}

使用帮助文档中的构建，帮助命令将显示一些关于该主题的基本帮助。没有参数，它显示所有可用的帮助主题。

**Help 命令比在线手册更最新。**

> 示例: #help alias

将显示 aliasses 的帮助文件。

> 示例: #help %*

这将显示所有帮助文件。要创建一个包含您将使用的所有内部帮助文件的文件: 
```
#buffer clear;
#help %*;
#buffer write help.txt
````

## Highlight

> 语法: #highlight {message} {color}

Highlight 命令将向 highlight 列表中添加一条消息。如果消息匹配，它将根据给定的颜色代码进行着色。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。突出显示消息部分不应使用 %0 变量。

可用的颜色代码是:reset, light, faint, underscore, blink, reverse, dim, black, red, green, yellow, blue, magenta, cyan, white, b black, b red, b green, b yellow, b blue, b magenta, b cyan, b white。

如果你的终端支持 256 种颜色，额外的颜色代码是: azure, ebony, jade, lime, orange, pink, silver, tan, violet, light azure, light ebony, light jade, light lime, light orange, light pink, light silver, light tan, light violet。

您也可以使用颜色代码[color codes](#colors)。

```
示例: 
#high {^{你|你的}%*} {light cyan}
```

这将用浅青色突出以 “你” 和 “你的” 开头的行。在 pvp 战斗中发现失明或被诅咒很有用。

```
示例: 
#high {%* tells you '%*'} {<ace>}
```

注释: 您可以使用 #unhighlight 命令删除高亮显示。

另可参见: [Action](#action), [Gag](#gag), [Prompt](#prompt) and [Substitute](#substitute).

## History

> 语法:#history {command} {参数}

默认情况下，历史命令与设置为 “!” 的重复字符一起使用。命令历史记录是手动输入命令的列表，默认情况下，每个会话都会记住最后 1000 个唯一命令，这可以用 [config](#config) 命令来更改。

您也可以通过按 ctrl-r 交互搜索历史列表，这与 ctrl-p (上一个) 和 ctrl-n (下一个) 一起工作。

每个会话都有自己的历史列表，从启动会话继承而来。使用`#kill or #kill histories`将清除历史列表。

启动/退出 tintin 时，启动会话将尝试自动加载/保存命令历史记录。存储在历史文件`.tintin/history.txt`中。
```
来自xgg@pkuxkx的说明：
这里的.tintin目录在当前登录终端的用户目录中
```

**#history {delete}**

#history delete历史删除将删除命令历史记录中的最后一个命令。

**#history {insert} {command}**

#History insert 将在命令历史记录的末尾添加给定的命令。

**#history {list}**

#history list历史列表将显示命令历史记录中的所有条目。

**#history {read} {filename}**

#History read 允许在以前保存的命令历史列表中读取。使用事件触发器[Event](#event)可以在会话打开时执行此操作。

**#history {write} {filename}**

#History write 允许将命令历史列表写入文件。使用事件触发器[Event](#event)可以在会话关闭时执行此操作。

另可参见: [Alias](#alias), [Cursor](#cursor), [Keypad](#keypad), [Macro](#macro), [Speedwalk](#speedwalk) and [Tab](#tab).

## If

> 语法: #if {condition} {true} {false}

条件是 c 风格的数学或正则表达式。字符串必须用引号 `""` 包围。在判断真假部分中，任何无零结果都将作为命令执行。如果结果等于零，它将作为可选 false 部分中的命令执行。

当使用 == 或 != 比较字符串时，左边的字符串是原始字符串，右边的字符串是正则表达式。当使用 < and > 或 <= and >= 时，会执行基本的字符串比较。

有关更多信息，请参见 [Mathexp](#mathematics) 和 [Regexp](#regex) 上的帮助文件。
```
示例:
#action {%0 gives you %1 gold coins.}
{
    #if {%1 > 5000} {thank %0}
}
```
如果有人给你 5000 多个金币，你会感谢他们的。
```
来自man@pkuxkx的疑惑：

为什么 $a==好的 不行，
因为这是一个字符串，
必须用引号包围。
示例：
"$a"=="好的"
```
注释: 另请参见 #else 、 #elseif 、 #switch 和 #while。

另可参见: [Case](#case), [Default](#default), [Else](#else), [Elseif](#elseif), [Switch](#switch) and [Regex](#regex).

## Ignore

> 语法: #ignore {listname} {argument}

如果没有参数 ignore 将显示您可以忽略的列表。如果给定一个参数，它将切换指定的列表标志。您可以使用 ON 或 OFF 作为参数更具体地更改忽略标志。

> 示例: #ignore actions off

如果要暂时禁用所有触发器，操作将不再触发，这很有用。

忽略时，以下列表类型的行为没有变化: classes, commands, configurations, paths, and pathdirs。

另可参见: [Class](#class), [Debug](#debug), [Info](#info), [Kill](#kill) and [Message](#message).

## Info

> 语法: #info

Info 命令将显示每个列表类型的节点数量，以及每个列表的忽略、消息和调试状态。

> 语法: #info cpu

这将显示TinTin内部 cpu 使用情况的概述。

另可参见: [Class](#class), [Debug](#debug), [Ignore](#ignore), [Kill](#kill) and [Message](#message).

## Keypad

当Tintin++ 启动时，它会向终端发送 \e= 以启用终端的应用键盘模式，使用 #showme {\e>} 可以禁用该模式。

```
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

禁用键盘模式后，numlock on 将为您提供配置 A，numlock off 将为您提供配置 B。启用键盘模式后，您将获得配置 C。

- **支持 keypad mode 的终端**

Linux Console, PuTTY, Eterm, aterm.

- **不支持 keypad mode 的终端**

RXVT on Cygwin, Windows Console, Gnome Terminal, Konsole

- **特殊终端**

RXVT 需要关闭 numlock 才能启用配置 C。

Xterm 可能需要在 `ctrl-leftclick` 菜单中禁用`Alt/NumLock`修饰符`(num-lock)`。或编辑 `~/.Xresources` 并添加 `XTerm*VT100.numLock:false`

Mac OS X 终端要求在终端-> 窗口设置-> 仿真中启用 "strict vt100 keypad behavior"。

另可参见: [Alias](#alias), [Cursor](#cursor), [History](#history), [Macro](#macro), [Speedwalk](#speedwalk) and [Tab](#tab).

## Kill

> 语法: #kill {trigger type} {argument}

没有参数的 kill 命令将删除每个列表中的每个节点。这包括标记的路径、路径和配置。如果你想在新的脚本文件中阅读并想从头开始，这很有用。

在给定列表中使用 kill 将删除指定的列表，例如: `#kill alias`。

此外，您可以同时给出列表和参数，在这种情况下，只会杀死列表中的匹配触发器。

> 示例: #kill histories tell %*

这将从命令历史列表中删除所有 tell 命令。

另可参见: [Class](#class), [Debug](#debug), [Ignore](#ignore), [Info](#info) and [Message](#message).

## Line

> 语法: #line {option} {argument}

Line 命令提供各种基于行的操作。

**#line {log} {\<filename>} {[text]}**

#Line log 将给定的文本记录到给定的文件名中。如果没有给出文本参数，则显示的下一行将被记录到给定的文件中。如果文本参数中使用了任何TinTin++ 颜色代码，它们将被翻译为 ANSI 颜色代码。根据 #config {LOG} 设置，日志记录格式将是 HTML 、 RAW 或普通。

**#line {logverbatim} {\<filename>} {[text]}**

#Line logverbatim 的工作方式与 #line log 完全一样，只是文本参数中的颜色代码、变量和函数不会被替换。

**#line {gag}**

当被调用时，显示的下一行将被屏蔽。当操作在显示其触发的行之前触发时，在操作中使用 #line gag 将导致触发行不显示。

**#line {ignore} {argument}**

参数在没有检查任何触发器的情况下执行。如果你想在不触发任何动作的情况下使用 #showme 来避免触发循环，这很有用。

**#line {quiet} {argument}**

参数是通过静默系统消息来执行的。

**#line strip {argument}**

该参数是在删除了所有 VT100 和 ANSI 颜色代码后执行的。

**#line substitute {options} {argument}**

可以通过使用命令分隔符分隔多个选项。有效选项有:

- Variables变量: 替换所有变量
- Functions功能: 替换所有功能
- Colors颜色: 替换所有TinTin颜色代码
- Escapes转义: 替代所有转义字符
- Secure安全: 避开所有大括号、变量、函数和命令分隔符

**#line verbose {argument}**

详细执行参数。

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
```
上面的示例将所有 tells 记录到 tells.log 文件中，除非发件人在忽略列表中，否则在这种情况下，tell 会被屏蔽。

## List

> 语法：#list {variable} {option} {argument}

指令|效果
:-|:-
#list {var} {add} {item}|将 {item} 添加到列表中
#list {var} {clear}|清空给定列表
#list {var} {collapse}|将列表转换为变量
#list {var} {create} {item}|使用 {items} 创建列表
#list {var} {delete} {index} {number}|删除位于 {index} 的项目,{number} 是可选的。
#list {var} {explode}|将列表转换为字符列表
#list {var} {insert} {index} {string}|在给定索引处插入 {string}
#list {var} {find} {string} {variable}|返回找到的索引
#list {var} {get} {index} {variable}|将项目复制到 {variable}
#list {var} {order} {string}|按数字顺序插入项目
#list {var} {shuffle}|重新排序列表
#list {var} {set} {index} {string}|更改 {index} 处的项目
#list {var} {simplify} {variable}|将简单列表复制到 {variable}
#list {var} {size} {variable}|将列表大小复制到 {variable}
#list {var} {sort} {string}|按字母顺序插入项目
#list {var} {tokenize} {string}|创建字符列表

索引应该在 1 和列表长度之间。你也可以给出负值，在这种情况下 -1 等于列表中的最后一项，-2 为倒数第二个，依次类推。

插入项目时，正索引将在给定索引处插入，而负索引将附加到项目。

添加和创建选项也允许使用多个项目，最好是用分号分隔的项目。

对于空列表或不存在列表，返回长度为 0。

您可以使用 $var[1] 直接访问列表变量中的元素,例如：$var[2]，$var[-1] 等。

另可参见：[Break](#break), [Continue](#continue), [Foreach](#foreach), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Lists

TinTin有几种不同类型的列表，它们的行为方式相当普遍。为了正确解释列表，在讨论更复杂的类型之前，首先解释最基本的变量类型是最容易的。

- 基本变量: 标准 key = value 变量。
- 简单列表: 包含分号分隔字段的字符串。 `{a;b;c}`。可以保存为变量。
- 大括号列表: 用大括号分隔字段的字符串。 `{a}{b}{c}`。由于表也使用大括号，大括号列表不能存储为变量，因此必须将它们存储为简单列表。
- Table: 将此视为嵌套在另一个变量中的变量。或者作为包含在另一个变量中的变量。
- List: 使用整数作为索引的表。也称为数组。#List 命令是将表用作数组的实用程序命令。

**Simple Variables**

> 示例: <br>
#variable {simple} {Hello World!}<br>
#showme $simple

要查看 “简单” 变量是否存在，您可以使用 &simple，如果变量不存在，它将显示 0，如果变量存在，它将显示变量的索引。

如果你有多个变量，它们按字母顺序和数字排序。虽然对于简单变量来说，这并不完全相关，但是第一个变量有索引 1 、第二个变量索引 2 等等。

变量名需要有字母、数字和下划线。如果您需要使用非标准变量名，可以使用大括号。

> 示例:<br>
#variable {:)} {Happy!};<br>
#showme ${:)}

可以使用它们的索引访问变量。虽然对于表来说主要是有用的，但是对于简单的变量来说可以这样做。第一个变量使用 + 1，第二个变量使用 + 2，等等。最后一个变量使用-1，第二个最后一个变量使用-2，等等。

> 示例: <br>
#showme 第一个变量是: ${+1}

**Removing Variables**

要删除变量，请使用 #unvariable 或 #unvar (每个命令都可以缩写)。可以使用 #unvar {var 1} {var 2} {etc} 同时删除多个变量。

变量对于每个会话都是唯一的，因此，如果您有多个会话，从一个会话中删除变量不会将其从其他会话中删除。

如果删除变量表，则该表中包含的所有变量也将被删除。

**Simple Lists**

简单列表是包含分号分隔字段的字符串。可以将命令作为简单列表输入，例如: #showme {a}; #showme {b} 将作为两个命令执行一行。

有几个命令以一个简单的列表作为输入，这些命令是:` #foreach、#line substitute、#path load、#list create 和 #highlight`。

**Brace Lists**

大括号列表是用大括号分隔字段的字符串。大多数命令的参数都采用大括号列表，例如: #session {x} {mud.com} {1234} {mud.tin}。Session 命令接受 4 个参数，第四个参数 (命令文件) 是可选的。

将简单列表作为输入的命令也将接受括号列表，请记住，您必须将括号列表嵌入额外的括号集中，例如:`#path load {{n}{s}{w}}`，与:`#path load {n;s;w}`相同。

不能将大括号列表存储为变量，因为 TinTin++ 会将它们与表混淆。您可以使用: `#list {bracelist} {create} {{a}{b}{c}}` 将大括号列表转换为表变量，这在内部看起来如下: `{{1}{a}{2}{b}{3}{c}}`。然后，您可以使用: `#list {bracelist} {simplify} {simplelist}` 将此表转换为简单列表，该列表将在 $simplelist 变量中存储。

在TinTin++ 中，大括号很难被转义。使用 `\{` 或 `\}` 将不起作用。这是由于几个因素造成的，但主要是向后兼容性。要转义大括号，您必须使用 `\x7B` 和 `\x7D` 的十六进制符号来定义大括号。有关转义选项的列表，请参见 #help escape，帮助文件还将提醒您如何转义大括号。

**Tables**

表是存储在变量中的键/值对。创建和访问表有几种方法。
```
示例:
#variable {friendlist}{
   {dzp}{dzp@hotmail.com}         
   {xgg}{xgg@gmail.com}
}
```
这将创建一个包含两个条目的好友列表，键是好友的名称，值是好友的电子邮件地址。您可以使用: `#showme {$friendlist[dzp]}` 看到 dzp 的电子邮件地址。您也可以将此表定义如下:
```
示例:
#variable {friendlist[dzp]} {dzp@hotmail.com}
#variable {friendlist[xgg]} {xgg@gmail.com}
```
这将创建与以前使用的单行声明完全相同的表。要查看表使用中的第一个键: `*friendlist[+1]`，请查看表使用中的第一个值: `$friendlist[+1]`。要查看表的大小，请使用 `&friendlist[]`。要打印所有朋友的括号列表，请使用 `*friendlist[%*]`，打印名称以字母 “a” 开头的所有朋友的括号列表: `*freindlist[a%*]`。类似地，看看你的朋友数量，他们的名字以你会使用的字母 “b” 结尾 `&friendlist[%*b]`。

有关正则表达式选项的简要概述，请参见 #help regexp。虽然 TinTin++ 支持 PCRE (与 perl 兼容的正则表达式)，但它将它们嵌入了自己的正则表达式语法中，该语法更简单、侵入性更小, 同时仍然允许那些需要 PCRE 的人充分发挥 PCRE 的力量。

> 示例: #unvariable {friendlist[xgg]}

这将从好友列表中删除 {xgg}。要删除您将使用的整个friendlist: `#unvariable {friendlist}`。
```
示例: 
#variable {friendlist} {
   {dzp} {
      {email}{dzp@hotmail.com} {phone}{123456}
   }
}
```
集合的数量是没有限制的，只需增加更多的大括号。要在此示例中查看 dzp 的电子邮件，您将使用: `#showme {$friendlist[dzp][email]}`。
```
来自dzp@pkuxkx的高级数据结构示例:

#var JMapData-rooms {
{26} {{id}{26}{name}{客店}{links}{up;west}{area}{扬州}{center}{45}{map}{客店二楼〓北大街-----客店}{desc}{这是一家价钱低廉的客栈，生意非常兴隆。外地游客多选择这里落脚，你可以在这里打听到各地的风土人情。店小二里里外外忙得团团转，接待着南腔北调的客人。客店的主人从不露面，他究竟是谁，有各种各样的猜测。墙上挂着一个牌子(paizi)。}{cost}{0}{exits}{{q;u}{142}{q;w}{27}}{objs}{{天神随从}{tianshen suicong}{店小二}{xiao er}{彭波}{peng bo}{扬州的客店留言板}{26}{酉鸡}{zodiac animal}}}}

打印26号room的全部数据：
#showme ${JMapData-rooms}[26]
#精简代码长度
#var room {${JMapData-rooms}[26]}
打印26号room的第一层键：
#showme $room[]
打印26号room的id：
#showme $room[id]
打印26号room的出口：
#showme $room[exits][]
打印26号room的出口个数：
#showme &room[exits][]
打印26号room的第一个出口的键：
#showme *room[exits][+1]
打印26号room的最后一个出口的值：
#showme $room[exits][-1]

高级数据结构可大幅度简化代码。
```

**Lists**

除了数字排序之外，表格按字母顺序排序。如果你想自己确定排序顺序，你可以使用 #list 命令来帮助你将表用作数组。

> 示例: <br>
#action {%1 chats %2} {#list chats add {%0}}

每次收到聊天时，它都会被添加到 “chats” 列表变量的末尾。  
在内部，这看起来像：  
```
#variable {chats}
{
  {1}{xgg chats Hi}
  {2}{dzp chats Hi xgg}
  {3}{xgg chats Bye}
  {4}{dzp chats xgg bye}
}
```

#List 命令是在表实现之前编写的，因此 get 、 set 和 size 选项是多余的。

**The list command**

> 语法: <br>
#list {\<variable>} {\<option>} {\<arguments>}

TinTin++ 中的列表是具有数字索引的表 (又名关联数组)。List 命令通过在删除或插入项目时自动重新编号项目来更容易模拟数组行为。

当 list 命令需要索引时，应该提供 1 到列表长度之间的值。也可以给出负值，在这种情况下，-1 等于列表中的最后一项，-2 等于倒数第二项等。

您可以使用索引直接显示列表中的项目，例如: `$var[1] 、$var[2] 、$var[-1]` 等。

要使用 [foreach](#foreach) 命令循环浏览列表中的所有项目，请使用 `$<list>[%*]`。

**#list {\<list>} {add} {\<argument1>} {\<argument2>} {...}**

#List add 将为提供的每个参数向给定列表添加一个项目。

**#list {\<list>} {clear}**

#List clear 将清空给定的列表变量。该命令相当于: `#variable {<variable>} {}`

**#list {\<list>} {create} {\<argument1>} {\<argument2>} {...}**

#List create 将清除给定的列表，并为提供的每个参数添加一个项目。

**#list {\<list>} {delete} {\<index>} {[number]**

#List delete 将删除给定索引处的项目。Number 参数是要删除的项数，如果省略 1， 项将被删除。

**#list {\<list>} {find} {\<argument>} {\<variable>}**

#List find 允许搜索与提供的参数匹配的项目。如果找不到匹配项，则将目标变量设置为 0，否则将变量设置为包含匹配项的索引。

**#list {\<list>} {get} {\<indext>} {\<variable>}**

#List get 将在提供的索引中检索列表的项目。如果索引不存在，则目标变量设置为 0，否则目标变量设置为包含找到的索引的值。或者，您可以使用 `$list [<index>]` 使用表的接口检索值。

**#list {\<list>} {insert} {\<index>} {\<argument>}**

#List insert 将在给定索引处插入项目。如果索引是正数，则在给定索引处创建项目。如果索引是负数，则在下一个索引处创建项目。因此，使用-1 将在列表的末尾附加一个新项，使用 1 将在列表的开头添加一个新项。

**#list {\<list>} {set} {\<index>} {\<argument>}**

#List set 将提供的索引的值更改为给定的参数。或者，您可以使用: `#variable {<list>[<index>]} {<argument>}`使用表的接口更改值。

**#list {\<list>} {simplify} {\<variable>}**

#List simplify 将表保存为简单的半冒号分隔列表。

**#list {\<list>} {size} {\<variable>}**

#List size 将检索列表中的项目数，并将其存储在提供的目标变量中。或者，您可以使用: `&list[]` 
使用表的接口检索列表中的项目数。

**#list {\<list>} {sort} {\<argument>}**

#List sort 将按字母顺序插入提供的参数。

**#list {\<list>} {tokenize} {\<argument>}**

#List tokenize 使用列表标记将把给定的参数变成一个字符列表。 `{haha}` 将成为 `{{1}{h}{2}{a}{3}{h}{4}{a}}`。如果你想执行低级文本处理，这很有用。

**Parsing**

使用 `#loop、#foreach、#while或#<number>`有多种解析列表和表的方法。

#Loop 接受两个数字参数，第一个数字递增或递减，直到它与第二个数字匹配。循环计数器的值存储在提供的变量中。

#Foreach 将简单列表或大括号列表作为其第一个参数。Foreach 将遍历列表中的每个项目，并将值存储在提供的变量中。

#While 将对第一个参数执行 if 检查，如果结果为 true，则执行第二个参数中的命令。然后，它再次对第一个参数执行 if 检查。它将继续重复，直到 if 检查返回 0，或者用控制流命令中断循环。

#\<Number> 将执行提供的参数 “number” 次。<br>
例如:`#4 #showme beep!\A`

下面是一些例子：
```
示例:
#list friends create {bob;bubba;zorro}
```
在内部，这看起来像： <br>`{{1}{bob}{2}{bubba}{3}{zorro}}`<br>可以通过各种方式解析列表。
```
示例: 
#foreach {$friends[%*]} {name} 
{
    #showme $name
}

示例: 
#foreach {*friends[%*]} {index} 
{
    #showme $friends[$index]
}

示例: 
#loop {1} {&friends[]} {index} 
{
    #showme $friends[+$index]
}

示例: 
#math index 1;
#while {&friends[+$index]} 
{
    #showme $friends[+$index];
    #math index $index + 1
}

示例: 
#math index 1;
#&friends[] 
{
    #showme $friends[+$index];
    #math index $index + 1
}
```
上面的五个例子中的每一个都执行相同的任务：打印朋友列表中的三个名字。

如果你想在执行脚本时更好地了解幕后发生的事情，你可以使用 “#debug all on”。要停止查看调试信息，请使用 “#debug all off”。

**Optimization**

TinTin++ 表在保持在 100 个项目下时速度非常快。一旦表的长度超过 10000 个项目，在旧平台上插入和删除文件开头或中间的项目时可能会出现性能问题。

如果从文件中加载一个大表，确保它被排序是很重要的，当使用 #write 保存一个表时，它会自动排序。

如果您注意到大型表的性能问题，创建哈希表相对容易。

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
以上脚本将快速存储和检索超过 100万个项目。遍历哈希表也相对容易。
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

另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [Loop](#loop), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Local

> 语法: #local {variable name} {string}

Local 命令设置局部变量。与常规变量不同，局部变量只会在创建它的事件持续时间内留在内存中。它们的访问方式与常规变量相同。

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
另可参见: [Format](#format), [Function](#function), [Math](#math), [Replace](#replace), [Script](#script) and [Variable](#variable).

## Log

> 语法：#log {APPEND|OVERWRITE|OFF} {filename}

Log 命令将滚动区域中接收到的所有数据记录到指定的文件名中。模式为 o (覆盖) 或 a (附加)，OFF 参数结束记录。

使用 config 命令，您可以指定用于日志文件的数据类型。这些是: raw原始 (也打印转义代码) 、plain普通 (带转义代码) 、html超文本标记语言 (将转义颜色代码转换为 html 颜色代码)。

> 示例: #log o mylog.txt

这将把所有的 mud 输出写入 mylog.txt。如果您使用 #showme 命令，它也将被记录到文件中，除非您在启用 #split 的情况下显示滚动区域之外的内容。

您可以使用 #line log 命令将单个行记录到日志文件中。
```
示例: 
#act {~%1 chats '%2'} {
   #line log comms.txt %1 chats '%2'
}
```
注释: 您可以使用 #buffer write 命令将整个 scrollback 缓冲区保存到文件中。
```
示例: 
#alias savebuffer {
    #format date %t %F;
    #buffer write log_$date.txt
}
```
您可以使用 #history write 命令将命令历史记录记录到文件中。

另可参见: [Read](#read), [Scan](#scan), [Textin](#textin) and [Write](#write).

## Loop

> 语法: #loop {min} {max} {variable} {commands}

循环命令的工作方式类似于C语言的简化for循环， min 和 max 参数应该是数字。该命令将递增或递减 (取决于数字)，直到达到第二个数字。对于每一个 `in/de-cremention`，将执行命令部分。`in/de-cremention` 计数器的值将存储在变量中，可以在命令部分使用。

> 示例: #loop 1 3 cnt {say $cnt}

这等于: say 1;say 2;say 3

另可参见: [Break](#beak), [Continue](#continue), [Foreach](#foreach), [List](#list), [Parse](#parse), [Repeat](#repeat), [Return](#return) and [While](#while).

## Macro

> 语法: #macro {key sequence} {commands}

按下功能键时发送给终端的键序列可能会因操作系统和终端而异，要了解发送的顺序，您可以启用转换元配置选项。您可以通过按 ctrl-v 为下一次按键启用元转换模式。

如果你想创建一个宏，每当你按下 F1 时，它都会执行`kill dzp`，你要执行以下操作:
```
示例: 
#macro {(按F1键)} {kill dzp} 
-- 宏现在应该可以工作了。
```
默认情况下，tintin 模拟 bash 输入编辑。可以使用与 #cursor 命令相结合的宏来改变TinTin的输入编辑行为。

注意: 您可以使用 #unmacro 命令删除宏。

另可参见: [Alias](#alias), [Cursor](#cursor), [History](#history), [Keypad](#keypad), [Speedwalk](#speedwalk) and [Tab](#tab).

## Map

> 语法: #map {option} {argument}

TinTin++ 有一个功能强大的自动化程序，它使用类似于 Diku MUDs 的房间系统，这意味着奇怪的地图布局和奇怪的出口配置不是一个重大问题。Mapper 提供了改进可视化地图显示的工具。有关基本路径跟踪，请参见路[Path](#path)。

**#map create {size}**

此命令创建初始地图。默认情况下，大小为 50,000，可以使用 #map resize 命令随时更改。如果你玩的是使用 MSDP 或 GMCP 提供房间号码的MUDs，你必须将它增加到报告的最高房间号码。增加地图的大小不会降低性能。

**#map goto {location}**

创建地图时，您不会自动进入地图。默认情况下，创建了房间号 (vnum) 1，因此您可以使用 `#map goto 1` 转到它。一旦您进入地图，当您四处走动时，新房间会使用 pathdir 命令定义移动命令。默认情况下，n, ne, e, se, s, sw, w, nw, u, d被定义。

**#map map {radius} {filename} {a|v}**

要查看地图，您可以使用 #map。然而，必须不断键入 #map 是令人讨厌的。可以使用 #split 显示 vt100 地图。  
要执行:   

> #split 16 1   
#map flag vtmap 

第一个命令将顶部分割线设置为 16，底部分割线设置为 1。如果您想要更小或更大的地图显示，可以使用 10 、 13 、 19 、 22 等, 尽管对于默认显示设置，更改需要是 3 的倍数。

如果你不需要显示对角线出口，更喜欢更紧凑的外观，你可以使用 `#map flag AsciiGraphics off`。这将启用使用 UTF-8 框绘图字符的标准显示，结果可能会因使用的字体而异。

如果你想在不同的终端中显示地图，打开一个新的终端，启动 tt++，然后输入: 
> #port init mapper 4051 

在你的MUDs终端中，输入: 
> #ses mapper localhost 4051 

这将映射程序会话连接到您在另一个终端窗口中初始化的端口。  
接下来，在 MUD 会话中定义以下事件: 

```
#EVENT {MAP ENTER ROOM} {
  #map map 80x24 mapvar v;
  #mapper #line sub {secure;var} #send {$mapvar}
}
```

**#map undo**

如果你不小心走进墙上，mapper会创建一个新的房间。您可以使用 `#map undo` 轻松修复此错误。如果你想在地图上四处移动而不在MUDs上四处移动，你可以使用: #map move {direction}。要手动删除房间，您可以使用: #map delete {direction}。

**#map write {filename}**

您可以使用 #map write 保存地图，加载地图可以使用 #map read。

**#map leave**

您可以使用 #map leave 离开地图，地图仍然存在，但是您的移动命令将不再被跟踪。你可以使用 #map return 返回你离开地图时所在的房间。如果使用 #map read，返回点将设置为保存地图时所在的房间。

**#map set {option} {value}**

可以使用 #map set roomname {name} 设置房间名称。您必须手动执行此操作，或者创建触发器手动设置房间名称。设置房间名称后，您可以使用 #map goto 作为访问房间名称的参数。如果有两个同名的房间，#map goto 会去附近的房间。如果你总是想去同一个房间，你应该记住房间号码。您可以通过提供额外的参数来进一步缩小匹配范围。
```
例如: 
#map goto {武庙} {n;w} {roomarea} {扬州}
```
您可以使用 #map set roomweight {value} 设置房间权重。默认情况下，权重设置为 1.0，表示穿过房间的难度。如果你有一个湖泊作为替代路线，并且穿越水房比普通房间慢 4 倍，那么你可以将湖房的权重设置为 4.0 。如果湖宽 3 个房间，总权重是 12。如果绕着湖泊散步的权重小于 12 ，穿越湖泊权重大于 12 ，mapper将沿着湖走一条路线。
```
来自一位不愿扬名大佬的注释:

tt的map信息本身就记录了周边房间号，
还能设置权重，
通过权重很容易就能实现河两边分两次遍历，
不需要额外的代码。

一个NPC只给一个大概范围，
可能在河这边也可能在对岸，
没有权重控制，简单广度优先的话，
会来来回回的坐船。
渡口到对岸权重999即可。

权重用来计算GPS路径也很有用，
能做马车不坐船，能穿洞不坐车，
不同门派不同需求，
score捕获了信息，自动修改权重即可。
```
可以使用 #map set roomsymbol {value} 设置房间符号。符号应该是可以上色的一、二、三个字符。例如，你可以用 “S” 标记商店，并根据商店的类型对 “S” 进行着色。

**#map run {location} {delay}**

Run 命令将让TinTin找到到给定位置的最短路径，并执行到达那里的移动命令。您可以以浮点精度提供秒为单位的延迟，例如: #map run {dark alley} {0.5}

**#map insert {direction} {flag}**

Insert 命令对于添加名为 void room 的间隔房间很有用。房间经常重叠，通过增加房间空间，你可以延伸出出口。例如: #map insert north void。一旦创建了空房间，你就不能进入空房间，所以你必须在相邻的房间中使用 #map info 来找到房间 vnum, 然后使用 #map goto {vnum} 访问。

也可以隐藏整个区域，直到你输入它，为了做到这一点，你也想设置隐藏标志。例如:#map insert north {void;hide}。

**#map exit {exit}<br>
{COMMAND|DIRECTION|FLAG|GET|NAME|SAVE|SET|VNUM}<br>
{argument}**

默认情况下，退出命令设置为退出名称。如果你想自动打开门，你可以使用以下方式: #map exit {e} {command} {open door;e}。当使用 #map run 时，它将执行 {open door;e} 而不是 {e}。

如果你有一个不寻常的出口，你可以给它一个方向。例如:`#map exit {enter portal} direction {s}`。也接受类似于 #pathdir 提供的数字方向。这允许mapper显示位于门户之外的房间，尽管你必须注意没有通往南方的实际出口。

**#map at {location} {command}**

在给定位置执行命令。如果位置不存在，则不执行命令。如果你想遍历所有 vnums 并访问所有房间来执行某种操作，这将非常有用。

**#map color<br>
{BACKGROUND|EXIT|HERE|PATH|ROOM}<br>
{COLOR CODE}**

设置颜色。要将背景设置为蓝色，您可以使用 #map color background <884>。要将房间颜色设置为暗红色，您可以使用 #map color room <218>。

**#map delete {exit|vnum}**

删除给定出口或房间 vnum 的房间。

**#map dig {exit|vnum} {new|vnum}**

#Map dig {vnum} 将使用给定的 vnum 创建一个新房间，除非已经存在具有该 vnum 的房间。

#Map dig {exit} 将在给定方向创建一个新的出口。如果一个房间占据了这个空间，出口将与那个房间相连，否则将创建一个新的房间。

#Map dig {exit} {new} 将在给定方向创建一个新的出口，将始终创建一个新的房间。

#Map dig {exit} {vnum} 将在给定方向创建一个新的出口，该出口指向具有给定 vnum 的房间。如果这个房间不存在，将创建一个带有这个 vnum 的新房间。

**#map exit {exit}<br>
{COMMAND|DIRECTION|FLAG|GET|NAME|SAVE|SET|VNUM}<br>
{argument}**

#Map exit {exit} {NAME} {argument} 将设置移动命令。如果名称设置为 “and”，并且键入 “and”，这将使您跟随退出。实际执行的移动命令可以用 #map exit {exit} {command} 设置。名称和命令通常是相同的。

#Map exit {exit} {COMMAND} {argument} 将设置发送到服务器的移动命令。例如 {open door;n}

#Map exit {exit} {DIRECTION} {argument} 将设置退出的方向。这可以是与 PATHDIR 命令使用的数字参数相同的数字参数。

#Map exit {exit} {FLAG} {argument}将设置退出标志。这一定是个数字，使用 #map exitflag 设置退出标志更容易。

#Map exit {exit} {GET} {variable} 将退出数据保存到给定变量中。

#Map exit {exit} {SET} {argument} 将退出数据设置为给定的参数。参数可以是表。

#Map exit {exit} {SAVE} {variable} 将退出信息 (commands/direction/flags/name/vnum) 保存到给定变量中。

#Map exit {exit} {VNUM} {argument} 将 exit vnum 设置为给定的参数。这是出口通向的房间的索引号。

**#map exitflag {exit} {HIDE|AVOID} {ON|OFF}**

#Map exitflag {exit} 将显示退出标志的状态。

#Map exitflag {exit} {HIDE} 启用后，此出口之外的房间将不会显示在地图上。用于隐藏重叠区域。

#Map exitflag {exit} {AVOID} 启用时，在搜索到给定描述的路径时，mapper不会使用 exit。

**#map explore {exit}**

mapper将探索给定的出口，直到到达十字路口或死胡同。路径存储在 #path 中，随后可以与 #walk 一起使用。对于走过漫长的道路而不必记住任何目的地特别有用。

**#map find {location} {...}**

mapper会找到位置。路径存储在 #path 中。该位置可以存在多个参数，其中第一个参数应该是房间名称或房间 vnum。

如果你想进一步缩小范围，你可以使用以下键/值对:
```
第二、三个大括号必须匹配
#map find {location} {roomname} {argument} the room's name must match argument.

#map find {location} {roomexits} {argument} the room's exit must match argument, for example {n;e;u}.

#map find {location} {roomdesc} {argument} the room's description must match argument.

#map find {location} {roomarea} {argument} the room's area must match argument.

#map find {location} {roomnote} {argument} the room's note must match argument.

#map find {location} {roomterrain} {argument} the room's terrain must match argument.

#map find {location} {roomflag} {number} the room's flag must match number.
```
例如，可以使用几个键/值对来找到房间:
```
示例: 
#map find {A small clearing} {roomexits} {n;e;s;w} {roomarea} {The holy grove} {roomterrain} {Forest}
```
Goto、link、list、run、delete、at 和 link 命令也可以使用这些搜索选项。delete和dig命令只接受 vnum 。

**#map flag <br>
{ASCIIGRAPHICS|ASCIIVNUMS|NOFOLLOW|STATIC|VTMAP}<br> 
{ON|OFF}**

ASCIIGRAPHICS: 默认情况下启用此标志，并绘制一张有点宽敞的地图，显示 NE SE SW NW 出口、单向出口、上下出口和房间符号。禁用时，它将默认为地图图例，该图例使用紧凑的 UTF-8 框绘图字符来显示和退出。

ASCIIVNUMS: 启用时，ASCIIGRAPHICS 模式将更改为不再显示单向出口和房间符号，而是替换房间 vnum。用于编辑或调试地图。

MUDFONT：这是一种不太受支持的实验显示模式。它需要特殊的字体和 #map legend 的正确配置。

NOFOLLOW: 启用时，当您输入移动命令时，地图不会尝试跟随。使用 #PATHDIR 定义移动命令。对于 MSDP 和 GMCP 自动映射脚本很有用。

STATIC静态: 启用时，当进入未映射方向时，不再自动创建新房间。当你完成地图绘制并经常意外撞到墙壁时，这很有用。

SYMBOLGRAPHICS符号图形: 启用时，ASCIIGRAPHICS 模式被禁用，紧凑地图模式被启用，通过设置房间符号，可以覆盖 UTF-8 的退出图形。显示荒野地图很有用。

VTMAP: 启用时，地图会显示在顶部提示栏中。这需要一个支持 VT100 的终端，并使用 #split。例如: #split 16 1。

**#map goto {location}**

此命令将将您在地图中的位置移动到给定的目标房间。

**#map get {option} {variable}**

此命令允许您将世界和房间信息存储到变量中。
```
选项有: 
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
**#map info**

这将向您展示您当前所在房间的一些世界数据和房间数据。

**#map insert {exit} {roomflags}**

这将在提供的出口插入一个新房间。如果你想同时设置多个房间标志，你必须用半冒号将它们分开。

> 示例: #map insert {e} {void;hide}

**#map jump {x} {y} {z}**

此命令类似于 #map goto，只是您提供了相对于当前所在房间的坐标。

**#map leave**

让你离开地图。当进入一个不可切换的迷宫时很有用。你可以使用 #map return 返回你最后一个已知的房间。

**#map legend**

图例包含对用于显示地图的绘图字符的引用。

紧凑显示模式使用前 16 个字符。它只显示值N E S W exits为n=1 e=2 s=4 w=8。0指数是指没有出口的房间。第一个指数是指有一个出口通向北方的房间。第二个指标是一个房间，有一个出口通向东方。第三个指数是一个出口朝北向东的房间，等等。位于索引 1+4+8=13 的房间，出口通向北、南、西。索引应该是 ASCII 字符的 32 到 254 之间的数字，或者 UTF-8 字符的hex序列。如果 #config 字符集设置为 UTF-8，TinTin++ 将自动用 UTF-8 框绘图字符初始化新创建的地图。

仅部分使用了指数 16 至 31。在紧凑模式下，索引 16 用于当前位置。在 MUDFONT 模式下，当前位置使用索引 17 和 18。

指数 32 95 用于 MUDFONT 显示模式。指数 32 到 63 显示 NW W SW S exits 值为n=1 nw=2 w=4 sw=8 s=16。指数 64 到 95 显示 NE E SE S exits 值为 n=1 ne=2 e=4 se=8 s=16。

默认情况下，MUDFONT 字符映射到从 U+E000 开始的第一个 Unicode 专用区域。在 Windows 上，这将与您可以在下面下载的两个 EUDC (最终用户定义字符) 文件一起使用。

[EUDC.EUF](https://tintin.sourceforge.io/download/EUDC.EUF) and [EUDC.TTE](https://tintin.sourceforge.io/download/EUDC.TTE)

必须使用 7zip 或类似的实用程序将这些文件复制到 C:/Windows/Fonts 目录中。您不能使用 Windows 自带的复制例程复制文件，因为它会尝试安装字体，这不是您想要的。

要修改 EUDC 文件，必须启动私有字符编辑器程序。默认情况下应该安装它。进行更改后，您已经使用文件-> 字体链接-> 所有字体的链接来完成更改。EUDC 文件是a proof of concept。

**#map link {direction} {location} {both}**

此命令将在指向给定位置的给定方向创建单向出口。如果方向是有效的路径目录，您可以提供 {both} 作为第三个参数来创建双向退出。

**#map list {location}**

这个命令列出了所有匹配的房间和它们的距离。您可以使用`#map list {<location>} {variable} {<variablename>}`将列表存储在变量中。

**#map map {<x>x<y>} {filename} {a|v}**

`#Map map {<x>x<y>}` 向屏幕显示具有给定尺寸的地图。

`#Map map {<x>x<y>} {filename}` 将 map 显示写入给定的文件名。

`#Map map {<x>x<y>} {filename} {a}` 将 map 显示写入文件，附加到现有文件中。

`#Map map {<x>x<y>} {variable} {v}` 将地图显示保存到给定变量。

**#map move {exit}**

这与实际移动命令相同，更新地图上的位置并创建新房间。

当你跟踪某人并希望地图跟随时，这很有用。当然，您必须使用 #map move 创建操作才能正常工作。

**#map read {filename}**

将加载给定的文件名。您可以使用 #map goto 进入地图，也可以使用 #map return，它会将您带回保存地图的房间。

**#map resize {size}**

调整地图大小，设置最大房间数。

**#map return**

离开地图或加载地图后，将您返回到最后一个已知的房间。

**#map roomflag {AVOID|HIDE|LEAVE|VOID|STATIC}**

#map roomflag avoid: 设置时，“地图查找” 将避免穿过该房间的路线。避免陷阱和攻击性暴徒很有用。

#map roomflag hide: 设置时，“#map” 将不会在这个房间之外显示地图。当映射重叠的区域或不一致构建的区域时，除非使用空房间，否则您也需要此标志来防止自动链接。

#map roomflag leave: 当你带着这个标志进入房间时，你会自动离开地图。当设置在带有随机出口的迷宫入口处时很有用。

#map roomflag void: 当设置房间时，房间变成了一个间距房间，可以用来连接重叠的区域。一个空房间应该只有两个出口。当你进入一个空房间时，你会被移动到连接房间，直到你进入一个非空房间。要访问空房间，必须使用 #map goto 或 #map jump。

#map roomflag static: 设置时，当四处走动时，房间将不再自动链接。用于绘制迷宫。

**#map run {destination} {delay}**

#Map run {location} 将找到通向给定位置的路径，并执行移动命令来到达那里。延迟是可选的浮点数字，在每个移动命令之间添加延迟。

> 示例: #map run {The dump} {0.25}

**#map set {option} {variable}**

此命令允许您设置房间信息。

```
选项有: 
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
**#map travel {exit} {delay}**

#map travel {exit} {delay}对于穿越长道路很有用。该命令将沿着给定的出口移动，并将继续移动，直到到达死胡同或十字路口。延迟是可选的浮点数字，在每个移动命令之间添加延迟。

> 示例: #map travel e

**#map undo**

将撤消您最后一个重要的地图命令。如果这个命令创建了一个房间或链接，它将被删除。如果这个命令涉及移动，它会将你移回上一个房间。如果你走进一个不存在的方向，那就很有用了。

**#map uninsert {exit}**

这个命令与 #map insert 完全相反。它将删除出口通向的房间，并将出口连接到被删除房间之外的房间。

**#map {vnum} {number}**

将 roomvnum 更改为给定的 vnum。

**#map {vnum} {low} {high}**

将设置roomvnum。低和高是一个数字范围。如果最低数量不可用，则在找到可用的 vnum 之前，vnum 会递增。如果最高号码不可用，命令将失败。

**#map {write} {filename}**

将地图保存到给定的文件名。建议偶尔创建备份，因为很容易混淆 #map write 和 #write。

**#help map**

#Help map 应该为您提供关于可用地图选项的其他信息。输入部分命令可能会为您提供有用的语法建议或概述，请记住这一点。

另可参见: [Path](#path) and [Pathdir](#pathdir).

## Math

> 语法: #math {variable} {mathematical expression}

有关可以使用的运算符列表，请参见数学手册条目[mathematics](#mathematics)。

math允许您执行数学计算，并将结果存储在给定变量中。它还允许字符串和 regexp 比较。

> 示例: #math sumvar {(1 + 1) * 10}

这个基本操作将在 sumvar 中存储结果 (20)。

如果计算包含浮点数字，结果将以与精度最高的参数相同的精度存储为浮点数字。

> 示例: #math var {1.0 / 4}

将结果 (即 0.2) 存储在 var 中。使用 1.00/4 将存储 0.25。

> 示例: #math var 2d6

D 代表骰子，2d6 相当于投掷两个 6 面骰子。如果你需要 1 到 100 之间的随机数，你可以使用 1d100。如果你需要 0 到 9 之间的随机数，你可以使用 1d10-1。

```
来自xgg@pkuxkx的注释：

骰子只能从1开始，
所以当范围不是从1开始时，需要对数值进行差值运算。

示例：
#function {rnd} {#math {result} {1 d (%2 - %1 + 1) + %1 - 1}}

#showme 从100-200范围抽取随机数: @rnd{100;200}
```

示例: 其他运算符的行为或多或少与预期的相同。

另可参见: [Format](#format), [Function](#function), [Local](#local), [Replace](#replace), [Script](#script) and [Variable](#variable).

## Mathematics

数学表达式用于计算和boolean if 检查。TinTin++ 支持全套 C 操作和一些额外的操作。以下是用于数值运算的运算符的优先级列表。

运算符	|优先级	|描述
:-  |:-    |:-
\!  |00|逻辑非
\!	  |00|按位非
\*	  |01|整数乘
\** |01|整数幂
\/	  |01|整数除以
\//	 |01|整数开平方根or立方根
\%	  |01|整数模
d	   |01|整数掷骰子随机
\+	  |02|整数加法
\-	  |02|整数减法
\>> 	|03|右移位
\<< |03|	左移位
\>	  |04|逻辑大于
\>= |04|逻辑大于等于
\<	  |04|逻辑小于
\<=  |04|逻辑小于等于
\==	 |05|逻辑等值
\!=	 |05|逻辑非等值
\&  	|06|按位与
\^	  |07	|按位异或
\|	  |08	|按位或
\&&  |	9	|逻辑与
\^^	  |10	|逻辑异或
\|\|	 |11|逻辑或

使用括号可以忽略运算符优先级，例如 `(1+1)*2` 等于 4，而 `1+1*2` 等于 3。

这些运算符中的一些也可以用于字符串。字符串必须用双引号括起来。

运算符	|优先级	|描述
:-  |:-    |:-
\>  |04|字母顺序大于
\>= |04|字母顺序大于等于
\<	  |04|字母顺序小于
\<=	 |04|字母顺序小于等于
\== |05|正则等值
\!= |05	|正则非等值

运算符`> >= < <=`执行基本的字符串比较。`==!=` 运算符执行正则表达式，左边的参数是字符串，右边的参数是正则表达式。例如，`“bla”==“%*a”` 将评估为 1 (true)。

另可参见: [Colors](#colors), [Escape Codes](#escape-codes) and [Regular Expressions](#regular-expressions).

## Message

> 语法: #message {listname} {argument}

没有参数消息将显示您可以切换的列表。如果没有给出参数，它将切换指定的列表标志。您可以使用 ON 或 OFF 作为参数更具体地更改消息标志。

> 示例: #message variable off

一旦执行的变量被创建或删除，它们将不再创建消息。请记住，只有在手动输入命令或以详细方式执行命令时，才会显示消息。

#Config {verbose} {on} 将导致在读取显示 #read 的脚本文件时生成消息。

#Line {verbose} {argument} 将导致参数在 verbose 模式下执行，显示所有消息。

#Line {quiet} {argument} 将导致在 quiet 模式下执行参数，不会显示任何消息。

另可参见: [Class](#class), [Debug](#debug), [Ignore](#ignore), [Info](#info) and [Kill](#kill).

## Metric System

名称|符号|因数
:-|:-|:-
百万|M|1000000
千|K|1000
毫|m|0.001
微|u|0.000 001

另可参见：[Echo](#echo),[Format](#format) and [Math](#math).

## MSDP

MSDP 是 #port 功能的一部分。请参阅 `#help event` 附加文档，因为所有 MSDP 事件都可以作为常规事件。

可以使用[ MSDP 协议 ](https://tintin.sourceforge.io/protocols/msdp) 查询可用的 MSDP 事件，如文档中所述。

另可参见：[Event](#event),[Port](#port).

## MSLP

TinTin++ 支持MSLP（Mud服务器链接协议)。请参阅 `#help event` 附加文档，因为所有 MSLP 事件都可以作为常规事件使用。

可以使用[ MSLP 协议 ](https://tintin.mudhalla.net/protocols/mslp) 查询可用的 MSLP 事件，如文档中所述。


另可参见：[Event](#event),[Port](#port).

## Nop

> 语法: #nop

这个命令 “nop” 意味着 “no operation”，如果你不想做一件事，它会很有用。

> 示例: #act {&} {#nop} {0}

一些 MUDs 允许你使用 “&” 来分离命令，同时仍然允许玩家在 “say” 或 “tll” 中使用它。这将允许一些狡猾的玩家在没有这种保护的情况下滥用你的触发器。因此，如果消息包含 “&” 字符，则不会触发易受攻击的操作，因为一次只允许触发 1 个操作。

在脚本中留下注释也可以使用 #nop。

> 示例: #nop {这是一条注释。}

## Parse

> 语法: #parse {string} {variable} {commands}

Parse 命令就像一个简化的循环。TinTin将遍历访问每个字符的给定字符串，该字符串将存储在给定变量中，可以在命令部分使用。
```
示例: 
#parse {hello} {character} {say $character!}
这等于：
say h!;say e!;say l!;say l!;say o!
```
虽然通常使用有限，但是parse可以用于一些实用的东西，比如使用 . 作为快速行走捷径。

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
另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Repeat](#repeat), [Return](#return) and [While](#while).

## Path

> 语法:   
#path {del|end|ins|load|map|new|save|run|walk} {argument}


Path 命令是一种快速简单的方法，可以记录您的移动，并创建一个命令列表，以便从一个位置移动到另一个位置并返回。要获得更高级的映射程序，请查看 [#map](#map) 命令。

**#path {new}**

此命令启动路径跟踪模式。如果输入移动命令 (用 #pathdir 列出)，它将被添加到路径中。

**#path {end}**

使用 #path new 启动路径跟踪后，您可以使用 #path end 停止。这不会删除创建的路径，尽管再次键入 #path new 会。

**#path {map}**

此命令显示到目前为止创建的路径，它显示命令列表，而不是图形地图。

**#path {ins} {forward command} {backward command}**

有时当你从这里走到那里时，你需要打开门，使用这个选项，你可以将命令插入你正在创建的路径中。当创建从 A 到 B 的路径时，也会自动创建从 B 到 A 的向后路径。因此，第二个参数是为向后路径插入的命令。
```
示例: 
#path ins {open north} {};n;
#path ins {} {open south}
```
**#path {del}**

移除路径中的最后一个移动。<br>
这在撞墙时十分有用。
```
示例: 
#act {这个方向没有出路} {#path del}
```
**#path {save} {forward|backward} {variable}**

此命令将创建的路径保存到提供的变量中，您必须指定是向前还是向后保存路径。你可以用 f 和 b。如果使用: #path save f AtoB，您可以使用: $AtoB 执行保存的路径。
```
示例: 
#path new;n;n;n;e;e;e;
#path save backward return;
$return
```
**#path {load} {variable}**

此命令将加载任何给定的变量作为路径，并且不需要与移动相关。

**#path {run} {delay}**

要使此命令工作，您必须创建或加载了路径。执行时，路径中的所有命令都会被删除并立即执行，除非您提供可选的延迟参数，以延迟给定浮点秒数的每个命令之间的执行。

> 示例: #path run 0.5

**#path {walk} {forward|backward}**

要使此命令工作，您必须创建或加载了路径。执行时，路径队列中的下一个命令将被删除并执行。如果到达路径的末尾，这将触发路径事件的末尾。
```
示例: 
#tick {slowwalk} {#walk f} {0.5};
#event {END OF PATH} {#untick slowwalk}
```
另可参见: [Map](#map) and [Pathdir](#pathdir).

## Pathdir

> 语法: #pathdir {forward direction} {backward direction} {coord}

默认情况下，TinTin设置了最常用的移动命令，这意味着你通常不必费心处理路径。#Path 和 #map 命令使用路径。

第一个参数是方向，第二个参数是相反的方向。north的反方向是south等。

第三个参数是空间坐标。一般来说，每个基数方向都应该有一个唯一的值，该值是 (例如 1 、 2 、 4 、 8 、 16 、 32 、 64 等) 2的幂。复合方向除外，复合方向的值应为每个组件方向的值之和。例如，如果 “n”值是 1，而 “e” 是 2，那么你 “ne” 的值是 3 (1+2)。#Map 功能工作需要此值。

```
来自xgg@pkuxk的说明：
自定义命令只能是1-63之间的值。
比如enter，out。
```
> 示例: #pathdir {ue} {dw} {18}

在上面的例子中，18 是 16(u) 和 2(e) 的总和。当你键入 ue 时，一旦设置，映射程序就知道你在向上和向东移动。请记住，您还必须设置映射程序的反向 {dw} {ue} {40} 路径才能正常工作。

注意: 您可以使用 #unpathdir 命令删除路径。如果你的MUDs没有使用 ne se sw nw存在 (默认设置)，你可以使用 #unpath ne se sw nw 来移除它们。

另可参见: [Map](#map) and [Path](#path).

## Port

> 语法: #port {command} {argument}

#Port 命令用于创建与其他 mud 客户端 (包括您自己的客户端) 的对等连接，通常用于更新状态窗口。如果你想让别人从另一台机器上连接，你必须交换 ip地址和端口号。您可以使用 #session 命令连接到端口。

**#port {init} {name} {port} {file}**

#port init 启动您的端口。文件参数是可选的。该命令创建具有给定名称的新会话，该会话接受给定端口的传入套接字连接。

**#port {call} {address} {port}**

创建低级远程套接字连接。

**#port {color} {color names}**

设置端口消息的颜色，必须是有效的颜色名称或颜色代码。

**#port {dnd}**

切换请勿打扰模式，拒绝新的socket连接。

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

关闭socket连接。


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
```
此示例将事件设置为仅允许从本地主机连接的 IPs。

```
示例:
#nop Launch tt++ in a new terminal and execute:

#port init commwindow 4052
#port prefix {}

#nop In your mud session running in a different terminal execute:

#gts #ses comms localhost 4052
#act {~%* chats '%*'} {#comms #send {%0}}
#showme <128>Bubba chats 'Testing if this works'
```
此示例设置显示聊天的通信窗口。创建新会话时，它将成为活动会话，通过使用 #gts (启动会话)，活动会话在执行命令后返回到原始会话。

如果上述解释没有生效，以下可能是: 您有一个名为 “mud” 的会话，该会话执行 #gts {argument}。因为 #gts 是一个未知的命令 ，TinTin检查 “gts” 是否是会话名称，因为这是它暂时启动 gts 并执行参数的情况, 执行参数后，TinTin重新启动调用会话，在这种情况下，会话名为 “mud”。

另可参见: [All](#all), [Run](#run), [Session](#session), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

## Prompt

> 语法: #prompt {message} {newmessage} {row}

此命令的工作方式与替代命令substitute非常相似，仅在拆分模式#split下工作。如果没有给出行号，它将替换 mud 消息并将其放在拆分行中。

可选参数row允许提示自定义拆分屏幕。正数将写入提示 #rows up 从屏幕底部。负数将写下提示 #rows down 从屏幕顶部。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。

> 示例: #prompt {[%1/%2hp]} {[<078>%1/%2hp]}

这将在状态行中打印匹配的行，将颜色设置为暗淡的白色。脚本部分提供了一个更高级的示例。

注意: 您可以使用 #unprompt 命令删除提示。

另可参见: [Action](#action), [Gag](#gag), [Highlight](#highlight) and [Substitute](#substitude).

## Read

> 语法: #read {filename}

此命令将在命令文件中读取。

> 示例: #read autolevel.tin

这将在你制作的文件中读取，其中包含 aliasses 、 action 、 tickers 等，以参与一些淘气的自动升级。

TinTin++ 将命令字符设置为命令文件中找到的第一个字符，默认情况下命令字符设置为 “#”。

如果您想在读取文件时看到更多信息，请使用: #config {verbose} {on}。

请记住，文件中使用的每个开口大括号 {必须与闭合大括号} 相匹配。如果不这样做，您将收到错误消息，并且文件不会加载。

另可参见: [Log](#log), [Scan](#scan), [Textin](#textin) and [Write](#write).

## Regex

> 语法: #regex {string} {expression} {true} {false}

#Regex 命令 (正则表达式的缩写) 用于将给定字符串与给定正则表达式进行比较。变量存储在 &1 到 &99 中，&0 保存整个匹配的子字符串。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。

以下(懒惰)匹配项在 %1-%99 + 1 处可用：

参数|说明
:-|:-
%a|匹配零到任意数量的除换行符以外的字符
%A|匹配零到任意数量的换行符
%d|匹配零到任意数量的数字
%D|匹配零到任意数量的非数字
%p|匹配零到任意数量的可打印字符
%P|匹配零到任意数量的不可打印字符
%s|匹配零到任意数量的空格
%S|匹配零到任意数量的非空格
%u|匹配零到任意数量的unicode字符
%U|匹配零到任意数量的非unicode字符
%w|匹配零到任意数量的字母
%W|匹配零到任意数量的非字母
%+|匹配一到任意数量的字符
%?|匹配零到一个字符
%.|匹配一个字符
%*|匹配零到任意数量的字符
%i|匹配时不区分大小写
%I|匹配时区分大小写(默认)

如果要匹配 1 个数字，请使用 %+1d，如果要匹配 3-5 个空格使用 %+3..5s，如果你想在 0-1 个字母之间匹配使用 %+0..1w。

匹配项将自动存储到 %1 和 %99 之间的值。从 %1 开始，每个正则表达式递增 1。

如果您使用 %15 作为正则表达式，下一个未编号的正则表达式将是 %16。

要防止存储匹配项，请使用 %!*、%!w 等。

```
示例: 
#regex {Hello World} {%* World}
{#showme Matched &1 World}
{#showme no match}

示例: 
#regexp {bli bla blo} {bli {.*} blo} {#showme &1}
```  
```
来自xgg@pkuxkx的示例：

在北侠中抓取闲聊频道id时，
#act {^【闲聊】%*(%1 ||} {
  #var lastid %2
};
正常用了一段时间后发现会被表情污染：
【闲聊】...(@_@)。(xgg || pure dzp)
此时变量抓取错误，
$lastid = {@_@)。(xgg}

指定匹配类型字母即可解决冲突。
#act {^【闲聊】%*(%w ||} {
  #var lastid %2
};
```  

另可参见: [Case](#case), [Default](#default), [Else](#else), [Elseif](#elseif), [If](#if) and [Switch](#switch).

## Regular Expressions

Regular Expressions、Regex或Regexp是定义搜索模式的字符序列。自从 1980 以后，就有了编写正则表达式的不同语法，其中使用最广泛的是 POSIX 语法和类似但更高级的 Perl 标准。TinTin++ 支持被称为 PCRE (Perl 兼容正则表达式) 的 Perl 标准。

正则表达式是TinTin++ 的一个组成部分，但是请记住，TinTin不允许直接使用正则表达式, 相反，它使用更简单的中间语法，当需要时，它仍然允许更复杂的表达式。

以下命令利用正则表达式: action, alias, elseif, gag, grep, highlight, if, kill, local, math, prompt, regexp, replace, substitute, switch, variable, and while。其他几个命令以次要的方式使用正则表达式。幸运的是，基础知识非常容易学习。

**TinTin++ Regular Expression**

正则表达式有以下支持。
```
^ 匹配行首。
$ 匹配行尾。
\ 转义字符。

%1-%99 匹配任意文本并保存在相应索引中。
%0 匹配所有文本。
{ } 嵌入与 perl 兼容的正则表达式，存储匹配项。
%!{ } 嵌入 perc 兼容的正则表达式，不存储匹配项。
[ ] . + | ( ) ? *等符号除非在大括号内使用，否则被视为普通文本。请记住，除非使用 %!{}，否则 {} 会自动替换为 ()。
```

tt++|	描述 |POSIX
:- |:- |:-
\%d	|将匹配零到任意量的数字|([0-9]*?)
\%D	|将匹配零到任意数量的非数字|([^0-9]*?)
\%i	|匹配不区分大小写|	(?i)
\%I	|匹配区分大小写(默认)|(?-i)
\%s |将匹配零到任意数量的空格|	([\r\n\t ]*?)
\%S	 |将匹配零到任意数量的非空格|	([^\r\n\t ]*?)
\%w |	将匹配零到任意数量的单词字符|([A-Za-z0-9_]*?)
\%W |	将匹配零到任意数量的非单词字符|([^A-Za-z0-9_]*?)
\%?	|匹配 0 个或 1 个字符|(.??)
\%.	|匹配一个字符|	(.)
\%+	|将匹配一个到与任意数量的字符|(.+?)
\%*	|将匹配零到任意数量的字符|(.*?)

**Variables**

如果在操作中使用 %1 执行匹配，则匹配的字符串存储在 %1 变量中，该变量可用于操作正文。

> 示例: %1 says 'Tickle me'} {tickle %1}

如果使用 %2，则匹配存储在 %2 中，以此类推。如果使用未编号的匹配，如 %* 或  %S，该索引则匹配存储在最后使用的索引处。

> 示例: %3 says '%*'} {#if {"%4" == "Tickle me"} {tickle %3}}

最大变量索引为 99。如果以 %* 开始操作，匹配将存储在 %1 中。当在操作正文中使用时，永远不应该在操作的触发部分使用 %0，%0 包含匹配的字符串的所有部分。

要防止存储匹配项，请使用 %!* 、 %!w 等。

**Perl Compatible Regular Expressions**

您可以使用大括号 {} 嵌入 PCRE (Perl 兼容正则表达式)，除非使用 %!{}，否则这些大括号将被() 替换。

**Or**

您可以使用 | 字符在 PCRE 中分离替代方案。
```
示例: 
#act {%* scratches {his|her|its} butt.} {
  mutter Someone should wash %2 hands..
}
```
**Brackets**

您可以使用括号对 PCRE 中的替代方案和范围进行分组。
```
示例: 
#act {%* says 'Who is number {[1-9]}} {
   say $number[%2] is number %2
}
```
只有当有人提供 1 到 9 之间的数字时，该示例才会触发。任何其他字符都会导致操作不触发。
```
示例: 
#act {%* says 'Set password to {[^0-9]*}$} {
 say The password must contain at least one number, not for security reasons, but just to annoy you.
} {4}
```
当 ^ 字符在括号内使用时，它会创建反向搜索，除了 0 到 9 之间的数字之外，[^0-9] 匹配每个字符。

**Quantification**

匹配后放置的限定符指定允许匹配发生的频率。

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

TinTin 正则表达式在 PCRE 中自动添加括号，例如 %* 翻译为 (.*？)。PCRE 中的副命题导致执行优先级发生类似于数学表达式的变化，但副命题也导致匹配存储到变量中。

当嵌套多个副命题集时，每个嵌套都按照外观顺序分配自己的数值变量。

> 示例: #act {%* chats '{Mu(ha)+}'} {chat %2ha!}

如果有人说Muha，你会说Muhaha，如果有人说Muhaha，你会说Muhahaha。

**Lazy vs Greedy**

默认的正则表达式匹配是贪婪的，这意味着 {.*} 将捕获尽可能多的文本。
```
示例: 
#regex {bli bla blo} {^{.*} {.*}$} {#showme Arg1=(&1) Arg2=(&2)}
这将显示:Arg1=(bli bla) Arg2=(blo)。

示例: 
#regex {bli bla blo} {^{.*?} {.*?}$} {#showme Arg1=(&1) Arg2=(&2)}
这将显示:Arg1=(bli) Arg2=(bla blo)。
```
**Escape Codes**

PCRE 支持以下转义代码。

PCRE	|描述	|POSIX
:-|:-|:-
\\A	|匹配行首|^	
\\b	|匹配单词边界|(^|\r|\n|\t| |$)	
\\B|	匹配非单词边界|[^\r\n\t ]	
\\c|插入控制字符|	\c	
\\d	|匹配数字|	[0-9]	
\\D|	匹配非数字|	[^0-9]	
\\e	|插入转义字符|\e	
\\f	|插入表单输入字符|\f	
\\n	|插入表单换行字符|	\n	
\\r|插入回车字符	|	\r	
\\s|匹配空格	|	[\r\n\t ]	
\\S	|匹配非空格	|[^\r\n\t ]	
\\t	|插入 tab 字符|\t	
\\w|	匹配字母、数字和下划线|	[A-Za-z0-9_]	
\\W	|匹配非字母、数字和下划线|[^A-Za-z0-9_]	
\\x	|插入十六进制字符|\x	
\\Z|	匹配字符串结束|$

`\s` 匹配一个空格，`\s+` 匹配一个或多个空格。

**Color triggers**

使文本触发器更容易匹配，(Actions, Gags, Highlights, Prompts, and Substitutes)的颜色代码会被删除。如果要创建颜色触发器，必须使用 ~(tilda) 启动触发器。使用 #config {convert meta} on 使转义代码可见。
```
示例: 
#action {~\e[1;37m%1} {#var roomname %1}
```
如果房间名称是亮白色MUDs上唯一的一行，这个颜色触发器将保存房间名称。

***

这涵盖了基础知识。PCRE 有更多的选择，其中大部分有点模糊，所以你必须阅读 PCRE 手册才能获得更多信息。

另可参见: [Colors](#colors), [Escape Codes](#escape-codes) and [Mathematics](#mathematics).

## Repeat

> 语法: #[number] {commands}

有时您希望多次重复相同的命令。这是实现这一目标的最简单方法。

> 示例: #10 buy bread

这将使你执行 “买面包” 10 次。

另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Return](#return) and [While](#while).

## Replace

> 语法: #replace {variable} {oldtext} {newtext}

此命令将在 oldtext 中搜索给定字符串的变量，并将其替换为 newtext 中给出的字符串。

如果将 newtext 留空，则将删除旧文本匹配。

```
示例: 
#var {test} {bli bla blo};
#replace {test} {bl} {tr}
```
这将变量测试从 “bli bla blo” 更改为 “tri tra tro”。

请记住，旧文本已经替换了转义代码 (而新文本没有)，所以如果你想替换一个 “\” 字符，你需要输入 “\\\”

另可参见: [Format](#format), [Function](#function), [Local](#local), [Math](#math), [Script](#script) and [Variable](#variable).

## Return

> 语法: #return {text}

可以使用 return 命令从正在执行的触发器中断开。

在 #function 函数中，您可以使用 #return 和参数来断开函数并设置结果变量。

另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat) and [While](#while).

## Run

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

## Scan

> 语法: #scan {abort|read}

Scan 命令读取文件名并将其发送到屏幕上，就好像它是MUDs输出一样。这对于将 ansi 文件转换为 html 和读取日志文件非常有用。

包括接收到的行事件在内的操作和其他触发器将在每一行触发，并且可以通过发出: #scan abort 来中止扫描。

另可参见: [Log](#log), [Read](#read), [Scan](#scan), [Textin](#textin) and [Write](#write).

## Screen

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

## Screen Reader

> 语法：#config {SCREEN READER} {ON|OFF}

屏幕阅读器模式通过使用 `#config screen on` 启用。屏幕阅读器模式的主要目的是向服务器报告屏幕阅读器正在使用 [MTTS 标准](http://tintin.sourceforge.net/protocols/mtts)。  

启用屏幕阅读器模式后，TinTin++ 将尝试删除可能可视的元素。

另可参见：[Config](#config).

## Script

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

## Send

> 语法: #send {text}

直接将文本发送到 MUD，如果你想从 escape 代码开始，这很有用。

#Send 将自动附加换行府，您可以用 \ 结束换行，以防止这种情况发生。

另可参见：[Textin](#textin).

## Session

> 语法: #session {name} {address} {port} {file}

将以给定的名称开始会话，连接到指定的地址和端口，加载可选文件。
```
示例: 
#ses pku mud.pkuxkx.com 8080
```
当然，如果你真的想去某个地方，你必须填写其他东西。Mud 连接器提供了大量可搜索的 muds 列表。

其他选项是 #session + 和 - 转到下一个或上一个会话。只有当你正在多次播放时，这才有效。`#session <number>` 激活对应于给定号码的 session。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

## Session name

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

## Showme

> 语法: #showme {message} {line number}

Showme 命令显示的消息可以被触发，并且可以用于调试操作、替换等。由于变量也被替换，这也可以用于显示信息。

> 示例: #showme $bla

如果定义了变量 “bla”，这将显示 bla 设置为的任何内容。

行号是可选的，工作方式与 [#prompt](#prompt) 命令中的行号相同。

另可参见: [Buffer](#buffer), [Echo](#echo) and [Grep](#grep).

## Snoop

> 语法: #snoop {sessionname}

此命令将切换会话的 snoop 状态。即使会话在后台，窥探会话也会显示其服务器输出。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session](#session), [Session Name](#session-name), [SSL](#ssl) and [Zap](#zap).

## Speedwalk

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

## Split

> 语法: #split

这将分割屏幕，导致屏幕的顶部接收MUDs输出，底部接收键盘输入。这允许您在不影响提示的情况下输入MUDs文本。

> 语法: #split {bottom row} {top row}

这是分割命令的更高级用法，允许您更精确地定义分割屏幕的MUDs输出部分。

如果您拆分屏幕，建议使用提示命令捕获提示并将其放在拆分行上，否则将在最后一个提示上打印新的MUDs输出。

如果您使用的是 #map 命令，您可以通过使用: #map flag vtmap 在顶部分割部分显示自动地图。
```
示例: 
#map create;
#map goto 1;
#split 16 1;
#map flag vtmap;
#parse eewssdeeeunnweewssdeeeunwesnewnssdeeeunnsewsnwesdwwwunw tmp #map move $tmp
```
注意: 您可以使用 #unsplit 命令删除拆分屏幕。

## SSL

> 语法: #ssl {name} {address} {port} {file}

将以给定的名称开始会话，连接到指定的地址和端口，加载可选的文件名。

> 示例: 
#ssl pku mud.pkuxkx.com 8080

除了将 ssl (安全套接字层) 添加到会话之外，#SSL 命令类似于 #session。为了 SSL 工作，需要安装 GnuTLS。


另可参见: [All](#all), [Port](#port), [Run](#run), [Session Name](#session-name), [Snoop](#snoop), [SSL](#ssl) and [Zap](#zap).

## Statements

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

## Substitute

> 语法: #substitute {message} {newmessage} {priority}

#Substitute 命令允许您更改MUDs输出。%1-99 变量从消息中被替换，可以在替换的新消息部分使用。消息部分不应使用 %0 变量。优先级部分是可选的，并确定替代部分的优先级，默认为 5。

有关模式匹配的信息，请参见正则表达式[Regular Expressions'](#regular-expressions)一节。

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

## Suspend

> 语法: #suspend

这将在后台放置TinTin++，您将返回到 shell。按 ctrl-z 会做同样的事情。你可以通过键入 fg 来返回TinTin++。

## Switch

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

## System

> 语法: #system {commands}

系统命令允许您在 shell 中执行命令。

> 示例: #system ls

如果你忘记了你想阅读的文件的确切名称或顺序，这很有用。

注意: 您也可以使用 #script 和 #run 命令来执行 shell 命令。

另可参见: [Script](#script) and [Run](#run).

## Tab

> 语法: #tab {completionword}

Tab 命令将完成 word 添加到选项卡完成列表中。按下 “tab” 键时，TinTin将在您的 tab 列表中搜索最佳匹配。对于长命令很有用。

如果您在没有定义标签的情况下单击标签，tintin 将使用 scrollback buffer 查找匹配项。

> 示例: #tab muhahaha

键入 mu，然后按 tab，会出现这个邪恶的命令。

注意: 您可以使用 “untab” 命令删除标签。

另可参见: [Alias](#alias), [Cursor](#curse), [History](#history), [Keypad](#keypad), [Macro](#macro) and [Speedwalk](#speedwalk).

## Textin

> 语法: #textin {filename} {delay}

这将在文件中读取，并将每一行发送到MUDs。Tintin 不会解析文本。将脚本文件转储到 mud 的注释编辑器或类似的命令中很有用。请记住，如果您一次发送太多数据，大多数 muds 都会关闭您的连接。使用可选的延迟参数在每个命令之间添加一个小延迟。

> 示例: #textin desc1.txt 0.2

会在 olc 编辑器中加载 desc1 的数据。

另可参见: [Log](#log), [Read](#read), [Scan](#scan) and [Write](#write).

## Ticker

> 语法: #ticker {name} {commands} {interval}

名称部分可以是任何你想要的，取消只需要 unticker 命令。每隔 x 秒执行一次命令，这在间隔部分中指定。

> 示例: #ticker {autosave} {save} {300}

这将使 TinTin 每 300 秒执行一次save命令。

注意: 您可以使用 #untic 命令删除定时器。

另可参见: [Delay](#delay) and [Event](#event).

## Time

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
%H|2位数字 24 小时制。(00...23)
%I|2位数字 12 小时制。(01...12)
%j|一年中的 3 位数数字日 (001...366)
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

另可参见：[Echo](#echo),[Event](#event) and [Format](#format).

## Variable

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

注意: 您可以使用 #unvariable 命令删除变量。

另可参见: [Format](#format), [Function](#function), [Local](#local), [Math](#math), [List](#list), [Replace](#replace) and [Script](#script).

## While

> 语法: #while {variable} {commands}

While 命令的工作方式类似于 c 中的 while 命令。一旦条件等于 0，while 循环将停止。

```
示例:
#list var create a b c d
#while {\&var[]} {#showme $var[+1];#unvar var[+1]}
```
另可参见: [Break](#break), [Continue](#continue), [Foreach](#foreach), [List](#list), [Loop](#loop), [Parse](#parse), [Repeat](#repeat) and [Return](#return).

## Wildcards

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
另可参见: [Regular Expressions](#regular-expressions).

## Write

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

## Zap

> 语法: #zap {session}

如果没有参数，这将关闭当前活动会话。如果没有活动会话，它将关闭 TinTin++。如果提供会话名称，它将关闭给定的会话。

另可参见: [All](#all), [Port](#port), [Run](#run), [Session](#session), [Session Name](#session-name), [Snoop](#snoop) and [SSL](#ssl).

# 关于
***
**文档来自[TinTin++官网](https://tintin.sourceforge.io/)**<br>

**翻译者：xgg@pkuxkx**<br>
**贡献者：dzp@pkuxkx**<br>

**继续阅读:[ 返回导航 ](#导航)**
***