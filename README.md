# Using PeopleSoft

PeopleSoft is a curse on humanity.  

I'm not even sure what "PeopleSoft" (PS) entails, but the curse for me is the web-based user interface to CRUDing on the backend database. I actually feel sorry for anyone who uses it, and you can spot on a screen it a mile away. The tight, small fonts and little boxes littered all over the screen. There's no responsive behavior, it's ugly, slow and unintuitive. There's no modern look to the elements (a la Bootstrap, etc.), boxes are too small for content they are to hold, and changes are impossible. Why? PS is used by large organizations, with multiple levels of committees for approving fixes. Then there's the dreaded spinners and apparent calls to the server with each change of focus for each entry element. There's also no "save an exit" button (it's always click to save, then another click to exit. And, the "Are you sure you want to exit" warning doesn't have a "Save and Exit" option).  

No one should be forced to use such an awful interface, but a lot of us have to, since it's the backend that runs many large organizations. In my case, a major American university. I must use PS to tell the university about my local department's scheduling plans for upcoming terms (what classes, where, times of day, intructor names, etc.). From here, the data goes to student registration pages (also some derivative of PS), payroll, etc. Yuk.

Internally, I am able to create a CSV file containing all information about my department's upcoming course offerings. Something like this:

```
ASTR-101,01,01,LEC,053 -0215,MTWR,03:10 PM,04:00 PM,Y,70,E,last1,first1,emplid1,,
ASTR-102,01,01,LEC,,MTWR,,,Y,120,E,last2,first2,emplid2,,
ASTR-102,02,02,LEC,053 -0206,MTWR,04:10 PM,05:00 PM,Y,70,E,last3,first3,emplid3,,
ASTR-324,01,01,LEC,053 -0215,MTWR,01:10 PM,02:00 PM,Y,48,E,last4,first4,emplid4,,
GEOL-102,01,01,LEC,,MW,07:40 AM,09:00 AM,Y,120,E,last5,first5,emplid5,,
GEOL-102,02,9999,DIS,180 -0233,W,10:10 AM,11:00 AM,Y,30,N,last6,first6,emplid6,,
```
Here you can see classes, week days, times, etc. Making this CSV is also a lot of work, but more so on the side of planning.  The genetic algorithm I used to do this planning is another  topic, but nonetheless, this is our schedule, and it must go into PS by a certain deadline 4 times a year. When I first started as my department's scheduler, I would print this on paper, get out a ruler for keeping track, and type each line into PS. Usually to the tune of 180 classes or so. I know this is crazy, but in large organizations, printing data on one computer to enter into another computer is pretty common.

At one point a while back, I said "enough."  A friend who does web-development once showed me a testing tool called "Selenium," so I decided to take a look.  This project is how I used Selenium to read in my CSV and  type it into PS for me.

# Selenium

[Selenium](https://www.selenium.dev)
