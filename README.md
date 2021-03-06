FreeSWITCH Vagrant Box
======================

A quick and easy FreeSWITCH box for playing/hacking on. 

This uses [Vagrant](http://www.vagrantup.com) to spin up a local virtual machine and will install FreeSWITCH for you automatically on the vm. 

Installation
------------

1. Install [Virtual Box](https://www.virtualbox.org/) - a cross platform virtual machine program by Oracle

2. Install [Vagrant](http://www.vagrantup.com) - a virtual machine provisioner making it easier than ever to automate virtual machine setups

3. Check out/download the code...

4. In your terminal, go to the code directory and type: `vagrant up` (FYI - on first usage this takes a LONG TIME time to download and then install FreeSWITCH. Go grab some lunch... and maybe dinner. FreeSWITCH takes a while to install. :-)

That is all! You now have FreeSWITCH running in a virtual machine on your local box.


Usage
------

You can access the VM through SSH on IP 12.0.0.1 on the standard port. This is a host-only network that isn't exposed to the web.
I will add an alternate configuration in the Vagrantfile so you can expose this box to the ouside world if you so choose.

After you have installed for the first time with `vagrant up`, you can:

1. Shutdown the vm for later using `vagrant halt` (to boot back up simply use `vagrant up` again)
2. Pause the vm in its current stat using `vagrant suspend` (to resume the vm use `vagrant resume`)

Update
------

On newer version of vagrant you will need to repackage the box.

This is what it may look like... windows 8 different story will get back to you on that..

A Vagrant 1.0.x state file was found for this environment. Vagrant has
gone ahead and auto-upgraded this to the latest format. Everything
should continue working as normal. Beware, however, that older versions
of Vagrant may no longer be used with this environment.

However, in case anything went wrong, the old dotfile was backed up
to the location below. If everything is okay, it is safe to remove
this backup.

run: vagrant box repackage base virtualbox

also, when you login the box hasnt set the read/write flag.

1. run: sudo su
2. run: chmod 775 `find /usr/local/freeswitch -type d`  
