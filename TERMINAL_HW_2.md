## 1. Make a folder named dir_1: 
```
$ mkdir dir_1
```
***
## 2. Go to the folder dir_1:
```
$ cd dir_1
```
***
## 3. Create a folder named inner_dir_1:
```
$ mkdir dir_1
```
***
## 4. Create a folder named inner_dir_1:
```
$ pwd
```
*Result: /d/HW_QA_Vadim's/dir_1*
***
## 5. While located inside the dir_1 folder, create an empty text file named tf_1.txt:
```
$ touch tf_1.txt
```
***
## 6. While located the dir_1 folder, create a text file named tf_2.txt using the command cat with the following lines:
```
$ cat > tf_2.txt
the first 1
the second 2
the third 3
```
***
## 7. Go to the inner_dir_1 folder:
```
$ cd inner_dir_1
```
***
## 8. Use the cat command to create a text file named tf_3.txt with any lines:
```
$ cat > tf_3.txt
Vestibulum eu arcu vel ipsum efficitur luctus id pulvinar sem.
Proin vehicula mauris in facilisis mattis.
Phasellus condimentum erat ultricies lacus sagittis aliquet.
Morbi et nulla ornare, elementum nisi eu, tempor est.
Nulla quis erat et urna maximus dictum.
```
***
## 9. Use the cat command to add the line "the second 2" to the text file tf_3.txt:
```
$ cat >> tf_3.txt
the second 2
```
***
## 10. Use the cat command to add the line "the sec 2" to the text file tf_3.txt:
```
$ cat >> tf_3.txt
the sec 2
```
***
## 11. Use the cat command to add the line "the sec 3" to the text file tf_2.txt:
```
$ cat >> ../tf_2.txt
the sec 3
```
***
## 12. Use the cat command to add the line "the SeCoNd 2" to the text file tf_3.txt:
```
$ cat >> tf_3.txt
the SeCoNd 2
```
***
## 13. Use the cat command to add the line "the seConD 2" to the text file tf_2.txt:
```
$ cat >> ../tf_2.txt
the sec 3
the seConD 2
```
***
## 14. Create a text file named tf_4.txt with 15 lines:
```
$ seq 15 | cat > tf_4.txt
```
***
## 15. Create a text file named tF_5.txt with 13 lines:
```
$ seq 13 | cat > tF_5.txt
```
***
## 16. Display a list of all files in the folder:
```
$ ls
```
*Result: tF_5.txt  tf_3.txt  tf_4.txt*
***
## 17. Go out of the inner_dir_1 folder:
```
$ cd ..
```
***
## 18. Display the contents of the file tf_3.txt in the terminal:
```
$ cat inner_dir_1/tf_3.txt
Vestibulum eu arcu vel ipsum efficitur luctus id pulvinar sem.
Proin vehicula mauris in facilisis mattis.
Phasellus condimentum erat ultricies lacus sagittis aliquet.
Morbi et nulla ornare, elementum nisi eu, tempor est.
Nulla quis erat et urna maximus dictum.
the second 2
the sec 2
the SecoNd 2
```
***
## 19. Find the path to the file tf_4.txt:
```
$ find . -name "tf_4.txt"
```
*Result: ./inner_dir_1/tf_4.txt*
***
## 20. Clear the contents of the file tf_4.txt without deleting the file itself:
```
$ > inner_dir_1/tf_4.txt
```
***
## 21. Find the paths to files that have "tf" in their name:
```
$ find . -name "*tf*"
```
*Result:
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./tf_1.txt
./tf_2.txt
./tf_4.txt*
***
## 22. Find the paths to files that have "tf" in their name with letters in any case:
```
$ find . -iname "*tf*"
```
*Result: 
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./inner_dir_1/tF_5.txt
./tf_1.txt
./tf_2.txt
./tf_4.txt*
***
## 23. Find lines in files that contain the letter combination "sec" in the current folder:
```
$ grep "sec" ./*
```
*Result: 
grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
./tf_2.txt:thr sec 3
./tf_2.txt:the sec 3*
***
## 24. Find lines in files that contain the letter combination "sec" in any case in the current folder:
```
$ grep -i "sec" ./*
```
*Result: 
grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
./tf_2.txt:thr sec 3
./tf_2.txt:the sec 3
./tf_2.txt:the seComD 2*
***
## 25. Find lines in files that contain only the "sec" letter combination in the current folder:
```
$ grep -w "sec" ./*
```
*Result: 
grep: ./inner_dir_1: Is a directory
./tf_2.txt:thr sec 3
./tf_2.txt:the sec 3*
***
## 26.Find lines in files that contain only the "sec" letter combination in any case in the current folder:
```
$ grep -i -w "sec" ./*
```
*Result: 
grep: ./inner_dir_1: Is a directory
./tf_2.txt:the sec 3
./tf_2.txt:the sec 3*
***
## 27. Find lines in files that contain the letter combination "second" in the current folder:
```
$ grep -r "second" ./
```
*Result: 
./inner_dir_1/tf_3.txt:the second 2
./tf_2.txt:the second 2*
***
## 28. Find lines in files that contain the letter combination "second" in any case in the current folder:
```
$ grep -r -i "second" ./*
```
*Result: 
./inner_dir_1/tf_3.txt:the second 2
./inner_dir_1/tf_3.txt:the SecoNd 2
./tf_2.txt:the second 2*
***
## 29.Find lines in files that contain the letter combination "second" in all subfolders:
```
$ grep -r "second"
```
*Result: 
inner_dir_1/tf_3.txt:the second 2
tf_2.txt:the second 2*
***
## 30.Find only the path and file name in lines that contain the letter combination "second" in the current folder:
```
$ grep -ls "second" ./*
```
*Result: ./tf_2.txt*
***
## 31. Find all lines in all files that do not contain the combination "second":
```
$ grep -r -v "second" *
```
*Result: 
inner_dir_1/tf_3.txt:Vestibulum eu arcu vel ipsum efficitur luctus id pulvinar sem.
inner_dir_1/tf_3.txt:Proin vehicula mauris in facilisis mattis.
inner_dir_1/tf_3.txt:Phasellus condimentum erat ultricies lacus sagittis aliquet.
inner_dir_1/tf_3.txt:Morbi et nulla ornare, elementum nisi eu, tempor est.
inner_dir_1/tf_3.txt:Nulla quis erat et urna maximus dictum.
inner_dir_1/tf_3.txt:the sec 2
inner_dir_1/tf_3.txt:the SecoNd 2
inner_dir_1/tF_5.txt:1
inner_dir_1/tF_5.txt:2
inner_dir_1/tF_5.txt:3
inner_dir_1/tF_5.txt:4
inner_dir_1/tF_5.txt:5
inner_dir_1/tF_5.txt:6
inner_dir_1/tF_5.txt:7
inner_dir_1/tF_5.txt:8
inner_dir_1/tF_5.txt:9
inner_dir_1/tF_5.txt:10
inner_dir_1/tF_5.txt:11
inner_dir_1/tF_5.txt:12
inner_dir_1/tF_5.txt:13
tf_2.txt:the first 1
tf_2.txt:the third 3
tf_2.txt:the sec 3
tf_2.txt:the sec 3
tf_2.txt:the seComD 2*
***
## 32. Find only the names and paths of files that do not contain the combination "second":
```
$ grep -r -v "second" *
```
*Result: 
inner_dir_1/tf_3.txt:Vestibulum eu arcu vel ipsum efficitur luctus id pulvinar sem.
inner_dir_1/tf_3.txt:Proin vehicula mauris in facilisis mattis.
inner_dir_1/tf_3.txt:Phasellus condimentum erat ultricies lacus sagittis aliquet.
inner_dir_1/tf_3.txt:Morbi et nulla ornare, elementum nisi eu, tempor est.
inner_dir_1/tf_3.txt:Nulla quis erat et urna maximus dictum.
inner_dir_1/tf_3.txt:the sec 2
inner_dir_1/tf_3.txt:the SecoNd 2
inner_dir_1/tF_5.txt:1
inner_dir_1/tF_5.txt:2
inner_dir_1/tF_5.txt:3
inner_dir_1/tF_5.txt:4
inner_dir_1/tF_5.txt:5
inner_dir_1/tF_5.txt:6
inner_dir_1/tF_5.txt:7
inner_dir_1/tF_5.txt:8
inner_dir_1/tF_5.txt:9
inner_dir_1/tF_5.txt:10
inner_dir_1/tF_5.txt:11
inner_dir_1/tF_5.txt:12
inner_dir_1/tF_5.txt:13
tf_2.txt:the first 1
tf_2.txt:the third 3
tf_2.txt:thr sec 3
tf_2.txt:the sec 3
tf_2.txt:the seComD 2*
***
## 33. Display the last 4 lines of any text file in the terminal:
```
$ tail -n4 inner_dir_1/tf_3.txt
```
*Result:
Nulla quis erat et urna maximus dictum.
the second 2
the sec 2
the SecoNd 2*
***
## 34. Display the first 4 lines of any text file in the terminal:
```
$ head -n4 inner_dir_1/tf_3.txt
```
*Result: 
Vestibulum eu arcu vel ipsum efficitur luctus id pulvinar sem.
Proin vehicula mauris in facilisis mattis.
Phasellus condimentum erat ultricies lacus sagittis aliquet.
Morbi et nulla ornare, elementum nisi eu, tempor est.*
***
## 35. One-line command. Create a folder and create a text file with content:
```
$ mkdir inner_dir_2 && cat > inner_dir_2/file_1.txt
```
*Result: 
Suspendisse sed leo accumsan, semper nisl a, aliquam felis.
Cras in dui viverra, convallis turpis ut, pretium ex.
Integer cursus quam porta, imperdiet purus at, imperdiet orci.
Quisque eleifend nisi eget tellus placerat blandit.*
***
## 36. One-line command. Move all text files that contain the word "sec" in their content to any single folder:
```
$ grep -r -l -w "sec" | xargs mv -t inner_dir_2
```
***
## 37. One-line command. Copy all text files that contain the word "sec" in their content to any single folder:
```
$ grep -r -l -w "sec" | xargs cp -t inner_dir_1
```
***
## 38. One-line command. Find all lines with "sec" in all text files, copy and paste these lines into one newly created text file:
```
$ grep -r -h sec | xargs echo >> new_tf.txt
```
***
## 39. One-line command. Delete text files that contain the word "sec" in their content:
```
$ grep -r -l -w sec | xargs rm
```
***
## 40. Simply output the string "Good job!!" to the terminal:
```
$ echo Good job!
```
*Result: Good job!*
***