# quickemu-mod
Quickemu Mod - Virtual Machine Launcher  -  A menu interfaced version of quickemu .....

In response to https://github.com/quickemu-project/quickemu/issues/572  Windows 10 VM won't launch after upgrade from 4.3 to 4.4

&  https://github.com/quickemu-project/quickemu/issues/553  2022-08 Security Update for Windows fails to install

I started looking at the Martin's quickemu script, in depth  :rofl:



![Screenshot at 2023-02-19 10-06-08](https://user-images.githubusercontent.com/3956806/219939020-f3d8c512-4366-4186-8979-eebc879ed2aa.png)

Use this script along-side original quickemu or as a backwardly compatible drop-in replacement.

Currently in beta 1.   QuickGet-Mod to follow shortly, depending on how this fork works out.  

New added fixes & features. Very configurable. Windows Hypervisor Recipes ... See the settings file.

## Install

Currently, set up with the original quickemu as normal.  https://github.com/quickemu-project/quickemu

Then, download the qmod zip to your VMs folder.  The settings file has full details for location tweaks and other features.

Make sure you have given the scripts "allow executing" +x permissions.  

![Screenshot at 2023-02-19 10-27-48](https://user-images.githubusercontent.com/3956806/219940371-fb1b778c-3bbc-4739-bdad-caee87a29d18.jpg)



And that your file manager is set to 'ask each time' in the behaviour section.  Some desktops will be slightly different ...


![Screenshot at 2023-02-19 10-30-38](https://user-images.githubusercontent.com/3956806/219940035-9d4df156-8309-4845-8432-05941749dda1.png)

Set your terminal screen width to wide enough, maybe.

![term-tweak](https://user-images.githubusercontent.com/3956806/219943219-ddbe3547-bcd6-4d48-afb0-b549c4810a9c.png)


Click and go. 👍

## Issues & Pull Requests

Hopefully there won't be too many issues. I want to get on with finishing the modded version of QuickGet ...

I have included a (Visual Studio) Code workspace file to help anyone doing editing. The global shellcheck supression will help with all the 'args' warnings that come from the original quickemu code.  (may adapt for other editors too)

Please make any pull requests annotated. Explain how the code works so everyone can follow what's going on. 

Everyone codes differently, I know, but I think readabilty & KISS (keep it simple & straightforward) is key.

http://mywiki.wooledge.org/BashGuide/Practices#Readability 

No densely packed lines of unexplained regex style hieroglyphics, please, to put it another way. 😃
