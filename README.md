
<img width="1161" height="536" alt="image" src="https://github.com/user-attachments/assets/e548ee3d-7aa4-42f7-87e9-671ab282c58c" />

## Rectangle Drawing Configuration Menu

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

## Number Printing Configuration Menu

This menu allows users to customize the format and field widths for printing numeric output.

<img width="781" height="239" alt="image" src="https://github.com/user-attachments/assets/40513098-8e1b-4d36-bd22-af4a17803df2" />

## Case 2: Configure Print Number Options

- The user is shown Menu 2 and prompted to select an option from `0 – 5`.
- To prevent invalid inputs from defaulting to `0` and exiting the menu, the program initializes the option variable to `6` to keep the loop running until a valid input is provided.
- Input validation is done using a helper function to ensure all values are within the allowed range.

#### Sub-options:
- **Case 1**: Configure field 1 width (range: 8 to 30)
- **Case 2**: Configure field 2 width (range: 8 to 30)
- **Case 3**: Configure field 3 width (range: 24 to 60) — for scientific notation formatting
- **Case 4**: Configure field 4 width (range: 8 to 30)
- **Case 5**: Set floating point precision — relevant to main menu Case 4

If an invalid input is entered, the user is prompted to enter a valid value.

- **Input `0`**: Returns to the main menu

## Rectangle Drawing and Calculation

### Case 3: Input Rectangle Dimensions and Draw

This case allows the user to input custom dimensions for a rectangle, validate them, perform calculations (area, perimeter, center), and print the rectangle.

<img width="694" height="379" alt="image" src="https://github.com/user-attachments/assets/e5e60f90-1a5e-41f6-894f-1cbc11ba3399" />


#### Step-by-Step Logic

1. **User Input**
   - Prompt for **length** (valid range: 3 to 100).
   - Prompt for **breadth** (valid range: 3 to 20).
   - Validation includes:
     - Ensuring the input is numeric.
     - Ensuring it's a **whole number** (no decimals).
     - Ensuring the number is within the allowed range.

2. **Validation Flow**
   - If input is non-numeric → prompt again.
   - If input is a decimal → prompt for a whole number.
   - If out of range → inform user and re-prompt.

3. **Calculations**
   - Once valid, store the inputs as the rectangle’s **length** and **breadth**.
   - Calculate:
     - **Perimeter** = 2 × (length + breadth)
     - **Area** = length × breadth
     - **Center point(s)** = (length / 2, breadth / 2)
       - If dimensions are odd/even, center may result in 1, 2, or 4 center points.

4. **Drawing Logic**
   - The rectangle is drawn **row by row**, left to right.
   - At each position:
     - If it's a **perimeter**, print the perimeter character.
     - If it's a **center** and `markRectCenter = true`, print the center character(s).
     - If it's a **corner** and `markRectCorner = true`, print the corner character(s).
     - Else, print a space `' '`.

5. **Special Drawing Conditions**
   - **Center**:
     - Depending on whether length and breadth are even/odd, the center is represented by 1, 2, or 4 characters.
   - **Corners**:
     - If enabled, four corner markers are printed at the rectangle’s corners.

6. **Looping**
   - The drawing process continues until all rows and columns are filled, completing the rectangle.

  
## Number Transformation and Formatting

### Case 4: Input Number and Display Formatted Outputs

This case allows the user to input a number, which the system then formats and displays in various mathematical and data type forms.

<img width="764" height="412" alt="image" src="https://github.com/user-attachments/assets/00dc6bdb-95de-42ad-a07f-574c8123ae11" />


#### Step-by-Step Logic

1. **User Input**
   - The system prompts the user to enter a number.
   - If the input is invalid (e.g., not numeric), it will prompt again until a valid number is entered.

2. **Return**
   - After displaying all formatted outputs, the system returns to the main menu automatically.

## Exit Program

### Case 5: Terminate the Application

- If the user inputs **5**, the system will safely terminate and close the program.
- If the user inputs any other number outside the expected range (0–5), the system will prompt them with a message to enter a number between **0 and 5**.
