🖥️ MARIE Odd-Sum to Hexadecimal Converter
A MARIE (Machine Architecture that is Really Intuitive and Easy) assembly program that reads a sequence of integers, accumulates the sum of odd numbers, and outputs the result in hexadecimal format.

📋 Description
This program demonstrates low-level assembly concepts using the MARIE architecture, including:

Sequential input handling via a loop
Conditional branching (odd/even detection)
Accumulation / summation
Decimal-to-hexadecimal conversion through repeated subtraction


⚙️ How It Works
1. Input Loop
The program reads 8 numbers from input one at a time, controlled by a counter variable initialized to 8.
2. Odd Number Check
Each number is tested:

If num == 0 → treated as even-adjacent, passed to a secondary check
If num - 1 == 0 (i.e., num == 1) → considered odd, added to sum
Otherwise → jumps to false (error output)


⚠️ Note: The current odd-check logic only fully handles 0 and 1. A complete odd/even check using modulo 2 is not yet implemented.

3. Sum Accumulation
When a valid odd number is found, it is added to the running sum. The counter is decremented, and the loop continues until all 8 inputs are processed.
4. Hexadecimal Conversion
After the loop, the sum is converted to a two-digit hexadecimal value:

Repeatedly subtracts 16 from sum, counting iterations in hex1
The remainder is stored in hex2
Outputs hex1 (the 16s place) followed by hex2 (the units place)

5. Error Handling
If an even number is encountered, the program outputs -1 and halts.

🗂️ Program Variables
VariableInitial ValuePurposecounter8Tracks remaining input countnum0Stores current input numbersum0Accumulates odd number sumhex10Hex output: 16s digithex20Hex output: units digitOne1Constant: 1Zero0Constant: 0Sixteen16Constant: 16 (for hex conv.)error-1Error output value

🚀 Usage

Open the program in a MARIE simulator (e.g., MARIE.js or the official MARIE simulator).
Load the .mas or .marie source file.
Run the program and enter 8 integer values when prompted.
The program will output:

The hexadecimal representation of the sum of odd inputs (two values: high digit, low digit)
Or -1 if an even number is encountered



