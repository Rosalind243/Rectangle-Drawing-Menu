## Rectangle Drawing Configuration Menu

<img width="1161" height="536" alt="image" src="https://github.com/user-attachments/assets/e548ee3d-7aa4-42f7-87e9-671ab282c58c" />

This menu allows users to configure how rectangles are drawn in the console. It is accessible from **Case 1** of the main menu.

<img width="801" height="273" alt="image" src="https://github.com/user-attachments/assets/f2ceb323-4d93-4f96-ac97-ea48db934fd4" />

### Case 1: Configure Draw Rectangle Options

- The system displays the draw rectangle options menu and prompts the user to input a number between `0 – 5`.
- If the user enters an invalid input (outside the range), they will be notified and prompted again.
- To avoid invalid input defaulting the menu selection to `0` and kicking the user out, the program uses a fallback value (e.g., `int = 6`) to keep the menu loop running smoothly.
- Selecting this option toggles `markRectCenter` **on or off**, depending on its current state.

### Case 2: Toggle Corner Marking

- Functions the same as Case 1, but toggles `markRectCorner` instead of the center.

### Case 3, 4, 5: Change Drawing Characters

- The system prompts the user to input a **new character** for:
  - **Case 3**: Rectangle center
  - **Case 4**: Rectangle corner
  - **Case 5**: Rectangle perimeter
- If the input is not within the `0 – 5` range, the system informs the user and requests a valid input.

### Input `0`: Return to Main Menu

- If the user enters `0` at any point in this configuration menu, the system will return to the main menu.
