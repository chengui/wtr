---
layout: post
title: "Weekly Tech Report 2015-11-30"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, jenkins, docker, ant, gradle, android, kvm, libvirt]
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

+   [Analysis of Libvirt Virtualization Library] [libvirt-analysis]

    Libvirt is a Linux API implemented Linux virtualization, and it supports 
    varies of VM monitors, including Xen, KVM and QEMU. And this article explores
    the usage and architect of libvirt.

[libvirt-analysis]: http://www.ibm.com/developerworks/cn/linux/l-libvirt/index.html

+   [Using Ant to Automate Building Android Applications] [using-ant]

    This tutorial will show you how to incorporate an Ant build script into your
    Android projects, create your release package ready for Marketplace 
    deployment in one step, create a build configuration using a properties 
    file, and alter your source files based on the configuration.

[using-ant]: http://www.androidengineer.com/2010/06/using-ant-to-automate-building-android.html

+   [Embrace Gradle: Next Generation Automation Building Tool] [embrace-gradle]

    Gradle uses Groovy instead of XML, provides dependencies management, and
    supports Maven, Ivy repository, this article will introduce how to use
    gradle to build Java project, as well as gradle wrapper.

[embrace-gradle]: http://www.xinthink.com/gradle/2013/05/01/gradle-intro.html

### Article

+   [Cloning VMs with KVM] [clone-kvm]

    It illustrates how to use KVM to adapt two usecases: long-running VMs to run
    services, to do development, and ongoing deploys; short-lived VMs to run
    single-node or multi-node tests.

[clone-kvm]: http://www.greenhills.co.uk/2013/03/24/cloning-vms-with-kvm.html

+   [Running and Building Android Project from Command Line] [android-cmd]

    It presents how to create Android project from command line, and how to use
    ant to build Android project, also what problems would be meet during the
    operation.

[android-cmd]: http://blog.csdn.net/dlmu2001/article/details/6588295

+   [Packing Android App with ANT] [android-ant]

    It deeply explains what steps would be taken when using ANT to build Android
    App, and how to apply in build.xml of ANT.

[android-ant]: http://blog.csdn.net/liuhe688/article/details/6679879

+   [Automation Packing with ANT + ProGuard + Sign] [ant-proguard]

    A code snippet of build.xml of ANT with ProGuard and Signing enabled.

[ant-proguard]: http://www.oschina.net/code/snippet_16_6782

+   [Structure of Gradle Wrapper Cache Directory] [gradle-cache]

    Analyze the directory structure of Gradle wrapper cache.

[gradle-cache]: http://www.liudonghua.com/?p=380

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

+   [Help KVM/Virsh](https://help.ubuntu.com/community/KVM/Virsh)

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

+   [Gradle Plugin User Guide](http://tools.android.com/tech-docs/new-build-system/user-guide)

    Gradle is an advanced build system as well as an advanced build toolkit 
    allowing to create custom build logic through plugins.

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

+   [Android NDK build with ANT script] [problem-3]

    Call `ndk-build` from your `-pre-build` target, like this:

        <target name="-pre-build">
            <exec executable="${ndk.dir}/ndk-build" failonerror="true"/>
        </target>
        
        <target name="clean" depends="android_rules.clean">
            <exec executable="${ndk.dir}/ndk-build" failonerror="true">
                <arg value="clean"/>
            </exec>
        </target>

[problem-3]: http://stackoverflow.com/questions/7432449/android-ndk-build-with-ant-script

+   [Building Android sample project using Ant] [problem-4]

    Before running ant task, execute this command:

        $ android update project --target <build target> --path <path to project>

[problem-4]: http://stackoverflow.com/questions/5572304/building-android-sample-project-using-ant

+   [Latest ant in Fedora 14 is 1.7 but I need ant 1.8] [problem-5]

    Get all rpm needed and install it with yum:

        $ wget -r -A.rpm k -nc -l1 -e robots=off http://kojipkgs.fedoraproject.org/packages/ant/1.8.2/3.fc15/noarch/
        $ su -c ' yum --nogpgcheck install $(find kojipkgs.fedoraproject.org/ -name "*.rpm") '

[problem-5]: http://stackoverflow.com/questions/5240846/latest-ant-in-fedora-14-is-1-7-but-i-need-ant-1-8


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/