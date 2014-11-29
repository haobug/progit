[![Build Status](https://secure.travis-ci.org/haobug/progit.png?branch=master)](https://travis-ci.org/haobug/progit)

# Pro Git Book Contents

这是《Pro Git》书的源代码。在共同创作 署名-相同方式共享 3.0（CC-NC-SA 3.0）
协议下发布。愿你喜欢，希望帮助你学习 Git，或者你可以在亚马逊网站订购 Apress
的纸质版本：

http://tinyurl.com/amazonprogit

当然你也可以在这下载到电子版本：

http://git-scm.com/book/

已经完整翻译成 10 种语言。

# 生成电子书

在 Fedora (16 或者更新的版) 你可以运行这样的命令：

    $ yum install ruby calibre rubygems ruby-devel rubygem-ruby-debug rubygem-rdiscount
    $ makeebooks en  # will produce a mobi

在 MacOS 上你可以：
	
1. 安装 ruby 和 rubygems
2. `$ gem install rdiscount`
3. 下载并安装 Calibre for MacOS. 如果想生成 pdf 你还需要下面的依赖：
    * pandoc: http://johnmacfarlane.net/pandoc/installing.html
    * xelatex: http://tug.org/mactex/
4. `$ makeebooks zh` #会生成 .mobi 格式电子书

在 Windows 上你可以这样：
	
1. 安装 ruby 和相关工具 http://rubyinstaller.org/downloads/
    * RubyInstaller (ruby & gem)
    * Development Kit (to build rdiscount gem)
2. 打开 `cmd` 然后 `$ gem install rdiscount`
3. 安装 Calibre for Windows http://calibre-ebook.com/download
4. `$ SET ebook_convert_path=c:\Program Files\Calibre2\ebook-convert.exe`. 按照你的 Calibre 安装路径修改。
5. 生成电子书:
    * `$ ruby makeebooks vi` #会生成 .mobi 格式电子书
    * `$ SET FORMAT=epub` 然后 `$ ruby makeebooks vi` #会生成 .epub 格式电子书

## pandoc 注意点

请尽量使用 Pandoc 的 1.11.1 或者更新的版本；因为旧版本（比如 1.9.1.1上）有一个 [bug](https://github.com/jgm/pandoc/issues/964) 会隐藏波浪号`~`后面一个单词。你可以用 `pandoc -v` 检查你的安装的是哪个版本。

# 勘误

如果你发现了任何技术上的错误，或者需要更正的，请直接[提交一个 issue](https://github.com/progit/progit/issues/new) 维护人员都会处理的。


# 翻译

如果你有兴趣翻译这本书，你的成果会被放到 git-scm.com 网站上。请把你的
翻译放在适当的子目录中，使用
[ISO 639](http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) 语言代码
命名，并且发起一个 pull request.

# 发起一个 pull request

* 你的文件内容请使用 UTF-8 编码。
* 不要把对原始英文的改动和翻译混在一起提交。
* 当你改动了一个翻译时，请在你的 pull request 以及你的 commit 消息前面添加 ISO 639 语言代码，比如 `[de] Update chapter 2`这样。请只 push 已经会存在的文件。
* 确保你的改动是可以自动 merged 的。维护人员不能做手工的 merge 工作。
* 确保发动能正确处理生成 PDF，电子书，或者 git-scm.com 网站。
