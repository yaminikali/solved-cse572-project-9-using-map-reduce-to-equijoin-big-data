Download Link: https://assignmentchef.com/product/solved-cse572-project-9-using-map-reduce-to-equijoin-big-data
<br>
The required task is to write a map-reduce program that will perform equijoin.

<ul>

 <li>The code should be in Java (use <strong>Java 1.8.x</strong>) using Hadoop Framework (use <strong>Hadoop </strong></li>

</ul>

<strong>2.7.x</strong>).

<ul>

 <li>The code would take two inputs, one would be the HDFS location of the file on which the equijoin should be performed and other would be the HDFS location of the file, where the output should be stored.</li>

</ul>




<h1>Format of the Input File: –</h1>

Table1Name, Table1JoinColumn, Table1Other Column1, Table1OtherColumn2, ……..

Table2Name, Table2JoinColumn, Table2Other Column1, Table2OtherColumn2, ………




<h1>Format of the Output File: –</h1>

If Table1JoinColumn value is equal to Table2JoinColumn value, simply append both line side by side for Output. If Table1JoinColumn value does not match any value of Table2JoinColumn, simply remove them for the output file. You should not include two joins contains same row (No duplicate joins in output file).




<h1>Note: –</h1>

Table1JoinColumn and Table2JoinColumn would both be Integer or Real or Double or Float, basically Numeric.




<h1>Example Input : –</h1>

R, 2, Don, Larson, Newark, 555-3221

S, 1, 33000, 10000, part1

S, 2, 18000, 2000, part1

S, 2, 20000, 1800, part1

R, 3, Sal, Maglite, Nutley, 555-6905

S, 3, 24000, 5000, part1

S, 4, 22000, 7000, part1

R, 4, Bob, Turley, Passaic, 555-8908

<h1>Example Output: –</h1>

R, 2, Don, Larson, Newark, 555-3221, S, 2, 18000, 2000, part1

R, 2, Don, Larson, Newark, 555-3221, S, 2, 20000, 1800, part1

R, 3, Sal, Maglite, Nutley, 555-6905, S, 3, 24000, 5000, part1

S, 4, 22000, 7000, part1, R, 4, Bob, Turley, Passaic, 555-8908




<strong>Another correct answer is: </strong>

R, 2, Don, Larson, Newark, 555-3221, S, 2, 18000, 2000, part1

R, 2, Don, Larson, Newark, 555-3221, S, 2, 20000, 1800, part1

R, 3, Sal, Maglite, Nutley, 555-6905, S, 3, 24000, 5000, part1

R, 4, Bob, Turley, Passaic, 555-8908, S, 4, 22000, 7000, part1




So it means that whether R is before S is not required in the result. But you cannot have both

S, 4, 22000, 7000, part1, R, 4, Bob, Turley, Passaic, 555-8908 and

R, 4, Bob, Turley, Passaic, 555-8908, S, 4, 22000, 7000, part1 in the output.




You cannot assume that the table are R and S all the time. They can be other two tables. Number of tables in the input are exactly 2.


