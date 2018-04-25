== Installation Instructions ==

1. Ensure that rfr is executable.

  $ chmod +x ~/Projects/remove-from-recents/rfr

2. Edit rfr with xed/vi/nano so as to make the automatic item removal utility more applicable to the end user.
   The row to edit is line 3, mostly the **.zaux** part.

3. Make rfr available "anywhere".

  3.1. Add the following line to the end of the file ~/.bashrc

export PATH=$PATH:/home/$USER/Projects/remove-from-recents

  3.2. Copy rfr to /home/$USER/.local/bin/. or to /home/$USER/bin/. or to /usr/local/bin or
       to whichever particular location specified in $PATH.
       Use the following command to discover the value in $PATH.

  $ echo $PATH

4. Test rfr.

  4.1. Bring up a Recents view.

    4.1.1. Right-click on the Super menu and click on **Preferences**.  Under **Plugins** tab,
           check **Show recent documents plugin**.  Your Super menu should now show Recents places and Recents list.

    4.1.2. Browse "recent:///" with Nautilus or Nemo or any of your file and folder explorer.

  4.2. Fire up a console terminal and issue rfr with an argument and without an argument.  An acceptable and valid
       argument is actually a prefix to an item to be removed with its full and complete pathname.

