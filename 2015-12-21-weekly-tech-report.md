---
layout: post
title: "Weekly Tech Report 2015-12-21"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, github, kvm, libvirt, android]
---
{% include JB/setup %}

## Weekly Tech Report 2015-12-21

### Learning

+   [GitHub Awesome Courses] [awesome-computer]

    A summary in Chinese for [Awesome Courses] on [GitHub], including computer
    science, and many languages, etc

    > [GitHub Awesome Courses: C++ Resources] [awesome-c++]  
    > [GitHub Awesome Courses: C Resources] [awesome-c]  
    > [GitHub Awesome Courses: Java Resources] [awesome-java]  
    > [GitHub Awesome Courses: Go Resources] [awesome-go]  
    > [GitHub Awesome Courses: PHP Resources] [awesome-php]  
    > [GitHub Awesome Courses: Python Resources] [awesome-python]  
    > [GitHub Awesome Courses: Sysadmin Resources] [awesome-sysadmin]  
    > [GitHub Awesome Courses: Web Optimizing Resources] [awesome-web]  
    > [GitHub Awesome Courses: React Resources] [awesome-react]

[github]: https://github.com
[awesome courses]: https://github.com/prakhar1989/awesome-courses
[awesome-computer]: http://top.jobbole.com/18025/
[awesome-c++]: http://top.jobbole.com/14380/
[awesome-c]: http://top.jobbole.com/17557/
[awesome-java]: http://top.jobbole.com/15689/
[awesome-go]: http://top.jobbole.com/3600/
[awesome-php]: http://top.jobbole.com/3260/
[awesome-python]: http://top.jobbole.com/4866/
[awesome-sysadmin]: http://top.jobbole.com/2942/
[awesome-web]: http://top.jobbole.com/15613/
[awesome-react]: http://top.jobbole.com/15576/

+   [KVM Intro] [kvm-intro]

    Kernel-Based Virtual Machine, or KVM, is a kernel module on Linux, which
    enables Linux to be a Hypervisor. KVM is native full-virtualization solution
    on Linux, while QEMU is a pure software implementing of virtualization.
    
    > [1. Intro and Installation] [kvm-intro]  
    > [2. CPU and Memory Virtualization] [kvm-intro-2]  
    > [3. I/O: QEMU Full-Virtualization and Para-Virtualization] [kvm-intro-3]  
    > [4. I/O: PCI/PCIe Devices Allocating and SR-IOV] [kvm-intro-4]  
    > [5. Libvirt Inro] [kvm-intro-5]  
    > [6. Nova: Managing QEMU/KVM VM via Libvirt] [kvm-intro-6]  
    > [7. Snapshot] [kvm-intro-7]  
    > [8. Migration] [kvm-intro-8]

[kvm-intro]: http://www.cnblogs.com/sammyliu/p/4543110.html
[kvm-intro-2]: http://www.cnblogs.com/sammyliu/p/4543597.html
[kvm-intro-3]: http://www.cnblogs.com/sammyliu/p/4543657.html
[kvm-intro-4]: http://www.cnblogs.com/sammyliu/p/4548194.html
[kvm-intro-5]: http://www.cnblogs.com/sammyliu/p/4558638.html
[kvm-intro-6]: http://www.cnblogs.com/sammyliu/p/4568188.html
[kvm-intro-7]: http://www.cnblogs.com/sammyliu/p/4468757.html
[kvm-intro-8]: http://www.cnblogs.com/sammyliu/p/4572287.html%20

+   [Libvirt Virtualiztion Wiki Pages] [libvirt-wiki]

    This is the libvirt WIKI for user contributed content. Libvirt is a toolkit
    to interact with the virtualization capabilities, with the goal "to provide
    a common and stable layer sufficient to securely manage domains on a node",
    and you can find any related topic at this wiki site about libvirt.

    > [Libvirt Networking] [libvirt-network]  
    > [Virsh Command Reference] [virsh-command]

[libvirt-wiki]: http://wiki.libvirt.org/page/Main_Page
[libvirt-network]: http://wiki.libvirt.org/page/Networking
[virsh-command]: http://libvirt.org/sources/virshcmdref/html-single/

### Article

+   [Setup Hugo Blog Step by Step] [hugo-step]

    Hugo is a lightweighting static pages generator, based on template system of
    GO language. This article presents how to build a personal blog using Hugo
    step by step.

[hugo-step]: https://www.goodmemory.cc/%E4%B8%80%E6%AD%A5%E4%B8%80%E6%AD%A5%E6%95%99%E4%BD%A0%E7%94%A8hugo%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2/

+   [Memory Allocator] [memory-alloc]

    The essential thoughts of meomery allocator are similar, the difference are
    algorithms and metadata. It mentions [ptmalloc], [tcmalloc], and [jemalloc],
    also summarizes three essential thoughts:
    + basic design: define memory pool by chunks, small memory sorted by size 
      class, big memory managed by pages (4K)
    + recycle and prediction: merge small memory when neccessary, keep memory on
      condition, release to system if not used any more
    + optimize multi-thread performance: in multi-thread, each thread ownes a
      separated memory segment, Thread Local Storage, or TLS, to avoid locking

[memory-alloc]: http://blog.csdn.net/horkychen/article/details/35735103
[ptmalloc]: http://download.csdn.net/download/csuideal/4829502
[tcmalloc]: http://jamesgolick.com/2013/5/19/how-tcmalloc-works.html
[jemalloc]: http://wangkaisino.blog.163.com/blog/static/1870444202011431112323846/

+   [Android Push by PHP and MQTT] [push-demo]

    Pratise Android Push using PHP and MQTT, the original demo is from Tokudu

    > [Relly Small Message Broker download] [rsmb-download]  
    > [PHP MQTT with SAM download] [phpmqtt-download]  
    > [Android Push Demo] [pushdemo-download]

[push-demo]: http://blog.csdn.net/wuzehai02/article/details/8150159
[rsmb-download]: http://download.csdn.net/detail/wuzehai02/4735055
[phpmqtt-download]: http://download.csdn.net/detail/wuzehai02/4735078
[pushdemo-download]: http://download.csdn.net/detail/wuzehai02/4735172

+   [Knowledge About Floating-point Number You Should Know] [float-know]

    In binary format, floating-point number is formed by: Sign (1bit) + Exponent
    (8bits) + Mantissa (23bits). Usally floating-point number is normalized in
    computer -- assume that the leading binary digit is always 1, but to resolve
    precision lost, denormalized number is used, in which the leading digit is
    0; in many numerical calculation, denormalized floating-point number would
    result out unexcepted output.

[float-know]: http://blog.jobbole.com/86371/

+   [Summary of Learning Libvirt] [libvirt-summary]

    Virtual Cloud is implemented by three steps: virtualization, vm management,
    and cloud management. The article gives a summary of libvirt, libvirt api
    and virtsh.

[libvirt-summary]: http://blog.csdn.net/gaoxingnengjisuan/article/details/9674315

+   [Kvm Qemu Libvirt] [kvm-libvirt]

    It gives a clarify about three virtualization terms: kvm, qemu, and libvirt.

[kvm-libvirt]: http://kiwik.github.io/openstack/2014/05/04/KVM-QEMU-libvirt/

+   [CentOS/Redhat: KVM Bridged Network Configuration] [centos-bridge]

    With bridged networking you can share actual network device with KVM machines.
    You can choose to put multiple segments into one bridged network or to divide
    it into different networks interconnected by routers. The article shows how
    to setup bridged networking on CentOS or Redhat.

[centos-bridge]: http://www.cyberciti.biz/faq/rhel-linux-kvm-virtualization-bridged-networking-with-libvirt/

### Blog

+   [Xun TA](http://www.xuntayizhan.com/)

    A website telling story, recommending content, searching interest things

    > [Meet Programmer Boyfriend] [program-bf]  
    > [Love of Geek] [geek-love]

[program-bf]: http://www.xuntayizhan.com/blog/yu-jian-cheng-xu-yuan-nan-you/
[geek-love]: http://www.xuntayizhan.com/blog/ji-ke-ai-qing-zhi-yi-ai-ta-hai-shi-ai-wo/

+   [Inventory RSS Reader without Google Reader](http://www.williamlong.info/archives/3408.html)

    Google Reader had been closed, some alternatives could be chosen: [Feedly]
    , [XianGuo], [YouDao], [QQ Mail], [Douban 9taps]

[feedly]: http://www.feedly.com/
[xianguo]: http://xianguo.com/reader/
[youdao]: http://reader.youdao.com/
[qq mail]: https://mail.qq.com/
[douban 9taps]: http://9.douban.com/reader/

### Open Source

+   [Awesome Courses](https://github.com/prakhar1989/awesome-courses)

    A great share sponsored by prakhar1989 which makes awesome courses within
    university pages available online for free.

+   [Sherlock](https://github.com/phodal/sherlock)

    A plot tool to generate skill tree based on D3.js and KnockOut.js. Similar
    project by the same author: [Awesome Developer] and [Book Tree].

[awesome developer]: https://github.com/phodal/developer
[book tree]: https://github.com/phodal/booktree

+   [reveal.js](https://github.com/hakimel/reveal.js)

    A framework for easily creating beautiful presentations using HTML. Slides
    are written using HTML or Markdown, try it at <http://slides.com>.

+   [flask_reveal](https://github.com/dongweiming/flask_reveal)

    An online presentation looking like [slid.es](http://slid.es), based on
    [flask]/[mongoengine] and [reveal.js]

[flask]: https://github.com/mitsuhiko/flask
[mongoengine]: https://github.com/MongoEngine/mongoengine
[reveal.js]: https://github.com/hakimel/reveal.js

### Problems

+   [How do I connect to my running VM via virsh?] [problem-virsh]

    To enable `virsh console <domain>` to access vm console, you may insert the
    following code into <devices> closure of domain XML file:

        <serial type='pty'>
            <target port='0'/>
        </serial>
        <console type='pty'>
            <target type='serial' port='0'/>
        </console>
    or you can do more, with appending `console=ttyS0,115200` to the guest kernel
    command line, and then starting it, see [here] [problem-virdev]:

        $ virsh start vm --console

[problem-virsh]: http://askubuntu.com/questions/156564/how-do-i-connect-to-my-running-vm-via-virsh
[problem-virdev]: http://wiki.libvirt.org/page/Error_%22internal_error_cannot_find_character_device%22_when_trying_to_connect_a_domain's_console

+   [libvirt: fetch ipv4 address from guest] [problem-libvirt]

    You can get ip address from MAC address and ARP table:

        $ virsh domiflist <domain>
        $ arp -e
    or you can just read the lease file:

        $ cat /var/lib/libvirt/dnsmasq/default.leases

[problem-libvirt]: http://stackoverflow.com/questions/19057915/libvirt-fetch-ipv4-address-from-guest

+   [Splitting a Byte array] [problem-split]

    To split a byte array, you can use [Array.copyofRange] in Java 1.6 or higher,
    (or possible [System.arraycopy] in an older java version).
    *I suspect that why can't convert byte array to string, and split it to two
    string, then convert strings to byte arrays???*

[problem-split]: http://stackoverflow.com/questions/2253912/splitting-a-byte-array
[array.copyofrange]: http://java.sun.com/javase/6/docs/api/java/util/Arrays.html#copyOfRange%28byte%5b%5d,%20int,%20int%29
[system.arraycopy]: http://java.sun.com/j2se/1.5.0/docs/api/java/lang/System.html#arraycopy%28java.lang.Object,%20int,%20java.lang.Object,%20int,%20int%29

+   [How can I generate an MD5 hash?] [problem-md5]

    The `MessageDigest` can provide you with an instance of the MD5 digest.

        import java.security.*;
        ..
        byte[] bytesOfMessage = yourString.getBytes("UTF-8");
        MessageDigest md = MessageDigest.getInstance("MD5");
        byte[] thedigest = md.digest(bytesOfMessage);
    Sometimes you may create hex string also, try following code to convert a
    byte to hex string, it avoids hex string length to be 31, missing leading 0

        hexString.append(Integer.toHexString(0xFF & thedigest[i]));

[problem-md5]: http://stackoverflow.com/questions/415953/how-can-i-generate-an-md5-hash

+   [Insert string in beginning of another string] [problem-insert]

    You can use [StringBuilder.insert] doing this:

        _sb.insert(0, "Hello ");
    or you can use + operator on String:

        String s2 = "Hello " + _s;

[problem-insert]: http://stackoverflow.com/questions/1475807/insert-string-in-beginning-of-another-string

+   [Outofmemory Error in ObjectInputStream] [problem-oom]

    The Object serialization in Java migth cause this OOM, it's recommended:

        oos = new ObjectOutputStream(outFile);
        oos.writeObject(obj);
        oos.reset();
        oos.flush();
    see [JDK-4363937: ObjectOutputStream is creating a memory leak] [jdk-4363937]

[problem-oom]: http://www.coderanch.com/t/504342/java-io/java/Outofmemory-Error-ObjectInputStream
[jdk-4363937]: http://bugs.java.com/bugdatabase/view_bug.do?bug_id=4363937


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/
