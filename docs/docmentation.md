Sorting Algorithm Visualization - Documentation
Overview
This project is a Sorting Algorithm Visualizer built using Python and the Pygame library. The visualizer provides an interactive interface to demonstrate how different sorting algorithms work by animating the sorting process step by step.

Features
Sorting Algorithms Supported
Bubble Sort
Insertion Sort
Sorting Order Options
Ascending Order
Descending Order
Keyboard Controls
R - Reset the array
SPACE - Start sorting
A - Set sorting order to Ascending
D - Set sorting order to Descending
I - Switch to Insertion Sort
B - Switch to Bubble Sort

Getting Started
Prerequisites
Make sure you have Python installed on your system along with the Pygame library.
Installation Steps
Clone the repository or download the source code.
Install the required dependencies:
 pip install pygame


Run the main script to start the visualizer:
 python main.py



Keyboard Controls
The following keyboard controls are available:
Reset Array: Press R to reset the array to a new random sequence.
Start Sorting: Press SPACE to begin sorting.
Choose Sorting Order:
A: Sort in Ascending order.
D: Sort in Descending order.
Switch Sorting Algorithms:
I: Use Insertion Sort.
B: Use Bubble Sort.

Technologies Used
Programming Language: Python
Library: Pygame

How It Works
Animation
The application generates a random set of bars, where the height of each bar corresponds to the value of an element in the array. As the algorithm progresses, the bars are rearranged step-by-step to demonstrate the sorting process visually.
Sorting Algorithms
Bubble Sort: Compares adjacent elements and swaps them if they are in the wrong order. This process is repeated until the array is sorted.
Insertion Sort: Builds the sorted array one item at a time by repeatedly inserting elements into their correct positions.
Sorting Order
You can toggle between ascending and descending orders using the keyboard shortcuts (A and D).


Future Improvements
Add more sorting algorithms (e.g., Quick Sort, Merge Sort, etc.).
Implement additional customization options for bar colors and speed of sorting.
Add sound effects for each comparison and swap operation.

Contribution
Contributions are welcome! Feel free to open an issue or submit a pull request to improve the project.

License
This project is licensed under the MIT License. See the LICENSE file for details.

