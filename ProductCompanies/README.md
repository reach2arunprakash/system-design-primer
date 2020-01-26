
* [Arrays and Strings](#Arrays-and-Strings)
* [Linked Lists](#Linked-Lists)
* [Stacks and Queues](#Stacks-and-Queues)
* [Trees and Graph](#Trees-and-Graph)
* [Bit Manipulation](#Bit-Manipulation)
* [Math and Logic Puzzles](#Math-and-Logic-Puzzles)
* [Recursion and Dynamic Programming](#Recursion-and-Dynamic-Programming)
* [System Design and Scalability](#System-Design-and-Scalability)
* [Testing](#Testing)
* [C and C++](#C-and-C++)



# Arrays and Strings

1.  **Is Unique**: Implement an algorithm to determine if a string has all unique characters. What if you cannot use additional data structures?
2.  **Check Permutation**: Given two strings, write a method to decide if one is a permutation of the other.
3.  **URLify**: Write a method to replace all spaces in a string with '%20'. You may assume that the string has sufficient space at the end to hold the additional characters, and that you are given the "true" length of the string.
4.  **Palindrome Permutation**: Given a string, write a function to check if it is a permutation of a palindrome. A palindrome is a word or phrase that is the same forwards and backwards. A permutation is a rearrangement of letters. The palindrome does not need to be limited to just dictionary words.
5.  **One Away**: There are three types of edits that can be performed on strings: insert a character, remove a character, or replace a character. Given two strings, write a function to check if they are one edit (or zero edits) away.
6.  **String Compression**: Implement a method to perform basic string compression using the counts of repeated characters. For example, the string aabcccccaaa would become a2b1c5a3. If the "compressed" string would not become smaller than the original string, your method should return the original string. You can assume the string has only uppercase and lowercase letters (a - z).
7.  **Rotate Matrix**: Given an image represented by an NxN matrix, where each pixel in the image is 4 bytes, write a method to rotate the image by 90 degrees. can you do this in place?
8.  **Zero Matrix**: Write an algorithm such that if an element in an MxN matrix is 0, its entire row and column are set to 0.
9.  **String Rotation**: Assume you have a method isSubstring which checks if one word is a substring of another. Given two strings, S1 and S2, write code to check if S2 is a rotation of S1 using only one call to isSubstring (e.g., "waterbottle" is a rotation of "erbottlewat").


# Linked Lists

1.  **Remove Dups**: Write code to remove duplicates from an unsorted linked list.
    How would you solve this problem if a temporary buffer is not allowed?
2.  **Return Kth to Last**: Implement an algorithm to find the kth to last element of a singly linked list.
3.  **Delete Middle Node**: Implement an algorithm to delete a node in the middle (i.e., any node but the first and last node, not necessarily the exact middle) of a singly linked list, given only access to that node.
4.  **Partition**: Write code to partition a linked list around a value x, such that all nodes less than x come before all nodes greater than or equal to x. lf x is contained within the list, the values of x only need to be after the elements less than x (see below). The partition element x can appear anywhere in the "right partition"; it does not need to appear between the left and right partitions.
5.  **Sum Lists**: You have two numbers represented by a linked list, where each node contains a single digit. The digits are stored in reverse order, such that the 1 's digit is at the head of the list. Write a function that adds the two numbers and returns the sum as a linked list.
6.  **Palindrome**: Implement a function to check if a linked list is a palindrome.
7.  **Intersection**: Given two (singly) linked lists, determine if the two lists intersect. Return the intersecting node. Note that the intersection is defined based on reference, not value. That is, if the kth node of the first linked list is the exact same node (by reference) as the jth node of the second linked list, then they are intersecting.
8.  **Loop Detection**: Given a circular linked list, implement an algorithm that returns the node at the beginning of the loop. DEFINITION Circular linked list: A (corrupt) linked list in which a node's next pointer points to an earlier node, so as to make a loop in the linked list.

# Stacks and Queues

1.  **Three in One**: Describe how you could use a single array to implement three stacks.
2.  **Stack Min**: How would you design a stack which, in addition to push and pop, has a function min which returns the minimum element? Push, pop and min should all operate in O(1) time.
3.  **Stack of Plates**: Imagine a (literal) stack of plates. If the stack gets too high, it might topple. Therefore, in real life, we would likely start a new stack when the previous stack exceeds some threshold. Implement a data structure SetOfStacks that mimics this. SetOfStacks should be composed of several stacks and should create a new stack once the previous one exceeds capacity. SetOfStacks.push() and SetOfStacks.pop() should behave identically to a single stack (that is, pop ( ) should return the same values as it would if there were just a single stack).
4.  **Queue via Stacks**: Implement a MyQueue class which implements a queue using two stacks.
5.  **Sort Stack**: Write a program to sort a stack such that the smallest items are on the top. You can use an additional temporary stack, but you may not copy the elements into any other data structure (such as an array). The stack supports the following operations: push, pop, peek, and isEmpty.
6.  **Animal Shelter**: An animal shelter, which holds only dogs and cats, operates on a strictly"first in, first out" basis. People must adopt either the "oldest" (based on arrival time) of all animals at the shelter, or they can select whether they would prefer a dog or a cat (and will receive the oldest animal of that type). They cannot select which specific animal they would like. Create the data structures to maintain this system and implement operations such as enqueue, dequeueAny, dequeueDog, and dequeueCat. You may use the built-in Linked List data structure.

# Trees and Graph

1.  **Route Between Nodes**: Given a directed graph, design an algorithm to find out whether there is a route between two nodes.
2.  **Minimal Tree**: Given a sorted (increasing order) array with unique integer elements, write an algorithm to create a binary search tree with minimal height.
3.  **List of Depths**: Given a binary tree, design an algorithm which creates a linked list of all the nodes at each depth (e.g., if you have a tree with depth 0, you'll have 0 linked lists).
4.  **Check Balanced**: Implement a function to check if a binary tree is balanced. For the purposes of this question, a balanced tree is defined to be a tree such that the heights of the two subtrees of any node never differ by more than one.
5.  **Validate BST**: Implement a function to check if a binary tree is a binary search tree.
6.  **Successor**: Write an algorithm to find the "next" node (i .e., in-order successor) of a given node in a binary search tree. You may assume that each node has a link to its parent.
7.  **Build Order**: You are given a list of projects and a list of dependencies (which is a list of pairs of projects, where the second project is dependent on the first project). All of a project's dependencies must be built before the project is. Find a build order that will allow the projects to be built. If there is no valid build order, return an error.
    EXAMPLE
    Input:
    projects: a, b, c, d, e, f
    dependencies: (a, d), (f, b), (b, d), (f, a), (d, c)
    Output: f, e, a, b, d, c
8.  **First Common Ancestor**: Design an algorithm and write code to find the first common ancestor of two nodes in a binary tree. Avoid storing additional nodes in a data structure. NOTE: This is not necessarily a binary search tree.
9.  **BST Sequences**: A binary search tree was created by traversing through an array from left to right and inserting each element. Given a binary search tree with distinct elements, print all possible arrays that could have led to this tree.
10.  **Check Subtree**: T1 and T2 are two very large binary trees, with T1 much bigger than T2. Create an algorithm to determine if T2 is a subtree of T1. A tree T2 is a subtree of T1 if there exists a node n in T1 such that the subtree of n is identical to T2. That is, if you cut off the tree at node n, the two trees would be identical.
11.  **Random Node**: You are implementing a binary tree class from scratch which, in addition to insert, find, and delete, has a method getRandomNode() which returns a random node from the tree. All nodes should be equally likely to be chosen. Design and implement an algorithm for getRandomNode, and explain how you would implement the rest of the methods.
12.  **Paths with Sum**: You are given a binary tree in which each node contains an integer value (which might be positive or negative). Design an algorithm to count the number of paths that sum to a given value. The path does not need to start or end at the root or a leaf, but it must go downwards (traveling only from parent nodes to child nodes).

# Bit Manipulation
1.  **Insertion**: You are given two 32-bit numbers, N and M, and two bit positions, i and j. Write a method to insert M into N such that M starts at bit j and ends at bit i. You can assume that the bits j through i have enough space to fit all of M. That is, if M = 10011, you can assume that there are at least 5 bits between j and i. You would not, for example, have j = 3 and i = 2, because M could not fully fit between bit 3 and bit 2.
    EXAMPLE
    Input: N = 10000000000, M = 10011, i = 2, j = 6
    Output: N 10001001100
2.  **Binary to String**: Given a real number between 0 and 1 (e.g., 0.72) that is passed in as a double, print the binary representation. If the number cannot be represented accurately in binary with at most 32 characters, print "ERROR:"
3.  **Flip Bit to Win**: You have an integer and you can flip exactly one bit from a 13 to a 1. Write code to find the length of the longest sequence of ls you could create.
    EXAMPLE
    Input: 1775  ( or: 1113111131111 )
    Output: 8
4.  **Next Number**: Given a positive integer, print the next smallest and the next largest number that have the same number of 1 bits in their binary representation.
5.  **Debugger**: Explain what the following code does: ( (n & (n -1) ) e) .
6.  **Conversion**: Write a function to determine the number of bits you would need to flip to convert integer A to integer B.
    EXAMPLE
    Input: 29 ( or: 111101 ), 15 ( or: 01111)
    Output: 2
7.  **Pairwise Swap**: Write a program to swap odd and even bits in an integer with as few instructions as possible (e.g., bit 0 and bit 1 are swapped, bit 2 and bit 3 are swapped, and so on).
8.  **Draw Line**: A monochrome screen is stored as a single array of bytes, allowing eight consecutive pixels to be stored in one byte. The screen has width w, where w is divisible by 8 (that is, no byte will be split across rows). The height of the screen, of course, can be derived from the length of the array and the width. Implement a function that draws a horizontal line from (x1, y) to (x2, y) . 
    The method signature should look something like:
    drawLine( byte[] screen, int width, int x1, int x2, int y )
    
# Math and Logic Puzzles

1.  **The Heavy Pill**: You have 20 bottles of pills. 19 bottles have 1.0 gram pills, but one has pills of weight 1.1 grams. Given a scale that provides an exact measurement, how would you find the heavy bottle? You can only use the scale once.
2.  **Basketball**: You have a basketball hoop and someone says that you can play one of two games.
    Game 1: You get one shot to make the hoop.
    Game 2: You get three shots and you have to make two of three shots.
    If p is the probability of making a particular shot, for which values of p should you pick one game or the other?
3.  **Dominos**: There is an 8x8 chessboard in which two diagonally opposite corners have been cut off. You are given 31 dominos, and a single domino can cover exactly two squares. Can you use the 31 dominos to cover the entire board? Prove your answer (by providing an example or showing why it's impossible).
4.  **Ants on a Triangle**: There are three ants on different vertices of a triangle. What is the probability of collision (between any two or all of them) if they start walking on the sides of the triangle? Assume that each ant randomly picks a direction, with either direction being equally likely to be chosen, and that they walk at the same speed.
    Similarly, find the probability of collision with n ants on an n-vertex polygon.
5.  **Jugs of Water**: You have a five-quart jug, a three-quart jug, and an unlimited supply of water (but no measuring cups). How would you come up with exactly four quarts of water? Note that the jugs are oddly shaped, such that filling up exactly "half" of the jug would be impossible.
6.  **Blue-Eyed Island**: A bunch of people are living on an island, when a visitor comes with a strange order: all blue-eyed people must leave the island as soon as possible. There will be a flight out at 8:00 pm every evening. Each person can see everyone else's eye color, but they do not know their own (nor is anyone allowed to tell them). Additionally, they do not know how many people have blue eyes, although they do know that at least one person does. How many days will it take the blue-eyed people to leave?
7.  **The Apocalypse**: In the new post-apocalyptic world, the world queen is desperately concerned about the birth rate. Therefore, she decrees that all families should ensure that they have one girl or else they face massive fines. If all families abide by this policy-that is, they have continue to have children until they have one girl, at which point they immediately stop-what will the gender ratio of the new generation be? (Assume that the odds of someone having a boy or a girl on any given pregnancy is equal.) Solve this out logically and then write a computer simulation of it.
8.  **The Egg Drop Problem**: There is a building of 100 floors. If an egg drops from the Nth floor or above, it will break. If it's dropped from any floor below, it will not break. You're given two eggs. Find N, while minimizing the number of drops for the worst case.
9.  **100 Lockers**: There are 100 closed lockers in a hallway. A man begins by opening all 100 lockers. Next, he closes every second locker. Then, on his third pass, he toggles every third locker (closes it if it is open or opens it if it is closed). This process continues for 100 passes, such that on each pass i, the man toggles every ith locker. After his 100th pass in the hallway, in which he toggles only locker #100, how many lockers are open?
10.  **Poison**: You have 1000 bottles of soda, and exactly one is poisoned. You have 10 test strips which can be used to detect poison. A single drop of poison will turn the test strip positive permanently. You can put any number of drops on a test strip at once and you can reuse a test strip as many times as you'd like (as long as the results are negative). However, you can only run tests once per day and it takes seven days to return a result. How would you figure out the poisoned bottle in as few days as possible?
    FOLLOW UP
Write code to simulate your approach.

# Recursion and Dynamic Programming

1. **Triple Step**: A child is running up a staircase with n steps and can hop either 1 step, 2 steps, or 3 steps at a time. Implement a method to count how many possible ways the child can run up the stairs.
2. **Robot in a Grid**: Imagine a robot sitting on the upper left corner of grid with r rows and c columns. The robot can only move in two directions, right and down, but certain cells are "off limits" such that the robot cannot step on them. Design an algorithm to find a path for the robot from the top left to the bottom right.
3. **Magic Index**: A magic index in an array A [ 0 ... n -1 ] is defined to be an index such that A[ i ] = i. Given a sorted array of distinct integers, write a method to find a magic index, if one exists, in array A.
    FOLLOW UP
    What if the values are not distinct?
4. **Power Set**: Write a method to return all subsets of a set.
5. **Recursive Multiply**: Write a recursive function to multiply two positive integers without using the * operator. You can use addition, subtraction, and bit shifting, but you should minimize the number of those operations.
6. **Towers of Hano**i: In the classic problem of the Towers of Hanoi, you have 3 towers and N disks of different sizes which can slide onto any tower. The puzzle starts with disks sorted in ascending order of size from top to bottom ( i.e., each disk sits on top of an even larger one). You have the following constraints:
    (1) Only one disk can be moved at a time.
    (2) A disk is slid off the top of one tower onto another tower.
    (3) A disk cannot be placed on top of a smaller disk.
    Write a program to move the disks from the first tower to the last using stacks.
7. **Permutations without Dups**: Write a method to compute all permutations of a string of unique characters.
8. **Permutations with Dups**: Write a method to compute all permutations of a string whose characters are not necessarily unique. The list of permutations should not have duplicates.
9. **Parens**: Implement an algorithm to print all valid (e.g., properly opened and closed) combinations of n pairs of parentheses.
    EXAMPLE
    Input: 3
    Output:( ( ( ) ) ), ( ( ) ( ) ),( ( ) ) ( ), ( ) ( ( ) ), ( ) ( ) ( )
10. **Paint Fill**: Implement the "paint fill" function that one might see on many image editing programs. That is, given a screen (represented by a two-dimensional array of colors), a point, and a new color, fill in the surrounding area until the color changes from the original color.
11. **Coins**: Given an infinite number of quarters (25 cents), dimes (10 cents), nickels (5 cents), and pennies (1 cent), write code to calculate the number of ways of representing n cents.
12. **Eight Queens:** Write an algorithm to print all ways of arranging eight queens on an 8x8 chess board so that none of them share the same row, column, or diagonal. In this case, "diagonal" means all diagonals, not just the two that bisect the board.
13. **Stack of Boxes:** You have a stack of n boxes, with widths Wi heights hi and depths di. The boxes cannot be rotated and can only be stacked on top of one another if each box in the stack is strictly larger than the box above it in width, height, and depth. Implement a method to compute the height of the tallest possible stack. The height of a stack is the sum of the heights of each box.
14. **Boolean Evaluation:** Given a boolean expression consisting of the symbols 0 (false), 1 (true), & (AND), | (OR), and ^ (XOR), and a desired boolean result value result, implement a function to count the number of ways of parenthesizing the expression such that it evaluates to result.
    EXAMPLE
    countEval( "1^0|0|1", false )  -> 2
    countEval( "0 & 0 & 0 & 1^1|0", true ) -> 10

# System Design and Scalability

1. **Stock Data**: Imagine you are building some sort of service that will be called by up to 1,000 client applications to get simple end-of-day stock price information (open, close, high, low). You may assume that you already have the data, and you can store it in any format you wish. How would you design the client-facing service that provides the information to client applications? You are responsible for the development, rollout, and ongoing monitoring and maintenance of the feed. Describe the different methods you considered and why you would recommend your approach. Your service can use any technologies you wish, and can distribute the information to the client applications in any mechanism you choose.
2. **Social Network**: How would you design the data structures for a very large social network like Facebook or Linkedln ? Describe how you would design an algorithm to show the shortest path between two people (e.g., Me -> Bob -> Susan -> Jason -> You).
3. **Web Crawler:** If you were designing a web crawler, how would you avoid getting into infinite loops?
4. **Duplicate URLs:** You have 10 billion URLs. How do you detect the duplicate documents? In this case, assume "duplicate" means that the URLs are identical.
5. **Cache**: Imagine a web server for a simplified search engine. This system has 100 machines to respond to search queries, which may then call out using processSearch(string query) to another cluster of machines to actually get the result. The machine which responds to a given query is chosen at random, so you cannot guarantee that the same machine will always respond to the same request. The method processSearch is very expensive. Design a caching mechanism for the most recent queries. Be sure to explain how you would update the cache when data changes.
6. **Sales Rank:** A large eCommerce company wishes to list the best-selling products, overall and by category. For example, one product might be the #1 056th best-selling product overall but the #13th best-selling product under "Sports Equipment" and the #24th best-selling product under "Safety." Describe how you would design this system.
7. **Personal Financial Manager**: Explain how you would design a personal financial manager (like Mint.com). This system would connect to your bank accounts, analyze your spending habits, and make recommendations.
8. **Pastebin**: Design a system like Pastebin, where a user can enter a piece of text and get a randomly generated URL to access it.

# Testing

1. **Mistake:** Find the mistake(s) in the following code:
```c++
    unsigned int i;
    for (i = 100; i >= 0; --i)
       printf("%d\n", i);
```
2. **Random Crashes:** You are given the source to an application which crashes when it is run. After running it ten times in a debugger, you find it never crashes in the same place. The application is single threaded, and uses only the C standard library. What programming errors could be causing this crash? How would you test each one?
3. **Chess Test:** We have the following method used in a chess game: boolean canMoveTo( int x, int y) . This method is part of the P ieee class and returns whether or not the piece can move to position (x, y). Explain how you would test this method.
4. **No Test Tools:** How would you load test a webpage without using any test tools?
5. **Test an ATM:** How would you test an ATM in a distributed banking system?

# C and C++

1.  **Last K Lines**: Write a method to print the last K lines of an input file using C++.
2.  **Reverse String**: Implement a function void reverse( char* str) in C or C++ which reverses a null-terminated string.
3.  **Hash Table vs. STL Map**: Compare and contrast a hash table and an STL map. How is a hash table implemented? If the number of inputs is small, which data structure options can be used instead of a hash table?
4.  **Virtual Functions**: How do virtual functions work in (++?
5.  **Shallow vs. Deep Copy**: What is the difference between deep copy and shallow copy? Explain how you would use each.
6.  **Volatile**: What is the significance of the keyword "volatile" in C?
7.  **Virtual Base Class**: Why does a destructor in base class need to be declared virtual?
8.  **Copy Node**: Write a method that takes a pointer to a Node structure as a parameter and returns a complete copy of the passed in data structure. The Node data structure contains two pointers to other Nodes.
9.  **Smart Pointe**r: Write a smart pointer class. A smart pointer is a data type, usually implemented with templates, that simulates a pointer while also providing automatic garbage collection. It automatically counts the number of references to a SmartPointer<T* > object and frees the object of type T when the reference count hits zero.
10.  **Malloc**: Write an aligned malloc and free function that supports allocating memory such that the memory address returned is divisible by a specific power of two. EXAMPLE align_malloc (1000 ,128) will return a memory address that is a multiple of 128 and that points to memory of size 1000 bytes. aligned_free () will free memory allocated by align_malloc.
11.  **2D Alloc**: Write a function in C called my2DAlloe which allocates a two-dimensional array. Minimize the number of calls to malloc and make sure that the memory is accessible by the notation arr[i][j].
