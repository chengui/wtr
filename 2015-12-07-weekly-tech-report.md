---
layout: post
title: "Weekly Tech Report 2015-12-07"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, vagrant, jenkins, virtualbox, ssl, msbuild, nant]
---
{% include JB/setup %}

## Weekly Tech Report 2015-12-07

### Learning

+   [make ci easier with Jenkins CI and Vagrant] [jenkins-vagrant]

    A good thought of using Vagrant to isolate the Jenkins build environment, 
    which would add a vagrant box as a new slave node with vagrant ssh key. See
    discussions at [How to combine Vagrant with Jenkins] [sf-jenkins]

[jenkins-vagrant]: http://www.larrycaiyu.com/blog/2011/10/21/make-ci-easier-with-jenkins-ci-and-vagrant/
[sf-jenkins]: http://stackoverflow.com/questions/6941547/how-to-combine-vagrant-with-jenkins-for-the-perfect-continuous-integration-envir

+   [How to control virtual machines (virtalbox) using VBoxManage] [vm-vboxmanage]

    A simple introduction for using VBoxManage

[vm-vboxmanage]: http://www.ubuntugeek.com/how-to-control-virtual-machines-virtualbox-using-vboxmanage.html

+   [Multi-Machine Vagrant with YAML] [vagrant-yaml]

    It describes a technique for simplifying the use of multi-machine Vagrantfiles
    by extracting configuration data into a separate YAML file.

[vagrant-yaml]: http://blog.scottlowe.org/2014/10/22/multi-machine-vagrant-with-yaml/

+   [Getting Started with Jenkins, Git and MSBuild] [andyfrench-start]

    In this series, it will start with Jenkins, Git and MSBuild to setup
    automatic build service and unit test on Windows:

    > [Getting Started with Jenkins, Git and MSBuild] [andyfrench-start]
    > [Automatically triggering a Jenkins build on Git commit] [andyfrench-git]
    > [Running NUnit tests with Jenkins] [andyfrench-nunit]

[andyfrench-start]: http://www.andyfrench.info/2015/03/getting-started-with-jenkins-git-and.html
[andyfrench-git]: http://www.andyfrench.info/2015/03/automatically-triggering-jenkins-build.html
[andyfrench-nunit]: http://www.andyfrench.info/2015/03/running-nunit-tests-with-jenkins.html

+   [Jenkins Brief] [jenkins-brief]

    A Chinese blog with brief introduction to Jenkins:

    > [Jenkins, CruiseControl and Hudson] [jenkins-brief]
    > [Jenkins Basic] [jenkins-brief-2]
    > [Jenkins Questions] [jenkins-brief-3]

[jenkins-brief]: http://blog.csdn.net/OnlyQi/article/details/7340149
[jenkins-brief-2]: http://blog.csdn.net/onlyqi/article/details/7076915
[jenkins-brief-3]: http://blog.csdn.net/OnlyQi/article/details/7340223

+   [Jenkins Slave Nodes] [jenkins-slave]

    Jenkins Slave Nodes are small Java "Client" processes that connect back to
    a "Master" Jenkins instance over the Java Network Lauch Protocol (JNLP).

[jenkins-slave]: http://www.donaldsimpson.co.uk/2011/10/06/jenkins-slave-nodes/

+   [Continuous Integration Seting Up Based on Jenkins] [ci-jenkins]

    Continuous Integration is a development practise, like Jenkins. This gives
    some basic concepts of Jenkins, and presents how to rapidly setup CI server
    by Jenkins.

[ci-jenkins]: http://www.ibm.com/developerworks/cn/java/j-lo-jenkins/index.html

+   [Coninuous Integration with MSBuild and Jenkins] [ci-msbuild]

    In this article, it presents writing your own MSBuild script from scatch,
    then setup a Jenkins build job on any code changes from your repository and
    run the MSBuild script.

    > [Continuous Integration with MSBuild and Jenkins – Part 1] [ci-msbuild]
    > [Continuous Integration with MSBuild and Jenkins – Part 2] [ci-msbuild-2]

[ci-msbuild]: http://www.infoq.com/articles/MSBuild-1
[ci-msbuild-2]: http://www.infoq.com/articles/MSBuild-2

+   [A .NET Build Server without Visual Studio] [build-wo-vs]

    It shows some researches on how to accomplish building .NET project without
    installing Visual Studio. Although NuGet can be used as a long term solution
    , this article provides a workaroud for short term solution.

    > [Building .NET projects is a world of pain] [build-dotnet]
    > [A less terrible .NET project build with NuGet] [dotnet-nuget]

[build-wo-vs]: http://nickberardi.com/a-net-build-server-without-visual-studio/
[build-dotnet]: http://blog.maartenballiauw.be/post/2014/04/11/Building-NET-projects-is-a-world-of-pain-and-heres-how-we-should-solve-it.aspx
[dotnet-nuget]: http://haacked.com/archive/2014/04/15/nuget-build-dependencies/

### Docs

+   [Jenkins Wiki] [jenkins-wiki]

    Three pages in the wiki and the usages of plugins:

    + [Meet Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Meet+Jenkins)
    + [Use Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Use+Jenkins)
    + [Extend Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Extend+Jenkins)

[jenkins-wiki]: https://wiki.jenkins-ci.org/display/JENKINS/Home

+   [VBoxManage Manual] [vbox-manual]

    VBoxManage is the command-line interface to VirtualBox, it exposes really
    all the features of the virtualization engine, even those that cannot (yet)
    be accessed from the GUI.

[vbox-manual]: http://www.virtualbox.org/manual/ch08.html

### Article

+   [Troubleshooting story - Java HTTP client crashes on connections] [ssl-crash]

    To find out a SSL handshake issue, it makes a basic HTTP code snippet to
    test it. Then the cause is located at Java-1.7.0 not Java-1.8.0, and proved
    to associate with Java external library. The memory-mapped files, which 
    include loaded library give a clue to the root cause. Simply upgrade `nss`
    to solve the problem:

        sudo yum upgrade nss

[ssl-crash]: http://blog.backslasher.net/java-ssl-crash.html

+   [Configure Subversion to trust a given SSL certificate] [svn-ssl]

    Configure `ssl-authority-files` property in `servers` under `/etc/subversion`
    or `~/.subversion`:

        [gobal]
        ssl-authority-files=/etc/ssl/certs/example.pem;/etc/ssl/certs/another.pem

    Or use the --trust-server-cert (and --non-interactive for non-prompt) from 
    command line.

[svn-ssl]: http://www.microhowto.info/howto/configure_subversion_to_trust_a_given_ssl_certificate.html

+   [Jenkins Build Server with Vagrant] [vagrant-jenkins]

    It describes how to setup a "pre-packaged" build server with Vagrant, see
    the Vagrant file and a provisioning script to create a Debian-based Jenkins 
    server, including Java, Ant and Tomcat at [Gist] [vagrant-gist]

[vagrant-jenkins]: http://automation.better-than.tv/info.html
[vagrant-gist]: https://gist.github.com/aweijnitz/9628014b766e02f0a4c8

### Blog

+   [Jenrry Qu] [jerry-qu]

    Focus on WEB development

[jerry-qu]: https://imququ.com/

### Open Source

+   [Jenkins Vagrant Plugin](https://github.com/jenkinsci/vagrant-plugin)

    Vagrant plugin for Jenkins, see [Jenkins Wiki] [jenkins-va-plugin]

[jenkins-va-plugin]: https://wiki.jenkins-ci.org/display/JENKINS/Vagrant-plugin

+   [vagrantbox.es](https://github.com/garethr/vagrantboxes-heroku)

    Repository for <http://www.vagrantbox.es/>, a list of public boxes

+   [veewee](https://github.com/jedi4ever/veewee)

    A tool for easily building custom Vagrant base boxes, KVMs, and VM images

+   [NAnt](https://github.com/nant/nant)

    A free .NET build tool, and it can work well with Windows with .NET/Mono and
    Linux with Mono.

### Problems

+   [Jenkins cannot access to SVN (https://)] [problem-1]

    Connect to SVN repo from command line as user jenkins on server and accept
    all certificates permanently (p). It will create `~/.subversion/auth`.

[problem-1]: http://stackoverflow.com/questions/17464993/jenkins-cannot-acces-to-svn-https/19598786

+   [How to save a remote server SSL certificate locally as a file] [problem-2]

    Try command line:

        $ openssl s_client -connect {HOSTNAME}:{PORT} -showcerts

    Also see [Using openssl to get the certificate from a server] [problem-21].

[problem-2]: http://superuser.com/questions/97201/how-to-save-a-remote-server-ssl-certificate-locally-as-a-file
[problem-21]: http://stackoverflow.com/questions/7885785/using-openssl-to-get-the-certificate-from-a-server

+   [Subversion integration problem] [problem-3]

    When intergrating redmine with external subversion repository reachable via
    https, you could change line `SVN_BIN = "svn" inf file
    `REDMINE_ROOT/lib/redmine/scm/adapters/subversion_adapter.rb` to 

        SVN_BIN = "svn --config-dir /path/to/your/repo/config

[problem-3]: https://www.redmine.org/boards/2/topics/11896

+   [svn won't accept my invalid certificate] [problem-4]

    When adding `ssl-authority-files` property in `/root/.subversion/servers`,
    it still doesn't work, the error on validating server certificate is that
    the certificate does not match the server's hostnmae, need correct the CN
    field to regenerate one.

[problem-4]: http://serverfault.com/questions/27006/svn-wont-accept-my-invalid-certificate

+   [Failed to fetch URL https://dl-ssl.google.com/android/repository/repository.xml] [problem-5]

    If you are using SDK Manager as GUI, try to force to use `http` not `https`,
    or setting up a https proxy in Setting.
    If you are using android sdk from command line, try to fix the following
    line in file `android-sdk-linux_x86/tools/android`, see [Issue 21359]:

        exec "$java_cmd" \
            -Xmx256M $os_opts $java_debug \
            -Dcom.android.sdkmanager.toolsdir="$progdir" \
            -Dhttps.proxyHost=your.proxy.com -Dhttps.proxyPort=8888 \
            -Dhttp.proxyUser=your_proxy_username -Dhttp.proxyPassword=somePassword\
            -classpath "$jarpath:$swtpath/swt.jar" \
            com.android.sdkmanager.Main "$@"

[problem-5]: http://stackoverflow.com/questions/3808167/android-sdk-manager-gives-failed-to-fetch-url-https-dl-ssl-google-com-android
[issue 21359]: https://code.google.com/p/android/issues/detail?id=21359

+   [How to run several boxes with Vagrant] [problem-6]

    You can use `config.vm.define VM_NAME` to define multi-machines in one Vagrantfile

[problem-6]: http://stackoverflow.com/questions/23888381/how-to-run-several-boxes-with-vagrant

+   [What is the default Jenkins password?] [problem-7]

    Try to update password of user jenkins:

        $ sudo passwd jenkins

[problem-7]: http://stackoverflow.com/questions/15227305/what-is-the-default-jenkins-password

+   [NAnt or MSBuild, which one to choose and when?] [problem-8]

    + **NAnt**:
        + Cross-platform
        + Ant compatible
        + Integrated with NUnit and NDoc
    + **MSBuild**:
        + Built-in to .NET
        + Integrated with Visual Studio
        + Easy to get started

[problem-8]: http://stackoverflow.com/questions/476163/nant-or-msbuild-which-one-to-choose-and-when


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/
