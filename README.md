
# CLASS SCHEDULE OPTIMIZATION USING ALGORITHMIC PATHFINDING
 This, being my first research project, represents my foray into the world of solving real-world problems.
  I hold it close to my heart for its sentimental value and to remind myself that it's not essential
  to make it perfect for it to be worthwhile.

---

Conestoga High School, as of 2018, had over 2,000 students across a 320,000+ squarefoot floorplan. At that 
the hallway was should-to-should packed walking in between classes throughout the 8-period school day. Student's
with rooms assigned across the school one after another were often late for the next period. To alleviate
the hallway traffic without changing the layout of the building, my capstone project aimed to minimize the 
distance students would travel between classes throughout the day.

To do this, the school floor plan had to be transcribed into a machine readable 2-dimensional array with 
unique identifiers for rooms, hallways, walls, and stairwells. This array could be used to calculate the
distance between two rooms by summing the "cost" of traversing each tile and minimizing it using the A*
pathfinding algorithm.

![2nd floor encoding](https://github.com/hayitsian/Highschool-Capstone-Project/blob/main/2nd%20floor%20encoding.png)

The next problem, however, is impossible to solve. Minimizing the distance of traversing to any `n` points
while beginning and ending at the same point is known as the travelling salesman problem. This mathematical
 problem is known as NP-complete complexity, meaning no algorithm is capable of always outputing the
 most optimal pathway in a reasonable amount of time, even with an infinite memory stack. As such, heuristic 
 algorithms are employed to reduce the solution space. One easy to implement algorithm is the nearest neighbor,
 which selects the next class by picking the room closest to the current class.

 ![bar chart](https://github.com/hayitsian/Highschool-Capstone-Project/blob/main/bar%20chart%20before%20after.png)
 When using a random sampling of 20 students stratified across the four grade levels, the algorithm reduced 
 the total distance traveled for each student by 45%.
 
 Future considerations to advancing this project include implementing a conflict matrix for when rooms 
 and/or faculty are available to teach a particular class, improving the code through good object-oriented
 programming techniques, and developing an easier-to-use application.
