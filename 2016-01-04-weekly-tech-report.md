---
layout: post
title: "Weekly Tech Report 2016-01-04"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, mqtt, android, paho]
---
{% include JB/setup %}

## Weekly Tech Report 2016-01-04

### Learning

+   [MQTT Essentials] [mqtt-essentials]

	The HiveMQ blog posts the blog series of MQTT Essentials, it's a good summary
	to MQTT protocol.

	> [1. Introducing MQTT] [mqtt-essent-1]  
	> [2. Publish / Subscribe] [mqtt-essent-2]  
	> [3. Client, Broker and Connection Establishment] [mqtt-essent-3]  
	> [4. MQTT Publish, Subscribe and Unsubscribe] [mqtt-essent-4]  
	> [5. MQTT Topics & Best Practices] [mqtt-essent-5]  
	> [6. MQTT Quality of Service Levels] [mqtt-essent-6]  
	> [7. Persistent Session and Queuing Messages] [mqtt-essent-7]  
	> [8. Retained Messages] [mqtt-essent-8]  
	> [9. Last Will and Testament] [mqtt-essent-9]  
	> [10. Keep Alive and Client Take-Over] [mqtt-essent-10]  
	> [Special: MQTT over Websockets] [mqtt-essent-11]

[mqtt-essentials]: http://forkbomb-blog.de/2015/all-you-need-to-know-about-mqtt
[mqtt-essent-1]: http://www.hivemq.com/mqtt-essentials-part-1-introducing-mqtt/
[mqtt-essent-2]: http://www.hivemq.com/mqtt-essentials-part2-publish-subscribe/
[mqtt-essent-3]: http://www.hivemq.com/mqtt-essentials-part-3-client-broker-connection-establishment/
[mqtt-essent-4]: http://www.hivemq.com/mqtt-essentials-part-4-mqtt-publish-subscribe-unsubscribe/
[mqtt-essent-5]: http://www.hivemq.com/mqtt-essentials-part-5-mqtt-topics-best-practices/
[mqtt-essent-6]: http://www.hivemq.com/mqtt-essentials-part-6-mqtt-quality-of-service-levels/
[mqtt-essent-7]: http://www.hivemq.com/mqtt-essentials-part-7-persistent-session-queuing-messages/
[mqtt-essent-8]: http://www.hivemq.com/mqtt-essentials-part-8-retained-messages/
[mqtt-essent-9]: http://www.hivemq.com/mqtt-essentials-part-9-last-will-and-testament/
[mqtt-essent-10]: http://www.hivemq.com/mqtt-essentials-part-10-alive-client-take-over/
[mqtt-essent-11]: http://www.hivemq.com/mqtt-essentials-special-mqtt-over-websockets/

+   [MQTT Community Wiki] [mqtt-wiki]

    The goal is to collect useful content to help users and developers navigate
    around the MQTT community and understand how best to make use of the 
    technology.

[mqtt-wiki]: https://github.com/mqtt/mqtt.github.io/wiki

+   [MQTT Protocol Specification] [mqtt-spec]

    MQTT is a Client/Server publish/subscribe messaging transport protocol, it's
    ligth weight, open, simple, and designed so as to be easy to implement.

    > [OASIS Standard Specification] [mqtt-spec]  
    > [IBM/Eurotech Specification] [mqtt-ibm]  
    > [MQTT Man Page] [mqtt-man]  
    > [Involve Android Phone to IoT via WebSphere MQTT] [mqtt-iot]

[mqtt-spec]: http://docs.oasis-open.org/mqtt/mqtt/v3.1.1/os/mqtt-v3.1.1-os.html
[mqtt-ibm]: http://public.dhe.ibm.com/software/dw/webservices/ws-mqtt/mqtt-v3r1.html
[mqtt-man]: http://mosquitto.org/man/mqtt-7.html
[mqtt-iot]: https://www.ibm.com/developerworks/cn/websphere/library/techarticles/1109_wangb_mqandroid/1109_wangb_mqandroid.html

### Article

+   [Reading Notes of "TCP/IP Illustrated"] [read-notes-tcp]

    A reading notes in chinese for the classic book "TCP/IP Illustrated".

[read-notes-tcp]: http://www.cnblogs.com/fengzanfeng/articles/1339347.html

+   [Deep Experiment on Android Permissions] [deep-android-perm]

    Android Permissions has different levels: normal, dangerous, signature, 
    signature or system. To perform your permission, you must declare <permission>
    tags on AndroidManifest.xml.

[deep-android-perm]: http://blog.csdn.net/t12x3456/article/details/7749200

+   [Complete Android Permissions] [comp-android-perm]

    Developer must declare the permissions they needed on AndroidManifest.xml,
    for the sake of security. It lists all permissions in Chinese.

[comp-android-perm]: http://www.cnblogs.com/ganzhijie/archive/2010/08/21/1805573.html

+   [Mosquitto and Broker] [mosquitto-broker]

    Mosquitto is a messaging broker implementation under BSD license. This article
    presents a demonstrated practise of Mosquitto on Windows Cygwin.

[mosquitto-broker]: http://blog.csdn.net/akof1314/article/details/7494572

+   [Practical MQTT with Paho] [practical-paho]

    A practical piece presents how to write a MQTT demo with Paho.

[practical-paho]: http://www.infoq.com/articles/practical-mqtt-with-paho

+   [An Exmaple of Using TLS with Paho Embedded C++ Client] [paho-mbed]

    It shows how to work with TLS by using CyaSSL TLS library on mbed platform.

[paho-mbed]: http://modelbasedtesting.co.uk/?p=181

+   [How to make MQTT connection work over SSL] [mqtt-ssl]

    It shows how to make the Paho Java client and the ActiveMQ broker talk over 
    SSL, both parties have to be supplied with neccessary digital cerificaties.

[mqtt-ssl]: https://github.com/Hill30/mqtt-client/wiki/How-to-make-MQTT-connection-work-over-SSL

+   [How to Use BKS in HTTPS] [keytool-bks]

    You can use keytool to create bks-format keystore file, and use it in HTTPS.

[keytool-bks]: http://www.cnblogs.com/duwei/p/3671966.html

+   [MQTT and CoAP, IoT Protocols] [mqtt-coap]

    The two protocols used in IoT, also two of the most promising for small devices
    are MQTT and CoAP, MQTT gives flexibility for binary data, and CoAP is designed
    for interoperability with the web.

[mqtt-coap]: https://eclipse.org/community/eclipse_newsletter/2014/february/article2.php

### Blog

+   [Learning Eclipse Paho: MQTT Implementation] [learning-paho]

    A summary of learning Eclipse Paho project, including an overview of MQTT,
    MQTT packet description, and source analysis of CommsSender/CommsReceiver.

	> [1. Paho: MQTT Implementation] [learning-paho]  
	> [2. Socket Internal Paho] [learning-paho-2]  
	> [3. Investigate Android Push] [learning-paho-3]

[learning-paho]: http://blog.csdn.net/yangzl2008/article/details/8861069
[learning-paho-2]: http://blog.csdn.net/yangzl2008/article/details/8866066
[learning-paho-3]: http://blog.csdn.net/yangzl2008/article/details/8860621

+   [5 Reasons to Replace PowerPoint with Google Slides] [google-slides]

    Why makes the switch for PowerPoint to Google Slides:
    +   Built For Collaboration
    +   Simple UI Encourage Simpler Presentation
    +   Offline Access for Editing and Presenting
    +   Access Presentation from Any Device
    +   Easy Web Publishing and Sharing

[google-slides]: https://www.insidehighered.com/blogs/technology-and-learning/5-reasons-replace-powerpoint-google-slides

### Open Source

+   [Paho MQTT/C](http://git.eclipse.org/c/paho/org.eclipse.paho.mqtt.c.git)

    A MQTT publish/subscribe client implementations in C language for use on 
    embedded platform

+   [PickMeUp](https://github.com/ibm-messaging/mqtt-PickMeUp.git)

    A sample ride sharing application that accompanies IBM Redbooks "Building 
    Realtime Mobile Solutions with MQTT and IBM Message Sight"

+   [MQTT.js](https://www.npmjs.com/package/mqtt)

    A client library for the MQTT protocal, written in JavaScript for node.js
    and the browser, it's under MIT license

### Problems

+   [checkSelfPermission always returns PERMISSION_GRANTED] [problem-p]

    For Android verision < Android M (6.0), everything will be ok. For Android
    M, if targetSdkVersion >= VERSOIN_CODES.M (23), Context#checkSelfPermission
    is ok, else use PermissionChecker#checkSelfPermission instead.

[problem-p]: http://my.oschina.net/u/990728/blog/549914?fromerr=PvyCq00O

+   [java.lang.SecurityException: Requires READ_PHONE_STATE] [problem-s]

    Append permission declaration on AndroidManifest.xml, see [here] [problem-s2]:

        <uses-permission android:name="android.permission.READ_PHONE_STATE" />

[problem-s]: http://www.cnblogs.com/dava/p/3698126.html
[problem-s2]: http://stackoverflow.com/questions/7178941/android-read-phone-state

+   [SSL23_GET_CLIENT_HELLO:unknown protocol] [problem-c]

    Correct protocol in server URI to "ssl://" and add `sslopts.enableServerAuth = 0`

[problem-c]: http://www.bandh.de/2015/02/05/using-tls-in-the-paho-mqtt-c-api-together-with-the-mosquitto-browser/

+   [How to Display Hidden Characters in vim?] [problem-v]

    Use the commands, see [Make Vim show ALL white spaces] [problem-v2]:

        :set listchars=eol:$,tab:>-,trail:~,extends:>,precedes:<
        :set list

[problem-v]: http://askubuntu.com/questions/74485/how-to-display-hidden-characters-in-vim
[problem-v2]: http://stackoverflow.com/questions/1675688/make-vim-show-all-white-spaces-as-a-character

+   [What happens if I define a 0-size array in C/C++?] [problem-z]

    Zero-size array is not allowed in standard C/C++, however it's been current
    use in C to indicate a variable length structure. See [GCC Doc] [problem-z2]
    and [zero length arrays vs. pointers] [problem-z3].

[problem-z]: http://stackoverflow.com/questions/9722632/what-happens-if-i-define-a-0-size-array-in-c-c
[problem-z2]: https://gcc.gnu.org/onlinedocs/gcc/Zero-Length.html
[problem-z3]: http://stackoverflow.com/questions/627364/zero-length-arrays-vs-pointers


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/



