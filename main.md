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
#### This is what I got 
```
grep -c words ./technical/911report/chapter-1.txt
1
```
This means that in file `chapter-1` only has one word of the word `words`

#### Example two:
This time I did the samething as above but intead of putting `chapter-1` at the end I put `*`.  
