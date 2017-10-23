Welcome to Simple Vagrant!
===================
> #### info

This virtual machine has simple and easy settings for configure it
in your web projects.
> #### how to install short

If [those](#you-should-have-to-installed)  apps installed in your linux, you can clone and run vagrant simple <br> 
Clone this project, delete .example from the files name and run ```vagrant up```

----------

Before run vagrant machine you should have to installed <br>
virtualbox: ```sudo apt-get install virtualbox``` or [here][1] <br>
vagrant: ```sudo apt-get install vagrant```  or [here][2] <br>
also your system must has vagrant hostmanager: <br>
```vagrant plugin install vagrant-hostmanager``` or [here][3] <br>

----------

> #### how to install full 
 
 - Clone project from your system: <br>
 ``` git clone https://github.com/sobwoofer/simple-vagrant.git ``` <br>
 - Go to simple-vagrant folder and rename file ```Vagrantfile.example``` to ``` Vagrantfile```
open it and configure your domens like: 
``` 
domains = {
      example:  'example.dev',
      example2:  'myDomain.com',
      apiDomain:  'api'
    } 
```
and for finishing visualisation you can add your domains varaibles (not required) for example:
```
config.vm.post_up_message = "Example URL: http://#{domains[:example]}\n} Second Domain: http://#{domains[:example2]}\n"
```
 - Go to vagrant/config folder and rename file ```vagrant-local.yml.example``` to ```vagrant-local.yml ```
 Also you can change machine name, IP, CPU cores, and RAM memory in this file.
 recommended insert into this file [your personal github token][4].

 - Go to vagrant/nginx folder and ```rename app.conf.example``` to ```app.conf```
 You also can add nginx server configurations sections for your new domains for example:
``` 
 server{
 ...
 }
 server{
  ...
 }
```
 
 
 
  [1]: https://www.virtualbox.org/wiki/Linux_Downloads
  [2]: https://www.vagrantup.com/downloads.html
  [3]: https://github.com/devopsgroup-io/vagrant-hostmanager
  [4]: https://github.com/settings/tokens