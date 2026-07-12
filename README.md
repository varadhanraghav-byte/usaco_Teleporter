# Usaco_Teleporter
## Link: https://usaco.org/index.php?page=viewproblem2&cpid=807
## problem statement : 
One of the farming chores Farmer John dislikes the most is hauling around lots of cow manure. In order to streamline this process, he comes up with a brilliant invention: the manure teleporter! Instead of hauling manure between two points in a cart behind his tractor, he can use the manure teleporter to instantly transport manure from one location to another.
Farmer John's farm is built along a single long straight road, so any location on his farm can be described simply using its position along this road (effectively a point on the number line). A teleporter is described by two numbers x and y, where manure brought to location x can be instantly transported to location, or vice versa.

Farmer John wants to transport manure from location a to location b, and he has built a teleporter that might be helpful during this process (of course, he doesn't need to use the teleporter if it doesn't help). Please help him determine the minimum amount of total distance he needs to haul the manure using his tractor.

### INPUT FORMAT:
The first and only line of input contains four space-separated integers: a and b, describing the start and end locations, followed by x and y describing the teleporter. All positions are integers in the range 0…100 and they are not necessarily distinct from each-other.
### OUTPUT FORMAT:
Print a single integer giving the minimum distance Farmer John needs to haul manure in his tractor.
### SAMPLE INPUT:
3 10 8 2
### SAMPLE OUTPUT:
3

**Problem credits: Brian Dean**
## Algorithm:
Read four integers a, b, x, y from input.
case1 = |b - a| (direct route, no teleporter).
case2 = |a - x| + |b - y| (drive to x, teleport to y, drive to b).
case3 = |a - y| + |b - x| (drive to y, teleport to x, drive to b).
answer = minimum of case1, case2, case3.
Print answer.
## Explanation : 

Farmer John needs to move manure from location a to location b along a straight road.
He also has a teleporter connecting two points, x and y, which can move manure instantly between them in either direction.
He can choose to use the teleporter or not - whichever gives the shorter total tractor distance.
Using the tractor to travel between any two points costs distance equal to the absolute difference between their positions.
Teleporting itself costs zero distance, since it is instant.
The goal is to find the minimum total tractor distance needed to get the manure from a to b, considering both the option of not using the teleporter and the option of using it (in either direction).
The input gives four integers: a, b, x, y, all between 0 and 100.
The output should be a single integer: the minimum possible tractor distance.
