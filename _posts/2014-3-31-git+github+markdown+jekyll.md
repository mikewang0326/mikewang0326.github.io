---

layout: post
categories: [Computer Vision]
tags: [增强现实 ,AR, 机器视觉, 算法]

---

  按：
    
   本文是以对git，github熟悉为前提的。

### 一，	Install Jekyll in windows
   

   　　　[http://www.madhur.co.in/blog/2011/09/01/runningjekyllwindows.html](http://www.madhur.co.in/blog/2011/09/01/runningjekyllwindows.html "install jekyll in windows")


　　　**Note**：

　　　1，	安装完成Ruby之后，需要设置Ruby的环境变量，之后的命令都基于此。

　　　2，	在执行 **gem install jekyll** 命令的时候，会耗时很长，没有关系，继续执行第二步。




###二，	Github pages
　　　[http://pages.github.com/](http://pages.github.com/ "github pages")

　　　目的：创建网站的repository，静态的相关文件都会存放在这里

###三，	Template

　　　借用了模板：[http://ellochen.github.io/](http://ellochen.github.io/)

　　　拷贝到对应的文件夹即可。

###四，	Jekyll和github page 关联
　　　[https://help.github.com/articles/using-jekyll-with-pages#keeping-jekyll-up-to-date](https://help.github.com/articles/using-jekyll-with-pages#keeping-jekyll-up-to-date)


　　　执行**gem install github-pages**命令，安装相应的关联包。

　　　附加的，可以安装jekyll与github相关的插件：

　　　[https://help.github.com/articles/using-jekyll-plugins-with-github-pages](https://help.github.com/articles/using-jekyll-plugins-with-github-pages)

###五，	Build

 　　　在对应的文件夹下，执行**jekyll build**命令。

###六，	Publish
　　　**Note**：

　　　　　　commit 之后，不会立即生效。初次publish的时候，会有如下的提示：

　![first publish delay page](https://raw.githubusercontent.com/mikewang0326/raw.mikewang0326.github.io/master/post/2014-3-31-git+github+markdown+jekyll/first_publish_delay_page.jpg)

###七，遇到的问题

　　　***1.error: invalid byte sequence in GBK***

　　　[http://jekyllrb.com/docs/windows/#installation](http://jekyllrb.com/docs/windows/#installation)

　　　解决方法：

　　　　　　　　执行命令: **chcp 65001**


　　　***2.Missing dependency: rdiscount***

　　　　其实是我拷贝的模板，安装的一个插件。

　　　　查看网上资料发现，原因是Jekyll默认的markdown解析器**maruku**对中文支持不够完善，所以果断换成**RDiscount**解析器，问题得到解决。

　　　　执行命令**gem install rdiscount**


　　　***3.Could not find a valid gem 'rdiscount' (>= 0)***

　　　　[https://github.com/davidfstr/rdiscount](https://github.com/davidfstr/rdiscount)


![first publish delay page](https://raw.githubusercontent.com/mikewang0326/raw.mikewang0326.github.io/master/post/2014-3-31-git+github+markdown+jekyll/error_can_not_find_a_valid_gem_rdiscount.jpg)
 
　　　***4.因为被墙掉的缘故，只能本地安装。***


　　　　下载地址：[http://rubygems.org/gems/rdiscount/versions/2.1.7](http://rubygems.org/gems/rdiscount/versions/2.1.7)


　　　　cd到对应文件夹下，执行命令：**gem install rdiscount-2.1.7.gem --local**


　　　***5.之后继续检查缺少的gem库，执行命令jekyll serve –watch***

　　　　错误信息如下：

![first publish delay page](https://raw.githubusercontent.com/mikewang0326/raw.mikewang0326.github.io/master/post/2014-3-31-git+github+markdown+jekyll/command_jekyll_serve_watch.jpg)
 
　　　　同样的方法，在本地安装。


　　　***6.invalid byte sequence in GBK。***

　　　　编码的问题，解决方案，根据对应的版本选择即可：

　　　　[http://kaiimeng.cn/my-first-octopress-blog/](http://kaiimeng.cn/my-first-octopress-blog/)


　　　***7.增加dispus***

　　　　拷贝模板后，评论功能失效，注册dispus账户，更新name即可

　　　***8.没有反馈邮件的问题***

　　　　犯了一个特别2b的问题，就是google page的名字必须和github的账号名字一致。

###八，	如何调试
　　　其实就是如何输出log，帮助查找问题

　　　***1.cd到目录下***

　　　***2.执行jekyll serve，即可在http://localhost:4000看到相应的页面效果。如果有问题，也会报错。***

###九，	中文乱码的问题
　　　[http://www.cnblogs.com/aleda/articles/Jekyll-in-Windows-following-Chinese-encoding-problem-solutions.html
](http://www.cnblogs.com/aleda/articles/Jekyll-in-Windows-following-Chinese-encoding-problem-solutions.html
)

###十，	其他
　　　***1.问题8耗费了很长的时间，建议阅读文档的时候一定细致。***

　　　***2.和模板的作者邮件沟通了下，虽然没帮助解决问题，但是心里上安慰踏实很多。***

　　　***3.最终发了封邮件给github的service，反应了下问题，不知道是不是因为是付费用户的缘故，反馈很快，很快解决了问题。***



       
