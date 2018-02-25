# vagrant-spectral-workbench

## Requirements:  <br/>
Works for Windows, Linux and Mac.  
<br/>
Install **Github's** [Github Desktop](https://desktop.github.com/) ***(just if you don't have it installed already.)***

Install **Oracle** [Virtualbox](https://www.virtualbox.org/wiki/Downloads) ***version 5.2.x***

Install **Hashicorp** [Vagrant](https://www.vagrantup.com/downloads.html) ***version 2.x***

Your computer should be capable to run virtual computers. If not check more [documentation](http://bce.berkeley.edu/enabling-virtualization-in-your-pc-bios.html) about how to activate virtualization functions.

#### About Vagrant:
Vagrant is a tool that wraps LAMP environments and serves it easy and ordered for those who work a lot developing software. So this is the right tool to keep your computer clean and easy.

For our pourpose we'll use vagrant as a wraper of the [Spectral Workbench](https://spectralworkbench.org/) server. To use it locally as our own offline DIY spectrometry system.

#### Instructions to Run the server:

*Once you have installed all the Requirements.*

Open your prefered console emulator, then enter to a desired directory in which you'll clone the repository (folder with files to run vagrant):

Execute the next commands on your terminal:
```
git clone https://github.com/kny5/vagrant-spectral-workbench.git
```

```
cd vagrant-spectral-workbench && vagrant up
```
This command will download the vagrant box and compile the internal guest environment. You only have to wait.

Once the process have finished you need to launch the box by executing this:
```
vagrant ssh -c "cd $HOME/spectral-workbench && ./run-spectral.sh"
```
This command will launch the server using the ssh protocol.

Finally you only need to open your prefered web browser and open this url:

[localhost:8080](localhost:8080)

And Voilá.

#### Instructions to stop the server:
<br/>
This box have a database that records all your data, so don't worry about loose your data.

If you want to preserve the current state of your server just execute this inside the vagrant-spectral-workbench folder/directory:

```
vagrant suspend
```
If you want to restore your last suspended state:
```
vagrant resume
```
If you want to stop your server definitively:
```
vagrant halt
```
If you have any kind of failure attempt to shutdown the server:
```
vagrant ssh -c "sudo poweroff"
```
This is work sponsored by no one at all. Please consider to send money for a cold beer to [KNY5](https://cash.me/$kny5). C:
