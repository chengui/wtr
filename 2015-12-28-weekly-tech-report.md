---
layout: post
title: "Weekly Tech Report 2015-12-28"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, markdown, android, ant, gradle, mustache]
---
{% include JB/setup %}

## Weekly Tech Report 2015-12-28

### Learning

+   [Markdown Basic and Syntax] [markdown]
    
    Markdown is a lightweight markup language with plain text, created by [John 
    Gruber] and [Aaron Swartz]. It is enabling people "to write using an 
    easy-to-read, easy-to-write plain text format, and optionally convert it to 
    structurally valid XHTML (or HTML)” ([Wikipedia][markdown wiki]).

    > Markdown Basic: <http://daringfireball.net/projects/markdown/basics>  
    > Markdown Syntax: <http://daringfireball.net/projects/markdown/syntax>  
    > Basic in Chinese: <http://wowubuntu.com/markdown/basic.html>  
    > Syntax in Chinese: <http://wowubuntu.com/markdown/index.html>  

[markdown]: http://daringfireball.net/projects/markdown/
[john gruber]: https://en.wikipedia.org/wiki/John_Gruber
[aaron swartz]: https://en.wikipedia.org/wiki/Aaron_Swartz
[markdown wiki]: https://en.wikipedia.org/wiki/Markdown

+   [PHP Markdown Extra] [markdown-extra]

    Markdown Extra is an extension to PHP/Python/Ruby Markdown implementing, and
    adds some missing features in plain Markdown syntax. It is supported in some
    [Content Management System], including [Drupal], [TYPO3], and [MediaWiki].

[markdown-extra]: https://michelf.ca/projects/php-markdown/extra/
[content management system]: https://en.wikipedia.org/wiki/Content_management_system
[Drupal]: https://drupal.org/project/markdowneditor
[TYPO3]: http://typo3.org/extensions/repository/view/markdown_content
[MediaWiki]: http://www.mediawiki.org/wiki/Extension:MarkdownExtraParser

+   [GitHub Flavoured Markdown] [markdown-gfm]

    GitHub Flavoured Markdown, or GFM, is used by GitHub across the site -- in
    issues, comments, and pull requests. It differs from stardard Markdown in a
    few significant ways, and adds some additional functionality.

    > Matering Markdown: <https://guides.github.com/features/mastering-markdown/>   
    > Writing on GitHub: <https://help.github.com/categories/writing-on-github/>

[markdown-gfm]: https://help.github.com/articles/github-flavored-markdown/

+   [Pandoc and Pandoc Markdown] [pandoc]

    Pandoc is an open-source document converter, widely used as a writing tool
    and as a basis for publishing workflows. The most thoroughly supported file
    format is an extension to Markdown. It is used by [Architect] and [RStudio]
    with Markdown files, statistical analysis in [R] and processed with [Knitr].

    > Pandoc Website: <http://pandoc.org/>  
    > Pandoc Markdown: <http://pandoc.org/README.html#pandocs-markdown>  
    > Syntax in Chinese: <http://pages.tzengyuxio.me/pandoc/>

[pandoc]: https://en.wikipedia.org/wiki/Pandoc
[architect]: https://en.wikipedia.org/wiki/Architect_(software)
[rstudio]: https://en.wikipedia.org/wiki/RStudio
[r]: https://en.wikipedia.org/wiki/R_(programming_language)
[knitr]: https://en.wikipedia.org/wiki/Knitr

+   [Mustache template system] [mustache]

    Mustache is a simple web template system, is described as a "logic-less"
    system, with named "Mustache" because of heavy use of curly braces {}, that
    resemble a sideways *moustache*. It is used mainly for mobile and web 
    application.

    > Mustache Website: <http://mustache.github.io/>  
    > Mustache Tutorial: <http://coenraets.org/blog/2011/12/tutorial-html-templates-with-mustache-js/>  
    > Mustache Samples: <http://coenraets.org/tutorials/mustache/>

[mustache]: https://en.wikipedia.org/wiki/Moustache

+   [Android Build System Overview] [android-build]

    The Android build system is the toolkit you use to build, test, run and 
    package your apps. The build system can run as an integrated tool from the 
    Android Studio menu and independently from the command line. 

    > Managine projects from CLI: <http://developer.android.com/tools/projects/projects-cmdline.html>  
    > Building projects from CLI: <http://developer.android.com/tools/building/building-cmdline.html>

[android-build]: http://developer.android.com/sdk/installing/studio-build.html

+   [Build Android Application From Linux Command Line] [android-cli]

    How to build Android project on Linux distro? The series presents the whole
    procedure of building android project from Linux command line, including
    how to use Android NDK/SDK of Linux version, how to build Android package by
    using Ant, how to sign Android apk and etc.

    > [1. About Android Projects] [android-cli]  
    > [2. Managing Projects From Command Line] [android-cli-2]  
    > [3. Workflow of Building] [android-cli-3]  
    > [4. Building From Command Line] [android-cli-4]  
    > [5. Ant Building Command] [android-cli-5]  
    > [6. Signing Android Application] [android-cli-6]  
    > [7. Automatic Building] [android-cli-7]

[android-cli]: http://www.cnblogs.com/ifantastic/p/3976742.html
[android-cli-2]: http://www.cnblogs.com/ifantastic/p/3977022.html
[android-cli-3]: http://www.cnblogs.com/ifantastic/p/3977672.html
[android-cli-4]: http://www.cnblogs.com/ifantastic/p/3979063.html
[android-cli-5]: http://www.cnblogs.com/ifantastic/p/3979260.html
[android-cli-6]: http://www.cnblogs.com/ifantastic/p/3981017.html
[android-cli-7]: http://www.cnblogs.com/ifantastic/p/3981295.html

+   [Gradle Learning] [gradle-learn]

    A series about learning Gradle, a build system used for Java application.
    It includes creating build tasks, gradle syntax, increment building, gradle
    plugin, dependencies and etc.

    > [1. Quick Start to Gradle] [gradle-learn]  
    > [2. Multi Ways to Create Tasks] [gradle-learn-2]  
    > [3. Understand Gradle Syntax] [gradle-learn-3]  
    > [4. Incremental Building] [gradle-learn-4]  
    > [5. Customize Porject Property] [gradle-learn-5]  
    > [6. Use Java Plugin] [gradle-learn-6]  
    > [7. Dependencies Management] [gradle-learn-7]  
    > [8. Building Multi-Projects] [gradle-learn-8]  
    > [9. Customize Build Task] [gradle-learn-9]  
    > [10. Customize Gradle Plugin] [gradle-learn-10]  
    > Gradle Learning: <https://github.com/davenkin/gradle-learning>

[gradle-learn]: http://www.cnblogs.com/davenkin/p/gradle-learning-1.html
[gradle-learn-2]: http://www.cnblogs.com/davenkin/p/gradle-learning-2.html
[gradle-learn-3]: http://www.cnblogs.com/davenkin/p/gradle-learning-3.html
[gradle-learn-4]: http://www.cnblogs.com/davenkin/p/gradle-learning-4.html
[gradle-learn-5]: http://www.cnblogs.com/davenkin/p/gradle-learning-5.html
[gradle-learn-6]: http://www.cnblogs.com/davenkin/p/gradle-learning-6.html
[gradle-learn-7]: http://www.cnblogs.com/davenkin/p/gradle-learning-7.html
[gradle-learn-8]: http://www.cnblogs.com/davenkin/p/gradle-learning-8.html
[gradle-learn-9]: http://www.cnblogs.com/davenkin/p/gradle-learning-9.html
[gradle-learn-10]: http://www.cnblogs.com/davenkin/p/gradle-learning-10.html

+   [Getting Started With Gradle] [gradle-start]

    A Chinese translation of [Getting Started with Gradle Inroduction] 
    [gradle-intro]. Gradle is a build tool, based on Groovy DSL, and it's used
    in nowadays Android Build System. The series includes building Java project,
    building web application, building multi-projects application, dependencies
    and etc.

    > [1. Brief Intro] [gradle-start]  
    > [2. First Java Project] [gradle-start-2]  
    > [3. Dependencies Management] [gradle-start-3]  
    > [4. Building Binary Release] [gradle-start-4]  
    > [5. Building Multi-Projects] [gradle-start-5]  
    > [6. Building Web Application] [gradle-start-6]  
    > Gradle Examples: <https://github.com/pkainulainen/gradle-examples>

[gradle-start]: http://blog.jobbole.com/71999/
[gradle-start-2]: http://blog.jobbole.com/72558/
[gradle-start-3]: http://blog.jobbole.com/72992/
[gradle-start-4]: http://blog.jobbole.com/80340/
[gradle-start-5]: http://blog.jobbole.com/84471/
[gradle-start-6]: http://blog.jobbole.com/94707/
[gradle-intro]: http://www.petrikainulainen.net/programming/gradle/getting-started-with-gradle-introduction/

### Article

+   [Getting started to Markdown] [sspai]

    A brief intro of Markdown, including syntax and application.

[sspai]: http://sspai.com/25137

+   [A talk of Markdown writing] [yangzhiping]

    How to use Markdown to resolve problems in writing? How to use Markdown + R
    to write scentific article.

[yangzhiping]: http://www.yangzhiping.com/tech/r-markdown-knitr.html

+   [How to be more productive] [how-product]

    A Chinese translation of [HOWTO: Be more productive] [HOWTO], described how
    to spend time efficiently.

[how-product]: http://pages.tzengyuxio.me/articles/how-to-be-more-productive.html
[howto]: http://www.aaronsw.com/weblog/productivity

+   [Getting Started with Ant] [ant-start]

    Apache Ant is a build tool based on Java, similar to Make, but getting rid 
    of the disadvantage of Make. The article presents how to ue Ant in Windows.

[ant-start]: http://www.java3z.com/cwbwebhome/article/article2/2764.html

### Blog

+   [Yihui Xie] [yihui]

    He has been developing some [R] packages, such as [animation], [formatR], 
    and [knitr], as described, he likes [GitHub], [LyX] and [pandoc]. 

[yihui]: http://yihui.name/
[animation]: http://yihui.name/animation/
[formatr]: http://yihui.name/formatR/
[github]: https://github.com
[lyx]: http://www.lyx.org/

+   [Poem of Gongzhizhen] [gongzhizhen]

    A Chinese poem website, the page includes all poems authored by Gongzhizhen,
    who had lived in Qing dynasty.

[gongzhizhen]: http://www.ziyexing.cn/shici/gongzhizhen/gongzhizhen.htm

### Open Source

+   [Apache Ant](http://ant.apache.org/)

    Apache Ant is a Java library and cli tool to build Java Applications.

+   [JekyII](https://github.com/jekyll/jekyll)

    Jekyll is a blog-aware, static site generator in Ruby.

+   [Remark](https://github.com/gnab/remark)

    Remark is a simple, in-browser, markdown-driven slideshow tool.

+   [JPackage](http://www.jpackage.org/index.php)

    JPackage is a packaging tool for Java software on Linux distros, including
    rpm-based, deb-based, and urpmi-based as well.


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/
