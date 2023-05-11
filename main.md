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
### Option two: **`-i`**
In example two I have choose to use `-i`.  
The `-i` option will be used to search for the given sentence that matches the word we search for and this is case insensitve.
#### Example one  
It will be the same as calling option `-c`, but change the `-c` to `-i`.  
```
grep words ./technical/911report/chapter-1.txt
    The controller only heard something unintelligible; he did not hear the specific words "we have some planes." The next transmission came seconds later: American 11: Nobody move. Everything will be okay. If you try to make any moves, you'll endanger yourself and the airplane. Just stay quiet.
```  
#### Example two
I did the samething for option `-c` exmaple two, but this time the code wasn't that helpful to look at...
```
grep words ./technical/911report/*  
./technical/911report/chapter-1.txt:    The controller only heard something unintelligible; he did not hear the specific words "we have some planes." The next transmission came seconds later: American 11: Nobody move. Everything will be okay. If you try to make any moves, you'll endanger yourself and the airplane. Just stay quiet.
./technical/911report/chapter-10.txt:            Rice said President Bush began the meeting with the words, "We're at war," and that Director of Central Intelligence George Tenet said
./technical/911report/chapter-13.1.txt:                until the summer-if then. In other words, the new administration- like others before
./technical/911report/chapter-13.2.txt:            89. Ibid. The CVR clearly captured the words of the hijackers, including words in
./technical/911report/chapter-2.txt:                accepted way to transliterate Arabic words and names into English. We have relied on
./technical/911report/chapter-3.txt:                foreign intelligence information. In other words, the authorities of the FISA law
./technical/911report/chapter-3.txt:            In the words of Deputy Secretary of State Strobe Talbott, Washington's Pakistan
./technical/911report/chapter-3.txt:                        "surprise.""Commerce" and "marriage" often are codewords for terrorist
./technical/911report/chapter-5.txt:                taught the three operatives basic English words and phrases. He showed them how to
./technical/911report/chapter-5.txt:                read phone books, interpret airline timetables, use the Internet, use code words in
./technical/911report/chapter-6.txt:            In other words, the Yemenis provided strong evidence connecting the Cole attack to al
./technical/911report/chapter-6.txt:                telling him that they were waiting for the magic words from the CIA and the FBI. Nor
./technical/911report/chapter-6.txt:                presidential directive, leaving it a "hollow shell of words without deeds." The CIA
./technical/911report/chapter-7.txt:                to KSM, who then trained Hanjour for a few days in the use of code words.
./technical/911report/chapter-7.txt:                provided them with a few basic English words and phrases.
./technical/911report/chapter-7.txt:                Zacarias Moussaoui. Binalshibh soon contacted KSM and, using code words, reported
```
We can only clearly see the out put for the first file, others were very hard to see.  
