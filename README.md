# **Lab 3**
## Researching Commands
In this lab report, I will choose `grep` as my command.  
### Option One **`-c`**
The option `-c` is used to count the number of occurrences strings that you are looking for in a file.  
This option is useful when you need to look for all the occurrences key strings in these files.  

#### Example one:
I called the `grep` command and use `-c` option for counting the number of occurences of the string `words` in the file `chapter-1.txt`.  
```
grep -c words ./technical/911report/chapter-1.txt
```
#### This is the output
```
grep -c words ./technical/911report/chapter-1.txt
1
```
This means that in file `chapter-1` only has one string of the word `words`

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
The `-i` option will be used to search for the given sentence that matches the string we search for and this is case insensitve.
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

### Option three: **`-v`**
The option `-v` option is used to return all the line that does not match the string that you are looking for.  
#### Example one 
This give use all the lines but the line that contines `words`.  
```
(base) zhenchenglin@ZhenchengdeMacBook-Pro docsearch % grep -v words ./technical/911report/chapter-1.txt



"WE HAVE SOME PLANES"

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.

    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.

INSIDE THE FOUR FLIGHTS

(There are about 700 line hiden)
...
    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.
```                                         
#### Example two
When using `-v` on big file like this will be very useless do to the large amount of output.
```
./technical/plos/pmed.0020249.txt:        with lower, and thus more realistic, challenge doses.
./technical/plos/pmed.0020249.txt:        The belief that experiments involving realistically low challenge doses require
./technical/plos/pmed.0020249.txt:        unfeasibly large numbers of animals has prevented the development of low-dose challenge
./technical/plos/pmed.0020249.txt:        models. In this theoretical study, we show that, contrary to this widely held belief,
./technical/plos/pmed.0020249.txt:        low-dose challenge experiments can be designed such that they do not require large numbers
./technical/plos/pmed.0020249.txt:        of animals. Using statistical power analysis, we compare two experimental designs (see
./technical/plos/pmed.0020249.txt:        Figure 1): (i) a single low-dose challenge design in which each animal is challenged only
./technical/plos/pmed.0020249.txt:        once, and (ii) a repeated low-dose challenge design in which each animal is challenged
./technical/plos/pmed.0020249.txt:        until it is infected or a predetermined maximum number of challenges is reached. We find
./technical/plos/pmed.0020249.txt:        that the repeated low-dose challenge design does not require unfeasibly large numbers of
./technical/plos/pmed.0020249.txt:        animals.
```

### Option four: Using `|`
This is call "Piping output to grep".  
Piping the output of a command to `grep` for pattern matching
`|` takes a standard ouput of one process and passes it as standard input into another process
#### Example one
```
ps aux | grep "java"
zhenchenglin     37442   2.2  0.3 46800572  44972   ??  S     1May23 230:58.22 /Users/zhenchenglin/eclipse/java-2023-03/Eclipse.app/Contents/MacOS/eclipse
zhenchenglin     82860   0.0  0.0 408111792   1168 s013  S+   11:26PM   0:00.00 grep java
```
### Example two
```
(base) zhenchenglin@ZhenchengdeMacBook-Pro docsearch % cat ./technical/911report/chapter-1.txt | grep "error"
    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.
...
(Hiden lines)
    At the White House, the video teleconference was conducted from the Situation Room by Richard Clarke, a special assistant to the president long involved in counterterrorism. Logs indicate that it began at 9:25 and included the CIA; the FBI; the departments of State, Justice, and Defense; the FAA; and the White House shelter. The FAA and CIA joined at 9:40. The first topic addressed in the White House video teleconference-at about 9:40-was the physical security of the President, the White House, and federal agencies. Immediately thereafter it was reported that a plane had hit the Pentagon. We found no evidence that video teleconference participants had any prior information that American 77 had been hijacked and was heading directly toward Washington. Indeed, it is not clear to us that the video teleconference was fully under way before 9:37, when the Pentagon was struck.
The Pentagon Teleconferences. Inside the National Military Command Center, the deputy director for operations immediately thought the second strike was a terrorist attack. The job of the NMCC in such an emergency is to gather the relevant parties and establish the chain of command between the National Command Authority-the president and the secretary of defense- and those who need to carry out their orders.
    * All times given for this conference call are estimates, which we and the Department of Defense believe to be accurate within a � 3 minute margin of error.
````
Which this is another example that shows that takes ones output as input to another.



# **All THE ABOVE INFORMATION WHERE FORM [Here](https://man7.org/linux/man-pages/man1/grep.1.html)**
