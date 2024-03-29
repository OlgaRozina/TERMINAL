## 1. Check where am I:
```
$pwd
```
*The current directory is /<HW_QA_Vadim's>.*
***
## 2. Make a new folder:
```
$pwd
$ mkdir dir_main
```
*A new folder called "dir_main" was created.*
***
## 3. Go to the created folder:
```
$pwd
$ cd dir_main
```
*Redirect to folder dir_main.*
***
## 4. Create 3 new folders:
```
$pwd
$ mkdir dir_1 dir_2 dir_3
```
*Create dir_1 dir_2 dir_3 folders.*
***
## 5.Go into one of the files:
```
$ cd dir_1
```
*Redirect to folder dir_1.*
***
## 6.Create 5 files (3 -.txt, 2 -.json):
```
$ touch 1.txt 2.txt 3.txt 4.json 5.json
```
*Create 1.txt 2.txt 3.txt 4.json 5.json files.*
***
## 7. Create 3 new folders:
```
 mkdir dir_1_1 dir_1_2 dir_1_3
```
*Create dir_1_1 dir_1_2 dir_1_3 folders.*
***
## 8. Show the list of current folder elements:
```
 $ ls
```
*Results: 1.txt  2.txt  3.txt  4.json  5.json  dir_1_1/  dir_1_2/  dir_1_3/*
***
## 9.Open one of txt files
## 10.Write anything in this file
## 11. Save and quit: 
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
## 12. Go to the directory located 1 level above:
```
 $ cd ..
```
*Redirect to folder dir_main*
***
## 13. Move any 2 files to any folder: 
```
 $ mv dir_1/1.txt dir_1/2.txt dir_2
```
*1.txt 2.txt files are moved in dir_2 folder.*
***
## 14. Copy any 2 files to any folder:
```
$ cp dir_1/4.json dir_1/5.json dir_2 
```
*4.json 5.json files are copyed in dir_2 folder.*
***
## 15. Find a file by name:
```
$ find dir_2 -name "1.txt"
```
*dir_2/1.txt is found.*
****
## 16. Show file content in real time, filtered by a keyword:
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
## 16.1. Open file manually from GUI and write a several new line
*(for example, Integer eleifend erat interdum consequat molestie.
Fusce sit amet libero dignissim, consequat lorem sit amet, condimentum tortor)*
```
Displays a test with added lines.
```
***
## 17. Show several of the first lines from the text file:
```
 $ head -n 4 dir_2/1.txt
```
*Results:Praesent et tortor mattis, sagittis nisi eu, lobortis velit.
Duis ultricies leo a maximus dictum.
In rutrum arcu ut sapien malesuada, vel sollicitudin urna ullamcorper.
Fusce et quam sagittis, consequat arcu ac, efficitur magna.*
***
## 18. Show several of the last lines from the text file: 
```
 $ tail -n 4 dir_2/1.txt
```
*Results: Donec congue erat id tortor blandit finibus.
Vestibulum eu ligula et odio dignissim tincidunt euismod sit amet quam.
Integer eleifend erat interdum consequat molestie.
Fusce sit amet libero dignissim, consequat lorem sit amet, condimentum tortor.*
***
## 19. Show content of a large file:
```
 $ less dir_2/1.txt
```
*We see this file content and can navigate. To make navigation easier in this case, you can e.g.:
type -N to show string numbers
type /Fusce to find all "Fusce" words in this file
after the previous command, type / and Enter to go to the next found keyword in the file press space to go to the next page.*
***
## 20. Show current date and time:
```
 $ date
```
*Results: Mon Apr 17 16:45:35     2023*
***
## 21.Send an http request to the server http://162.55.220.72:5005/terminal-hw-request
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
## 22. Write a bash script which does the steps above (№ 3-8,13) 
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
