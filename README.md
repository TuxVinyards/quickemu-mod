# quickemu-mod  / quickemu-tools
Quickemu Mod - Virtual Machine Launcher  -  A menu interfaced version of quickemu.

### Combines the benefits of the command line with the ease of the graphical.

Added fixes & features:

- Manage multiple snapshots. Recover Disk Space. 
- Toggle boot-up & temporary MSRS's 
- Fix problems from quickemu upgrades & Windows booting 
- Graphical style interface 
- Full technical output with optional extra diagnostics 
- Easy customising

Choice of just the tool set, or the full modded run-time.

![Screenshot at 2023-02-22 12-59-04-1920](https://user-images.githubusercontent.com/3956806/220619057-f63883d2-4d0d-4130-94e1-d444f1567be4.jpg)

Use along-side original quickemu or as a drop-in replacement.  

Select VM from a multi-folder list: 

![term-tweak](https://user-images.githubusercontent.com/3956806/219943219-ddbe3547-bcd6-4d48-afb0-b549c4810a9c.png)

## Install

The initial set up should be with the original quickemu as normal.  https://github.com/quickemu-project/quickemu

Click here on the 'Code' button, then 'Download ZIP'

![Screenshot at 2023-02-21 10-49-29-560](https://user-images.githubusercontent.com/3956806/220318265-e05b5f26-54b6-49e7-bc60-79df14b08a89.png) 

The simplest method is just to place files quickemu-mod & qmod_settings next to your VM .conf files.

Click and go. 👍

![Screenshot at 2023-02-19 10-30-38](https://user-images.githubusercontent.com/3956806/219940035-9d4df156-8309-4845-8432-05941749dda1.png)

Or add files straight to the system so they can be called straight from the terminal:
```
sudo cp quickemu-mod /usr/bin qmod

cp qmod_settings $HOME/.qmod_settings

# For just the tools set:

sudo cp quickemu-tools /usr/bin qtools

```

![quickemu-tools-ui](https://user-images.githubusercontent.com/3956806/222104440-7f347c2a-d912-4c54-aa24-e38fa05e61a7.png)

Read the qmod main file & settings file for further details on location and other features.


## Tweaks

Make sure you have given the scripts "allow executing" +x permissions.  

![Screenshot at 2023-02-19 10-27-48](https://user-images.githubusercontent.com/3956806/219940371-fb1b778c-3bbc-4739-bdad-caee87a29d18.jpg)

Your file manager may need setting to 'ask each time' in the behaviour section.  Some desktops will be slightly different ...



## Issues & Pull Requests

In response to https://github.com/quickemu-project/quickemu/issues/572  Windows 10 VM won't launch after upgrade from 4.3 to 4.4 &  https://github.com/quickemu-project/quickemu/issues/553  2022-08 Security Update for Windows fails to install, I started looking at Martin's quickemu script, in depth  :rofl:

Currently in beta 1.  Hopefully there won't be too many issues. I want to get on with finishing the modded version of QuickGet ...

For Windows Updates & Boot problems, for see my comments and notes to those issues, on Martin's pages.

I have included a (Visual Studio) Code workspace file to help anyone doing editing. The global shellcheck supression will help with all the 'args' warnings that come from the original quickemu code  (may adapt for other editors too).

Please make any pull requests annotated. Everyone codes differently, I know, but I think readabilty & KISS (keep it simple & straightforward) is key. Explain how the code works so everyone can follow what's going on.

http://mywiki.wooledge.org/BashGuide/Practices#Readability 

No densely packed lines of unexplained regex style hieroglyphics, please, to put it another way. 😃
