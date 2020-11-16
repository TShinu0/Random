# Introduction to Files and Directories in Linux

## Directories and Files

  
Basics on Directories and files

Linux stores data and programs in  **files**. These are organized in directories. In a simple way, a directory is just a file that contains other files (or directories).

The part of the hard disk where you are authorised to save data is calle your  **home directory**. Normally all the data you want will be saved in files and directories in your home directory. To find your home directory (if you need), type:

  -  echo $HOME

The symbol **~** can also be used for your home directory.

There is a general directory called  **/tmp**  where every user can write files. But files in /tmp usually get removed (erased) when the system boots or periodically, so you should not store in /tmp data that you want to keep permanently.

  
  
## What is in a name?

A file can be fully and uniquely identified by its full name, including all directories to which it belongs. The system starts at the root directory, with name  **/**  The it "splits" into (sub)directories, and these split further, and so on, until you get to a file. For example, a home directory could be  **/usr15/pablo**, on which there is a directory called  **programming**, with a directory inside called  **include**, on which there is a file called  **time.h**  The the full path of this last file will be

   - /usr15/pablo/programming/include/time.h

  
  
Creating and Removing directories

To make a new directory do:

   - mkdir directory-name

To remove a directory that does **not** files inside do:

 -   rmdir directory-name

If the directory has files, you can do the following:

  -  rm -rv directory-name

and you will be asked for each file (or subdirectory) if you want to remove it; or

   - `rm` -frv directory-name

that will remove all files (and subdirectories) without asking any questions.  
  
Changing the working directory

To change ("enter") into a directory do:

   - `cd` directory-name

This assumes that the new directory is a subdirectory of the one you are currently working on. If that is not the case, you will have to type the name, for example:

   - cd /usr/local/share/bin

To go to your home directory do simply:

   - cd

  
  
Renaming directories

To change the name of a directory do:

   - mv directory-name new-name

It will move all the files inside as well.  
  
Creating and Removing files

Creating files can be done in many different ways. Here are a few examples:

-   With an editor (see the section on editors later in this manual):
    
      -  editor file-name
    
-   By copying an existing file:
    
       - cp existing-file new-file
    
-   By type stuff directly into a file:
    
       - cat > file
    
    This will remove the contents of the file, it is has something. If you just want to append to that file do:
    
       - cat >> file
    
    Finish the command by typing  **Ctrl-D**
-   Creating an empty file:
    
       - touch file-name
    

  
  
Renaming files

Similar to renaming a directoty:

   - mv file-name new-name

  
  
Looking at the content of a file

Again, there are many ways to look at it:

-   With an eidtor:
    
       - editor file-name
    
    Be careful since this can change the contents of the fyle (assuming you have "write" permissions for that file).
-   With  **less**:
    
       less file-name
    
    Quit typing  **q**  Here are some other commands that work with  **less**
    
    key stroke    command
    ------------------------------------------------
    Space Bar     for another page
    b or w        to move backwards one page
    d             to move forward half a page
    u             to move backwards half a page
    g             to go to the beginning of the file
    G             to go to the end of the file
    q             to quit
    
-   With  **more**:
    
       more file-name
    
    Quit typing  **q**
-   With cat:
    
       cat file-name
    
    This will type all contents of the file in the screen, so if it is too long you will not be able to see the whole file; use  **less**  or  **more**  instead.

Not all files can be read in the screen. Some times after looking at the contents of a file your screen gets into some "funny" characters; to go back to the regular characters use

   reset

Type this command even if you can't read what is shown in the screen. Perhaps you need to do it twice before your screen comes back to normal.

### Check the below commands in your Linux OS  You'll Discover more in the way
  

| **Type of file** | **Common Extensions** | **Programs to open file** |
| --------------- | ------------- | -------------------- |
| Text | .txt, .text | less, more, cat |
| Images | .jpg, .gif, .pnm, .xpm, .bpm | xv, display
|PostScript| .ps | gv, ghostview
|PDF|.pdf|acroread, gv
|DOS-generated|.rtf, .doc, .xls|openoffice (soffice), abiword
|ZIP compression|.zip|unzip
|GZIP compression|.gz|gunzip
|BZIP compression|.bz, .bz2|bunzip, bunzip2
|Tar archive|.tar|tar
|Tar and gzip compression|.tar.gz, .tgz|tar -z
|Tar and bzip compression|.tar.bz, .tar.bz2|tar -j
|DOS excutable|.exe|strings
|Movie|.mpeg, .mpg|mplayer, totem, xmovie
|cpio archive|.cpio|cpio
|ar archive|.ar|ar
|Debian archive|.deb|less
|Redhat archive|.rpm|rpm
|sound|.wav|bplay
|MP3 sound|.mp3|mpg321
|HTML|.html, .htm|firefox, mozilla, netscape, lynx

Types of files

The system has files of many different type (though for the operating system they are all equivalent). To find the type of a file do

   file file-name

As discussed above, a directory is just a file whose contents are file (names). Another interesting \lq\lq type\rq\rq\ of files are  **symbolic links**; a symbolic link is just another name for a file. Why should you do that? Suppose you have some interesting information on how to use ppp, and you want to have it in your directory called ppp-info as well as in the directory called doc. You could save the file in the ppp-info directory and then copy it to the doc directory. Or you can just have the data in the file howto-ppp in the ppp-info directory and then do (from the doc directory, assuming doc and ppp-info are in the same \lq\lq level\rq\rq ):

   - ln -s ../ppp-info/howto-ppp howto-ppp

Then you can see the howto-ppp from either the ppp-info or the doc directory. Having two files with the same name in this case is okay since the full names are different (the full names will include the directories names, which are different). Both files are equal, editing one will make the changes in the other, since, after all, one file contains the data and the other is just a name. However, there is a difference at the time of removing the files: if you remove the file ppp-info/howto-ppp then the file doc/howto-ppp will be a name for a non-existing file, so it will have nothing in it. But if you remove doc/howto-ppp the data will remain in ppp-info/howto-ppp, since after all what you have done is just to remove a name.  
  
Permissions

In Linux files come with permissions, a way to decide who can read, write (or execute) a file. These permissions are divided into three parts: those for the owner (user) of the file, those for the group to which the owner belongs and then permissions for all the other users (each account, besides a name, has a group or groups to which it belongs; the groups are generally used for administrative stuff). From the point of view of what is allowed to do in a file or directory, permissions are for reading, writing and executing.

To look at the permissions of a file you can use the command

  -  ls -l file-name

The first ten characters will give you the type of file (- for a file, l for a link and d for a directory), the permissions of the owner, the group and all other users. So, if we forget the first character we have read, write and execute permissions. If the permission is granted then the letters r, w or x will appear in the output; otherwise a symbol - will appear. For example, a file with read and write permissions for the owner, read for the group and execute for others (a strange combination!) will show as

- -rw-r----x

To change the permissions of a file or directory you can use the chmod command. Just put first the accounts to which you want to apply the changes (u for user or owner, g for group and o for others), then whether to grant (+) or remove (-) permissions and then r, w or x for the corresponding type of permission. For example

   chmod g+rw file-name
   chmod o-rw file-name

will grant read and write permissions to the group for file-name and remove those same permissions for all other users (of course, the owner falls in the group, so he/she will have permissions).
