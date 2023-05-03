##__1. Check where am I:__
```
$pwd
/d/HW_QA_Vadim's
```
*The current directory is /<HW_QA_Vadim's>.*
***
##__2. Make a new folder:__
```
$pwd
$ mkdir dir_main
```
*A new folder called "dir_main" was created.*
***
##__3. Go to the created folder:__
```
$pwd
$ cd dir_main
```
*Redirect to folder dir_main.*
***
##__4. Create 3 new folders:__
```
$pwd
$ mkdir dir_1 dir_2 dir_3
```
*Create dir_1 dir_2 dir_3 folders.*
***
##__5.Go into one of the files:__
```
$ cd dir_1
```
*Redirect to folder dir_1.*
***
##__6.Create 5 files (3 -.txt, 2 -.json):__
```
$ touch 1.txt 2.txt 3.txt 4.json 5.json
```
*Create 1.txt 2.txt 3.txt 4.json 5.json files.*
***
##__7. Create 3 new folders:__
```
 mkdir dir_1_1 dir_1_2 dir_1_3
```
*Create dir_1_1 dir_1_2 dir_1_3 folders.*
***
##__8. Show the list of current folder elements:__
```
 $ ls
```
*Results: 1.txt  2.txt  3.txt  4.json  5.json  dir_1_1/  dir_1_2/  dir_1_3/*
***
##__9.Open one of txt files__
##__10.Write anything in this file__
##__11. Save and quit:__
```
 $ cat > 1.txt
Praesent et tortor mattis, sagittis nisi eu, lobortis velit.
Duis ultricies leo a maximus dictum.
In rutrum arcu ut sapien malesuada, vel sollicitudin urna ullamcorper.
Fusce et quam sagittis, consequat arcu ac, efficitur magna.
Nunc viverra mi vel odio iaculis condimentum.
Nunc in magna vestibulum, vehicula turpis nec, dictum orci.
Donec congue erat id tortor blandit finibus.
Vestibulum eu ligula et odio dignissim tincidunt euismod sit amet quam.
```

*After adding text, press Ctrl+C to save and quit the file.
Need to make sure that the entry is added, for this you need to enter the following command:*
```
$ cat 1.txt
```
*The written text is displayed.*
***
##__12. Go to the directory located 1 level above:__
```
 $ cd ..
```
*Redirect to folder dir_main*
***
##__13. Move any 2 files to any folder:__
```
 $ mv dir_1/1.txt dir_1/2.txt dir_2
```
*1.txt 2.txt files are moved in dir_2 folder.*
***
##__14. Copy any 2 files to any folder:__
```
$ cp dir_1/4.json dir_1/5.json dir_2 
```
*4.json 5.json files are copyed in dir_2 folder.*
***
##__15. Find a file by name:__
```
$ find dir_2 -name "1.txt"
```
*dir_2/1.txt is found.*
****
##__16. Show file content in real time, filtered by a keyword:__
```
$ tail -f dir_2/1.txt
```
*Results: Praesent et tortor mattis, sagittis nisi eu, lobortis velit.
Duis ultricies leo a maximus dictum.
In rutrum arcu ut sapien malesuada, vel sollicitudin urna ullamcorper.
Fusce et quam sagittis, consequat arcu ac, efficitur magna.
Nunc viverra mi vel odio iaculis condimentum.
Nunc in magna vestibulum, vehicula turpis nec, dictum orci.
Donec congue erat id tortor blandit finibus.
Vestibulum eu ligula et odio dignissim tincidunt euismod sit amet quam.*
****
##__16.1. Open file manually from GUI and write a several new line__
*(for example, Integer eleifend erat interdum consequat molestie.
Fusce sit amet libero dignissim, consequat lorem sit amet, condimentum tortor)*
```
Displays a test with added lines.
```
***
##__17. Show several of the first lines from the text file:__
```
 $ head -n 4 dir_2/1.txt
```
*Results:Praesent et tortor mattis, sagittis nisi eu, lobortis velit.
Duis ultricies leo a maximus dictum.
In rutrum arcu ut sapien malesuada, vel sollicitudin urna ullamcorper.
Fusce et quam sagittis, consequat arcu ac, efficitur magna.*
***
##__18. Show several of the last lines from the text file:__
```
 $ tail -n 4 dir_2/1.txt
```
*Results: Donec congue erat id tortor blandit finibus.
Vestibulum eu ligula et odio dignissim tincidunt euismod sit amet quam.
Integer eleifend erat interdum consequat molestie.
Fusce sit amet libero dignissim, consequat lorem sit amet, condimentum tortor.*
***
##__19. Show content of a large file:__
```
 $ less dir_2/1.txt
```
*We see this file content and can navigate. To make navigation easier in this case, you can e.g.:
type -N to show string numbers
type /Fusce to find all "Fusce" words in this file
after the previous command, type / and Enter to go to the next found keyword in the file press space to go to the next page.*
***
##__20. Show current date and time:__
```
 $ date
```
*Results: Mon Apr 17 16:45:35     2023*
***
##__21.Send an http request to the server http://162.55.220.72:5005/terminal-hw-request__
```
$ curl -v http://162.55.220.72:5005/terminal-hw-request
```
```
Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
        100   232  100   232    0     0   2137      0 --:--:-- --:--:-- --:--:--  2148<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
        <title>404 Not Found</title>
        <h1>Not Found</h1>
        <p>The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.</p>
  
```
***
##__22. Write a bash script which does the steps above (№ 3-8,13)__
```
 #!/bin/bash
 cd dir_main
 mkdir name1 name2 name3
 cd name1
 touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json
 mkdir name_1_1 name_1_2 name_1_3
 ls
 cd ..
 mv name1/file_1.txt name1/file_2.txt name2
$ ./mybashscript.sh
```
***