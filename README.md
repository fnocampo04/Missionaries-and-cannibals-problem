# Missionaries and cannibals problem
1.0 Initial problem

Use the backtracking method algorithm to implement a Python program that solves the missionaries and cannibals problem under the following rules:
- m missionaries and c cannibals (m >= c) must cross a river using a canoe with a capacity of at most p(m > c) passengers.
- Missionaries at no time may be accompanied by a larger number of cannibals.
- The program should describe how all the missionaries and cannibals used the canoe to cross from one bank of the river to the other.

1.1 Formalization of the problem

States: (M,C,B) with 0 <= M, C, B, where M,C and B represent the number of missionaries, cannibals and boat position respectively.

Initial state: (M, C, 1) → M, C are entered by the user.

Target state: (0,0,0)

Possible moves: Set as an integer P(boat capacity), all possible combinations to {0,1,2,...,P}, then add 1 since we assume the boat is on the left.

Next move: It is determined from the position of the boat, if it is 1(Left) the move to be tested is subtracted from the current state; otherwise it is added.

Valid status: A move is valid if it meets the requirements, for example 0 < M, C, M > C, among others.

Visited state: The visited valid movement is stored to avoid loops.

Solve function: Prune invalid states or no possible moves and add a solution in case of reaching the goal state.
