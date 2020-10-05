# Manipulation and Aggregation of Summer Olympic Games, Medal Tables 1896-2012. Project Overview
### The Case
It´s my first day in a Data Science advisory firm and my boss asks me to produce the __official Summer Olympic Games Medal Tables for all Editions from 1896 to 2012__. <br><br>
All I can use is a dataset with raw data containing over 31,000 medals (__summer.csv__) and the official Medal Tables for the Editions 1996 and 1976 from Wikipedia. (__wik_1996.csv__, __wik_1976.csv__). I used the two official Medal Tables as a __reference__ to check whether my code produces the correct output! <br><br>
My goal is to __minimize the divergence__ between my aggregated Medal Tables and the official Medal Tables. Let´s assume that the official number of Gold Medals for the United States in the Edition 1996 is 44 and my code produces 46. This is an absolute divergence of 2. <br> <br>
__Calculate the total absolute divergence for the Editions 1996 and 1976 (the "Score")!__ The __optimal Score is 0__! 

### Fortunately, I could to get some useful information from Sports experts: <br>

Medals awarded in __Team Events__ (one medal for each member of the team) only count as __one Medal__. For example, the Basketball Team of the United States won the Gold Medal in the Edition 2012. In total __12 Basketball Athletes__ from the United States were awarded with a Gold Medal. For the official Medal Table 2012, this only counts as __one Gold Medal__ for the United States!<br> <br>
All Events with __5 or less than 5 medals__ shall be deemed __Singles Events__. All Events with __more than 5 medals__ shall be deemed __Team Events__. It frequently happens that 2 or 3 Athletes share the Bronze medal. Therefore, in total 4 or 5 medals are awarded in these Singles Events. All of these medals count for the official Medal Table! It also happens in Team Events that two Teams share the Bronze medal. Also in this case, in total 4 medals count for the official Medal Table (1 Gold, 1 Silver, 2 Bronze).
<br><br>
To identify all unique Events, the __Event Gender matters__! There are __Men__ Events, __Women__ Events and __Mixed__ Events. Assume that the following medals have been awarded in __Mixed Events__:
- the Event is marked with "__mixed__" or "__pairs__"
- all "__Equestrian__" Events
- all "__Sailing__" Events __before 1988__ (until and including 1984)
- the following medals (index labels) were awarded in __Badminton mixed Double Events__: [21773, 21782, 21776, 21785, 21770, 21779, 23703, 23712, 23706, 23715, 23709, 23700, 25720, 25729, 25723, 25732, 25726, 25717, 27727, 27736, 27730, 27739, 27724, 27733, 29784, 29785, 29786, 29787, 29788, 29789]
