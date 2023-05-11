# **Lab 3**
## Researching Commands
In this lab report, I will choose `grep` as my command.  
### Option One **`-c`**
The option `-c` is used to count the number of occurrences words that you are looking for in a file.  
This option is useful when you need to look for all the occurrences key words in these files.  

#### Example one:
I called the `grep` command and use `-c` option for counting the number of occurences of the word `words` in the file `chapter-1.txt`.  
```
grep -c words ./technical/911report/chapter-1.txt
```
#### This is the output
```
grep -c words ./technical/911report/chapter-1.txt
1
```
This means that in file `chapter-1` only has one word of the word `words`

#### Example two:
This time I did the samething as above but intead of putting `chapter-1` at the end I put `*`.  
```
grep -c words ./technical/911report/*
```
The `*` will give us the counts of the `words` in all the files thats in the `911report` directory.  
This will return the count of occurrences of the `words` in each file.
#### This is the output
```
rep -c words ./technical/911report/*
./technical/911report/chapter-1.txt:1
./technical/911report/chapter-10.txt:1
./technical/911report/chapter-11.txt:0
./technical/911report/chapter-12.txt:0
./technical/911report/chapter-13.1.txt:1
./technical/911report/chapter-13.2.txt:1
./technical/911report/chapter-13.3.txt:0
./technical/911report/chapter-13.4.txt:0
./technical/911report/chapter-13.5.txt:0
./technical/911report/chapter-2.txt:1
./technical/911report/chapter-3.txt:3
./technical/911report/chapter-5.txt:2
./technical/911report/chapter-6.txt:3
./technical/911report/chapter-7.txt:3
./technical/911report/chapter-8.txt:0
./technical/911report/chapter-9.txt:0
./technical/911report/preface.txt:0
```
