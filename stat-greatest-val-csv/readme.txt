readme.txt -- for stat-greatest-val-csv

THE TASK
Read a data file, find the greatest value, column by column, and write the
data and greatest values out to a second file.

In detail, the following subtasks must be completed:

1. Write the implementation of the readSheet() method of
   StatsCsv. Reading from the file must be done with CsvReader.
   The main method (provided for you) in StatsCsv will call
   readSheet. (The data format is described below.)

2. The readSheet() method should store the data in sheet (an instance
   variable in StatsCsv).

3. Create a class named Stats in a separate file (Stats.java).
   The class Stats is used to compute the greatest values.

4. Write a method, Stats::greatestValue, that computes the greatest value for
   each column of task scores.

5. Stats::greatestValue should store the greatest value of each of the tasks
   in the row immediately following the last row of data.

6. Stats initialization: As implied by the provided code in
   StatsCsv.java, the Stats::Stats constructor takes three arguments:
   the number of rows used, the number of columns used, and a matrix
   of String values.

7. The constructor should call greatestValue.

8. Write the implementation of the writeSheet() method of
   StatsCsv. Writing from the file must be done with CsvWriter. The
   main method (provided for you) in StatsCsv will call
   writeSheet. (The data format is described below.)

See Data01.csv for the format of an input file. (Note that the input
   file name, Data01.csv, and the output file name, Data02.csv, are
   provided as constants---you should not change these names, and these
   files should be read from the current working directory.

The input data is organized by rows of people with scores on
tasks. Scores are integers. Columns are organized task by task.
You may assume that input data is valid.
The file looks like the following:

1st Name,2nd Name,Task 1,Task 2,Task 3,Task 4,Task 5,Task 6
Andrew,Andrews,10,0,0,0,0,4
Daniel,Boone,7,0,0,7,1,0
Italia,Flower,7,0,0,0,0,0
George,Joseph,10,5,0,7,10,9
Jackson,Kennedy,10,5,3,7,30,9
Sonny,Liston,10,1,1,5,1,8
MadDog,Miller,10,5,8,7,21,8
Kevin,Olson,10,0,1,7,1,6
Ronald,Reagan,10,5,0,7,30,9

If we format this information into rows and columns, the data in this
example looks like this:

1st Name  2nd Name   Task 1  Task 2  Task 3  Task 4  Task 5  Task 6
Andrew    Andrews    10      0       0       0       0       4
Daniel    Boone      7       0       0       7       1       0
Italia    Flower     7       0       0       0       0       0
George    Joseph     10      5       0       7       10      9
Jackson   Kennedy    10      5       3       7       30      9
Sonny     Liston     10      1       1       5       1       8
MadDog    Miller     10      5       8       7       21      8
Kevin     Olson      10      0       1       7       1       6
Ronald    Reagan     10      5       0       7       30      9

The input data may have more or fewer rows and more or fewer columns.
However, no more than 16 rows and 16 columns are needed.

For this example the output (written to Data02.csv) should be:

1st Name,2nd Name,Task 1,Task 2,Task 3,Task 4,Task 5,Task 6
Andrew,Andrews,10,0,0,0,0,4
Daniel,Boone,7,0,0,7,1,0
Italia,Flower,7,0,0,0,0,0
George,Joseph,10,5,0,7,10,9
Jackson,Kennedy,10,5,3,7,30,9
Sonny,Liston,10,1,1,5,1,8
MadDog,Miller,10,5,8,7,21,8
Kevin,Olson,10,0,1,7,1,6
Ronald,Reagan,10,5,0,7,30,9
Greatest,Value,10,5,8,7,30,9

Note that only rows and columns with data are written.

If we format this information into rows and columns (your program will
not do this), the data in this example looks like this:

1st Name  2nd Name   Task 1  Task 2  Task 3  Task 4  Task 5  Task 6
Andrew    Andrews    10      0       0       0       0       4
Daniel    Boone      7       0       0       7       1       0
Italia    Flower     7       0       0       0       0       0
George    Joseph     10      5       0       7       10      9
Jackson   Kennedy    10      5       3       7       30      9
Sonny     Liston     10      1       1       5       1       8
MadDog    Miller     10      5       8       7       21      8
Kevin     Olson      10      0       1       7       1       6
Ronald    Reagan     10      5       0       7       30      9
Greatest  Value      10      5       8       7       30      9


Video demonstrations of a solution for this task are available.
    1. During the exam: as stat-greatest-val-csv.html in the "Solution Demonstration Videos"
       folder on the desktop in the exam delivery environment.
    2. During exam preparation, outside the exam environment.
       https://s3-us-west-2.amazonaws.com/proxor-video/video/stat-greatest-val-csv-transcoded.mp4
