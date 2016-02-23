---
layout: post
title: "Weekly Tech Report 2015-11-30"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, push, gitbook, gcm/c2dm, lemp]
---
{% include JB/setup %}

## Weekly Tech Report 2015-11-30

### Learning

+   [How to Implement Push Notifications for Android] [push-tokudu]

    There are 3 generally accepted ways to implement push notifications for your Android app:

    + Poll
    + SMS 
    + Persistent TCP/IP

    Some Chinese relevant translations or referrences:
    > [Push Implemented in Android] [push-imp]  
    > [Android Push Notifications Guide] [push-guide]  
    > [How to Implement PushService in Android] [push-service]  
    > [Android Server Push - MQTT] [push-mqtt]  
    > [Really Small Message Broker] [rsmb]

[push-tokudu]: http://tokudu.com/post/50024574938/how-to-implement-push-notifications-for-android
[push-imp]: http://www.cnblogs.com/xirihanlin/archive/2011/12/06/2277807.html
[push-guide]: http://blog.csdn.net/joshua_yu/article/details/6563587
[push-service]: http://www.linuxidc.com/Linux/2012-06/62778.htm
[push-mqtt]: http://fanfq.iteye.com/blog/1405385
[rsmb]: https://www.ibm.com/developerworks/community/groups/service/html/communityview?communityUuid=d5bedadd-e46f-4c97-af89-22d65ffee070

+   [Study of Open Source Alternatives for Android Push] [push-jpush]

    A study of open source Android Push from JPush.

[push-jpush]: http://blog.jpush.cn/android_push_opensource_androidpn_xmpp_openfire/

+   [How To Install LEMP stack on CentOS 6] [lemp]

    LEMP stack is a group of open source software to get web servers up and 
    running. The acronym stands for Linux, nginx, MySQL, and PHP.

[lemp]: https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-on-centos-6

### Article

+   [What and Where Are Heap And Stack?] [heap-stack]

    Chinese translation of [StackOverflow] [stackoverflow-heapstack].

[heap-stack]: http://blog.jobbole.com/75321/
[stackoverflow-heapstack]: http://stackoverflow.com/questions/79923/what-and-where-are-the-stack-and-heap

+   [Push service from Google] [push-c2dm]

    To do push, some open source alternatives are available, like [MQTT],
    [Deacon], [Urban Airship]. This article shows how to use C2DM from Google
    to support push service, check [it] [push-demo] out.

[push-c2dm]: http://mylifewithandroid.blogspot.hk/2010/10/push-service-from-google.html
[mqtt]: http://knolleary.net/arduino-client-for-mqtt/
[deacon]: http://deacon.daverea.com/
[urban airship]: http://github.com/urbanairship/android-push-library
[push-demo]: http://pallergabor.uw.hu/androidblog/push.zip

+   [Android Push Notifications using GCM, PHP and MySQL] [push-gcm]

    Using GCM service you can send data to your application whenever new data is
    available instead of making requests to server in timely fashion.

[push-gcm]: http://www.androidhive.info/2012/10/android-push-notifications-using-google-cloud-messaging-gcm-php-and-mysql/

+   [Android push notifications (tutorial)] [push-tutor]

    C2DM alternatives: MQTT, Urban Airship

[push-tutor]: https://blog.serverdensity.com/android-push-notifications-tutorial/

### Blog


### Docs

### Reading

+   [A Programmer Prepares] [gitbook-prepares]

    Being a programmer, what should be prepared.

[gitbook-prepares]: https://www.gitbook.com/book/leohxj/a-programmer-prepares

+   [LeetCode Solution] [gitbook-leetcode]

    Summary for LeetCode problems.

[gitbook-leetcode]: https://www.gitbook.com/book/siddontang/leetcode-solution

### Open Source

+   [Choosing An Open Source License](http://choosealicense.com/)

    which license is the best choice for you? MIT, Apache, GPL, etc.?

+   [GitBook](https://github.com/GitbookIO)

    The simplest way to turn an idea into a book

+   [AndroidPushNotificationsDemo](https://github.com/tokudu/AndroidPushNotificationsDemo)

    A example of an android app that receives push notifications using MQTT.
    See http://tokudu.com/2010/how-to-implement-push-notifications-for-android

+   [PhpMQTTClient](https://github.com/tokudu/PhpMQTTClient)

    This is a simple example of how send MQTT messages using PHP.
    See http://tokudu.com/2010/how-to-implement-push-notifications-for-android

+   [Android Push Notification](https://sourceforge.net/projects/androidpn/)

    An open source project to provide push notification support for Android -- a xmpp based notification server and a client tool kit.

### Problems

+   [Determine if a process exists from its Process ID] [problem-1]

    Use `kill()` with signal 0: `kill(pid, 0)`

    > if sig is 0, then no signal is sent, but error checking is still performed
    > , this can be used to check for the existence of a process ID or process
    > group ID.

[problem-1]: http://stackoverflow.com/questions/12601759/determine-if-a-process-exists-from-its-process-id

+   [mysql how to fix Access denied for user 'root'@'localhost'] [problem-2]

    Follow the steps:

        $ mysqld --skip-grant-tables
        $ mysql -u root mysql
        $mysql> UPDATE user SET Password=PASSWORD('password') where USER='root';
        $mysql> FLUSH PRIVILEGES;
        $ /etc/init.d/mysql restart

[problem-2]: http://superuser.com/questions/603026/mysql-how-to-fix-access-denied-for-user-rootlocalhost

+   [Resolving "No input file specified" error with Php and Nginx] [problem-3]

    Set right fastcgi_param for Nginx `SCRIPT_FILENAME`.
    See also [How To Solve "No input file specified" With php and Nginx] [problem-31].

[problem-3]: http://nginxlibrary.com/resolving-no-input-file-specified-error/
[problem-31]: https://blog.martinfjordvald.com/2011/01/no-input-file-specified-with-php-and-nginx/


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/