---
layout: post
title: "Weekly Tech Report 2015-11-30"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, jenkins, android, kvm, docker, qemu]
---
{% include JB/setup %}

## Weekly Tech Report 2015-11-30

### Learning

+   [How To Build Android Apps with Jenkins] [jenkins-android]

    To build Android Apps automatically, Jenkins is a good choice, integrated
    with version control like Git or Subversion, and Android build system Gradle
    or Ant.

    > [Building Gradle Projects with Jenkins CI] [build-gradle]  
    > [Jenkins Android Job Setup] [jenkins-job]  
    > [Configure your Android project on Jenkins] [config-android]

[jenkins-android]: https://www.digitalocean.com/community/tutorials/how-to-build-android-apps-with-jenkins
[build-gradle]: https://github.com/codepath/android_guides/wiki/Building-Gradle-Projects-with-Jenkins-CI
[jenkins-job]: http://flow.apphance.com/introduction/getting-started-with-projects/hello-android/android-project-setip
[config-android]: http://blog.zuehlke.com/en/configure-your-android-project-on-jenkins/

+   [Using Docker to run Jenkins jobs] [jenkins-docker]

    Dokcer helps to isolate a process and its dependencies, make it happen to
    start from the same initial state for each run, it is a very good property
    for CI to have reproducible without side effects.

    > [On Demand Jenkins Slaves Using Docker] [docker-slave]

[jenkins-docker]: https://iww.inria.fr/tech-zone/using-docker-to-run-jenkins-jobs/
[docker-slave]: https://developer.jboss.org/people/pgier/blog/2014/06/30/on-demand-jenkins-slaves-using-docker?_sscc=t

### Article

### Blog


+   [SmileJay](http://smilejay.com/)

    Focus on KVM appliance and Test technique

    > [Theory and Practice of KVM](http://smilejay.com/kvm_theory_practice/)


### Docs

+   [Docker Docs](https://docs.docker.com/)

    Docker is a platform for developers and sysadmins to develop, ship and run
    applications.

+   [QEMU Wiki](http://wiki.qemu.org/)

    QEMU is a generic and open source machine emulator and virtualizer. It can
    be used as a machine emulator, and also used as a virtualizer.

    > [Testing and System Images](http://wiki.qemu.org/Testing)
    > [QEMU/Images](https://en.wikibooks.org/wiki/QEMU/Images)
    > [CentOS 6.7 QEMU Image](https://stacklet.com/downloads/KVM-Disk-Image-CentOS-6.7-Lightweight-x86)

+   [Help KVM/Virsh]

    You can create, delete, run, stop, and manage your virtual machines from the
    command line, using a tool called virsh. Virsh is particularly useful for 
    advanced Linux administrators, interested in script or automating some 
    aspects of managing their virtual machines.

    > [KVM/Managing](https://help.ubuntu.com/community/KVM/Managing)

+   [The Android Source Code](https://source.android.com/source/index.html)

    Android is an open source software stack created for a wide array of devices
    with different form factors.

    > [Establishing a Build Environment](https://source.android.com/source/initializing.html)  
    > [Building the System](https://source.android.com/source/building.html)

+   [Virtualization SIG on CentOS](https://wiki.centos.org/SpecialInterestGroup/Virtualization)

    The CentOS Virt-SIG is a group of people coming together to promote and use 
    CentOS Linux as a base platform as a suitable platform for various 
    virtualisation efforts, and wants to build upon the already successfully 
    released Xen4CentOS project.

### Open Source

+   [libvirt-slave-plugin](https://github.com/jenkinsci/libvirt-slave-plugin)

    libvirt-slave-plugin for Jenkins CI adds a way to utilize guest domains 
    hosted on Xen or QEMU/KVM as build slaves.

+   [AndroidDevLinux](https://gist.github.com/venkateshshukla/9736261)

    Setting up your Linux for Android Application Development

### Problems

+   [failed to find Build Tools revision *.0.0] [problem-1]

    Try to update the version of Android SDK and Platform Tools, and confirm
    that <SDK>/tools and <SDK>/platform-tools are added into PATH.

[problem-1]: http://stackoverflow.com/questions/16619773/failed-to-import-new-gradle-project-failed-to-find-build-tools-revision-0-0

+   [failed to install docker on CentOS 6] [problem-2]

    > Docker requires a 64-bit installation regardless of your CentOS version. 
    > Also, your kernel must be 3.10 at minimum. CentOS 7 runs the 3.10 kernel, 
    > 6.5 does not. We make an exception for CentOS 6.5. To run Docker on 
    > CentOS-6.5 or later, you need kernel 2.6.32-431 or higher.
    >
    > from: https://docs.docker.com/installation/centos/

[problem-2]: http://www.projectatomic.io/blog/2015/07/docker-centos-6-and-you/