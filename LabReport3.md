# Lab Report 3 - Researching Commands 

# 4 interesting command-line options or alternate ways to use the `grep` command:

## 1) `grep -i` option:

**Ex.1)**

**Command:** 
```
grep -i "peoPLE" technical/911report/chapter-1.txt
```

**Output:** 
```
Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
    Sweeney calmly reported on her line that the plane had been hijacked; a man in first class had his throat slashed; two flight attendants had been stabbed-one was seriously hurt and was on oxygen while the other's wounds seemed minor; a doctor had been requested; the flight attendants were unable to contact the cockpit; and there was a bomb in the cockpit. Sweeney told Woodward that she and Ong were trying to relay as much information as they could to people on the ground.
    All on board, along with an unknown number of people in the tower, were killed instantly.
    All on board, along with an unknown number of people in the tower, were killed instantly.
    Callers reported that a passenger had been stabbed and that two people were lying on the floor of the cabin, injured or dead-possibly the captain and first officer. One caller reported that a flight attendant had been killed.
    Manager, New York Center: Okay. This is New York Center. We're watching the airplane. I also had conversation with American Airlines, and they've told us that they believe that one of their stewardesses was stabbed and that there are people in the cockpit that have control of the aircraft, and that's all the information they have right now.
```

**Ex.2)**

**Command:** 
```
grep -i "pReSiDeNt" technical/911report/preface.txt
```

**Output:**
```
 the President of the United States, the United States Congress, and the American
    To answer these questions, the Congress and the President created the National
    have been superb. We thank the Congress and the President. Executive branch agencies
```


## 2) `ls | grep` option:

**Ex.1)** 

**Command:** 
```
ls technical/911report | grep .txt
```

**Output:**
```
chapter-1.txt
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.1.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-2.txt
chapter-3.txt
chapter-5.txt
chapter-6.txt
chapter-7.txt
chapter-8.txt
chapter-9.txt
preface.txt
```

**Ex.2)**

**Command:**
```
ls technical/ | grep me
```

**Output:**
```
biomed
government
```

## 3) `grep -e` command:

**Ex.1)**

**Command:**
```
grep -e "house" -e "government" technical/911report/chapter-1.txt
```

**Output:**
```
Shortly after the first call, Barbara Olson reached her husband again. She reported that the pilot had announced that the flight had been hijacked, and she asked her husband what she should tell the captain to do. Ted Olson asked for her location and she replied that the aircraft was then flying over houses. Another passenger told her they were traveling northeast. The Solicitor General then informed his wife of the two previous hijackings and crashes. She did not display signs of panic and did not indicate any awareness of an impending crash. At that point, the second call was cut off.
Interagency Collaboration. The FAA and NORAD had developed protocols for working together in the event of a hijacking. As they existed on 9/11, the protocols for the FAA to obtain military assistance from NORAD required multiple levels of notification and approval at the highest levels of government.
    More than the actual events, inaccurate government accounts of those events made it appear that the military was notified in time to respond to two of the hijackings, raising questions about the adequacy of the response. Those accounts had the effect of deflecting questions about the military's capacity to obtain timely and accurate information from its own sources. In addition, they overstated the FAA's ability to provide the military with timely and useful information that morning.
    At 9:59, an Air Force lieutenant colonel working in the White House Military Office joined the conference and stated he had just talked to Deputy National Security Advisor Stephen Hadley. The White House requested (1) the implementation of continuity of government measures, (2) fighter escorts for Air Force One, and (3) a fighter combat air patrol over Washington, 
```

**Ex.2)** 

**Command:** 
```
ls technical/ | grep -e bio -e gov          
```

**Output:** 
```
biomed
government
```

## 4) `grep -v` command:

**Ex.1)**

**Command:**
```
ls technical/ | grep -v biomed  
```

**Output:** 
```
911report
government
plos
```

**Ex.2)** 

**Command:**
```
grep -v "the" technical/911report/preface.txt
```

**Output:** 
```
 PREFACE
                Democrats chosen by elected leaders from our nation's capital at a time of great
                avoid such tragedy again?
                27, 2002).
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                current and previous administrations who had responsibility for topics covered in
                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
                public testimony from 160 witnesses.
                learned.
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                political grievances, but its hostility toward us and our values is limitless. Its
                and equal rights for women. It makes no distinction between military and civilian
                targets. Collateral damage is not in its lexicon.
                and national security did not understand how grave this threat could be, and did not
                fault lines within our government-between foreign and domestic intelligence, and
                sharing information across a large and unwieldy government that had been built in a
                different era to confront different dangers.
                positive-an America that is safer, stronger, and wiser. That September day, we came
                accountability.
            As we complete our final report, we want to begin by thanking our fellow
                Commissioners, whose dedication to this task has been profound. We have reasoned
                built. They have given good advice, and faithfully carried out our guidance. They
                have searched records and produced a multitude of documents for us. We thank
                This final report is only a summary of what we have done, citing only a fraction of
                issues and organizations, we are conscious of our limits. We have not interviewed
                every knowledgeable person or found every relevant piece of paper. New information
                inevitably will come to light. We present this report as a foundation for a better
            We have listened to scores of overwhelming personal tragedies and astounding acts of
                preparing to respond if it becomes necessary. We emerge from this investigation with
                this process with strong opinions about what would work. All of us have had to
                citizens to study, reflect-and act.
            Thomas H. Kean, chair
            Lee H. Hamilton, vice chair
```

