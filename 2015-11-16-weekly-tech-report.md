---
layout: post
title: "Weekly Tech Report 2015-11-23"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, android, process, gdb, memory]
---
{% include JB/setup %}

## Weekly Tech Report 2015-11-30

### Learning

+   [Memory FAQ] [memory-faq]

    A very useful summary for understanding memory

[memory-faq]: http://landley.net/writing/memory-faq.txt

+   [Understanding the kill command] [proc-kill]

    This article covers the Linux kill command and how it sends signals to 
    terminate processes. Also why you should avoid using kill -9.

    > [Sending a Signal to Another Process: System Call kill()] [syscall-kill]

[proc-kill]: http://bencane.com/2014/04/01/understanding-the-kill-command-and-how-to-terminate-processes-in-linux/
[syscall-kill]: http://www.csl.mtu.edu/cs4411.ck/www/NOTES/signal/kill.html

+   [gdb debug an android application] [android-debug]

    How to remotely debug program on Android.

    > [Using gdb on Android] [android-gdb1]
    > [Using gdb to debug on Android] [android-gdb2]

[android-debug]: http://www.cnblogs.com/Fang3s/p/4097205.html
[android-gdb1]: http://blog.163.com/bjtornado@yeah/blog/static/69510484201081181657449/
[android-gdb2]: http://blog.csdn.net/jinzhuojun/article/details/7375048

+   [Tips for Optimizing Android* Application Memory Usage] [memory-tips]

    This article introduces Android Memory Management and explains various 
    aspects that play a role in the management system. Additionally, improving 
    memory management, detecting and avoiding memory leaks, and analyzing memory
    usage are covered.

[memory-tips]: https://software.intel.com/en-us/android/articles/tips-for-optimizing-android-application-memory-usage

+   [Analyze And Optimize Android Memory Usage] [memory-opt]

    To analyze memory usage:
    + procrank
    + dumpsys meminfo
    + adb shell showmap
    
    To optimize memory usage:
    + DDMS
    + MAT

    > [How To Discover Memory Usage of Android Application] [memory-usage]  
    > [Summary Analysis for Android Memory Usage] [memory-summary]

[memory-opt]: http://m.oschina.net/blog/186320
[memory-usage]: http://android.jobbole.com/80926/
[memory-summary]: http://kingbo203.iteye.com/blog/1988636

### Article


### Blog

+   [I Programmer] [i-programmer]

    A portal for programmers

[i-programmer]: http://www.i-programmer.info/

+   [Android Developers Blog] [android-blog]

    Official Blog for Android Developers.

    > [Process Stats: Understanding How Your App Uses RAM] [android-proc]  
    > [Memory Analysis for Android Application] [android-memory]

[android-blog]: http://android-developers.blogspot.hk/
[android-proc]: http://android-developers.blogspot.hk/2014/01/process-stats-understanding-how-your.html
[android-memory]: http://android-developers.blogspot.hk/2011/03/memory-analysis-for-android.html

### Docs

+   [Android Developers] [android-developers]

    > [Investigating Your RAM Usage] [android-debugging]  
    > [Memory Monitor Walkthrough] [android-monitor]

[android-developers]: http://developer.android.com/
[android-debugging]: http://developer.android.com/tools/debugging/debugging-memory.html
[android-monitor]: http://developer.android.com/tools/performance/memory-monitor/index.html

### Reading

+   [Dalvik VM Internals] [dalvik-internals]

[dalvik-internals]: http://fiona.dmcs.pl/podyplomowe_smtm/smob3/Presentation-Of-Dalvik-VM-Internals.pdf

### Problems

+   [cannot access memory at address 0X1] [problem-1]

    Confirm you has the permission and set the correct `solib-search-path`:
        set solib-search-path D:/android/android-ndk-r8d/samples/hello-jni/obj/local/armeabi

[problem-1]: http://stackoverflow.com/questions/14417895/cannot-access-memory-at-address-0x1-after-setting-up-gdb-and-eclipse-to-debug-sh

+   [A tool returned an error code from "Performing Post-Build Event..."] [problem-2]

    Set "properties -> Build Events -> Post-build event -> command line " to 
    empty on Virsual Studio.

[problem-2]: http://blog.csdn.net/lingxiu0613/article/details/6574914

+   [Dwarf Error: wrong version in compilation unit header] [problem-3]

    Changing `-g3` to `-g`, see also two solutions at [guiquanz.me]:
    + Upgrade gdb to match gcc
    + Add `-gdwarf-2 -gstrict-dwarf`

[problem-3]: http://stackoverflow.com/questions/11671009/dwarf-error-wrong-version-in-compilation-unit-header-is-4-should-be-2
[guiquanz.me]: http://guiquanz.me/2014/10/06/gdb-can-not-load-debug-information-for-bad-DWARF-version/

+   [How do I discover memory usage of my application in Android?] [problem-4]

    More details can be found at [Managine Your App's Memory] [android-docs]  
    Have a look at <http://www.pixelbeat.org/scripts/ps_mem.py>

[problem-4]: http://stackoverflow.com/questions/2298208/how-do-i-discover-memory-usage-of-my-application-in-android
[android-docs]: http://developer.android.com/training/articles/memory.html


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/