# Lab Report 3

## Find Command
### Command 1: -maxdepth
- **First Example :**
```
Juans-MacBook-Pro:technical juan$ find government -maxdepth 1
government
government/About_LSC
government/Env_Prot_Agen
government/Alcohol_Problems
government/Gen_Account_Office
government/Post_Rate_Comm
government/Media
```
   - The maxdepth command takes a postive integer n as an argument and descends at most n directory levels. Therefore, since we called -maxdepth with 1, it only descended to the directories in the government directory but did not descend into each directory.

- **Second Example:**
```
Juans-MacBook-Pro:technical juan$ find plos -maxdepth 0
plos
```
   - Similar to the first example, it only descends at most n direectory levels. However, since the given integer with -maxdepth was 0, it only descended to directory at the command line. Overall, this command can be very useful when we want to know which directories are within a specific directory which limits the amount of information you want to know.
  - Found useful information about maxdepth using the man find command at the terminal.

### Command 2: -type
- **First Example:**
```
Juans-MacBook-Pro:technical juan$ find government -type d
government
government/About_LSC
government/Env_Prot_Agen
government/Alcohol_Problems
government/Gen_Account_Office
government/Post_Rate_Comm
government/Media
```
   - The type command takes a specific letter which describes a file type and descends the those types of files. In our argument with -type, we put d as the file type which refers to directory. Therefore the government directory descended the file types that are directories.

- **Second Example:**
```
Juans-MacBook-Pro:technical juan$ find 911report -type f
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
   - In this example, we use a different file type. Instead of using d, we used f as a given argument which refers to regular files. Therefore, this command descended regular files within 911report. However, as we can see, the command line did not print because 911report is a directory and not of type f. Therefore, this command can be useful when we want to find specific types of files instead of looking at every file.
  - Found information of the type command using the man find command at the terminal.

### Command 3: -prune
- **First Example:**
```
Juans-MacBook-Pro:technical juan$ find plos -prune
plos
```
   - The prune command takes no argument. However, the prune command causes for find to not descend into the current file. Therefore, the only given output was the file given as an argument for find.

- **Second Example:**
```
Juans-MacBook-Pro:technical juan$ find biomed -prune
biomed
```
   - Similar to the first example, the prune comman caused for find to not descend into the biomed file. Therefore the prune command only gives the current file as the output. However, this command can be useful when a file can contain lots of files within it. Therefore, this command can be useful when trying to find out if a file can be found from the command find.
  - Found information about the prune command at the terminal using the man find command.

### Command 4: -ls
- **First Example:**
```
Juans-MacBook-Pro:technical juan$ find 911report -ls
24647405        0 drwxr-xr-x   19 juan             staff                 608 Apr 27 10:25 911report
24647413      520 -rwxr-xr-x    1 juan             staff              265912 Apr 27 10:23 911report/chapter-13.4.txt
24647414      576 -rwxr-xr-x    1 juan             staff              290993 Apr 27 10:23 911report/chapter-13.5.txt
24647410      176 -rwxr-xr-x    1 juan             staff               89854 Apr 27 10:23 911report/chapter-13.1.txt
24647411      216 -rwxr-xr-x    1 juan             staff              110568 Apr 27 10:23 911report/chapter-13.2.txt
24647412      296 -rwxr-xr-x    1 juan             staff              150467 Apr 27 10:23 911report/chapter-13.3.txt
24647416      520 -rwxr-xr-x    1 juan             staff              264360 Apr 27 10:23 911report/chapter-3.txt
24647415      160 -rwxr-xr-x    1 juan             staff               79803 Apr 27 10:23 911report/chapter-2.txt
24647406      232 -rwxr-xr-x    1 juan             staff              118656 Apr 27 10:23 911report/chapter-1.txt
24647417      200 -rwxr-xr-x    1 juan             staff               99008 Apr 27 10:23 911report/chapter-5.txt
24647418      296 -rwxr-xr-x    1 juan             staff              149063 Apr 27 10:23 911report/chapter-6.txt
24647419      256 -rwxr-xr-x    1 juan             staff              128370 Apr 27 10:23 911report/chapter-7.txt
24647421      296 -rwxr-xr-x    1 juan             staff              149644 Apr 27 10:23 911report/chapter-9.txt
24647420      168 -rwxr-xr-x    1 juan             staff               84835 Apr 27 10:23 911report/chapter-8.txt
24647422       24 -rwxr-xr-x    1 juan             staff                9332 Apr 27 10:23 911report/preface.txt
24647409      256 -rwxr-xr-x    1 juan             staff              127587 Apr 27 10:23 911report/chapter-12.txt
24647407       96 -rwxr-xr-x    1 juan             staff               47307 Apr 27 10:23 911report/chapter-10.txt
24647408      144 -rwxr-xr-x    1 juan             staff               71151 Apr 27 10:23 911report/chapter-11.txt
```
   - The ls command takes no argument as well. However, the ls command gives information of the given files such as its inode number, size, file permissions, owner, last modification, and pathname.
 
- **Second Example:**
```
Juans-MacBook-Pro:technical juan$ find government -maxdepth 1 -ls
24648262        0 drwxr-xr-x    8 juan             staff                 256 Apr 27 10:25 government
24648263        0 drwxr-xr-x   19 juan             staff                 608 Apr 27 10:25 government/About_LSC
24648286        0 drwxr-xr-x   16 juan             staff                 512 Apr 27 10:25 government/Env_Prot_Agen
24648281        0 drwxr-xr-x    6 juan             staff                 192 Apr 27 10:25 government/Alcohol_Problems
24648301        0 drwxr-xr-x   93 juan             staff                2976 Apr 27 10:25 government/Gen_Account_Office
24648539        0 drwxr-xr-x   16 juan             staff                 512 Apr 27 10:25 government/Post_Rate_Comm
24648393        0 drwxr-xr-x  147 juan             staff                4704 Apr 27 10:25 government/Media
```
   - Similar to the first example, the ls command gave information about the given files. However, in this example, we used the command -maxdepth as well which we already discussed about. Since we only went to the directoriese in the government directory, the ls command only applied to those directories. Therefore, from our output we can see information about the directories within the government directory. The ls command can be useful when one is trying to find useful and important information about a specific file.
  - Found information about ls command using man find in the terminal and at <https://www.redhat.com/sysadmin/linux-find-command> 
