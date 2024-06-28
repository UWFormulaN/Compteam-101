# Linux and Command 101

## What is a Operating System (OS)?
An Operating System is a piece/bundle of software packaged together that provides all the base functionality for a Computer to actually run. There are multiple types of operating systems and they each have their advantages and disadvantages. The main feature of a Operating System is to provide a Kernel, which is a bundle of Drivers and software that bridges the gap from communicating to indidual parts of your computer to the OS so that programs can communicate to those components and accomplish complex tasks such as Saving files, Drawing on your monitor, or communicating via a USB Cable. Most operating systems provide methods to run Programs or Aplications (Similar but different), provide a file system to organize your device, and often provide a Graphical User Interface (GUI) to let users use their computers using mouse clicks and visual features. Common Operating Systems used on Desktop/Laptop computers are Windows, MacOS and Linux and it's Distros. Additionally other OS's you may not have known are seperate are, and are all extremely specialized for their own use cases are, Chrome OS, Android, IOS, IpadOS, WatchOS, WearOS and plenty more. (The following are some of their logos)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/33efb873-e2a4-4862-b539-34ca3302e624)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/d88cde40-06ae-40e8-a300-801b9a415fec)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/8636210d-2942-459e-aa23-9bc0074c5726)


## What is Linux?

Linux is a Open Source Unix based Operating System (OS). Created in 1969 as Unix by Bell Labs as a Non Open Source product, and later imporved uppon by Linus Torvald in 1991. The GNU Project started in 1983, with the goal of creating a full Unix Compatible Software System made up of only free software. In summary, the end goal of the Linux Operating System was to be a OS that anyone can contribute, improve or modify for free, and where all pieces of software that runs on it are free. For the most part this is true. Unlike Windows where a 120$ is needed to purchase a license, or MacOS which only comes on a Apple Device, installing Linux is completely free, and they allow you to modify your copy or improve the official copy to your hearts content. (Side note: Android is somewhat similar where all manufacturers can modify their copies for their specific phones, but it stands more or less in the middle between both groups due to multiple reasons). While you can't really "install Linux" directly, you need to download and install one of it's distros. The best way to think of a Distro is like a flavour of ice cream, while they are all ice cream they each provide slightly different and unique experiences. The easiest example of this is the difference betwen MacOS, IpadOS and IOS, each is slightly different in functionality, features and more optimized for the device they are installed on, but all of them can also do the barebones things and provide very similar experiences. 

Fun Fact : MacOS, IpadOS, IOS, WatchOS, VisionOS and other OS's built by Apple were built from and improved upon from Unix. So in a way, those OS's are kind of like Linux Distros. 

Examples of Linux Distros are as follows

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/66aeb7a8-4c17-4773-a983-7b8abbf8d798)

## Why does the CompTeam need to know Linux?

In the CompTeam we will be making a lot of tools, the majority of which will be through Docker, which is covered in a different 101. If you've ever experienced issues installing software because another piece of software conflicts with it, you'll understand the frustration the CompTeam feels often. We will experience this on steroids very often as we make tools for everyone to use. The complexity of every member using different OS's is already a headache, and what's more everyone may have different versions, each with unique setups and this can quickly cascade into problems that can only be solved by Factory Resetting a device. We would like to avoid that, which is why we will use Docker. Their motto is to fix the "Works on my machine" issue that a lot of people get, by creating "Containers" which are similar yet very different to Virtual Machines, which allow you to essentially create a new specific computer for a single task. Docker is very quick and efficient, and since ideally we would not like to buy a 120$ copy of windows everytime we make a new tool, Linux Distros like Ubunutu, which are free, easy to setup and easy to use are what we will use. 

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/435c57dc-4fd6-4615-a551-e726e57a099f)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/4e2b953a-0117-44c7-a9bb-c3eb49dc4d4d)


## Command Line

While a Linux Distro, such as one of the more popular ones, Ubuntu, do provide a GUI to interact with the computer easily, Linux is designed to be used primarily through the Command Line. Command Lines tend to be a little scary to learn due to how complex they can be, but this course will do it's best to teach you the basics and allow you to improve your computer skills vastly. In the background on computer, the majority of software actually end up using command line functionality, but and then just have a GUI bundled with it to visually display it. A good way to think about it is like Chefs in kitchenn which do a lot of work in the background (Command Line and Programs), and then the waiters/waitresses bring your meal to you (GUI). Since a lot of programs are built in different languages or apps that magically work together function by leveraging the Command Line. Additionally, some problems on your computer may only be solvable by Command Line, which is why growing confortable with it is important.

## Command Line Examples based on OS

Every OS has a Command Line Interface (CLI) that can be used to communicate with the compauter although most are named differently. The Vanilla defaults for each OS are as follows.

### Windows (Command Prompt)
On Windows we have the Command Prompt, When typing in the Windows search bar with CMD, or Command Prompt you can open it and it will look like the following. If you run it in Admninistrator Mode the text it will show will be a little different.

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/99762712-9696-4340-907f-c9de82694983)

Additionally Windows also has a few other Command Line apps, such as Powershell, but that is a command line app built specifically for Windows and managing it's security.

### Mac OS (Terminal)

On MacOS we have the Terminal App and as you'll notice in the next section it looks very similar to the Linux Terminal, which further shows how related they are. To open a Terminal go in spotlight and type Terminal, and open it, it should look something like the folowing. 

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/db1fc12b-1f88-4fee-b746-e94d6948a7d9)


### Linux (Terminal)

Finally we have Linux, similarly to MacOS you can search up MacOS to open it and it should look like the following

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/07967775-7509-4e77-bbee-be3f10d39086)


## Using the Command Line

While the Command Line may look a little scary it can also be really powerful once you understand how it works. Unlike GUI based OS's, Command Lines don't functional similarly at all. On a GUI you can navigate to different parts of the compauter using untuitive mouse clicks, but in a command line everything is done by text. 

First, to understand how a Command Line is navigated Open up your File Explorer App or something similar. The Best way to think about the Command Line is as if it is a Text Based File Explorer App. If your familar with file structures you'll know that each file has a Unique Path to be accessed on your computer, this is what is often displayed at the top of the File Explorer App, it is the Path to the Folder you are currently viewing. A Command Line works very similarly to that, it will place you inside a specific folder and you can do all your actions from there. On Windows your command Line will open in the C:/Users/Username path. This is the "Home" Directory for the user. On MacOS and Linux you'll notice that it's something like "Username@ComputerName: ~$", although it's hard to see the "~" (Tilda) signifies that you're also in the "Home" Directory, Unix based systems simplify this to make it easier. The equivalent path to this, is "/home/Username". Side Note: if you're on Windows and you open your "Downloads" folder, and you try to get the Path in the File Explorer it only gives you "Downloads" same with Desktop or Documents. Windows does a similar simplification in the File Explorer, where the true path of those Folders are in "C:/Users/Username/Downloads"


![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/b30218a9-57db-459e-9a3e-8c239fcdd0fe)


![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/8cb8a86f-9717-4bb0-ac7c-e14f817462d9)

The "Home" Directory is essentially equivalent to being on your desktop when you open your computer but it's not quite it either. In reality, your Desktop is it's own folder in the "Home" directory, the home directory is just the location that all data related to your account is stored. To show this the first command you will use is "ls" (if you're on Mac or Linux), if you're on Windows you need to use "dir". "ls" stands for list, and it's job is to list all files and folders in your current location. This is essentially the equivalent to seeing all the files and folders in File Explorer. 

Windows

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/bc87ee0a-f754-4d97-be39-0af4cb1e05e4)

Mac/Linux
![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/05f71d3d-ef12-495a-8b53-63642513a0b1)

Now if you haven't explored much of your Operating System structure you may not recognize a lof of these files or folders other than the commons like Downloads, Documents and Desktop. So let's navigate to a location that we can compare. The next command is "cd", "ls" and "cd" will often be used together in order to navigate through the computer. "cd" stands for Change Directory (side note: in computer terms a "folder" is actually called a "directory" but for simplicities sake I will continue saying folder). Now "cd" is a multi worded command, "cd" signifies to the computer that you want to use the Change Directory command but you also need to signify where you want to go, so you add the name of the **Folder** you want to move to. In this case let's go to Downloads, so input the following command on Windows and Linux

"cd Downloads"

Quick tip, navigation is Case sensitive, so if you don't properly capitalize it won't work, additionally if you start typing and you have the correct spelling, you can click "Tab" on your keyboard and it will autocomplete for you 

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/a8f31a6a-c771-405c-a2e4-d2e49f70462d)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/4ce212b4-659e-420d-86cd-a2e9b11d93f6)

Now you will notice that the Tilda is now "~/Downloads" or "C:/Users/Username/Downloads" on Windows. This shows you in which folder you are currently located, which is convenient. now if you type ls again, and compare with your File Explorer app, you should see all the matching files


(My Windows example isn't the best, but it should be very clear on a Mac OS and Linux Machine)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/e98e55d6-16f6-4640-a79d-d5eb3e547d1c)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/f179a251-85e9-40ba-8745-6d482e2fe6e7)


Additionally you can go multiple layers deep, or go backwards. I will show the example.

To move back up the folders, or go backwards in folders you can use the "cd ..", the ".." indicates you want to go back.

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/99923117-ca2b-4d56-ad3f-441c035e6760)

And now if I run the same command again I will show the Linux Structure a little more

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/e524a278-b51e-4202-b5fb-fafafd8baba9)

Now, if you're confortable with it and you know the directory structure well on you machine you can move multiple folders at a time by chaining the Folder Names. For example I'll show me going back to the Downloads folder.

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/09a88096-bc1b-4b69-b56e-42ea562ead3f)

As you see I am back at the same location. 

Another quick tip, be careful with "/" placements, on Linux, if you do "cd /folderName" you are telling the computer to look at the root level, and go to the folder you named. Where as if you don't add a "/" beforehand, you are telling it to look at your current location

For reference this is what the Linux Root looks like 

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/957a65d4-d6d1-4c6f-8a0d-c94c24d366fe)

Although it won't be used often to run a "EXE" like file in Linux, assuming it's already an "EXE" like file you can do "./filename.extension" and it will run the file. This will be shown later

Another useful command to know is "clear" once you type it in the terminal it essentially resets your screen. The command may be "cls" on different systems.

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/ee5147f8-7796-4ced-a307-b343e3102653)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/e630df0a-6f00-4317-b47c-8c7caba03900)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/8efe9179-a041-449b-9634-4cdaf37be567)

Now this is basically the bare minimum you'll need so far, until we get to Docker. But I will show a cool thing for Linux Users (and possibly MacOS, idk if it's built in)

In the Nanocar club, since we are majority nano, I have decided to exclusively use the "nano" editor when using Linux. So if you find a file you want to edit, when you are on Linux and you have "nano" installed you can do the following "nano filename.extension" and it will open the file for you to edit. The Following is an example

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/1e985ec2-9441-4124-9645-9bd2cf8ef7c6)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/edafad00-0838-4404-a7b8-6061b438f0d3)


A fun last exercise that you can do if you have Visual Studio Code installed on your device. Go and explore your device and find any directory you want. Once you've found it enter the folder you want to open. And then run "code .". If you have things installed correctly, Visual Studio Code should be opened up and will display your files

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/8e297915-1779-4455-92db-804f00760db5)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/84c477f3-5100-4f71-9cdc-fbf27f7a4d71)

![image](https://github.com/UWFormulaN/Compteam-101/assets/93613553/424f3b8b-7711-40a4-a323-441bdee5105a)

Now you have the basics of Linux and Command line navigation




## Summary

### Commands

- ls  (List)
Shows all files and folders in your curent directory

- cd (Change Directory)
Changes the folder you'r terminal will be located in. Used like "cd folderName"




