---
layout: post
title: "Weekly Tech Report 2015-11-09"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, java, pipe, log, watchdog]
---
{% include JB/setup %}

## Weekly Tech Report 2015-11-09

### Learning

+   [Introduction to Named Pipes] [pipe-intro]

    Pipe Madness:
        echo -n x | cat - pipe1 > pipe2 &
        cat <pipe2 > pipe1
    Neat named pipes:
        ls | tee >(grep foo | wc >foo.count) \
                 >(grep bar | wc >bar.count) \
                 | grep baz | wc >baz.count
                 
    > [Piping and Redirection](http://ryanstutorials.net/linuxtutorial/piping.php)

[pipe-intro]: http://www.linuxjournal.com/article/2156?page=0,0

### Course

+   [Collected Java Practices](http://www.javapractices.com/home/HomeAction.do)

    javapractices.com offers concise presentations of Java practices, tasks, and designs, illustrated with syntax-highlighted code examples.

    > [Conditional compile](http://www.javapractices.com/topic/TopicAction.do?Id=64)

### Article

+   [Kibana+Logstash+Elasticsearch for Log Querying] [log-elk]

    Chinese blog, Kibana is a web shell, LogStash is for collecting all logs, 
    Elasticsearch is for searching

    > [LogStash+Kibana3 Setting Up](http://www.tuicool.com/articles/eUf2Ab)  
    > [Installing ELK+redis](http://aofengblog.blog.163.com/blog/static/6317021201401664935685)
    > [Install LogStash on Centos](http://www.ttlsa.com/log-system/installing-logstash-on-rhel-and-centos/)
    > [LogStash, Log Analysis and Display](http://www.linuxidc.com/Linux/2014-03/97863.htm)

[log-elk]: http://www.cnblogs.com/ibook360/archive/2013/03/15/2961428.html

### Blog

+   [The Java Specialists' Newsletter](http://www.javaspecialists.eu/index.jsp)

    Community of Java programmers

### Docs

+   [The Java Tutorials](https://docs.oracle.com/javase/tutorial)

    > [Fork/Join](https://docs.oracle.com/javase/tutorial/essential/concurrency/forkjoin.html)  
    > [Fork and Join: Java Can Excel at Painless Parallel Programming Too!](http://www.oracle.com/technetwork/articles/java/fork-join-422606.html)

### Reading

+   [Linux Programmer's Guide] [linux-program]

    The Linux Programmer's Guide is meant to do what the name implies -- 
    It is to help Linux programmers understand the peculiarities of Linux.

[linux-program]: http://www.tldp.org/LDP/lpg/node1.html

+   [From Runtime.exec() to ProcessBuilder] [java-process]

    Before JDK 5.0, the only way to fork off a process and execute it local to
    the user runtime was to use the exec() method of the java.lang.Runtime 
    class. JDK 5.0 adds a new way of executing a command in a separate process,
    through a class called ProcessBuilder.

[java-process]: http://www.java-tips.org/java-se-tips-100019/88888889-java-util/426-from-runtimeexec-to-processbuilder.html

+   [Talk and Review: "LogStash, make log managing easy"] [logstash-review]

    James Turnbull writes the book "LogStash", and this article gives a brief
    review for this book.

[logstash-review]: http://www.infoq.com/cn/articles/review-the-logstash-book

### Open Source

+   [logstash](https://github.com/elastic/logstash)

    transport and process your logs, events, or other data  
    <https://www.elastic.co/products/logstash>

+   [Watchdog](https://github.com/dandaner/Watchdog)

    android java watchdog daemon

+   [watchdogd](https://github.com/smartkiosk/watchdogd)

    WatchDog communication daemon

+   [linux-watchdog](https://github.com/NHellFire/linux-watchdog)

    Linux watchdog daemon

### Problems

+   [What is operator new(unsigned int)?] [problem-1]

    _Znwj is new, and _Znaj is new[].

[problem-1]: http://reverseengineering.stackexchange.com/questions/4402/what-is-operator-newunsigned-int

+   [Why application is dying randomly?] [problem-2]

    When running out of memory, one of the risks might be going native.
    + [Fatal Signal 11](http://stackoverflow.com/questions/12575357/fatal-signal-11)
    + [Android NDK Segmentation Error](http://stackoverflow.com/questions/11244120/android-ndk-segmentation-error)
    + [SIGNAL 11 SIGSEGV crash Android](http://stackoverflow.com/questions/4973310/signal-11-sigsegv-crash-android)
    Conflicts between two threads.
    + [Invalid heap address and fatal signal 11](http://stackoverflow.com/questions/10662446/invalid-heap-address-and-fatal-signal-11)
    Memory Corruption.
    + [Fatal signal 11 and INVALID HEAP ADDRESS IN dlfree error when using glShaderBinary](http://stackoverflow.com/questions/12246312/fatal-signal-11-and-invalid-heap-address-in-dlfree-error-when-using-glshaderbina)

[problem-2]: http://stackoverflow.com/questions/13196013/why-application-is-dying-randomly

+   [Foolproof cross-platform process kill daemon] [problem-3]

    The problem essentially was a race condition.

[problem-3]: http://stackoverflow.com/questions/9400724/foolproof-cross-platform-process-kill-daemon

+   [Linux: Writing a watchdog to monitor multiple processes] [problem-4]

    Make it possible that the parent process watches over its children.
    Or use supervisor tools:  [Monit], [Supervise], [Upstart], [god], 
    [daemonize], [ daemontools], [supervisord], ...

[problem-4]: http://unix.stackexchange.com/questions/7658/linux-writing-a-watchdog-to-monitor-multiple-processes
[monit]: http://mmonit.com/monit/
[supervise]: http://cr.yp.to/daemontools/supervise.html
[upstart]: http://upstart.ubuntu.com/
[daemontools]: http://cr.yp.to/daemontools.html
[supervisord]: http://supervisord.org/
[god]: http://godrb.com/
[daemonize]: http://bmc.github.com/daemonize/

+   [Conditional Java compilation] [problem-5]

    There isn't any support for conditional compilation in Java. You 
    can set up 'final' fields and ifs to get the compiler to optimize 
    the compiled byte-codes.

    > [how to prevent code chunks from being compiled?] [problem-51]

[problem-5]: http://stackoverflow.com/questions/1922521/conditional-java-compilation
[problem-51]: http://stackoverflow.com/questions/4526113/java-conditional-compilation-how-to-prevent-code-chunks-from-being-compiled

+   [Why use a named pipe instead of a file?] [problem-6]

    a `named pipe` is a special instance of a file that has no contents on the filesystem.

[problem-6]: http://askubuntu.com/questions/449132/why-use-a-named-pipe-instead-of-a-file


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/