# Truck Routing Program

## Overview
This Truck Routing Program, coded in Python, utilizes the Greedy Algorithm to streamline delivery routes efficiently, beginning at a central hub and systematically selecting the nearest delivery point. It effectively manages 40 items, employing a hash table with chaining to resolve collisions, ensuring swift data retrieval with an O(1) average time complexity. The program is designed to maintain cumulative truck mileage under 140 miles and adhere to strict package delivery deadlines. The user-friendly interface logs each truck’s departure and return times, tracks total miles traveled, and offers real-time package updates.

## Features
- **Nearest Neighbor Algorithm Implementation**: Efficiently plans delivery routes by analyzing distances for each package and choosing the next closest address
- **Chaining Hash Table**: Utilizes a hash table with chaining to handle collisions, ensuring efficient and rapid access to package data. This method effectively manages collisions and maintains quick data retrieval despite increasing amounts of data.
- **Command Line Interface**: Provides a robust interface that allows users to interact with the program in real time. This interface displays critical data such as truck departure and return times, total miles traveled, and detailed updates on package status, including delivery deadlines and location changes. The interface also supports time-specific package tracking, enabling detailed queries at any given moment

## What I Learned
- **Advanced Python Proficiency**: Gained deeper knowledge of Python, focusing on how to implement and optimize data structures and algorithms in a real-world application. Enhanced understanding of hashing mechanisms and efficient data management.
- **Problem-Solving Capabilities**: Developed critical thinking and problem-solving skills by designing algorithms to handle complex logistics scenarios. Learned to troubleshoot and refine algorithms based on real-time data and constraints.
- **Algorithm Optimization**: Mastered the use of the Greedy Algorithm for route optimization, understanding its application in logistics to minimize travel distance and time.
- **System Design**: Enhanced skills in building user-friendly command-line interfaces that provide essential information dynamically and allow user interaction for real-time updates.
- **Performance Optimization**: Learned to analyze and improve the space and time complexities of a program, ensuring it runs efficiently under varying loads and maintains performance stability.


## Ways to Improve
- **Implement Advanced Optimization Algorithms**: Explore the use of Ant Colony Optimization (ACO) and Branch and Bound methods. ACO could provide a more dynamic and adaptive routing strategy, potentially optimizing for quicker deliveries based on real-time conditions. The Branch and Bound method, while slower, could systematically eliminate less efficient routes, ensuring the most optimal route is chosen for package deliveries.
- **Queue-Based Loading System**: Revisit the package loading strategy to optimize delivery routes upfront by loading packages into a queue, rather than relying on the greedy algorithm during delivery. This approach more accurately reflects real-world logistics practices.
- **Binary Search Tree for Package Management**: Consider replacing the chaining hash table with a binary search tree (BST) to maintain packages sorted by ID for fast retrieval, updates, and deletion. While this might increase the average complexity to O(log n), it could enhance the manageability and scalability of package data.
- **Graphical User Interface (GUI) Enhancement**: Replacing the command-line interface with a GUI could improve usability by providing intuitive navigation, real-time visualizations, and accessible design for non-technical users.

## Example of Mile Tracking
| Truck Number | Departure Time | Return Time | Distance Traveled |
|--------------|----------------|-------------|-------------------|
| 1            | 8:00:00        | 9:53:00     | 34 miles          |
| 2            | 9:54:00        | 12:04:40    | 35.9 miles        |
| 3            | 9:05:00        | 10:17:20    | 21.7 miles        |
| 2            | 10:20:00       | 12:19:40    | 39.2 miles        |

> All packages delivered by 12:19:40

> The total distance of all trucks traveled is 130.8 miles

## Example of Package Tracking at a Specific Time
| Package ID | Address           | City           | ZIP   | Weight | Deadline | Status    | Delivery Time | Truck Number |
|------------|-------------------|----------------|-------|--------|----------|-----------|---------------|--------------|
| 1          | 195 W Oakland Ave | Salt Lake City | 84115 | 21kg   | 10:30 AM | Delivered | 8:40:40       | 1            |
| 2          | 2530 S 500 E      | Salt Lake City | 84106 | 44kg   | EOD      | Delivered | 10:03:20      | 2            |
| 3          | 233 Canyon Rd     | Salt Lake City | 84103 | 2kg    | EOD      | En Route  | None          | 2            |
| 4          | 380 W 2880 S      | Salt Lake City | 84115 | 4kg    | EOD      | En Route  | None          | 2            |
| 5          | 410 S State St    | Salt Lake City | 84111 | 5kg    | EOD      | Delivered | 10:24:00      | 2            |

> **Note:** The full table contains 40 rows of data.