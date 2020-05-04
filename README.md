# Random
Random-stuff
#### I will need you to make 25 exercises by tonight on the following commands. 
#ls, mkdir, cd, cat, echo, touch, grep, tree #####

##1. ls --> ls - list directory contents

Intro :-->
            List  information  about  the FILEs (the current directory by default).
            `ls` is a command used to list files on the system. By passing flags to it 
            (eg: `-l`, `-r` etc.) we can decide which files get displayed first.

###Questions:--

            ####1. List all the files in the directory ?
            ####2. List the files in reverse alphabetical order ?
            ####3. List all the file directory with author of each file ?
            ####4. List all the files in a long listing format ?

##2. mkdir --> mkdir - make directories

Intro :--> 
            mkdir is a command to Create the DIRECTORY(ies), if they do not already exist.
            you can also create multiple directories print message for every directory
            using the flags like (eg: -v , -p ) 

###Questions:--

            ####1. create a directory named "Edyst" ?
            ####2. create multiple directory which contains "Edyst/Test" using flags ?
            ####3. create a directory with output showing directory created ?

##3. cd ---> cd - Current directory

Intro :--> 
            cd is the current directory to move between the directories in the spectific 
            folder or in file

###Questions:--

            ####1. Move from the curent Edyst directory to Test directroy ?
            ####2. Move back to the Home  directory in using ".."(Two dots represent parent directory) ?
            ####3. Move to the Edyst/Test/current directory using a single cd commend ?

##4. cat ---> cat - concatenate files and print on the standard output

Intro :---> 
            Concatenate FILE(s) to standard output.

###Questions:--

            ####1. display the data that contains in the file named "yolo.txt" ?
            ####2. Display the data that is in the file "yolo.txt" with numbering for each line ?
            ####3. Display the data that is in the file named "yolo.txt" without any empty output lines ?
            ####4. Display the data in the file named "yolo.txt" and with "$" at the end of each line ?

##5. echo ---> echo - display a line of text

Intro :---> 
            Echo the STRING(s) to standard output.

###Questions:--

            ####1. Print the line "Hello World!" using echo ?
            ####2. Use the echo commad to display "Hello World!" and a new line ?
            ####3. Print the line "Hello world!" and "hello" with tab space in between?


##6. touch --> touch - change file timestamps

Intro :--> 
            Update  the  access  and modification times of each FILE to the current
            time.
            A FILE argument that does not exist is created empty, unless -c  or  -h
            is supplied.
            A  FILE  argument  string of - is handled specially and causes touch to
            change the times of the file associated with standard output.
            Mandatory arguments to long options are  mandatory  for  short  options
            too.

###Questions:--

            ####1. Create a file named "world.txt" using touch ?
            ####2. Change the access time and modification time of the file "world.txt" to now ?

##7. Grep --> print lines that match patterns

Intro :-->  grep  searches  for PATTERNS in each FILE.  PATTERNS is one or patterns
            separated by newline characters, and grep prints each line that matches
            a pattern.

###Questions:--

            ####1.Output all the files consisting of name index ?
            ####2. Output all the files which has "s" as the begining of the filename ?
            ####3. list all the files that has letter "p" in its name ?
            ####4. List the files that has the extenstion at the end of the file as .html ?

##8. tree --->  tree - list contents of directories in a tree-like format.

Intro :-->  Tree is a recursive directory listing program that produces a depth in‐
       dented listing of files,  which  is  colorized  ala  dircolors  if  the
       LS_COLORS  environment  variable  is set and output is to tty.  With no
       arguments, tree lists the files in the current directory.  When  direc‐
       tory  arguments  are given, tree lists all the files and/or directories
       found in the given directories each in turn.  Upon completion of  list‐
       ing all files/directories found, tree returns the total number of files
       and/or directories listed.

###Questions:--

        ####1. list the tree of the current directory ?
        ####2. List only the directories ?
        ####3. list all the directories in tree matching the pattern [A-Z] ?
