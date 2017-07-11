---
layout: post
title: "Weekly Tech Report 2015-11-09"
date: 2015-11-09
description: "Weekly Tech Report"
category: wtr
tags: wtr android process gdb memory
excerpt: wtr
mathjax: true
---

* content
{:toc}

## Weekly Tech Report 2015-11-16

### Learning

+   [Memory FAQ] [memory-faq]

    A very useful summary for understanding memory

[memory-faq]: http://landley.net/writing/memory-faq.txt

+   [Unix Programming FAQ (v1.24)] [unix-faq]

    FAQ for Unix/Linux programmer.

[unix-faq]: http://www.lib.ru/UNIXFAQ/unixprogrfaq.txt

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


+   [pipe(7) - Linux man page] [pipe-man]

    > [Interprocess Communication (IPC), Pipes] [pipe-ipc]
    > [Pipe, Fork, Exec and Related Topics] [pipe-fork]
    > [Pipes and FIFOs] [pipe-chemnet]
    > [C Tutorial: Pipes] [pipe-rutgers]
    > [Programming with pipes] [pipe-program]

[pipe-man]: http://linux.die.net/man/7/pipe
[pipe-ipc]: https://www.cs.cf.ac.uk/Dave/C/node23.html
[pipe-fork]: http://www.cs.uleth.ca/~holzmann/C/system/pipeforkexec.html
[pipe-chemnet]: http://www.chemie.fu-berlin.de/chemnet/use/info/libc/libc_10.html
[pipe-rutgers]: https://www.cs.rutgers.edu/~pxk/416/notes/c-tutorials/pipe.html
[pipe-program]: http://crasseux.com/books/ctutorial/Programming-with-pipes.html

### Course

+   [Caltech Computer Science] [caltech-comp]

    The Computer Science Course for Caltech.edu

[caltech-comp]: http://users.cms.caltech.edu/~donnie/

+   [USNA Computer Science] [usna-comp]

    Including *Systems Programming*, *Operating Systems*.
    > [Lab 06: Fork-Exec-Wait, Repeat!] [usna-fork]

[usna-comp]: http://www.usna.edu/Users/cs/aviv/
[usna-fork]: http://www.usna.edu/Users/cs/aviv/classes/ic221/s14/lab/06/lab.html

+   [Regina Computer Science] [regina-comp]

    > [CS330 Intro to Processes, Forks & Exec] [regina-fork]

[regina-comp]: http://www.cs.uregina.ca/Links/class-info/330/
[regina-fork]: http://www.cs.uregina.ca/Links/class-info/330/Fork/fork.html

### Article

+   [Reap zombie processes using a SIGCHLD handler] [signal-sigcld]

    How to install a SIGCHLD handler for reaping zombie processes

    > [Linux Signals – Example C Program to Catch Signals] [signal-linux]
    > [System Interface Guide] [singal-syscall]

[signal-sigcld]: http://www.microhowto.info/howto/reap_zombie_processes_using_a_sigchld_handler.html
[signal-linux]: http://www.thegeekstuff.com/2012/03/catch-signals-sample-c-code/
[signal-syscall]: https://docs.oracle.com/cd/E19455-01/806-4750/signals-7/index.html

+   [YoLinux Tutorial: Fork, Exec and Process control] [yolinux-proc]

    fork(), vfork(), clone(), wait(), system(), popen(), exec(), execve(), 
    execl(), execlp(), execv(), execvp()

    > [Linux pipe] [pipe-csdn]

[yolinux-proc]: http://www.yolinux.com/TUTORIALS/ForkExecProcesses.html
[pipe-csdn]: http://blog.csdn.net/cation/article/details/2282866

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

+   [libc: Signal Handling] [libc-signal]

    The GNU C Library defines a variety of signal types to be handled by developer

    > [kill(2) - Linux man page] [man-kill]

[libc-signal]: http://www.gnu.org/software/libc/manual/html_node/Signal-Handling.html
[man-kill]: http://linux.die.net/man/2/kill

### Reading

+   [Dalvik VM Internals] [dalvik-internals]

    Dalvik means Android Runtime Virtual Machine

[dalvik-internals]: http://fiona.dmcs.pl/podyplomowe_smtm/smob3/Presentation-Of-Dalvik-VM-Internals.pdf

### Open Source

+   [chromeThread](https://github.com/lincleejun/chromeThread)

    chromeThread from open source project chrome browser.

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

+   [Which child process send SIGCHLD] [problem-5]

    > waitpid(): on success, returns the process ID of the child whose state has
    > changed;

[problem-5]: http://stackoverflow.com/questions/19814906/which-child-process-send-sigchld

+   [Understanding SIGCHLD when the child process terminates] [problem-5]

    The return value from `sleep()`:

    > Zero if the requested time has elapsed, or the number of seconds left to 
    > sleep, if the call was interrupted by a signal handler.

[problem-5]: http://stackoverflow.com/questions/14266485/understanding-sigchld-when-the-child-process-terminates

+   [C fork/exec with non-blocking pipe IO] [problem-6]

    One should **NOT** be trying to pass a child process a nonblocking descriptor.

    > [Example of nonblock in C] [problem-61]

[problem-6]: http://stackoverflow.com/questions/3326725/c-fork-exec-with-non-blocking-pipe-io
[problem-61]: http://www.chiark.greenend.org.uk/~peterb/linux/nonblock/pipe-testnonblock.c

+   [How to make child process die after parent exits?] [problem-7]

    + prctl(PR_SET_PDEATHSIG, SIGHUP);
    + TCP socket/lockfile polling
    + exchange 'parent' and 'child' process code
    + pipe communication
    + setgpid()
    + ...

    > [Designing a monitor process for monitoring and restarting processes] [problem-71]
    > [Grouping child processes with setgpid()] [problem-72]
    > [How can I handle sigchld in C] [problem-73]
    > [how to kill all child when parent exits] [problem-74]


[problem-7]: http://stackoverflow.com/questions/284325/how-to-make-child-process-die-after-parent-exits
[problem-71]: http://stackoverflow.com/questions/4126401/designing-a-monitor-process-for-monitoring-and-restarting-processes
[problem-72]: http://stackoverflow.com/questions/16639275/grouping-child-processes-with-setgpid
[problem-73]: http://stackoverflow.com/questions/7171722/how-can-i-handle-sigchld-in-c/7171836#7171836
[problem-74]: http://compgroups.net/comp.unix.programmer/how-to-kill-all-child-when-parent-exits/36841

+   [How to send a simple string between two programs using pipes?] [problem-8]

    Creating a FIFO by using the `mkfifo()` library function.

    > [UNIX Pipes Between Child Processes] [problem-81]

[problem-8]: http://stackoverflow.com/questions/2784500/how-to-send-a-simple-string-between-two-programs-using-pipes
[problem-81]: http://stackoverflow.com/questions/5060350/unix-pipes-between-child-processes


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/
