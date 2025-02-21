LOFFER是个可以帮助你get off from LOFTER的软件（我知道这个pun很烂）。

这是一个可以通过Fork直接发布在GitHub的Jekyll博客，你不需要编写代码或使用命令行即可获得一个部署在GitHub的博客。

当你看到不认识的术语，请忽略它，我知道程序员不说人话，我都不是程序员但是我已经开始意识到这是因为我们不知道这些概念用人话怎么说。

以下我会尽量用人话解说如何使用这个……LOFFER。

## 注意

LOFFER是一个**博客模板**，使用GitHub Pages发布个人博客是没有任何问题的。 **但是:**

- **请勿发布成人向内容** 
- **不要将大量图片上传到GitHub**

如有疑问，请阅读[GitHub Pages官方说明](https://pages.github.com/)。

另外，同人作品更好的发布平台是[AO3](https://archiveofourown.org/)，你想你发在AO3还有tag还有kudos还有人看，是吧？


## 如何使用

首先，这个博客主题适应手机阅读，但是，要使用它建立你自己的博客，你需要上电脑操作。

### 第一步 Fork到你的GitHub

请点击[GitHub](https://github.com/)，注册一个GitHub账户。我们可以理解Git就是个文件版本管理系统，本身并不需要会代码即可使用。

现在你看到的LOFFER，是作为一个GitHub上的Repository（代码库）存在的，你可以把这个代码库复制到你自己的GitHub账户中，这个操作叫做Fork。

点击[LOFFER](https://github.com/FromEndWorld/LOFFER)，进入LOFFER的GitHub Repository页面，然后点Fork：

![gif](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/fork.gif)

然后你立刻就可以看到LOFFER再次出现，这次它已经属于你了，这里我建议你重命名它，点击settings，给你的博客起个名字（请尽量使用字母而非中文）。

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/rename.png)

然后，向下拉页面，你会看到“GitHub Pages”，这是GitHub内置的网站host服务，选择master，如图所示：

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/pages.png)

在几秒钟后，刷新此页面，你通常会看到这个绿色的东西（如果没看到，多等一会），你的网站已经发布成功，点击这个链接，即可查看：

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/published.png)

你可能会看到网站长得很丑，请继续下一步.

### 第二步 设置站点信息

在你的博客的GitHub代码库页面里，选择Code，文件列表里选择_config.yml，点击打开，点击右上角笔形图标修改文档。

修改完成后，点击“Commit changes”。每次修改过代码库并且commit后，GitHub Pages都会自动重新发布网站，只要等上几分钟，再次刷新你的博客页面，就会看到你的修改了。

还有一点，**LOFFER使用的是MIT协议，大意就是全部开源随意使用，如果你要保留自己博文的权利，请编辑LICENSE文件，写上类似“_posts中的文档作者保留权利”这样的内容。**

### 第三步 发布博文

在你的博客的GitHub代码库页面里，点开_posts文件夹，这里面就是你的博客文章。

这些文章使用的格式是Markdown，文件后缀名是md，这是一种非常简单易用的有格式文本标记语言，你应该已经注意到，在LOFFER自带的示例性博文中有一篇中文的Markdown语法介绍。

更简单的办法是使用[Typora](https://typora.io/)，这是一个全图形化界面，全实时预览的Markdown写作软件，非常轻量，而且免费。

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/Typora.png)

在发布博文前，你需要在文章的头部添加这样的内容，包括你的文章标题，发布日期，作者名，和tag等。

    ---
    layout: post
    title: LOFFER文档
    date: 2019-06-02
    Author: 来自中世界
    categories: 
    tags: [sample, document]
    comments: true
    --- 

完成后，保存为.md文件，然后上传到_posts文件夹，commit，很快就可以在博客上看到新文章了。

### 可选：图片怎么办？

少量图片可以上传到images文件夹，然后在博文中添加。

但是GitHub用来当做图床有滥用之嫌，如果你的博客以图片为主，建议选择外链图床，例如[sm.ms](https://sm.ms/)就是和很好的选择。

如果想要寻找更适合自己的图床，敬请Google一下。

在博文中添加图片的Markdown语法是：`![图片名](URL)`

### 可选：添加评论区

LOFFER支持Disqus评论，虽然Disqus很丑，但是它是免费的，设置起来又方便，因此大家也就不要嫌弃它。

首先，注册一个[Disqus](https://disqus.com/)账户，我们可以选择这个免费方案：

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/Disqus-plan.png)

注册成功后，新建一个站点（site），以LOFFER为例设置步骤如下：

首先站点名LOFFER，生成了shortname是loffer，类型可以随便选。

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/Disqus-1.png)

安装时选择Jekyll。

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/Disqus-2.png)

最后填入你的博客地址，语言可以选中文，点Complete，即可！

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/Disqus-3.png)

然后需要回到你的博客，修改_config.yml文件，在disqus字段填上你的shortname，commit，完成！

### 导入LOFTER的内容

这部分由于LOFTER的导出文件十分~~优秀~~，需要另外解决。

诸位可以使用[墨问非名太太的脚本](http://underdream.lofter.com/post/38ea7d_1c5d8a983)，其中选择Jekyll输出即可。

我个人也在折腾一个脚本，目前还没有完全debug清楚，不管如何，请先在lofter里导出一下，存在本地也是好的，贴吧可以让2017以前所有内容全部消失，中国互联网，没什么不可能发生的。

## 致谢

* [Jekyll](https://github.com/jekyll/jekyll) - 这是本站存在的根基
* [Kiko-now](<https://github.com/aweekj/kiko-now>) - 我首先是fork这个主题，然后再其上进行修改汉化，才有了LOFFER
* [Font Awesome](<https://fontawesome.com/>) - 社交网络图标来自FontAwesome的免费开源内容



## 帮助这个项目

介绍更多人来使用它，摆脱lofter自由飞翔！

当然如果单说写同人的话，我还是建议大家都去AO3，但是自家博客自己架也很酷炫，你还可以选择很多其他的forkable Jeykll主题，GitHub上有很多，或者试试其他博客架设工具，例如Hexo，与代码斗其乐无穷。

最后，回到[LOFFER](https://github.com/FromEndWorld/LOFFER)，给我点一个☆吧！

![img](https://raw.githubusercontent.com/FromEndWorld/LOFFER/master/images/givemefive.png)