# Docker 101


## Summary
If you'd rather not look at or listen to my babbling the folowing Video does a great job at providing info quickly, effectively and goes more in depth. (WARNING COMEDY)

[Docker 101 Video](https://www.youtube.com/watch?v=rIrNIzy6U_g)


## What is Docker?

Put simply, Docker is the all in one solution to the common problem found in programming and computer management of "Works on my Machine". If you've never heard of the saying, it conveys the idea that an installation process for example, that is followed exactly the same way on 2 different devices will not work on one of them. If you've ever tried following a tutorial on YouTube for example, you may have run into this issue. The Tutorial shows the method but when you do it on your device it may not work. This is due to mutliple reasons, your environment, other softwares or tools you've installed, your hardware, and even your OS configuration. Docker aims to solve this issue through virtualization.


## Virtualization vs Emulation

Now a key concept in computing is the distinction between Emulation and Virtualization. These two are extremely different, and will give you very different performances. Emulation, which is what people may be more familiar with is the process of simulating an entire computer inside of another computer. These are commonly known as Virtual Machines or VMs. Popular software like Virtual Box, Hyper-V and more, create Virtual Machines of computers which you can then use. 

A intuitive example of a virtual machine would be Game Emulators. If you've tried to play old Nintendo, Sega, or other game from previous gaming generations and you don't have the console that ran the game, you are forced to use an emulator. Due to piracy protections for games and how they used to be designed some games from those generations can only play on those specific consoles. Nowadays these consoles go for way above a reasonable price on Ebay or just don't exist anymore. So clever hackers have managed to get some of these consoles and then reverse engineer it and get access to their code. From there, they can create software that simulates the console itself and then they can load games to play. For the most part Emulation is only possible on old and "weak" consoles in comparison to today. This is due to the computational complexity of emulating an entire console. While there are strides like dedicated hardware in Apple Silicon, or just general improvements and tricks to bypass emulation, it is still extremely difficult to simulate an entire computer. 

Speaking from experience, I've made a "Hackintosh" myself a few times, and even with my great PC (i7 9700k Overclocked @ 4.7GHz, RTX 4070, 48 GB Ram and very Fast SSDs) I could still only emulate a Mac Virtuoso with 4 Cores and 12 GB, at a dozen frames per second on a good day. Other uses for virtual machines are for protection, since it emulates it's own hardware, it's like creating a computer in the real world, so when doing dangerous things that may comprimise your computer's privacy, data, etc, a Virtual Machine can be used to accomplish the task and if something goes wrong, such as being hacked, you can just delete the Virtual Machine and make a new one, and your real computer won't be comprimised.

Now Virtualization on the other hand is another story. The Key distinction of Virtualization is that only the file structure of your OS is simulated as a different device. Otherwise the "Container" which is kind of like a virtual machine. Can still use the full power of all your computers hardware, with near native speeds. Containers can also still be used for dangerous tasks, and if compromised also wont reflect on the entire computer. This is due to the complex Docker Engine which allows you to simulate all manners of operating systems, or just packages on their own. Docker is mostly used to split up the resources on a single computer so that it can act like many servers and offer services. Large companies like Google use Docker, or their own version of it to allocate, split their servers and upscale when traffic is going up. Containers are also ultra fast and can be created in seconds, can do their job and then shut down when needed, so they are effective for handling sudden spikes in internet activity. Each Container also still acts like their own computer which has a lot of advatges in certain projects.

So Docker allows us to share containers between each other, which are specialized, and configured "OS Images" that have all the necessary things for a certain task. In the Nano Car club we use Docker to simulate Orca Quantum Chemistry software instances on our own devices while still taking access of parallalization (This is not possible on a normal Windows Device, so we make a Linux Container with Orca and OpenMPI, so that we do parallel tasks). Additionally, we can have multiple containers running at the same time, so you can run multiple Orca calculations at the same time in different containers and they will not interfere or mess each other up. They are also so quick and easy to use that all you need to do is download it, and then you can create one within a second. 


## Downloading a Docker Image

If you've ever played around with Git / Github, and specifically their command line tool, you may be a little familiar with the following concept. Doker functions by using base Images/ "OS's" that you then spin up to make a container. This allows you to store one copy of the OS image, and then docker will track the changes from the Base image it started with. This essentially allows you to make hundreds of containers, while using very little storage space. To download a base image you use the following command.

(Assuming you have Docker Desktop Open/ The Docker Engine Running)
```
docker pull nameofimage
```

A prime example is the Hello World Docker Image, which is used to check if you properly installed Docker

```
docker pull hello-world
```

Keep in mind that all container names are **lower case only and no spaces**, underscores or dashes may be present, but there will never be capitals or spaces

## Running a Docker Container

Now that you've downloaded an image we want to try and run it. To do this we use the "docker run" command. Here is an example

```
docker run hello-world
```

Running this in the Terminal, you should get the following message if you've installed docker properly

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/13725a0d-ebde-48fd-b79e-6658795ec537)

If you check your containers in Docker Desktop, you'll notice that the container you spawned is now shutdown and stopped, additional proof is that we are back to our C:/User/Username directory in the Command Prompt.

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/e502bf7c-a2d4-4ea1-ac00-20b87227bb9b)

This means that the Docker Container was a "one time use", so it ran, did it's job / finished, and then it shut down. This is useful for many containers or tasks, but maybe that isn't what we want to do. This brings us to the Next Command.

## Interactive Docker Containers

If we don't want our containers to be a one time use, we need to add a flag to the container as we launch it. This is the Interactive flag, denoted by "-it". 

Unfortunately the hello-world container is not designed to be interactive, which may be the case for a few more containers, so the -it flag wont work on it. So we will use a Linux Image to test it out.

Lets download a Ubuntu image using the following command.

Here is an example of it's usage.

First we will download the Ubuntu 22.04 Version. The Colon signifies the specific version you want to download, by default the version you download will be the latest. 

```
docker pull ubuntu:22.04
```

Now to run a Docker Instance.

```
docker run -it ubuntu:22.04
```

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/a4bef7e1-6214-4998-841f-1f2ca05f0187)

Using the "ls" command we can see the file structure of a linux system.

![image](https://github.com/user-attachments/assets/c1ea780f-0d82-475d-ab40-46dfe459819c)

This means that we are in a Linux Machine and Controlling it!

Now you treat it as your own playground. For example, let's try downloading Nano, a simple text editor for Linux.

Type in the following

```
apt-get update
apt-get install nano
```

You should receive something similar to the following

![image](https://github.com/user-attachments/assets/8fd82497-e6e4-4121-8f1b-f9de9bdc42c2)

Apt-get update was to update the "App Store" that Ubuntu uses, and then the second command was to install the Nano app.

Now if you change directories to "etc" and then look for a file to open using ls

```
cd etc
ls
```

![image](https://github.com/user-attachments/assets/ac3b0468-6b05-4427-bc5b-fc714f1abed0)

We will try opening "adduser.conf", do this by usuing the following command

```
nano adduser.conf
```

You'll receive something like this

![image](https://github.com/user-attachments/assets/a47a5049-0797-4dc0-bd0c-f2675a3b9494)

This means you've opened the File!

To navigate around you need to use the Arrow keys on your keyboard, mouses will not work. Then you can type or modify the file and then click "CTRL + X" and click enter twice to save. It should bring you back to where you were before entering the file.


## What's Next?

For now this is basically all the knowledge you'll need for the Nano Cars Club, with the exception of learning the specific Linux commands for Orca. The process of running a Orca Calculation on the ECE Server, on your personal device, or understanding the innerworkings of QChem and Discorca all hinges on what you've learnt in the 2 past 101s. The Next 101 you should follow is the one specifically for Running Orca Calculations. 




