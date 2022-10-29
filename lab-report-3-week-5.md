# __Lab Report 2 (Week 3)__

## __What does general "grep" command do?__

"grep" command is a command-line tool which is used to search for a string of characters in a file.

```
Basic form of grep command syntex : grep <_string of characters_> <_filename_>
```
```
[cs15lfa22df@ieng6-202]:911report:268$ grep Tuesday chapter-1.txt
    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had 
in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.
    On the morning of 9/11, there were only 37 passengers on United 93-33 in addition to the 4 hijackers. This was below the norm for Tuesday mornings during the summer of 2001. But there is no evidence that the hijackers manipulated passenger levels or purchased additional seats to facilitate their operation.
```

The "grep" command search through chapter-1.txt file for the lines where "Tuesday" is written. 

## __Option 1 "grep -h"__

"grep -h" command displays the matched lines, however it doesn't display the filename.

```

```

## __Option 2 "grep -n"__

- "grep -n" command displays the line number and the matched results.

   - _(First Version)_ By using command "grep -n"
```
[cs15lfa22df@ieng6-202]:911report:271$ grep -n Tuesday chapter-1.txt
6:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to 
Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania 
Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
62:    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 
A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight 
attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.
170:    On the morning of 9/11, there were only 37 passengers on United 93-33 in addition to the 4 hijackers. This was below the norm for Tuesda 
 mornings during the summer of 2001. But there is no evidence that the hijackers manipulated passenger levels or purchased additional seats to facilitate their operation.
```

```
[cs15lfa22df@ieng6-202]:~:278$ grep -n February docsearch/technical/911report/chapter-2.txt
6:            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
295:                the time he issued his February 1998 declaration of war, Bin Ladin had nurtured that
647:            In February 1996, Sudanese officials began approaching officials from the United
817:            The February 1998 fatwa thus seems to have been a kind of public launch of a renewed
844:                who were subsequently convicted in the February 1993 attack on the World Trade
891:            On February 23, 1998, Bin Ladin issued his public fatwa. The language had been in
910:                newspaper in London that had first published Bin Ladin's February fatwa, and it
```

```
[cs15lfa22df@ieng6-202]:~:320$ grep -n 18 */*/*/chapter-3.txt
docsearch/technical/911report/chapter-3.txt:15:            At 18 minutes after noon on February 26,1993, a huge bomb went off beneath the two    
docsearch/technical/911report/chapter-3.txt:1123:                wounded, 18 were killed, and the world's television screens showed images of an 
docsearch/technical/911report/chapter-3.txt:1776:            On May 18, CIA's managers reviewed a draft Memorandum of Notification (MON), a legaldocsearch/technical/911report/chapter-3.txt:2562:            The CIA reported on December 18 that Bin Ladin might be traveling to Kandahar and   
docsearch/technical/911report/chapter-3.txt:3081:                lately for direct US military action?"185There are no notes recording whether the
skill-demo1/technical/911report/chapter-3.txt:15:            At 18 minutes after noon on February 26,1993, a huge bomb went off beneath the two  
skill-demo1/technical/911report/chapter-3.txt:1123:                wounded, 18 were killed, and the world's television screens showed images of an
skill-demo1/technical/911report/chapter-3.txt:1776:            On May 18, CIA's managers reviewed a draft Memorandum of Notification (MON), a legal
skill-demo1/technical/911report/chapter-3.txt:2562:            The CIA reported on December 18 that Bin Ladin might be traveling to Kandahar and 
skill-demo1/technical/911report/chapter-3.txt:3081:                lately for direct US military action?"185There are no notes recording whether 
the
```


## __Option 3 "grep -v"__

"grep -l" command displays the list of filenames. 

```

```