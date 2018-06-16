# Introduction

**rfr** aka **Remove From Recents** is a primitively simple privacy enhancement utility that has the purpose
of selectively removing listed recent items from a Linux user account.  The recent items can be found in the
XML file:

  `~/.local/share/recently-used.xbel`

# Installation Instructions

0. Download rfr from github.com.

  ```
  $ cd ~
  $ git clone https://github.com/loloyd/remove-from-recents.git`
  ```

1. Ensure that rfr is executable.

  `$ chmod +x ~/remove-from-recents/rfr`

2. Optional: Edit rfr with xed, vi, nano or any text editor of your choice so as to make the
   automatic item removal utility more applicable to the end user.
   The row to edit is line 3, mostly the **.zaux** part.

3. Optional: Make rfr available "anywhere".  Use any of the following directions - 3.1 or 3.2.

  1. Add the following line to the end of the file `~/.bashrc`

  `export PATH=$PATH:/home/$USER/remove-from-recents`

  2. Copy the file `rfr` to `/home/$USER/.local/bin/.` or to `/home/$USER/bin/.` or to `/usr/local/bin` or
       to whichever particular location specified in $PATH.
       Use the following command to discover the value in $PATH.

  `$ echo $PATH`

4. Test rfr.

  1. Bring up a Recents view.

    1. Right-click on the Super menu and click on **Preferences**.  Under **Plugins** tab,
           check **Show recent documents plugin**.  Your Super menu should now show Recents places
           and Recents list.
    
    2. Browse `recent:///` with Nautilus or Nemo or any of your file and folder explorer.

  2. Fire up a console terminal and issue rfr with an argument and without an argument.  An acceptable
       and valid argument is actually a prefix to an item to be removed with its full and complete pathname.

# Usage Instructions

Simply issue the following console command:

  `$ rfr`

To remove recent items from the user's `Downloads` folder, issue the following console command `username` should be
replaced with an actual local Linux account username:

  `$ rfr /home/username/Downloads/`

To remove recent items with filenames that start with the letter `t` from the user's `Downloads` folder, issue the following console command `username` should be replaced with an actual local Linux account username:

  `$ rfr /home/username/Downloads/x`