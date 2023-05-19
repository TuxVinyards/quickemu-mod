# quickemu-mod  / quickemu-tools

## Choose the full modded run-time, or just the tool set

### Command line power with graphical ease

- Replaces quickgui (runtime monitoring)
- Simple mouse click start
- Improves Windows boot up
- Full & extra diagnostics
- Easy customising & installation

![Screenshot at 2023-02-22 12-59-04-1920](https://user-images.githubusercontent.com/3956806/220619057-f63883d2-4d0d-4130-94e1-d444f1567be4.jpg)

\@ 2023-05-15 Now available as a full wrapping script that still gives a menu interface and allows modding. This now replaces quickemu-tools as default to accompany quickemu original. Depending on your point of view, use it in a similar way to quickgui. But with more features. Start by mouse click on the .conf file:

![Screenshot at 2023-05-15 14-38-25](https://github.com/TuxVinyards/quickemu-mod/assets/3956806/1ef00a03-203e-4099-89f7-f5a703cbe920)

qMod remains in place, mainly for use with difficult legacy quickemu 4.2 to 4.4 Windows loading problems.

### qTools: Automates the one by one commands

- Manages multiple snapshots
- Toggles boot-up & temporary MSRS's

Recover gigabytes of qcow storage in moments with snapshot range selection.

![quickemu-tools-ui](https://user-images.githubusercontent.com/3956806/233839490-52f03884-188c-4173-bc71-25184bbb3bad.png)

Use along-side original quickemu or as a drop-in replacement.  

Select VM from a multi-folder list:

![term-tweak](https://user-images.githubusercontent.com/3956806/219943219-ddbe3547-bcd6-4d48-afb0-b549c4810a9c.png)

## Install

The initial set up should be with the original quickemu as normal.  <https://github.com/quickemu-project/quickemu>

Click on here on the 'Code' button, then 'Download ZIP' for the quickemu-mod files.

![Screenshot at 2023-02-21 10-49-29-560](https://user-images.githubusercontent.com/3956806/220318265-e05b5f26-54b6-49e7-bc60-79df14b08a89.png)

The simplest method is just to extract & place files quickemu-mod / wrap & qmod_settings next to your VM .conf files.  Click and go.

Alternatively, add the files to the system so they can be called straight from the terminal:

```bash
sudo cp quickemu-wrap /usr/bin/qwrap

sudo cp quickemu-mod /usr/bin/qmod

cp qmod_settings $HOME/.qmod_settings

# For just the tools set:

sudo cp quickemu-tools /usr/bin/qtools
```

You can also edit the .conf files to create individual mouse click starts for qwrap via your file manager from your VM folder.

Read the qmod main file & settings file for further details on location and other features.

Note the .dot when adding to ~ / $HOME which will tidy the file away as hidden. Edit via the script menu. (or ctrl-h etc to unhide).

Finally, whatever software you are using, standard good practice: always make backups of any critical VM's

## Issues

For Windows Updates & Boot problems, for see my comments and notes to those issues, on Martin's pages:

 <https://github.com/quickemu-project/quickemu/issues/572>  Windows 10 VM won't launch after upgrade from 4.3 to 4.4
 <https://github.com/quickemu-project/quickemu/issues/553>  2022-08 Security Update for Windows fails to install

Make sure you have given the scripts "allow executing" +x permissions.  

![Screenshot at 2023-02-19 10-27-48](https://user-images.githubusercontent.com/3956806/219940371-fb1b778c-3bbc-4739-bdad-caee87a29d18.jpg)

Your file manager may need setting to 'ask each time' in the behaviour section.  Some desktops will be slightly different ...

![Screenshot at 2023-02-19 10-30-38](https://user-images.githubusercontent.com/3956806/219940035-9d4df156-8309-4845-8432-05941749dda1.png)

## Pull Requests

Please make any pull requests annotated. Explain how the code works so everyone can follow what's going on.

No densely packed lines of unexplained regex style hieroglyphics, please.

<http://mywiki.wooledge.org/BashGuide/Practices#Readability>

## Changes

\@ 2023-05-15 I have found a way to get a full wrapping script that still gives a menu interface and allows modding. This now replaces quickemu-tools as default to accompany quickemu original. Depending on your point of view, use it in a similar way to quickgui. But with more features.

\@ 2023-05-19  Added the ability to store a record of the Qemu Virtual Hardware profile.  Esp. useful for Windows VM's.
Qwrap only (at present?)  See <https://github.com/quickemu-project/quickemu/issues/572#issuecomment-1531348755>

I am leaving qMod in place, mainly for use with difficult legacy quickemu 4.2 to 4.4 Windows loading problems.

Global shellcheck supression to help with all the 'args' warnings that come from the original quickemu code has now been moved to the file header.

\@ 2023-05 following comment <https://github.com/quickemu-project/quickemu/issues/572#issuecomment-1530824872>
for completeness, more options for TRIM and Hardware have been added to qmod

Also qmod now has a .conf editor dialogue & PR #434 hash bang starts from a mouse click on the .conf are now possible.

😃
