vagrant-xe11g
=============

Once upon a time, I had to install Oracle XE 11g for a course I was involved in. 
And I was the teacher, so really no chance to skip it.
Unfortunately I had only Linux machines around me, and this repo is the result of my efforts to make them work to the goal.

What follows are the instructions to follow my steps, but you're warned: if you can switch to Windows, *do it*. Trust me.


##Setup
By the way, I think you really need a x64 system and at least 4GB RAM. 
Can't say if it works on other confs, but I guess no.
I should mention maybe that I tried it on Ubuntu 12.04...
If some of your specs are different, maybe it's worth reading the [article that shed light on all of this] [1].

Anyway, here we are:
 0. Install VirtualBox, vagrant and puppet. 
 
   Check their websites first, but for puppet you can try:
  ```
wget https://apt.puppetlabs.com/puppetlabs-release-precise.deb 
sudo dpkg -i puppetlabs-release-precise.deb  
sudo apt-get update
```
 1. `cd` somewhere (the location where you want to put everything
 2. Clone this project or download it:
 
 `git clone https://github.com/lucaventurini/vagrant-xe11g.git`
 3. Copy the installation [file](http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html) you downloaded from the Oracle website here:

  ```
  cd vagrant-xe11g 
  cp somewhere/oracle-xe_11.2.0-2_amd64.deb .
  ```
 4. Cross your fingers (*really important*)
 5. `vagrant up`

By the way, the last step will download and set up a VM, so you can have a coffee now.

##Usage

The web interface will be now available at http://localhost:8080/apex/f?p=4950:2:2370103243114289::NO:::

* Password are "oracle" for system and sys. 
* Password for root is vagrant (all vagrant boxes).

##Credits

For anything else, thanks including, you should really check the [original repo](https://github.com/matthewbaldwin/vagrant-xe11g).
I just want to keep track of a wasted morning and what saved my day:

* the already mentioned repo
* this wonderful article: http://tuhrig.de/3-ways-of-installing-oracle-xe-11g-on-ubuntu/


That's all!

[1]: http://tuhrig.de/3-ways-of-installing-oracle-xe-11g-on-ubuntu/
