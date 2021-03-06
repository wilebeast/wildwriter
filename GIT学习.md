<html xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:ap="http://schemas.mindjet.com/MindManager/Application/2003" xmlns:cor="http://schemas.mindjet.com/MindManager/Core/2003">
<head>
<META http-equiv="Content-Type" content="text/html; charset=UTF-16">
<title>Outline of GIT学习</title>
<style type="text/css">#level1Indent { margin-left:  2em } </style>
<style type="text/css">#level2Indent { margin-left:  4em } </style>
<style type="text/css">#level3Indent { margin-left:  6em } </style>
<style type="text/css">#level4Indent { margin-left:  8em } </style>
<style type="text/css">#level5Indent { margin-left:  10em } </style>
<style type="text/css">#levelXIndent { margin-left:  12em } </style>
<style type="text/css">#level1Style { font-size: 11pt; font-weight: bold; margin-bottom: 0.5em; margin-left:  2em } </style>
<style type="text/css">#level2Style { font-size:  9pt; font-weight: bold; margin-top: 1em; margin-bottom: 0.5em } </style>
<style type="text/css">#level3Style { font-size:  8pt; font-weight: bold; margin-top: 1em; margin-bottom: 0.5em } </style>
<style type="text/css">#level4Style { font-size:  8pt; font-weight: bold; margin-top: 1em; margin-bottom: 0.5em } </style>
<style type="text/css">#level5Style { font-size:  8pt; font-weight: bold; margin-top: 1em; margin-bottom: 0.5em } </style>
<style type="text/css">#levelXStyle { font-size:  8pt; font-weight: bold; margin-top: 1em; margin-bottom: 0.5em } </style>
<style type="text/css">#notesStyle { font-size:  8pt; margin-bottom: 1em } </style>
</head>
<body>
<div id="level1Indent">
<div id="level1Style"> GIT学习</div>
</div>
<div id="level2Indent">
<div id="level2Style">1 起步</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.1 版本控制</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.1.1 目的</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.1.1 查看特定版本修订情况</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.1.2 案例</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">把文件添加到版本库</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">首先这里再明确一下，所有的版本控制系统，其实只能跟踪文本文件的改动，比如TXT文件，网页，所有的程序代码等等，Git也不例外。版本控制系统可以告诉你每次的改动，比如在第5行加了一个单词“Linux”，在第8行删了一个单词“Windows”。而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来，也就是只知道图片从100KB改成了120KB，但到底改了啥，版本控制系统不知道，也没法知道。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">不幸的是，Microsoft的Word格式是二进制格式，因此，版本控制系统是没法跟踪Word文件的改动的，前面我们举的例子只是为了演示，如果要真正使用版本控制系统，就要以纯文本方式编写文件。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">因为文本是有编码的，比如中文有常用的GBK编码，日文有Shift_JIS编码，如果没有历史遗留问题，强烈建议使用标准的UTF-8编码，所有语言使用同一种编码，既没有冲突，又被所有平台所支持。</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.1.2 优点</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.2.1 可以随意回溯过去，但是工作量增加的很少</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.1.3 分类</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.3.1 本地版本控制系统</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.1.1 RCS</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.1.2 现在还有电脑上有这个</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.3.2 集中化版本控制系统</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.2.1 解决不同系统的开发者协同</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.2.2 CVCS</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.2.3 多人可以协同，但是服务器不能出问题</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.3.3 分布式版本控制系统</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.3.1 DVCS</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.1.3.3.2 GIT、Bazaar、Darcs</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.1.3.1 区分</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.2 GIT简史</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.2.1 Linux内核开源项目的问题</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.2.2 Bitkeeper</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.2.2.1 2005年停止了免费使用</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.2.3 Linux Torvalds</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.2.3.1 开发GIT</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.2.3.2 要求</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.2.3.2.1 速度</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.2.3.2.2 简单的设计</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.2.3.2.3 对非线性开发模式强力支持</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.2.3.2.4 完全分布式</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.2.3.2.5 可以管理超大型规模项目</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.2.4 更好玩的版本</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.3 GIT基础</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.1 Git对待数据的方式</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.1.1 把数据看成对小型文件系统的一组快照</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.1.2 对待数据像是一个快照流</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.1.3 </div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.2 几乎所有操作都是本地执行</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.2.1 大部分操作可以瞬间完成</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.2.2 离线的时候也可以操作</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.3 git保持完整性</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.3.1 所有数据存储前都计算校验</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.3.2 这是git的底层哲学，不会出错</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.4 git一般只添加数据</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.4.1 执行的操作几乎只增加数据</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.4.2 很难逆操作或者清除数据</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.5 git三种状态</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.5.1 已经提交</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.5.1.1 数据已经安全地保存在本地数据库中</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.5.2 已经修改</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.5.2.1 修改了文件，但是还没有保存到数据库中</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.5.3 已经暂存</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.5.3.1 对一个已经修改文件的当前版本做了标记，使之包含在下一次提交的快照中</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.6 三个工作区域</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.6.1 git仓库（.git directory(Repository））</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.1.1 git用来保存项目的源数据和对象数据库的地方</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.1.2 最重要的部分</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.1.3 从其他计算机克隆仓库时，拷贝的就是这里的数据</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.6.2 工作目录（working directory）</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.2.1 对项目的某个版本独立提取出来的内容</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.2.2 从仓库的压缩数据库中提取出来的文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.2.3 放在硬盘上供使用和修改</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.6.3 暂存区域（staging area）</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.3.1 是一个文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.3.2 保存了下次讲提交的文件列表信息</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.3.3 一般在仓库目录中</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.3.6.3.4 有时候也被称之为索引</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.6.4 </div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.6.1 状态</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果 Git 目录中保存着的特定版本文件，就属于已提交状态。 如果作了修改并已放入暂存区域，就属于已暂存状态。 如果自上次取出后，作了修改但还没有放到暂存区域，就是已修改状态。</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.3.7 git工作流程</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.7.1 在工作目录中修改文件</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.7.2 暂存文件，将文件的快照放入暂存区域</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.3.7.3 提交更新，找到暂存区域的文件，将快照永久性存储到Git仓库目录</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.4 命令行</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.4.1 多种使用方式</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.4.1.1 原生的命令行模式</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.4.1.1.1 可以执行所有命令</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.4.1.1.2 学会了之后可以在任何其他软件都不成问题</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.4.1.2 GUI模式</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.4.2 系统</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.4.2.1 Mac</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.4.2.1.1 终端（Terminal）</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.4.2.2 Windows</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.4.2.2.1 命令窗口（Command Prompt）</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.4.2.2.2 PowerShell</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.4.3 这些命令将作为基础命令使用，必须掌握</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.5 安装Git</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.5.1 四种形式</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.5.1.1 On Linux</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.5.1.1.1 略</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.5.1.2 On Mac</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.5.1.3 On Windows</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.5.1.3.1 官方版本</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.5.1.3.2 Github for windows</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.5.1.4 从源码安装</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.5.2 《如何将Git安装到你的电脑上》</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.5.2.1 linus命令行</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.5.3 《廖雪峰-安装GIT》</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.6 首次设置Git</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.6.1 git config</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.1.1 获取和配置变量来控制git</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.1.2 存储位置</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.1 /etc/gitconfig</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.1.1 系统中对所有用户都普遍适用的配置</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.1.2 用-system选项，更改的就是这个</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.2 ~/.gitconfig</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.2.1 ~/.config/git/config</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.2.2 用户目录下的配置文件只适用于该用户</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.2.3 用-global选项，更改的就是这个文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.3 config</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.3.1 .git/config</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.3.2 这里的配置仅仅针对当前项目有效</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.3.3 每一个级别的配置都会覆盖上层的相同配置</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.2.3.4 这里的配置会覆盖/etc/gitconfig中的同名变量</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.1.3 windows特别说明</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.1.3.1 git找寻主目录的.gitconfig文件</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.6.2 用户信息</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.2.1 配置内容</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git config --global user.name "John Doe"</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git config --global user.email johndoe@example.com</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.2.1.1 个人用户名</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.2.1.2 电子邮件地址</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.2.2 -global选项</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">1.6.2.2.1 更改的是用户主目录下的那个</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.6.3 文本编辑器</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.6.4 查看配置信息</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.4.1 git config --list</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.6.4.2 git config user.name</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.6.5 本部分没有中文，请参考中文内容</div>
</div>
<div id="level3Indent">
<div id="level3Style">1.7 如何获取帮助</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.7.1 三种获取帮助的方式</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.7.1.1 $ git help &lt;verb&gt;</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.7.1.2 $ git &lt;verb&gt; help</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.7.1.3 $ man git-&lt;verb&gt;</div>
</div>
<div id="level4Indent">
<div id="level4Style">1.7.2 举例</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.7.2.1 获得config命令的手册</div>
</div>
<div id="level5Indent">
<div id="level5Style">1.7.2.2 $ git help config</div>
</div>
<div id="level2Indent">
<div id="level2Style">2 远程仓库的使用</div>
</div>
<div id="level3Indent">
<div id="level3Style">2.1 准备内容</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.1.1 注册Github服务器</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.1.2 创建SSH Key</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.1.2.1 假设拥有</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">2.1.2.1.1 主目录-.ssh目录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">2.1.2.1.2 id_rsa文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">2.1.2.1.3 id_rsa.pub文件</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.1.2.2 没有</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ ssh-keygen -t rsa -C "youremail@example.com"</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">你需要把邮件地址换成你自己的邮件地址，然后一路回车，使用默认值即可，由于这个Key也不是用于军事目的，所以也无需设置密码。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">2.1.2.2.1 ssh-keygen -t rsa -C "youremail@example.com"</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.1.3 登陆GitHUB设置</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">github-addkey-1</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">点“Add Key”，你就应该看到已经添加的Key：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">github-addkey-2</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">为什么GitHub需要SSH Key呢？因为GitHub需要识别出你推送的提交确实是你推送的，而不是别人冒充的，而Git支持SSH协议，所以，GitHub只要知道了你的公钥，就可以确认只有你自己才能推送。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">当然，GitHub允许你添加多个Key。假定你有若干电脑，你一会儿在公司提交，一会儿在家里提交，只要把每台电脑的Key都添加到GitHub，就可以在每台电脑上往GitHub推送了。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">最后友情提示，在GitHub上免费托管的Git仓库，任何人都可以看到喔（但只有你自己才能改）。所以，不要把敏感信息放进去。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果你不想让别人看到Git库，有两个办法，一个是交点保护费，让GitHub把公开的仓库变成私有的，这样别人就看不见了（不可读更不可写）。另一个办法是自己动手，搭一个Git服务器，因为是你自己的Git服务器，所以别人也是看不见的。这个方法我们后面会讲到的，相当简单，公司内部开发必备。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">确保你拥有一个GitHub账号后，我们就即将开始远程仓库的学习。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.1.3.1 如果下载图形界面的话，这步可以省略了</div>
</div>
<div id="level3Indent">
<div id="level3Style">2.2 添加远程库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">小结</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">关联后，使用命令git push -u origin master第一次推送master分支的所有内容；</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">分布式版本系统的最大好处之一是在本地工作完全不需要考虑远程库的存在，也就是有没有联网都可以正常工作，而SVN在没有联网的时候是拒绝干活的！当有网络的时候，再把本地提交推送一下就完成了同步，真是太方便了！</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.2.1 在Github上建立一个空库</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.2.2 把本地内容上传</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.2.2.1 git remote add origin git@github.com:michaelliao/learngit.git</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">请千万注意，把上面的michaelliao替换成你自己的GitHub账户名，否则，你在本地关联的就是我的远程库，关联没有问题，但是你以后推送是推不上去的，因为你的SSH Key公钥不在我的账户列表中。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.2.2.2 git push -u origin master</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.2.3 更新分布库</div>
</div>
<div id="level5Indent">
<div id="level5Style">2.2.3.1 git push origin master</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.2.4 SSH警告说明</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">SSH警告</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">当你第一次使用Git的clone或者push命令连接GitHub时，会得到一个警告：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">The authenticity of host 'github.com (xx.xx.xx.xx)' can't be established.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">RSA key fingerprint is xx.xx.xx.xx.xx.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Are you sure you want to continue connecting (yes/no)?</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这是因为Git使用SSH连接，而SSH连接在第一次验证GitHub服务器的Key时，需要你确认GitHub的Key的指纹信息是否真的来自GitHub的服务器，输入yes回车即可。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Git会输出一个警告，告诉你已经把GitHub的Key添加到本机的一个信任列表里了：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Warning: Permanently added 'github.com' (RSA) to the list of known hosts.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这个警告只会出现一次，后面的操作就不会有任何警告了。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果你实在担心有人冒充GitHub服务器，输入yes前可以对照GitHub的RSA Key的指纹信息是否与SSH连接给出的一致。</p>
</div>
</div>
<div id="level3Indent">
<div id="level3Style">2.3 从远程库克隆</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.3.1 用图形界面很容易实现了</div>
</div>
<div id="level4Indent">
<div id="level4Style">2.3.2 大幅度降低学习成本</div>
</div>
<div id="level2Indent">
<div id="level2Style">3 Git基础</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">本章内容涵盖你在使用 Git 完成各种工作中将要使用的各种基本命令。 在学习完本章之后，你应该能够配置并初始化一个仓库（repository）、开始或停止跟踪（track）文件、暂存（stage）或提交（commit)更改。 本章也将向你演示如何配置 Git 来忽略指定的文件和文件模式、如何迅速而简单地撤销错误操作、如何浏览你的项目的历史版本以及不同提交（commits）间的差异、如何向你的远程仓库推送（push）以及如何从你的远程仓库拉取（pull）文件。</p>
</div>
</div>
<div id="level3Indent">
<div id="level3Style">3.1 获取Git仓库（repository）</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.1.1 版本库-仓库</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.1.1 一个目录</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.1.2 所有的文件都可以被git管理</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.1.2.1 跟踪</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.1.2.2 还原</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.1.3 每个文件都能修改、删除</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.1.2 三种方法建立仓库</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.2.1 创建版本库</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.2.2 现有项目或目录中初始化仓库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">在现有目录中初始化仓库</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果你打算使用 Git 来对现有的项目进行管理，你只需要进入该项目目录并输入：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git init</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">该命令将创建一个名为 .git 的子目录，这个子目录含有你初始化的 Git 仓库中所有的必须文件，这些文件是 Git 仓库的骨干。 但是，在这个时候，我们仅仅是做了一个初始化的操作，你的项目里的文件还没有被跟踪。 (参见 Chapter 10 来了解更多关于到底 .git 文件夹中包含了哪些文件的信息。)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果你是在一个已经存在文件的文件夹（而不是空文件夹）中初始化 Git 仓库来进行版本控制的话，你应该开始跟踪这些文件并提交。 你可通过 git add 命令来实现对指定文件的跟踪，然后执行 git commit 提交：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add *.c</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add LICENSE</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git commit -m 'initial project version'</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">稍后我们再逐一解释每一条指令的意思。 现在，你已经得到了一个实际维护（或者说是跟踪）着若干个文件的 Git 仓库。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.2.3 从服务器克隆一个现有的GIt仓库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">克隆现有的仓库</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果你想获得一份已经存在了的 Git 仓库的拷贝，比如说，你想为某个开源项目贡献自己的一份力，这时就要用到 git clone 命令。 如果你对其它的 VCS 系统（比如说Subversion）很熟悉，请留心一下你所使用的命令是"clone"而不是"checkout"。 这是 Git 区别于其它版本控制系统的一个重要特性，Git 克隆的是该 Git 仓库服务器上的几乎所有数据，而不是仅仅复制完成你的工作所需要文件。 当你执行 git clone 命令的时候，默认配置下远程 Git 仓库中的每一个文件的每一个版本都将被拉取下来。 事实上，如果你的服务器的磁盘坏掉了，你通常可以使用任何一个克隆下来的用户端来重建服务器上的仓库（虽然可能会丢失某些服务器端的挂钩设置，但是所有版本的数据仍在，详见 “Getting Git on a Server” ）。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">克隆仓库的命令格式是 git clone [url] 。 比如，要克隆 Git 的可链接库 libgit2，可以用下面的命令：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git clone https://github.com/libgit2/libgit2</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这会在当前目录下创建一个名为 ``libgit2`` 的目录，并在这个目录下初始化一个 .git 文件夹，从远程仓库拉取下所有数据放入 .git 文件夹，然后从中读取最新版本的文件的拷贝。 如果你进入到这个新建的 libgit2 文件夹，你会发现所有的项目文件已经在里面了，准备就绪等待后续的开发和使用。 如果你想在克隆远程仓库的时候，自定义本地仓库的名字，你可以使用如下命令：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git clone https://github.com/libgit2/libgit2 mylibgit</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这将执行与上一个命令相同的操作，不过在本地创建的仓库名字变为 mylibgit。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Git 支持多种数据传输协议。 上面的例子使用的是 https:// 协议，不过你也可以使用 git:// 协议或者使用 SSH 传输协议，比如 user@server:path/to/repo.git 。 “Getting Git on a Server”将会介绍所有这些协议在服务器端如何配置使用，以及各种方式之间的利弊。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.2.3.1 相关问题可以去找萧队长询问</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.1.3 具体步骤</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">小结</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">现在总结一下今天学的两点内容：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">初始化一个Git仓库，使用git init命令。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">添加文件到Git仓库，分两步：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第一步，使用命令git add &lt;file&gt;，注意，可反复多次使用，添加多个文件；</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第二步，使用命令git commit，完成。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.3.1 建立空目录</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ mkdir learngit</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ cd learngit</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ pwd</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">/Users/michael/learngit</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">凡是有$的就是命令，没有的就是系统给的反馈</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> </p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.1.1 mkdir：建立目录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.1.2 cd：进入目录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.1.3 pwd：显示当前目录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.1.4 windows下目录不能有中文</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.3.2 把目录变成Git可以管理的仓库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git init</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Initialized empty Git repository in /Users/michael/learngit/.git/</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">凡是有$的就是命令，没有的就是系统给的反馈</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> </p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.2.1 $ git init</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.2.2 会在原有目录下建立.git目录，该目录是隐藏的</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.2.3 不可使用手动的方式修改该目录下的任何内容</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.2.4 ls -ah：显示隐藏目录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.2.5 了解.git文件夹中有哪些文件信息</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.1.3.3 将文件添加至仓库</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1 两个警告</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.1 不能对二进制文件进行版本控制</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">首先这里再明确一下，所有的版本控制系统，其实只能跟踪文本文件的改动，比如TXT文件，网页，所有的程序代码等等，Git也不例外。版本控制系统可以告诉你每次的改动，比如在第5行加了一个单词“Linux”，在第8行删了一个单词“Windows”。而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来，也就是只知道图片从100KB改成了120KB，但到底改了啥，版本控制系统不知道，也没法知道。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">不幸的是，Microsoft的Word格式是二进制格式，因此，版本控制系统是没法跟踪Word文件的改动的，前面我们举的例子只是为了演示，如果要真正使用版本控制系统，就要以纯文本方式编写文件。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">因为文本是有编码的，比如中文有常用的GBK编码，日文有Shift_JIS编码，如果没有历史遗留问题，强烈建议使用标准的UTF-8编码，所有语言使用同一种编码，既没有冲突，又被所有平台所支持。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.1.1 图片、视频</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.1.2 Word文档</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.2 不要用windows自带的文本工具</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.2.1 编码是用utf-8 without BOM</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">使用Windows的童鞋要特别注意：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">千万不要使用Windows自带的记事本编辑任何文本文件。原因是Microsoft开发记事本的团队使用了一个非常弱智的行为来保存UTF-8编码的文件，他们自作聪明地在每个文件开头添加了0xefbbbf（十六进制）的字符，你会遇到很多不可思议的问题，比如，网页第一行可能会显示一个“?”，明明正确的程序一编译就报语法错误，等等，都是由记事本的弱智行为带来的。建议你下载Notepad++代替记事本，不但功能强大，而且免费！记得把Notepad++的默认编码设置为UTF-8 without BOM即可：</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.1.2.2 notepad++</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.2 新建一个Readme.txt文件</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">内容：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Git is a version control system.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Git is free software.</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.2.1 一定要放置在目录中</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.3 git add：告知git将文件添加到仓库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第一步，用命令git add告诉Git，把文件添加到仓库：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add readme.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">执行上面的命令，没有任何显示，这就对了，Unix的哲学是“没有消息就是好消息”，说明添加成功。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.4 git commit：将文件提交到仓库</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第二步，用命令git commit告诉Git，把文件提交到仓库：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git commit -m "wrote a readme file"</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">[master (root-commit) cb926e7] wrote a readme file</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> 1 file changed, 2 insertions(+)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> create mode 100644 readme.txt</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.4.1 -m：本次提交的说明，可以是任意内容</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">简单解释一下git commit命令，-m后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">嫌麻烦不想输入-m "xxx"行不行？确实有办法可以这么干，但是强烈不建议你这么干，因为输入说明对自己对别人阅读都很重要。实在不想输入说明的童鞋请自行Google，我不告诉你这个参数。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">git commit命令执行成功后会告诉你，1个文件被改动（我们新添加的readme.txt文件），插入了两行内容（readme.txt有两行内容）。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.5 为什么要两部走：add commit</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.5.1 多次add文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.1.3.3.5.2 commit可以一次提交多个文件</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add file1.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add file2.txt file3.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git commit -m "add 3 files."</p>
</div>
</div>
<div id="level3Indent">
<div id="level3Style">3.2 记录每次更新到仓库</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.1 文件的状态变化周期</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.1.1 </div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.2 文件状态</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.2.1 分类</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1 已经跟踪</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.1 那些被纳入了版本控制的文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.2 在上一次快照中有它们的记录</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.3 在工作一段时间后</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.3.1 未修改</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.3.2 已修改</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.1.3.3 暂存区</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.2 未跟踪</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.2.1 除已跟踪文件以外的所有其它文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.2.2 不存在于上一次快照的记录中</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.1.2.3 也没有放入到暂存区</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.2.2 初次克隆的文件状态</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.2.1 所有文件都是已跟踪</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.2.2 未修改状态</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.2.3 更简化的说明《工作区和暂存区》</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.2.3.1 看懂了这个基本上就都明白了</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.3 查看文件状态</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.3.1 git status</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">要查看哪些文件处于什么状态，可以用 git status 命令。 如果在克隆仓库后立即使用此命令，会看到类似这样的输出：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">nothing to commit, working directory clean</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这说明你现在的工作目录相当干净。换句话说，所有已跟踪文件在上次提交后都未被更改过。 此外，上面的信息还表明，当前目录下没有出现任何处于未跟踪状态的新文件，否则 Git 会在这里列出来。 最后，该命令还显示了当前所在分支，并告诉你这个分支同远程服务器上对应的分支没有偏离。 现在，分支名是 ``master``,这是默认的分支名。 我们在 Chapter 3 会详细讨论分支和引用。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">现在，让我们在工程下创建一个新的 README 文件。 如果之前并不存在这个文件，使用 git status 命令，你将看到一个新的未跟踪文件：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ echo 'My Project' &gt; README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Untracked files:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">nothing added to commit but untracked files present (use "git add" to track)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">在状态报告中可以看到新建的 README 文件出现在 Untracked files 下面。 未跟踪的文件意味着 Git 在之前的快照（提交）中没有这些文件；Git 不会自动将之纳入跟踪范围，除非你明明白白地告诉它“我需要跟踪该文件”， 这样的处理让你不必担心将生成的二进制文件或其它不想被跟踪的文件包含进来。 不过现在的例子中，我们确实想要跟踪管理 README 这个文件。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.3.2 nothing to commit, working directory clean</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这说明你现在的工作目录相当干净。换句话说，所有已跟踪文件在上次提交后都未被更改过。 此外，上面的信息还表明，当前目录下没有出现任何处于未跟踪状态的新文件，否则 Git 会在这里列出来。 最后，该命令还显示了当前所在分支，并告诉你这个分支同远程服务器上对应的分支没有偏离。 现在，分支名是 ``master``,这是默认的分支名。 我们在 Chapter 3 会详细讨论分支和引用。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.3.3 nothing added to commit but untracked files present</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">在状态报告中可以看到新建的 README 文件出现在 Untracked files 下面。 未跟踪的文件意味着 Git 在之前的快照（提交）中没有这些文件；Git 不会自动将之纳入跟踪范围，除非你明明白白地告诉它“我需要跟踪该文件”， 这样的处理让你不必担心将生成的二进制文件或其它不想被跟踪的文件包含进来。 不过现在的例子中，我们确实想要跟踪管理 README 这个文件。</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.4 跟踪新文件</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.4.1 git add</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.1.1 Changes to be committed</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">只要在 Changes to be committed 这行下面的，就说明是已暂存状态。 如果此时提交，那么该文件此时此刻的版本将被留存在历史记录中。 你可能会想起之前我们使用 git init 后就运行了 git add (files) 命令，开始跟踪当前目录下的文件。 git add 命令使用文件或目录的路径作为参数；如果参数是目录的路径，该命令将递归地跟踪该目录下的所有文件。</p>
</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.1.1.1 暂存状态</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.4.2 该命令作用</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.2.1 可以用它开始跟踪新文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.2.2 把已跟踪的文件放到暂存区</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.2.3 用于合并时把有冲突的文件标记为已解决状态等</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.4.3 理解</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.4.3.1 添加内容到下一次提交中</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.5 暂存已修改文件</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.5.1 Changes not staged for commit</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.5.1.1 已跟踪文件的内容发生了变化</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.5.1.2 还没有放到暂存区</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.5.2 要暂存这次更新，需要运行 git add 命令</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.5.3 如果暂存后再次修改，必须再次暂存！</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">现在两个文件都已暂存，下次提交时就会一并记录到仓库。 假设此时，你想要在 CONTRIBUTING.md 里再加条注释， 重新编辑存盘后，准备好提交。 不过且慢，再运行 git status 看看：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ vim CONTRIBUTING.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes to be committed:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    new file:   README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    modified:   CONTRIBUTING.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes not staged for commit:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git add &lt;file&gt;..." to update what will be committed)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    modified:   CONTRIBUTING.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">怎么回事？ 现在 CONTRIBUTING.md 文件同时出现在暂存区和非暂存区。 这怎么可能呢？ 好吧，实际上 Git 只不过暂存了你运行 git add 命令时的版本， 如果你现在提交，CONTRIBUTING.md 的版本是你最后一次运行 git add 命令时的那个版本，而不是你运行 git commit 时，在工作目录中的当前版本。 所以，运行了 git add 之后又作了修订的文件，需要重新运行 git add 把最新版本重新暂存起来：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add CONTRIBUTING.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes to be committed:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    new file:   README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    modified:   CONTRIBUTING.md</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.5.4 具体案例请查看《管理修改》</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.6 状态简览</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.6.1 git status -s</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.6.2 状态说明</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1 M</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1.1 修改过的文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1.2 靠左</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1.2.1 该文件被修改了并放入了暂存区</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1.3 靠右</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.1.3.1 该文件被修改了但是还没放入暂存区</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.2 MM</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.2.1 工作区被修改并提交到暂存区后又在工作区中被修改了</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.3 A</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.3.1 新添加到暂存区中的文件</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.4 ??</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.6.2.4.1 新添加的未跟踪文件</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.7 忽略文件</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">一般我们总会有些文件无需纳入 Git 的管理，也不希望它们总出现在未跟踪文件列表。 通常都是些自动生成的文件，比如日志文件，或者编译过程中创建的临时文件等。 在这种情况下，我们可以创建一个名为 .gitignore 的文件，列出要忽略的文件模式。 来看一个实际的例子：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ cat .gitignore</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">*.[oa]</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">*~</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">第一行告诉 Git 忽略所有以 .o 或 .a 结尾的文件。一般这类对象文件和存档文件都是编译过程中出现的。 第二行告诉 Git 忽略所有以波浪符（~）结尾的文件，许多文本编辑软件（比如 Emacs）都用这样的文件名保存副本。 此外，你可能还需要忽略 log，tmp 或者 pid 目录，以及自动生成的文档等等。 要养成一开始就设置好 .gitignore 文件的习惯，以免将来误提交这类无用的文件。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">文件 .gitignore 的格式规范如下：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">所有空行或者以 ＃ 开头的行都会被 Git 忽略。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">可以使用标准的 glob 模式匹配。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">匹配模式以（/）结尾说明要忽略的是目录。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">要忽略指定模式以外的文件或目录，可以在模式前加上惊叹号（!）取反。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">所谓的 glob 模式是指 shell 所使用的简化了的正则表达式。 星号（*）匹配零个或多个任意字符；[abc] 匹配任何一个列在方括号中的字符（这个例子要么匹配一个 a，要么匹配一个 b，要么匹配一个 c）；问号（?）只匹配一个任意字符；如果在方括号中使用短划线分隔两个字符，表示所有在这两个字符范围内的都可以匹配（比如 [0-9] 表示匹配所有 0 到 9 的数字）。 使用两个星号（*) 表示匹配任意中间目录，比如a/**/z 可以匹配 a/z, a/b/z 或 a/b/c/z等。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">我们再看一个 .gitignore 文件的例子：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># no .a files</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">*.a</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># but do track lib.a, even though you're ignoring .a files above</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">!lib.a</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># only ignore the root TODO file, not subdir/TODO</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">/TODO</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># ignore all files in the build/ directory</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">build/</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># ignore doc/notes.txt, but not doc/server/arch.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">doc/*.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># ignore all .txt files in the doc/ directory</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">doc/**/*.txt</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">GitHub 有一个十分详细的针对数十种工程及语言的 .gitignore 文件列表，你可以在 https://github.com/github/gitignore 找到它.</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.7.1 有些文件无需纳入 Git 的管理，也不希望它们总出现在未跟踪文件列表</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.7.2 方法</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.7.2.1 建立文件夹.gitignore</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.7.2.2 ？</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.8 查看已暂存和未暂存的修改</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.8.1 git diff</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.9 提交更新</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">提交更新</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">现在的暂存区域已经准备妥当可以提交了。 在此之前，请一定要确认还有什么修改过的或新建的文件还没有 git add 过，否则提交的时候不会记录这些还没暂存起来的变化。 这些修改过的文件只保留在本地磁盘。 所以，每次准备提交前，先用 git status 看下，是不是都已暂存起来了， 然后再运行提交命令 git commit：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git commit</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">这种方式会启动文本编辑器以便输入本次提交的说明。 (默认会启用 shell 的环境变量 $EDITOR 所指定的软件，一般都是 vim 或 emacs。当然也可以按照 Chapter 1 介绍的方式，使用 git config --global core.editor 命令设定你喜欢的编辑软件。）</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">编辑器会显示类似下面的文本信息（本例选用 Vim 的屏显方式展示）：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># Please enter the commit message for your changes. Lines starting</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># with '#' will be ignored, and an empty message aborts the commit.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"># Changes to be committed:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">#  new file:   README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">#  modified:   CONTRIBUTING.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">#</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">~</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">~</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">~</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">".git/COMMIT_EDITMSG" 9L, 283C</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">可以看到，默认的提交消息包含最后一次运行 git status 的输出，放在注释行里，另外开头还有一空行，供你输入提交说明。 你完全可以去掉这些注释行，不过留着也没关系，多少能帮你回想起这次更新的内容有哪些。 (如果想要更详细的对修改了哪些内容的提示，可以用 -v 选项，这会将你所做的改变的 diff 输出放到编辑器中从而使你知道本次提交具体做了哪些修改。） 退出编辑器时，Git 会丢掉注释行，用你输入提交附带信息生成一次提交。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">另外，你也可以在 commit 命令后添加 -m 选项，将提交信息与命令放在同一行，如下所示：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git commit -m "Story 182: Fix benchmarks for speed"</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">[master 463dc4f] Story 182: Fix benchmarks for speed</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> 2 files changed, 2 insertions(+)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> create mode 100644 README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">好，现在你已经创建了第一个提交！ 可以看到，提交后它会告诉你，当前是在哪个分支（master）提交的，本次提交的完整 SHA-1 校验和是什么（463dc4f），以及在本次提交中，有多少文件修订过，多少行添加和删改过。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">请记住，提交时记录的是放在暂存区域的快照。 任何还未暂存的仍然保持已修改状态，可以在下次提交时纳入版本管理。 每一次运行提交操作，都是对你项目作一次快照，以后可以回到这个状态，或者进行比较。</p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.9.1 git commit</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.9.1.1 提交之前务必查看状态</div>
</div>
<div id="levelXIndent">
<div id="levelXStyle">3.2.9.1.2 没有暂存的，使用git add</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.9.2 可以把一个commit理解为一个快照</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.10 移除文件</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">移除文件</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">要从 Git 中移除某个文件，就必须要从已跟踪文件清单中移除（确切地说，是从暂存区域移除），然后提交。 可以用 git rm 命令完成此项工作，并连带从工作目录中删除指定的文件，这样以后就不会出现在未跟踪文件清单中了。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如果只是简单地从工作目录中手工删除文件，运行 git status 时就会在 “Changes not staged for commit” 部分（也就是 未暂存清单）看到：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ rm PROJECTS.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Your branch is up-to-date with 'origin/master'.</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes not staged for commit:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git add/rm &lt;file&gt;..." to update what will be committed)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">        deleted:    PROJECTS.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">no changes added to commit (use "git add" and/or "git commit -a")</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">然后再运行 git rm 记录此次移除文件的操作：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git rm PROJECTS.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">rm 'PROJECTS.md'</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes to be committed:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    deleted:    PROJECTS.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">下一次提交时，该文件就不再纳入版本管理了。 如果删除之前修改过并且已经放到暂存区域的话，则必须要用强制删除选项 -f（译注：即 force 的首字母）。 这是一种安全特性，用于防止误删还没有添加到快照的数据，这样的数据不能被 Git 恢复。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">另外一种情况是，我们想把文件从 Git 仓库中删除（亦即从暂存区域移除），但仍然希望保留在当前工作目录中。 换句话说，你想让文件保留在磁盘，但是并不想让 Git 继续跟踪。 当你忘记添加 .gitignore 文件，不小心把一个很大的日志文件或一堆 .a 这样的编译生成文件添加到暂存区时，这一做法尤其有用。 为达到这一目的，使用 --cached 选项：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git rm --cached README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">git rm 命令后面可以列出文件或者目录的名字，也可以使用 glob 模式。 比方说：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git rm log/\*.log</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">注意到星号 * 之前的反斜杠 \， 因为 Git 有它自己的文件模式扩展匹配方式，所以我们不用 shell 来帮忙展开。 此命令删除 log/ 目录下扩展名为 .log 的所有文件。 类似的比如：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git rm \*~</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">该命令为删除以 ~ 结尾的所有文件。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> </p>
</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.2.10.1 没有看懂，未来再说</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.11 移动文件</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">移动文件</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">不像其它的 VCS 系统，Git 并不显式跟踪文件移动操作。 如果在 Git 中重命名了某个文件，仓库中存储的元数据并不会体现出这是一次改名操作。 不过 Git 非常聪明，它会推断出究竟发生了什么，至于具体是如何做到的，我们稍后再谈。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">既然如此，当你看到 Git 的 mv 命令时一定会困惑不已。 要在 Git 中对文件改名，可以这么做：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git mv file_from file_to</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">它会恰如预期般正常工作。 实际上，即便此时查看状态信息，也会明白无误地看到关于重命名操作的说明：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git mv README.md README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git status</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">On branch master</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">Changes to be committed:</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">  (use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">    renamed:    README.md -&gt; README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">其实，运行 git mv 就相当于运行了下面三条命令：</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ mv README.md README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git rm README.md</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">$ git add README</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">如此分开操作，Git 也会意识到这是一次改名，所以不管何种方式结果都一样。 两者唯一的区别是，mv 是一条命令而另一种方式需要三条命令，直接用 git mv 轻便得多。 不过有时候用其他工具批处理改名的话，要记得在提交前删除老的文件名，再添加新的文件名。</p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.2.12 简化版本的《时光穿梭机》</div>
</div>
<div id="level3Indent">
<div id="level3Style">3.3 不同版本的穿梭方式</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.3.1 git reset --hard commit_id</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.3.1.1 在版本的历史之间穿梭</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.3.2 git log</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.3.2.1 穿梭前查看，了解回退到哪个版本</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.3.3 git reflog</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.3.3.1 重返未来，回到未来的哪个版本</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.3.4 官方复杂说明《查看提交历史》</div>
</div>
<div id="level3Indent">
<div id="level3Style">3.4 撤销修改</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.1 git checkout -- 文件名</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.2 第一种情况</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.2.1 修改了但是没有add到暂存区</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.2.2 直接使用命令</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.3 第二种情况</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.3.1 修改了已经add到暂存区</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.3.2 先使用git reset HEAD 文件名</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.3.3 再使用该命令</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.4 第三种情况</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.4.1 修改+add+commit</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.4.4.2 可以使用版本回退</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.5 总结</div>
<div id="notesStyle">
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">
<br></br>
</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml">场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。</p>
<p xmlns:pri="http://schemas.mindjet.com/MindManager/Primitive/2003" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.w3.org/1999/xhtml"> </p>
</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.4.6 另外一种版本</div>
</div>
<div id="level3Indent">
<div id="level3Style">3.5 删除文件</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.5.1 rm 文件名：删除文件</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.5.2 确实要删除文件</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.5.2.1 git rm 文件名</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.5.2.2 git commit</div>
</div>
<div id="level4Indent">
<div id="level4Style">3.5.3 删除错了，回退</div>
</div>
<div id="level5Indent">
<div id="level5Style">3.5.3.1 git checkout --文件名</div>
</div>
<div id="level2Indent">
<div id="level2Style">4 Git分支使用</div>
</div>
<div id="level3Indent">
<div id="level3Style">4.1 创建与合并分支</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.1 git branch：查看分支</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.2 git branch &lt;name&gt;：创建分支</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.3 git checkout &lt;name&gt;：切换分支</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.4 git checkout -b &lt;name&gt;：创建+切换分支：</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.5 git merge &lt;name&gt;：合并某分支到当前分支</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.1.6 git branch -d &lt;name&gt;：删除分支</div>
</div>
<div id="level3Indent">
<div id="level3Style">4.2 解决冲突的方案</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.2.1 git log --graph：查看分支合并图</div>
</div>
<div id="level3Indent">
<div id="level3Style">4.3 分支管理策略</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.3.1 master分支非常稳定</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.1.1 仅用来发布新版本</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.3.2 dev不稳定</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.2.1 用来工作</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.2.2 发布1.0版本的时候，把dev合并至master</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.2.3 在master上发布1.0版本</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.3.3 多个小伙伴</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.3.1 wangcc</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.3.2 caie</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.3.3 各自的分支</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.3.4 完成后合并至dev就好了</div>
</div>
<div id="level5Indent">
<div id="level5Style">4.3.3.5 </div>
</div>
<div id="level4Indent">
<div id="level4Style">4.3.4 git merge --no-ff -m "merge with no-ff" dev</div>
</div>
<div id="level3Indent">
<div id="level3Style">4.4 bug&amp;feature分支策略</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.4.1 因为关联不大，所以没有继续学习</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.4.2 但是理念都是在全新的分支上操作</div>
</div>
<div id="level3Indent">
<div id="level3Style">4.5 多人协作</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.5.1 首先，用git push origin branch-name推送自己的修改；</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.5.2 如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.5.3 如果合并有冲突，则解决冲突，并在本地提交；</div>
</div>
<div id="level4Indent">
<div id="level4Style">4.5.4 没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！</div>
</div>
<div id="level2Indent">
<div id="level2Style">5 标签使用</div>
</div>
<div id="level3Indent">
<div id="level3Style">5.1 git tag &lt;name&gt;：新建标签</div>
</div>
<div id="level2Indent">
<div id="level2Style">6 其他教程</div>
</div>
<div id="level3Indent">
<div id="level3Style">6.1 廖雪峰</div>
</div>
<div id="level3Indent">
<div id="level3Style">6.2 沉浸式学习</div>
</div>
<div id="level2Indent">
<div id="level2Style">7 应用</div>
</div>
<div id="level3Indent">
<div id="level3Style">7.1 《使用Git和MD编写精美图书》</div>
</div>
<div id="level3Indent">
<div id="level3Style">7.2 《如何使用Github进行在线写作》</div>
</div>
</body>
</html>
