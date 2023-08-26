# quickemu-mod  / quickemu-wrap

## Quickemu / Quickget wrapping script

### Powerful text based User Interface  

\@2023.08.26  

[qqX](https://github.com/TuxVinyards/qqX) is now released.  Check it out .... 

- An alternative to quickgui for more advanced users
- Extra diagnostics, easy customising & installation

- Features full wrapping of both Quickemu & Quickget

\@2023.07.28

- Now with zsync for developer daily-live iso's
- Second shared drive (experimental)
- And screen percentage dialog

![Screenshot at 2023-02-22 12-59-04-1920](https://user-images.githubusercontent.com/3956806/220619057-f63883d2-4d0d-4130-94e1-d444f1567be4.jpg)

![QGW](https://github.com/TuxVinyards/quickemu-mod/assets/3956806/c948f51a-a954-4180-ba62-1d5045e5f4fc)

\@ 2023-05-15 Wrapping script now replaces quickemu-tools as default to accompany quickemu original. Use it in a similar way to quickgui but with more features. Start by mouse click on the .conf file or type 'qwrap' at the terminal.

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

![73GiB-windows](https://github.com/TuxVinyards/quickemu-mod/assets/3956806/90e4f9fe-92e2-4163-a76d-4c9da775b7ee)

## Install

The initial set up should be with the original quickemu as normal.  <https://github.com/quickemu-project/quickemu>

Click on here on the 'Code' button, then 'Download ZIP' for the quickemu-mod files.

![Screenshot at 2023-02-21 10-49-29-560](https://user-images.githubusercontent.com/3956806/220318265-e05b5f26-54b6-49e7-bc60-79df14b08a89.png)

The settings file should be placed as `$HOME/.qmod_settings` To override the general settings, further instances may be placed in other individual folders as required.

It is recommended to place the wrap/mod files into the system, as below. This allows you to run them easily from any terminal & reduces the theoretical risk of any sudo calls becoming corrupted:

```bash
sudo cp quickemu-wrap /usr/bin/qwrap

sudo cp quickemu-mod /usr/bin/qmod

cp qmod_settings $HOME/.qmod_settings

# For just the tools set:

sudo cp quickemu-tools /usr/bin/qtools
```

The scripts will list the .conf files of any random folder if a right click is made in the file manager and the script is called from an opened-in terminal.

Another useful way to use the scripts from within a VM folder is to edit the .conf files. Changing the first line from
`#!/usr/bin/quickemu --vm  to  #!/usr/bin/quickemu-wrap --vm  or  #!/usr/bin/qwrap --vm  or similar`  
will allow mouse click starts for qwrap/mod via your file manager.

Read the in-script notes & the settings file for further details on location and other features.

Note the .dot when adding to ~ | $HOME will tidy the file away as hidden. Settings may be edited via the script menu or via ctrl-h etc to unhide.

The scripts have been carefully tested and have been written with plenty of preventative error handling routines. However, as with all software, please remember that standard good practice is to always make backups of anything critical.

## Updates

 \@ 2023/08 Quickemu-Wrap is probably to be seen as fairly complete and tested. The new follow-on project `qqX` to be shortly released, is intended to provide a more complete packaging for this script.

Some recent changes have added new values to the settings file.  When substituting your current wrap script with a newer one, you should also check the settings file for new options. The main script will supply default values for any new items but to change defaults you should paste the new lines into your current file.

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

\@2023.07.28

- Now with zsync for developer daily-live iso's
- Second shared drive.  Currently Experimental.  See recent discussion on quickemu's Discord channel. (with thanks to @gnudoc)

\@2023.07.21

- Add screen percent ui & setting dialog

\@2023.07.21

- Tweak Utils UI  &  add Virtual Hardware Record first install autorun

\@2023.07.18

- Make MSRS dialog less verbose by standard & add settings switch

\@2023.07.18

- Add a delete to trash function.  Fix some consequent array re-scan bugs.

\@2023.07.15  

- Improve the quickget process control.  Also includes the starts of qqX, which is 'coming-soon'

\@2023.07.08  

- Add more options to the Extra Qemu Args menu interface

\@2023/07/05  

- Now features full wrapping of both Quickemu & Quickget
- Improved settings file gives selectable versioning & non-limited VM folders

\@ 2023-06-20  From quickemu 4.8, the value " --screenpct xx"  may be used on SDL, where xx is a value from 25 to 100   (Linux VM's only)   This currently should be added to the settings file eg. `Extra_QE_Params="--screenpct 85"`

\@ 2023-05-15 I have found a way to get a full wrapping script that still gives a menu interface and allows modding. This now replaces quickemu-tools as default to accompany quickemu original. Depending on your point of view, use it in a similar way to quickgui. But with more features.

\@ 2023-05-19  Added the ability to store a record of the Qemu Virtual Hardware profile.  Esp. useful for Windows VM's.
Qwrap only (at present?)  See <https://github.com/quickemu-project/quickemu/issues/572#issuecomment-1531348755>

Also add quickemu version selection to the settings.

I am leaving qMod in place, mainly for use with difficult legacy quickemu 4.2 to 4.4 Windows loading problems.

Global shellcheck supression to help with all the 'args' warnings that come from the original quickemu code has now been moved to the file header.

\@ 2023-05 following comment <https://github.com/quickemu-project/quickemu/issues/572#issuecomment-1530824872>
for completeness, more options for TRIM and Hardware have been added to qmod

Also qmod now has a .conf editor dialogue & PR #434 hash bang starts from a mouse click on the .conf are now possible.

😃
