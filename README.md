# START

|[TinTin++](https://tintin.sourceforge.io/)
|[Termux](https://github.com/termux/termux-app)|  
|[TinTin++ • Github](https://github.com/scandum/tintin)
|[TinTin++中文手册](./Wiki.md)|  
|[北侠官网](http://pkuxkx.net/)
|[北侠Wiki](http://pkuxkx.net/wiki/)
|[北侠论坛](http://pkuxkx.net/forum/)
|[紫溪涧](http://zixijian.github.io)|

### 这里是做什么的？

本仓库用于存储 xgg@pkuxkx 的游戏配置，  
以及部分 TinTin++ 相关脚本和文档。

北大侠客行是一个 MUDs 文字游戏，  
Termux 是一个安卓系统上的终端模拟器，  
TinTin++ 是一个跨平台的 MUDs 客户端。  
支持：  
macOS,iOS,Android,Linux,Windows。  

北大侠客行可使用 TinTin++ 客户端连接，  
TinTin++ 可以运行在 Termux 上。

So：TinTin++ on Termux for pkuxkx。

__注：客户端用法与其他平台一致。__

### 安卓怎么进入MUDs游戏？

- 1.安装 Termux

style插件非必选，可配置字体和主题风格。  
api插件可以帮助使用安卓硬件等资源。

- 2.在 Termux 中安装必须软件及配置

Termux需要安装 MUDs 客户端，如：TinTin++ 、Go-Mud ，
环境配置可以帮助提升游戏体验(解决乱码和快速进入游戏)。

- 3.配置文件管理

对于没有图形界面的客户端，机器人脚本相当重要，初期建议先使用 xgg@pkuxkx 的机器人熟悉一下。

- 4.启动游戏客户端

这时候启动客户端进入游戏即可。

注：其他平台安装使用可访问[官网](https://tintin.mudhalla.net/install.php)。

***
请细致地阅读文中内容，  
请合理地使用搜索引擎，  
请合理地联想相同的方法和规律，  
有些内容不会在文中重复出现。
***

## 0。Termux

### Termux 简介

> 安卓系统高级终端模拟器。  
 使用 bash 和 zsh。  
 使用 nano 和 vim 编辑文件。  
 通过 ssh 访问服务器。  
 使用 gcc 和 clang 编译代码。  
 使用 python 控制台来作为掌上电脑。  
 使用 git 和 subversion 管理项目。  
 使用 frotz 运行基于文本的游戏。  
 双指捏合缩放界面。  
 长按弹出菜单。  
 PGDW PGUP 上下翻页。
 
### 下载安装 Termux

- 应用商店内搜索安装

- 访问[【Termux】](https://github.com/termux/termux-app)获取

### 一键初始化 Termux 环境

复制并执行下列命令：
```
bash <(curl -s -L https://raw.fastgit.org/zixijian/shell/master/shell/tt4t.sh)
```
然后将逍遥行等插件脚本放入内存卡（内部存储）根目录 tintin 文件夹即可开始游戏。  

注意：以下步骤可以不用做了，qaq 。

### 安装vim git screen tintin++

打开Termux输入如下指令安装「必须」软件：
> pkg up -y  
pkg install vim git screen tintin++ -y

__按行复制命令后按回车执行！！！__

__安装完毕后，可跳转到screen转码部分。__ 

--- 

注：Linuxdeploy 是一款能在安卓手机上利用 chroot 命令部署任意 linux 发行版的 app（需要 root 权限、比 Termux 更强大）。  
使用 Linuxdeploy 在手机上部署的 Debian 系统安装 `tintin++` 的路径在 `/usr/games/tt++`。

由于 Debian 上 tintin++ 版本比较老，    
也可以使用源码进行编译安装。

TinTin++ 可在 [【Github】](https://github.com/scandum/tintin) 获取源码。


Termux不用看下段内容。

```
Debian9编译安装tt++

1.安装编译环境
apt install gcc libgnutls-dev zlib1g-dev libpcre3-dev make cmake git -y
2.克隆源码到本地
git clone https://github.com/scandum/tintin.git tt
3.编译
cd tt/src/
./configure
make
4.复制可执行文件到/bin目录
cp tt++ /bin
```
Termux一般不用编译，仅列出方法。

```
Termux编译安装tt++

1.安装环境
pkg install git make cmake libgnutls zlib pcre wget -y
2.获取代码
git clone https://github.com/scandum/tintin.git tt
3.进行编译并拷贝二进制文件到bin目录
cd tt/src/
./configure
make
cp tt++ /data/data/com.termux/files/usr/bin/
或
cp tt++ $PREFIX/bin/
```


## 1。Termux相关

__此步骤非必要__

自定义工具条 Termux 版本号需大于 0.66，

使用 style 样式插件则签名必须一致，

建议使用 apk编辑器 签名后安装。

__工具条配置编辑方法如下__

使用vim文本编辑器编辑：

> mkdir ~/.termux<br>
vim ~/.termux/termux.properties

按字母 `i` 键开启插入模式，方向键控制光标：

```
extra-keys = [['ESC','+','-','HOME','UP','END','PGUP'],['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN']]
```
将以上内容复制粘贴到文本中，  
修改完毕后按 ESC 键退出编辑模式：

- 输入 `:wq` 保存
- 或大写模式按两下 ZZ 键

退出程序再进即可生效。

注：根据[官网](https://tintin.sourceforge.io/android.php)介绍，Termux 可以使用组合宏键。

__可根据需求对工具条进行定制__

以下是 xgg@pkuxkx 使用的工具条：

```
extra-keys = [['ESC','|','BACKSLASH','HOME','UP','END','PGUP','chat '],['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN','KEYBOARD']]
```

__个性化设置__

> vim ~/.bashrc

Termux 中可将常用命令设置别名，  
开启新窗口配置立即生效。   
善用别名可大幅简化操作。

```
export PS1='[\w]\$ '
export LS_OPTIONS='--color=auto'
eval "`dircolors`"
alias ls='ls $LS_OPTIONS'
alias ll='ls $LS_OPTIONS -l'
alias l='ls $LS_OPTIONS -lA'
alias tt='cd ~/tt && screen tt++ init.tt'
alias ck='vim ~/.termux/termux.properties'
```
此处 `tt` 命令就可以快速进入游戏。

## 2。screen、vim中文乱码

__TinTin++ 旧版本不支持 GBK 编码，  
新版本 2.02 以后添加了对中文的支持，  
新版本使用 #config charset 设置编码，  
旧版本使用 screen 进行转码。__

### 利用screen给tt++转码

> echo defencoding GBK > ~/.screenrc  
echo mousetrack off >> ~/.screenrc

以上命令效果等同于下列操作。

或使用vim文本编辑器编辑：

> vim ~/.screenrc

按字母i键开启插入模式，方向键控制光标，  
添加如下内容后保存：

```
defencoding GBK
mousetrack off
```
将以上内容复制粘贴到文本中，  
修改完毕后按 ESC 键退出编辑模式：

- 输入 `:wq` 保存
- 或大写模式按两下 `ZZ` 键

__只玩游戏做到这一步即可。__

### vim编辑脚本时中文乱码

> vim ~/.vimrc

添加如下内容后保存：

```
syntax on
set t_Co=256
set bg=dark
set autoindent
set hlsearch
colorscheme murphy
set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8
"set number
```

### 脚本中文乱码转换编码

1.vim 按 ESC 键退出编辑模式后输入下列命令：

```
:set fileencoding=gb18030
```

2.批量转换脚本编码

使用 [【gbk2utf8】](https://github.com/fluffos/gbk2utf8) 工具进行转换。

### vim语法高亮

输入指令：  
```
cd ~ && git clone https://github.com/LokiChaos/vim-tintin.git .vim
```

## 3。初始init.tt脚本

### 利用screen启动tintin++客户端

> screen tt++

连接服务端使用 `#ses` 命令，  
可选填账号密码参数，使用 `;` 间隔。

```
例:
#ses pku mud.pkuxkx.com 8080;username;password;
```

### 分屏

> #split

此命令可分割出输入行及 map 显示区域。

注：另可将配置先写入到文件，  
然后使用配置文件启动游戏。

```
1.新建文件
vim init.tt
2.添加如下内容后保存
#split
#config charset big5
#ses pku mud.pkuxkx.com 8080
```
### 进入游戏

> screen tt++ init.tt

### 管理配置文件及脚本

- 此处可将配置文件使用 git 上传至 github，  
这样更换环境后克隆仓库即可快速使用配置。

- 或者安装 ssh 使用 sftp 或 scp 传输。

- TinTin++ 官网提供了从电脑端 wintin++ 使用 `chat` 传输配置的方法。

- Termux 内建的 `termux-setup-storage` 接口可以在 `$HOME` 用户目录中创建一个对内部存储的符号链接，  
我们可以直接访问内存卡（内部存储）或者建立相应目录的符号链接。

以下将文件直接存放到手机上：

```
使用 Termux 管理的流程（本地推荐）：

1.建立符号链接
输入：termux-setup-storage
在弹出的权限要求中点击允许。
2.访问内存卡中的tt目录（自建）
cd $HOME/storage/shared/tt
3.内存卡中tt目录的符号链接到用户目录
ln -s $HOME/storage/shared/tt $HOME/tt
4.通过符号链接进入内存卡的tt目录
cd $HOME/tt

注:此处也可将 git仓库 克隆到内存卡中。
```

以下将文件存放到 github 上，手机存放副本：

```
使用 git 管理的流程（远程推荐）：

1.克隆仓库并指定文件夹名为 tt
git clone https://github.com/zixijian/tt.git tt
2.进入仓库（此处默认为用户目录）
cd tt
3.启动游戏
screen tt++ init.tt

更新新仓库内容输入指令（未启动游戏时）：
git pull

注：这里是 xgg@pkuxkx 的机器人脚本。
```

### screen 管理进程

- 组合键 `ctrl+a+d` 后台运行；
- `screen -list` 显示后台列表；
- `screen -r <进程id或名称>` 恢复进程到前台；

注：screen还能指定名称管理。

```
按组合键ctrl+a后，输入：
:sessionname xgg
回车确定，
按顺序按组合键ctrl+a+d进入后台，
screen -r xgg
返回游戏。
```

## 4。游戏指南

Termux 可以直接调用浏览器访问链接，
此处可快速验证 fullme。

> termux-open-url <链接>

TinTin++可以写触发器获取链接：  

```
#nop 简写;
#alias {fm} {fullme};
#nop 打印链接;
#alias {slink} {#showme $link};
#nop 手动调用浏览器;
#alias {mxp} {#sys termux-open-url $link};

#action {^http://fullme.pkuxkx.net/robot.php?filename=%1} {
  #var link {http://fullme.pkuxkx.net/robot.php?filename=%1};
  #nop mxp;
  #nop #system sh bot/fullme.sh %1;
};

#act {^http://fullme.pkuxkx.com/robot.php?filename=%1} {
	#var link {http://fullme.pkuxkx.com/robot.php?filename=%1};
  #nop mxp;
  #nop #system sh bot/fullme.sh %1;
};
```
SSH 连接安卓本机 chroot 容器，也可调用浏览器查看图片。

```
#alias {cmxp} {
    #sys unchroot am start -a android.intent.action.VIEW -d $link
};
```

__新手推荐丐帮污衣派__

> enter shudong;bai qiu

更多游戏信息访问：|[北侠Wiki](http://pkuxkx.net/wiki/)|[北侠论坛](http://pkuxkx.net/forum/)|

## 5。机器人使用

- 逍遥行：

逍遥行是一个非常实用的代步工具，  
内置了各个区域地标地点的连接路径。 

学习 tintin++ 语法时，   
推荐以[「逍遥行」](https://github.com/zixijian/tt/blob/master/goto.tt)为范例。

__指令必须从地标地点出发。__

注:地标地点自动触发并显示节点信息。

__命令 `gt` 查看逍遥行帮助，  
命令  `gt list` 查看可去地点信息，  
命令 `inquire list` 查看地标房间信息。__

- 更多语法及实例：

__详见：__|[TINTIN++中文手册](./Wiki.md)|  

- TINTIN++脚本指南

__详见：__|[TINTIN++脚本指南](./Guide.md)|  

- 炮爷语录拾遗

> 学莫便乎近其人。学之经莫速乎好其人，隆礼次之。  

快速学习一门知识，一个好的老师能事半功倍。  

__详见：__|[炮爷语录拾遗](./Special.md)|  

TINTIN++交流 QQ 群：951665549。

## 6。天高任鸟飞

> 挂到你天~荒地也老。    --- by 鲁迅。

# END