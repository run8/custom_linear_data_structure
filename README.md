# custom_linear_data_structure
Custom C++ Linear Data Structure

//////////// This info was taken from canvas on 05NOV19/////////////////////

General instructions:

Pick a group leader and mention his name to your instructor 
Create github project and on board all the members
Create a good communication channel
Create a check list of to do items
Sit down as a group and discuss strategies and architecture the project
Draw your UML digram, both your Simple_stat class UML and entire class interaction UML: you will earn a significant amount of credit for this
Ask for help and offer help: speak out if you need help

//////////
Learning objectives are to:

Study and apply linear structures learned in the class
Study and apply C++ standard containers
Study and apply C++ templates
Custom design of data structures
Draw   UML class and class interaction diagrams
Learn simple statistics operations 
Learn Git and GitHub operations
The solution objective of this project is to represent a series of numeric type (both integer and double) data (is called "data object" from now on) that offers LaTeX: \Theta\left(1\right)
Θ
(
1
)
 access to few statistics (mentioned below)  according to below properties:

typical data object has a lot of duplicate entries 
there is no limit to the number of unique data elements inside
data object supports simple statistics such as mode (Links to an external site.), median (Links to an external site.), mean (Links to an external site.) ,  standard deviation (Links to an external site.), min and max
fastest possible access to above statistics is paramount
so above statistics also represent a part of the state of the data object
both fast access and saving space is paramount; developer must strive to use the smallest space possible for storage and must give LaTeX: \Theta\left(1\right)
Θ
(
1
)
 access to above statistics when demanded
In addition to above mentioned states, your data structure must support below operations:
append: append new data from the end
removen (from any place): remove n number of a given data element
empty: delete all data
feed: append from from any standard C++ container (any that supports iteration) data type (std::array, std::vector, std::set, etc)). This may be bit hard. Search about this and really have a meaningful discussion within the team.  Only one feed method is allowed: this means no overloaded feed methods
search (fastest possible among the choices what we have  discussed in the class): must return the location of the first occurrence and repetition. For example, if the first occurrence of data value 20 is 3  and there are 10 of 20s, then you must return 3 and 10 as the search result of 20
array index operator, []: access each unique element through an index: overload the array index operator ([]) so that the ith data element in an instance of your data object, db can be accessed like db[i]
length_unique: number of unique elements in your data object
length_total: total number of elements in your data object
unique_set: return all the unique elements as an std::set
getters (all must be LaTeX: \Theta\left(1\right)
Θ
(
1
)
):
get_mode: returns the mode value of the current entire data set
get_median: returns the median value of the current entire data set
get_ mean: returns the mean value of the current entire data set
get_SD: returns the standard deviation  of the current entire data set
get_min: returns the minimum data item in the current entire data set
get_max: returns the maximum data item in the current entire data set 
Below are requirements and restrictions:

The principle data structure must be the most qualified linear structure we discussed so far in the class . So in the implementation you must use the code provided in Canvas also linked here
Updates (append, feed, removen) to the data object is possible though rare. However, the demands for above statistics is very frequent (You now understand why we need LaTeX: \Theta\left(1\right)
Θ
(
1
)
)
Though you must try to save space, your most important task is to give LaTeX: \Theta\left(1\right)
Θ
(
1
)
 access to above statistics; we are sacrificing the space for speed. In regard of this you are allowed to use other data structures and algorithms provided in the standard C++. You are not allowed to use any third party or external libraries (like boost)
Calculation of above statistics must be private internal operations. This means you have to calculate and update them as you create, insert, append, removen, and feed
Creation: only two constructors:
default: just empty data object
create by adding data items from any standard C++ container (any that supports iteration) data type (std::array, std::vector, std::set, etc)). This may be bit hard. Search about this and really have a meaningful discussion within the team
Removen: remove 1 to any (n) number of data item from the data object. You must validate the existence of n number of data item before the removal 
The data is heavily duplicated. In situations like this we discussed storing pointers as a solution in the class. However, you are not allowed to use this (storing pointers) method here.
You are not allowed to use any C/C++ math libraries
Write your entire solutions with the class name "Simple_stat" in a single header named "simple_stat.h" file and test it in a separate main program
In the same project since you will be using linear structures headers linked here, make sure those headers contain the copyright note, "

// From the software distribution accompanying the textbook

// "A Practical Introduction to Data Structures and Algorithm Analysis,

// Third Edition (C++)" by Clifford A. Shaffer.

// Source code Copyright (C) 2007-2011 by Clifford A. Shaffer."
This is very important as your project in GitHub is opensource. 
I updated code zip file I posted with this note. So if you download 
the latest linked here you are good to go.

Submission:

Each group member must have a GitHub account and must show in the project as an active contributor
Good readme.md page in github 
complete UML class digram for Simple_stat class and overall class interaction diagram for the entire project
Testing criteria: soon to be updated
