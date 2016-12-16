# vagrant-caravel-playground

Hello there, and glad you have made it! The main purpose for this repository is to help anyone curious about virtualization and provisioning to dive right in, get their feet wet, and learn some cool things. You will be using Vagrant, Ansible, and the open-source project by AirBnb called Caravel, in order to run a virtual machine, automatically provision it, and use Caravel to play with some interesting data! Sound good? Let's get started...

## Prerequisities

Outlined here are the bare necessities you will need in order to get your vagrant box running and provisioned. There are just 2 things that your host machine must have installed in order to follow on...

![Vagrant pic2](https://raw.githubusercontent.com/elsquash/vagrant-caravel-playground/master/pics/Vagrant_pic2.jpg)


### 1.) Vagrant

Since one of the main purposes of this repository is to help understand virtualization by using Vagrant, we will of course need Vagrant installed on our machine! This is very easy to do. Please download and install the latest version of Vagrant by visiting their downloads page [here](https://www.vagrantup.com/downloads.html).

On this page you can get the latest install for MacOS, Windows, CentOS, and more depending on what you need. Once you have done that, please move to the next step!

![VirtualBox pic](https://raw.githubusercontent.com/elsquash/vagrant-caravel-playground/master/pics/Virtual_box_pic.png)


### 2.) VirtualBox

There are multiple possibilities of how Vagrant boxes can actually be run on your host machine. But arguably the simplest way to do it is with VirutalBox. If you happen to visit Vagrant's [getting started guide](https://www.vagrantup.com/docs/getting-started/), they suggest Virtualbox because it is free, widely available on different platforms, and actually built-in to Vagrant itself. Go to VirtualBox's downloads page [here](https://www.virtualbox.org/wiki/Downloads) to install the latest version of Virtualbox for your machine. Once you have done that, the real fun can begin!


## Vagrant Up

If you have gotten to this section, you have successfully installed the latest version of Vagrant and VirtualBox for your machine. Now we are going to boot up a vagrant box. Documentation for starting/suspending/stopping/destroying vagrant boxes can be found [here](https://www.vagrantup.com/docs/getting-started/teardown.html). 

For now, open the command-line interface for your machine, and navigate to the root directory of this repo, whereever it is that you cloned it. Here is an example of where you may have put it on a windows machine:

```
cd /Users/JoshuaPeeling/Desktop/vagrant-caravel-playground
```

Once you are in the root directory, simply run the command:

```
vagrant up
```
You should see vagrant searching to see if you have the [geerlingguy/centos7](https://atlas.hashicorp.com/hashicorp/boxes/precise64) vagrant base box on your machine. This is because of the setting included in the Vagrantfile which has been included with this repo: 

```
config.vm.box = "geerlingguy/centos7"
```

This base box was chosen because it is friendly to VirtualBox. Visit Vagrant's [documentation on Vagrantfiles](https://www.vagrantup.com/docs/vagrantfile/) if you want to learn more about Vagrant files and what you can possibly set through them.

If you do not have the *geerlingguy/centos7* vagrant base box, Vagrant will grab it for you, and boot up the machine! This could take a few minutes if Vagrant has to go and retrieve the base box. That's okay though! You can go [discover vagrant boxes](https://atlas.hashicorp.com/boxes/search?utf8=%E2%9C%93&sort=&provider=&q=) during this time to see what the opensource community has to offer! 

Once the box has been retrieved and booted, you should be seeing a bit of output in your command-line interface. Move to the section below to see what should happen next.

## Provisioning

![Vagrant pic](https://raw.githubusercontent.com/elsquash/vagrant-caravel-playground/master/pics/ansible-logo.png)


Here is where Ansible comes into the picture. Once the vagrant box is up and running, Ansible will actually begin to install on the guest machine (this is another setting in the Vagrantfile). See Vagrant's own documentation on [integrating with Ansible](https://www.vagrantup.com/docs/provisioning/ansible_local.html) for more details. Once Ansible is installed locally on the guest machine, it will run the playbook.yml file and install all the necessary dependencies needed to successfully get Caravel up and running. 

If you want to know more about how Ansible works and how to create playbooks for provisioning, please check out [Ansible's documention](http://docs.ansible.com/ansible/index.html) for more info. There is a great 30 minute [introductory video](https://www.ansible.com/quick-start-video) they provide as well if you need a break from reading :)

Still here? Okay, this process will take a couple minutes. Installing Caravel on the guest machine can take a while, so sit back, maybe read through [how playbooks are structured](http://docs.ansible.com/ansible/playbooks.html), and wait for it to complete. How do you know Ansible completed the playbook? You should be given back control of your command-line interface, and see the output below:

```
PLAY RECAP *********************************************************************
default                    : ok=6    changed=4    unreachable=0    failed=0
```

Caravel should be running on the guest machine in the background now!

## Using Caravel

![Vagrant pic](https://raw.githubusercontent.com/elsquash/vagrant-caravel-playground/master/pics/caravel-screenshots.jpg)


If you have gotten to this section, then Ansible's playbook completed! Open your favorite browser, and go to:

```
localhost:5678
```

You should see Caravel running, and asking you to log in! The way the Vagrantfile included in the repo has been set up, the guest's port 8088 is forwarded to your host machine's port 5678. 

```
config.vm.network "forwarded_port", guest: 80, host: 4567
config.vm.network "forwarded_port", guest: 8088, host: 5678
```

To log into the test_user account please provide Caravel with these credentials:

```
username: test_user
password: password
```

Once logged in, you should be able to see a pre-loaded database of [CO2 emissions per capita](https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions/) of many different countries from 1950 to 2013. You are welcome to explore Caravel now as you please and manipulate data to your heart's content. Visit [Caravel's README](https://github.com/airbnb/caravel/blob/master/README.md) to watch a quick tutorial, and learn how to use Caravel if you have never used it before.

## Teardown

After you have had your fun, don't forget to shut down your brand new, provisioned vagrant box running Caravel!

```
vagrant halt
```

## Summary

I hope you have learned quite a bit about virtualization and provisioning using Vagrant, Ansible, and Caravel! All the documentation and links (above and below) will help you out majorly in understanding more about what went on in this project. If you run into problems, or have questions about something that went on here, please feel free to raise an issue. Thanks!


## Authors

* **Joshua Peeling** - [ElSquash](https://github.com/ElSquash)

## License

This project is open and free for anyone to use. Please site this repo as a source if you use it.

## Acknowledgments

* Vagrant documentation can be found here! https://www.vagrantup.com/docs/
* Ansible documentation can be found here! http://docs.ansible.com/ansible/index.html
* VirtualBox documentation can he found here! https://www.virtualbox.org/wiki/Documentation
* Caravel documentation can be found here! https://github.com/airbnb/caravel/blob/master/README.md
* The C0o2 data used in Caravel can he found here! http://bit.ly/2bcMrcY

* Pic 1: http://bit.ly/2bzbkS5
* Pic 2: http://bit.ly/2bx5n5Q
* Pic 3: http://bit.ly/2bwyxBp
* Pic 4: http://bit.ly/2bpV2rl
* Pic 5: http://bit.ly/2bcKRrw
