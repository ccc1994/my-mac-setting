# my-mac-setting

工欲善其事必先利其器, 这个项目主要是为了记录和分享自己的 mac 设置和工具集. 我时不时的也会改进自己的工具集和习惯, 所以这里的内容也会发生变化.

- [my-mac-setting](#my-mac-setting)
  - [语言设置](#%e8%af%ad%e8%a8%80%e8%ae%be%e7%bd%ae)
  - [输入设置](#%e8%be%93%e5%85%a5%e8%ae%be%e7%bd%ae)
    - [输入法切换](#%e8%be%93%e5%85%a5%e6%b3%95%e5%88%87%e6%8d%a2)
  - [浏览器及插件](#%e6%b5%8f%e8%a7%88%e5%99%a8%e5%8f%8a%e6%8f%92%e4%bb%b6)
    - [我的常用的 Chrome 插件](#%e6%88%91%e7%9a%84%e5%b8%b8%e7%94%a8%e7%9a%84-chrome-%e6%8f%92%e4%bb%b6)
  - [效率工具](#%e6%95%88%e7%8e%87%e5%b7%a5%e5%85%b7)
    - [Alfred](#alfred)
  - [开发相关](#%e5%bc%80%e5%8f%91%e7%9b%b8%e5%85%b3)
    - [vscode](#vscode)
    - [Homebrew](#homebrew)
      - [安装 brew](#%e5%ae%89%e8%a3%85-brew)
      - [安装 brew cask](#%e5%ae%89%e8%a3%85-brew-cask)
    - [Iterm2](#iterm2)
      - [safe-rm](#safe-rm)
      - [alias 命令别名](#alias-%e5%91%bd%e4%bb%a4%e5%88%ab%e5%90%8d)
    - [IDEA](#idea)
  - [软件](#%e8%bd%af%e4%bb%b6)
    - [欧陆词典](#%e6%ac%a7%e9%99%86%e8%af%8d%e5%85%b8)
    - [Notion](#notion)
    - [Charles](#charles)
    - [OminiGraffle](#ominigraffle)
    - [Foxmail](#foxmail)
    - [Xmind](#xmind)
    - [Showdowsocks/V2Ray](#showdowsocksv2ray)
    - [Time Out](#time-out)
    - [Karabiner Elements](#karabiner-elements)
    - [Xnip](#xnip)

## 语言设置

语言刻意设置的英文, 并不是装逼或者英语好, 抱着能多认识几个单词是几个的心态而已

## 输入设置

输入法目前用的是搜狗, 用搜狗的原因主要两点

1. 搜狗对一些新词或热点词会有更新(貌似 mac 自带没有)
2. 搜狗对于开发者来说会有很多友好的设置
   * 中文下使用英文标点, 这个在写代码的时候比较关键, 防止写代码的时候用的中文的标点导致一些问题, 所以我一直是用的英文标点
   * 中文与英文/数字间键入空格, 这个设置勾上, 格式会更规范些
   * 浏览器地址内默认使用英文
   * 自动在某些 app 切换到英文, 比如 iterm, IDEA 之类的开发软件

### 输入法切换

目前我用不是搜狗的中英文切换, 而是在系统输入法(ABC)和搜狗输入法之间切换. 主要原因是使用 vim 的插入模式和命令模式切换的问题, 切换到命令模式的时候如果是中文输入, 就会有问题, 当然像 IDEA 里也有插件解决这个问题, 插件会在进入命令模式时自动切换到英文输入法, 但是切回中文输入法时又会丢失中文输入法的中英文切换的状态. 所以我这里就干脆中文只用搜狗, 英文只用系统的 ABC.

切换的快捷键是 caps lock, 这里是被我改了, 因为中英文切换还是比较频繁的, 所以我希望用一个键位就能切换. 而大小写切换被我改成了 fn. 切换方法:

1. 先让原先的 caps lock 失效, 方法为 System Preferences -> Keyboard -> Modifier Keys, 将 caps lock 置为 No Action, 这时 caps lock 这个建位没有任何作用了
2. 然后利用 [Karabiner-Elements](https://pqrs.org/osx/karabiner/) 将 caps lock 映射到一个原本不存在的键位, 比如 f19
3. 最后在 System Preferences -> Keyboard -> Shorcut -> Input Source 里将输入法切换设置为 f19. 这样就让 caps lock 变成了输入法切换的快捷键
4. 让fn能进行为大小写切换. 也是在 System Preferences -> Keyboard -> Modifier Keys 里设置为 caps lock 的功能. 这里和 fn + F1~12 的组合并不冲突

当然这个解决方法并不完美, 大小写切换用 fn 不是特别方便, 且容易误触, 有种办法就是用 Karabiner-Elements 将长按或者双击 caps lock 变为大小写切换, 但实验中总会出现一些莫名其妙的问题, 所以放弃了, 后面大概也会再改进.

## 浏览器及插件

浏览器的话用的 Chrome, 如果对隐私比较注重的话推荐用 Firefox.

### 我的常用的 Chrome 插件

* [Extension Manager](https://chrome.google.com/webstore/detail/extension-manager/gjldcdngmdknpinoemndlidpcabkggco) 用来管理插件, 可以快速开启或关闭某个插件
* [彩云小译](https://fanyi.caiyunapp.com/#/) 目前用过的最好用的翻译插件, 相比 Google 翻译更快, 准确度个人感觉也更高, 并且有中英文对照, 在翻译的不好时可以看原文. 缺点是有时候中英文对照会挤在一起, 影响阅读.
* [Switchy Omega](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif) 切换浏览器的代理, 科学上网必备
* [Notion Web Clipper](https://chrome.google.com/webstore/detail/notion-web-clipper/knheggckgoiihginacbkhaalnibhilkk) 因为我记笔记用的 Notion 所以会有这个网页复制的插件, 不过没有印象笔记的插件好用
* [SourceGraph](https://chrome.google.com/webstore/detail/sourcegraph/dgjhfomjieaadpoljlnidmbgkdffpack) 用来浏览 Github 上的项目, 类似的插件有很多, 我倒没对比过
* [Vimium](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb) 在网页上使用 vim, 可以方便的切换 tab, 上下翻页, 用键盘点击任何一个可点击的元素等. 我常用的:

    * j 向下移动一小段
    * k 向上移动一小段
    * d 向下移动半页
    * u 向上移动半页
    * J 切换到左边的 tab
    * K 切换到右边的 tab
    * gi 聚焦到第一个输入框(用于进入搜索框)
    * gg 移动到网页最上面
    * G 移动到网页最下面
* [Ublock Oring](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm) 用来屏蔽广告, 非常好用, 并且支持在广告的区域右键可以手动屏幕该处的广告, 下次就不会看到了.

## 效率工具

### Alfred

必备神器, Spotlight 的替代. 并且可以自定义或下载其他人的 [WorkFlow](http://www.packal.org/workflow-search), 我的设置是通过 command + space 唤起 alfred.

我的 workflow:

* Encode / Decode
* Epoch Converter. 时间戳转化
* JetBrains - Open Project. 快速打开 IDEA 项目
* Kill Process
* portkiller
* What's My IP

这些都可以在[这里](http://www.packal.org/workflow-search)搜到

常用操作:
  
* 快速打开/切换软件. 搜索框输入字母进行搜索, 支持拼音, 并且搜索频率高的会优先, 所以常用的软件一个字符就能搞定了, 例如输入 c, 第一个就是 chrome, 输入 d 第一个就是钉钉
* 快速打开书签, 输入书签名, 然后选择列表项并打开对应的浏览器书签
* 搜索/打开文件或文件夹
* 打开 mac 设置. 比如 keyborad 打开键盘设置
  
配合 Alfred + 各类软件本身的快捷键 + vim + vimium,能够做到绝大部分操作都用键盘能够完成.

从效率上来说: 键盘 > Trackpad > 鼠标

## 开发相关

### vscode

编辑器应该大部分人都是用的 vscode, 应该是目前最好用的编辑器了, 不过个人目前不是深度使用, 主要开发还是用的 IDEA, 常用的功能就是 vscode 的多行编辑, 然后一些轻量简单的编辑工作.

### Homebrew

[Homebrew](https://brew.sh/)是Mac下的包管理工具, 可以方便的搭建某个开发环境或者安装某个工具

#### 安装 brew

打开终端运行以下命令

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

#### 安装 brew cask

brew cask是brew的扩展,可以安装 appstroe 的软件

    brew install cask

### Iterm2

[iterm2](https://iterm2.com/) 是 mac 自带的 Terminal 的替代, 功能强大, 主题我用的 [oh my zsh](https://ohmyz.sh/)

#### safe-rm

`rm -rf /` 这个命令相信大家都知道很危险, 我就不小心在 mac 上执行过一次(虽然立刻中止了), 这个设置就是为了避免发生类似的误删

下载 safe-rm

`brew install safe-rm`

查看 Path 路径
`echo $PATH`

添加软链接到 safe-rm

`ln -s /usr/local/bin/safe-rm /usr/local/bin/rm`

如果要删除这项设置的话

`rm /usr/local/bin/rm`

设置安全目录, 配置文件在 `/etc/safe-rm.conf`

我的配置:

    /private
    /Applications
    /Developer
    /Library
    /Network
    /System
    /Users
    /Volumes
    /
    ~/test
    ~/Documents

可以尝试删除 test, 会拒绝

#### alias 命令别名

设置命令别名, 简化一些常用的命令, 主要是 git 的别名(不记得从哪复制来的了...)

    -='cd -'
    ...=../..
    ....=../../..
    .....=../../../..
    ......=../../../../..
    1='cd -'
    2='cd -2'
    3='cd -3'
    4='cd -4'
    5='cd -5'
    6='cd -6'
    7='cd -7'
    8='cd -8'
    9='cd -9'
    _=sudo
    afind='ack -il'
    d='dirs -v | head -10'
    g=git
    ga='git add'
    gaa='git add --all'
    gapa='git add --patch'
    gau='git add --update'
    gb='git branch'
    gba='git branch -a'
    gbd='git branch -d'
    gbda='git branch --no-color --merged | command grep -vE "^(\*|\s*(master|develop|dev)\s*$)" | command xargs -n 1 git branch -d'
    gbl='git blame -b -w'
    gbnm='git branch --no-merged'
    gbr='git branch --remote'
    gbs='git bisect'
    gbsb='git bisect bad'
    gbsg='git bisect good'
    gbsr='git bisect reset'
    gbss='git bisect start'
    gc='git commit -v'
    'gc!'='git commit -v --amend'
    gca='git commit -v -a'
    'gca!'='git commit -v -a --amend'
    gcam='git commit -a -m'
    'gcan!'='git commit -v -a --no-edit --amend'
    'gcans!'='git commit -v -a -s --no-edit --amend'
    gcb='git checkout -b'
    gcd='git checkout develop'
    gcf='git config --list'
    gcl='git clone --recursive'
    gclean='git clean -fd'
    gcm='git checkout master'
    gcmsg='git commit -m'
    'gcn!'='git commit -v --no-edit --amend'
    gco='git checkout'
    gcount='git shortlog -sn'
    gcp='git cherry-pick'
    gcpa='git cherry-pick --abort'
    gcpc='git cherry-pick --continue'
    gcs='git commit -S'
    gcsm='git commit -s -m'
    gd='git diff'
    gdca='git diff --cached'
    gdct='git describe --tags `git rev-list --tags --max-count=1`'
    gdt='git diff-tree --no-commit-id --name-only -r'
    gdw='git diff --word-diff'
    gf='git fetch'
    gfa='git fetch --all --prune'
    gff='git flow feature'
    gfi='git flow init'
    gfo='git fetch origin'
    gg='git gui citool'
    gga='git gui citool --amend'
    ggpull='git pull origin $(git_current_branch)'
    ggpur=ggu
    ggpush='git push origin $(git_current_branch)'
    ggsup='git branch --set-upstream-to=origin/$(git_current_branch)'
    ghh='git help'
    gignore='git update-index --assume-unchanged'
    gignored='git ls-files -v | grep "^[[:lower:]]"'
    git-svn-dcommit-push='git svn dcommit && git push github master:svntrunk'
    gk='\gitk --all --branches'
    gke='\gitk --all $(git log -g --pretty=%h)'
    gl='git pull'
    glg='git log --stat'
    glgg='git log --graph'
    glgga='git log --graph --decorate --all'
    glgm='git log --graph --max-count=10'
    glgp='git log --stat -p'
    glo='git log --oneline --decorate'
    globurl='noglob urlglobber '
    glog='git log --oneline --decorate --graph'
    gloga='git log --oneline --decorate --graph --all'
    glol='git log --graph --pretty='\''%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --abbrev-commit'
    glola='git log --graph --pretty='\''%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --abbrev-commit --all'
    glp=_git_log_prettily
    glum='git pull upstream master'
    gm='git merge'
    gmom='git merge origin/master'
    gmt='git mergetool --no-prompt'
    gmtvim='git mergetool --no-prompt --tool=vimdiff'
    gmum='git merge upstream/master'
    gp='git push'
    gpd='git push --dry-run'
    gpoat='git push origin --all && git push origin --tags'
    gpristine='git reset --hard && git clean -dfx'
    gpsup='git push --set-upstream origin $(git_current_branch)'
    gpu='git push upstream'
    gpv='git push -v'
    gr='git remote'
    gra='git remote add'
    grb='git rebase'
    grba='git rebase --abort'
    grbc='git rebase --continue'
    grbi='git rebase -i'
    grbm='git rebase master'
    grbs='git rebase --skip'
    grep='grep  --color=auto --exclude-dir={.bzr,CVS,.git,.hg,.svn}'
    grh='git reset HEAD'
    grhh='git reset HEAD --hard'
    grmv='git remote rename'
    grrm='git remote remove'
    grset='git remote set-url'
    grt='cd $(git rev-parse --show-toplevel || echo ".")'
    gru='git reset --'
    grup='git remote update'
    grv='git remote -v'
    gsb='git status -sb'
    gsd='git svn dcommit'
    gsi='git submodule init'
    gsps='git show --pretty=short --show-signature'
    gsr='git svn rebase'
    gss='git status -s'
    gst='git status'
    gsta='git stash save'
    gstaa='git stash apply'
    gstc='git stash clear'
    gstd='git stash drop'
    gstl='git stash list'
    gstp='git stash pop'
    gsts='git stash show --text'
    gsu='git submodule update'
    gts='git tag -s'
    gtv='git tag | sort -V'
    gunignore='git update-index --no-assume-unchanged'
    gunwip='git log -n 1 | grep -q -c "\-\-wip\-\-" && git reset HEAD~1'
    gup='git pull --rebase'
    gupv='git pull --rebase -v'
    gwch='git whatchanged -p --abbrev-commit --pretty=medium'
    gwip='git add -A; git rm $(git ls-files --deleted) 2> /dev/null; git commit --no-verify -m "--wip-- [skip ci]"'
    history='fc -l 1'
    l='ls -lah'
    la='ls -lAh'
    ll='ls -lh'
    ls='ls -G'
    lsa='ls -lah'
    md='mkdir -p'
    please=sudo
    po=popd
    pu=pushd
    rd=rmdir
    run-help=man
    tailf='tail -f'
    which-command=whence

### IDEA

Java 开发环境自然用的 Jetbrain 家的 IntelliJ IDEA, 数据库终端用的 IDEA
 内置的. Code Review 用的 Upsource.

我的插件列表:

* [.gitignore](https://github.com/JetBrains/idea-gitignore) 一键生成 .gitignore 文件
* [Gsonformat](https://plugins.jetbrains.com/plugin/7654-gsonformat/) 通过 JSON 生成对应的POJO
* [IDE Features Trainer](https://plugins.jetbrains.com/plugin/index?xmlId=GsonFormat) 刚用 IDEA 可以通过这个来学习
* [Key Promoter X](https://plugins.jetbrains.com/plugin/9792-key-promoter-x/) 快捷键不熟悉的小伙伴必备
* [IDEA Vim](https://plugins.jetbrains.com/plugin/164-ideavim/) 如果想在编辑器里快速移动光标的话, 必备
* [IdeaVimExtension](https://plugins.jetbrains.com/plugin/index?xmlId=IdeaVimExtension) 解决 vim 切换模式时的输入法切换问题
* [JRebel](https://plugins.jetbrains.com/plugin/index?xmlId=JRebelPlugin) 热部署插件, 修改代码后不用重启应用
* [Lombok](https://plugins.jetbrains.com/plugin/index?xmlId=Lombook%20Plugin) 必备
* [MapStruct Support](https://plugins.jetbrains.com/plugin/index?xmlId=org.mapstruct.intellij) 如果你用了 mapstruct 作为对象复制属性的工具话, 需要这个插件
* [Maven Helper](https://plugins.jetbrains.com/plugin/index?xmlId=MavenRunHelper)
* [PlantUML](https://plugins.jetbrains.com/plugin/index?xmlId=PlantUML%20integration) 渲染 PlantUML
* [Rainbow Brackets](https://plugins.jetbrains.com/plugin/10080-rainbow-brackets/) 用颜色区分括号, 方便在嵌套多的时候找到括号的另一个对应
* [String Manipulation](https://plugins.jetbrains.com/plugin/index?xmlId=String%20Manipulation) 各种 String 的操作, 常用的是命名法切换

一般来说到插件中心按下载量都看一眼, 能找到挺多好用的插件.

## 软件

### 欧陆词典

之前是用的有道词典, 主要用来查词和记录生词, 并把生词同步到手机端. 但是 mac 上总是自动闪到其他软件后面, 并且取词功能感觉一般. 所以刚换到了欧陆词典, 目前使用中, 取词功能比有道好用些

### Notion

之前用的印象笔记, 但是用 markdown 记录的时候, 必须一边 markdown 原文, 一边渲染后的内容, 十分蛋疼, 并且使用起来也感觉没太多亮点. 目前换到了 Notion 对 markdown 支持更好, 用来做 todo list 也不错. 缺点就是 webclipper 不如印象笔记的好用, 速度相对也慢点.

### Charles

用来截取网络请求

### OminiGraffle

用来画一些流程图, 示例图等

### Foxmail

不是邮件重度用户, 用这个主要是邮件一分钟才拉一次, 所以邮件提醒也比较少(个人比较讨厌通知和软件图标右上角的未读计数)

### Xmind

平常用来画一些简单的思维导图, 用于整理学习笔记或者思路, 功能够用就行, 轻度用户不多做评论

### Showdowsocks/V2Ray

科学上网, 据说防火墙已经能够用深度学习识别 SS 协议的流量了, 可怕...  所以建议 V2Ray

### Time Out

这个主要是个人习惯, 用来设置在工作时间段间隔一定时间自动进入屏保, 用来提醒自己休息一下, 劳逸结合嘛

### Karabiner Elements

用来做一些键盘映射, 比如上面那个例子, 修改输入法和大小写切换的快捷键.

### Xnip

截图软件, 用聊天软件的也可以, 但是聊天软件不一定总是打开的
