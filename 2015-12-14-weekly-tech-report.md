---
layout: post
title: "Weekly Tech Report 2015-12-14"
description: "Weekly Tech Report"
category: wtr
tags: [wtr, vagrant, gradle, jenkins, android]
---
{% include JB/setup %}

## Weekly Tech Report 2015-12-14

### Learning

+   [How to Create a Vagrant Base Box from An Existing One] [howto-vabase]

    It describes how to create your own repackaged Vagrant box from an existing
    virtual machine.

        $ vagrant init hashicorp/precise64 # initialize vagrant box
        $ vagrant up # start vagrant box
        $ vagrant ssh # ssh into the box and customize it
        # apt-get install vim # install your needed packages
        # apt-get clean # remove apt cache
        # dd if=/dev/zero of=/EMPTY bs=1M && rm -f /EMPTY # "zero out" the drive
        # cat /dev/null > ~/.bash_history && history -c && exit
        $ vagrant package --output mynew.box # repackage into a new box
        $ vagrant destroy # destroy the source box
        $ rm Vagrantfile # delete the original Vagrantfile
        $ vagrant box add mynewbox mynew.box # add the new box into Vagrant
        $ vagrant init mynewbox # Initialize the new box
        
[howto-vabase]: https://scotch.io/tutorials/how-to-create-a-vagrant-base-box-from-an-existing-one

### Docs

+   [Vagrant Documentation] [vagrant-docs]

    Vagrant provides easy to configure repoducible and portable work environment
    built on top of industry-standard provision provider like VirtualBox, VMware
    , AWS and etc. It also supports Chef, Puppet to perform devops.

[vagrant-docs]: https://docs.vagrantup.com/v2/

+   [Gradle User Guide] [gradle-docs]

    Gradle is a build system supposed to be a quantum leap for build technology,
    and the user guide also represents dependency relationships between Gradle
    tasks by showing some diagrams which use something analogous to the UML 
    dependency notation.

[gradle-docs]: https://docs.gradle.org/current/userguide/userguide.html

+   [Android Plugin for Gradle] [android-gradle]

    The Android build system consists of an Android plugin for *Gradle*. As a
    result, you can build your Android apps from within Android Studio used a
    Gradle wrapper, or from the command line on where Android Studio is not
    installed (such as CI servers).

[android-gradle]: http://developer.android.com/tools/building/plugin-for-gradle.html

### Article

+   [Provisioning a Windows box with Vagrant, Chocolatey, and Puppet] [provision]

    Vagrant is cool enough, the only drawback seems it always more suited for
    \*Nix boxes only. This article will try Chocolatey and Puppet to overcome
    this gap, and to provision a Windows box quickly and cleanly. It will
    chronicle some of the trials and tribulations faced during the process. And
    continued at [Part 2] [provision2].
    

[provision]: http://www.tzehon.com/2014/01/20/provisioning-a-windows-box-with-vagrant-chocolatey-and-puppet-part-1/
[provision2]: http://www.tzehon.com/2014/02/16/provisioning-a-windows-box-with-vagrant-chocolatey-and-puppet-part-2/

+   [Provisioning Vagrant Windows Environments with PowerShell DSC] [win-dsc]

    This article describes an approach to provisioning using PowerShell Desired
    State Configuration (DSC) in Vagrant. And it includes the following steps:

    + Creating Windows Server 2012 Vagrant box by [Packer]
    + Setup Windows Management Framework and PowerShellGet
    + Utilize DSC configuration script in Vagrant shell provision script

[win-dsc]: https://dennypc.wordpress.com/2014/12/02/vagrant-provisioning-powershell-dsc/

+   [Creating a Windows 10 Base Box for Vagrant with VirtualBox] [vagrant-win10]

    It detailly describes how to create a Windows 10 base box for Vagrant by
    manual, four steps are performed:

    + Create a VirtualBox virtual machine
    + Install Windows on the virtual machine
    + Configure Windows for Vagrant
    + Package and Export the box through Vagrant

    [Creating a Windows Box with Vagrant 1.6] [vagrant-win2008] refers to the
    process to create Windows 2008.

[vagrant-win10]: http://huestones.co.uk/node/305
[vagrant-win2008]: https://dennypc.wordpress.com/2014/06/09/creating-a-windows-box-with-vagrant-1-6/

+   [Create a windows base box for vagrant] [vagrant-winbase]

    This is an article described how to create a windows box before vagrant
    merged `vagrant-windows` plugin, and is somewhat old nowadays, however it
    provides some scripts to perform Windows installation, which looks good and
    helpful [Windows Vagrant Base Box Setup Scripts] [vagrant-winscript]

[vagrant-winbase]: http://www.thomasvjames.com/2013/09/create-a-windows-base-box-for-vagrant/
[vagrant-winscript]: https://gist.github.com/davidroberts63/8497405

+   [Developing with vagrant and git on a windows environment] [vagrant-winold]

    This is somewhat outdated solution for using Vagrant on Windows host, now it
    is easy to do it since Vagrant supports to run on Windows host via WinRM.

[vagrant-winold]: https://enrise.com/2012/12/git-and-vagrant-in-a-windows-environment/
 
+   [Leave No Trace: How to Completely Erase Your Hard Drvies, SSDs and Thumb Drvies] [complete-erase]

    Erasing a file does **NOT** remove it from a storage device, it simply marks
    file space as availabe for reuse. To completely wipe all data, you should
    'zero-fill' or overwrite with other garbage data on a storage device.

[complete-erase]: http://gizmodo.com/5494427/leave-no-trace-how-to-completely-erase-your-hard-drives-ssds-and-thumb-drives

### Blog

### Open Source

+   [CoreOS](https://github.com/coreos)

    CoreOS is a minimal operating system that supports popular container system
    out of box. The operating system is designed to be operated in clusters, and
    engineered on most cloud providers. The site produces, maintains, utilizes
    open source software for Linux container and distributed system.

+   [vagrant-windows](https://github.com/WinRb/vagrant-windows)

    A vagrant plugin allows you to standup Windows guests using WinRM instead of
    SSH, and it has been merged into Vagrant now.

+   [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV)

    VVV is an open source Vagrant configuration focused on WordPress developement.
    It could act as a MAMP/XAMPP replacement, also as a scaffold to make your own
    changes. With Vagrant, you can use the exact same tools cross platforms.

+   [Chocolatey](https://chocolatey.org/)

    Chocolatey NuGet is a Machine package Manager for Windows, like apt-get or
    yum but for Windows. It's built on the NuGet infrastructure currently using
    PowerShell as its focus for delivering packages. And you can use it on devops
    tools like [Chef], [Puppet], and [Boxstarter]. ***Even Microsoft has decided
    to use Chocolatey's framework*** with the upcoming [OneGet] client.

[chef]: https://supermarket.getchef.com/cookbooks/chocolatey
[puppet]: https://forge.puppetlabs.com/rismoney/chocolatey
[boxstarter]: https://boxstarter.org/
[oneget]: https://github.com/OneGet/oneget

+   [dban](http://sourceforge.net/projects/dban/)

    Darik's Boot and Nuke (DBAN) is a hard drive disk wipe and data clearing
    utility. 

+   [S.M.A.R.T](http://sourceforge.net/projects/smartmontools/)

    a disk inspection and monitoring utility, control and monitor storage system
    built into most modern ATA and SCSI hard disks.

### Problems

+   [Howto cleanup disk space on CentOS] [problem-1]

    This is a big topic, you can start from removing old unused kernels, and
    cleaning up some temporary directories like /tmp, /var/log, /var/cache, etc.
    And it will be good to cleanup yum cache and undependency packages:

        $ yum clean all
        $ package-cleanup --dupes | xargs yum remove -y -
        $ package-cleanup --orphans | xargs yum remove -y -
        $ package-cleanup --leaves | xargs yum remove -y -

[problem-1]: https://www.centos.org/forums/viewtopic.php?t=15061

+   [Howto remove old kernels on RedHat/CentOS/Fedora] [problem-2]

    Generally system update in many times produces some unused old kernels, to
    remove old kernels, you can operate it by `yum-utils`:

        $ yum install yum-utils 
        $ package-cleanup --oldkernels --count=2

    or you can do it manually by yourself:

        $ rpm -qa kernel | grep -v `uname -r` | xargs rpm -e

[problem-2]: http://serverfault.com/questions/439090/how-to-free-up-space-on-rhel6-boot-safely

+   [Where does Vagrant download its .box files to?] [problem-3]

    When you type the following command to get the box directly from Vagrant:

        $ vagrant box add lucid32 http://files.vagrantup.com/lucid32.box

    Or you can download the box from vagrantcloud.com:

    +   Find the interested box on [Altas], e.g:
        <https://atlas.hashicorp.com/ubuntu/boxes/trusty64/versions/20150530.0.1>
    +   Replace the domain and add `/providers/virtualbox.box`:
        <https://vagrantcloud.com/ubuntu/boxes/trusty64/versions/20150530.0.1/providers/virtualbox.box>

    As mentioned in the docs, the fetched boxes will be by default stored at:

    + Mac OS X: ~/.vagrant.d/boxes
    + Windows: C:/Users/<USERNAME>/.vagrant.d/boxes

    To change the default path, you can set the environment variable:

        export VAGRANT_HOME=/your/new/path/goes/here/

[problem-3]: http://stackoverflow.com/questions/10155708/where-does-vagrant-download-its-box-files-to

+   [Howto change vagrant's default ssh port] [problem-4]

    As @mitchellh mentioned, it's likely a docs issue, and specifying the id may
    do the trick:

        # Must specified `id: "ssh"` in order to override the default forwarded SSH port.
        config.vm.network :forwarded_port, guest: 22, host: 2322, id: "ssh"

    Remember that, without `id: "ssh"`, you would get two fowarding ports: 2222 
    and 2322. See [Overriding the default ssh port in Vagrant] [problem-41].

[problem-4]: https://github.com/mitchellh/vagrant/issues/3232
[problem-41]: https://realguess.net/2015/10/06/overriding-the-default-forwarded-ssh-port-in-vagrant/

+   [Authentication failure after repackaging Vagrant box] [problem-5]

    This is a long discussion. As @Rustem#issuecomment-112052573 mentioned, the
    source box uses insecure keys with `config.ssh.insert_key = true` (default).
    For the random generated key pair, private key is set on your host machine
    at `.vagrant/machines/default/{provider}/private_key`, and public key is set
    on your VM at `~/.ssh/authorized_keys`. So when repackaging the box, the new
    box with random private key at `~/.ssh/authorized_keys` can't find any 
    privated key matched.
    So the first option is configuring your Vagrantfile before repackaging with
    `config.ssh.insert_key=false`, and optionally adding `vagrant.pub` to the
    `authorized_keys`:

        $ wget https://raw.githubusercontent.com/mitchellh/vagrant/master/keys/vagrant.pub -O .ssh/authorized_keys
        $ chmod 700 .ssh; chmod 600 .ssh/authorized_keys; chown -R vagrant:vagrant .ssh

    The second option is setting the default username/password in Vagrantfile:

        config.ssh.username='vagrant'
        config.ssh.password='vagrant' 

[problem-5]: https://github.com/mitchellh/vagrant/issues/5186

+   [How do I increase the hard disk size of the virtual machine?] [problem-6]

    Simply try the following command:

        $ VBoxManage modifyhd your_disk.vdi --resize size_in_MB

[problem-6]: http://askubuntu.com/questions/88647/how-do-i-increase-the-hard-disk-size-of-the-virtual-machine

+   [machine with name 'default' not configured] [vagrant-default]

    Sometimes it's caused by the obselete machines that are still in the global
    Vagrant environment. There are two ways to clean it up, by running command
    `vagrant global-status --prune`, or by deleting the unused machines under
    `./.vagrant/machines`.
    If you are using an image from the Hashicorp box index, you should not use
    an image just by running `vagrant up`, see [michaelheap]:

        $ vagrant box add ubuntu/trusty64
        $ rm Vagrantfile
        $ vagrant init ubuntu/trusty64
        $ vagrant up

    If you encouter this error when packaging a box, you might correct the box
    name by specifying `vagrant package --base <box_name>`, get your box_name by
    running `VBoxManage list vms`, see [Issue #5191] [issue-5191]
    
[vagrant-default]: https://github.com/smdahlen/vagrant-hostmanager/issues/102
[michaelheap]: https://michaelheap.com/the-machine-with-the-name-ubuntutrusty64-was-not-found-configured/
[issue-5191]: https://github.com/mitchellh/vagrant/issues/5191

+   [Where does the name come from when launching a vagrant box] [vagrant-name]

    When you boot up a vagrant box under a directory, the machine name showed in
    VirtualBox will be default format as DIRECTORY_default_TIMESTAMP. If you'd
    like to change the name, you can explicitly define a VM, or you can set the
    `name` attribute in a provider block, the latter has higher priority:

    + Set Provider Name
     
            Vagrant.configure('2') do |config|
              config.vm.box = "precise64"
              config.vm.box_url = "http://files.vagrantup.com/precise64.box"
              config.vm.provider :virtualbox do |vb|
                  vb.name = "foohost"
              end
            end

        *VirtualBox GUI Name: "foohost"*

    + Define VM
    
            Vagrant.configure('2') do |config|
              config.vm.box = "precise64"
              config.vm.box_url = "http://files.vagrantup.com/precise64.box"
              config.vm.define "foohost" do |foohost|
              end
            end

        *VirtualBox GUI Name: DIRECTORY_foohost_TIMESTAMP*

[vagrant-name]: http://stackoverflow.com/questions/17845637/vagrant-default-name

+   [What is dd if=/dev/zero of=/EMPTY bs=1M] [problem-9]

    This will create a sparse file, which allows better compression of the
    physical file containing the virtual disk.
    Also see [vagrant - no space left on device error] [problem-91].

[problem-9]: http://serverfault.com/questions/677021/what-is-dd-if-dev-zero-of-empty-bs-1m
[problem-91]: http://stackoverflow.com/questions/20081116/vagrant-no-space-left-on-device-error


[![Creative Commons License][CC png]][CC BY-NC 4.0]<br/>
This work is licensed under a [CC BY-NC 4.0][] License.

[cc png]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
[cc by-nc 4.0]: http://creativecommons.org/licenses/by-nc/4.0/
