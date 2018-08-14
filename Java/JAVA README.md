:::EXPLANATION:::

This is a simple filter program that will do AND searchs on the contents of the database.

The query is input on the command line when executing the program where the column and it's desired contents are given.

:::EXAMPLE SEARCHES:::

Use console to execute the java file after compiling it:

./BugSearch 1:Gatling 4:Logic 6:RA 7:L 8:F

./BugSearch 3:race 4:coordination

:::KEY FOR CLOUD BUG STUDY LABELS:::

Aspect:
Availability = A
Consistency = C
Performance = P
Reliability = R
Scalability = S
	
Software:
Load = A
Configuration = C
Error Handle = E
Hang = H
Logic = L
Optimization = O
Race = R
	
Implication:
Data Corrupt = C
Failed Operation = F
Data Loss = L
Performance = P
Data Stale = S
Component Down = T
