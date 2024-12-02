# basic_calculator.py


# Basic Calculator Program
# Author: Allan Davis
# Description: A simple calculator to perform addition, subtraction, multiplication, and division.

def basic_calculator():
    print("Welcome to the Basic Calculator!")  # Introduction message
    
    while True:  # Loop to allow multiple calculations
        try:
            # Get user inputs
            num1 = float(input("Enter the first number: "))  # First number
            num2 = float(input("Enter the second number: "))  # Second number
            operation = input("Enter the operation (+, -, *, /): ").strip()  # Operation
            
            # Perform the calculation
            if operation == '+':
                result = num1 + num2
                print(f"{num1} + {num2} = {result}")
            elif operation == '-':
                result = num1 - num2
                print(f"{num1} - {num2} = {result}")
            elif operation == '*':
                result = num1 * num2
                print(f"{num1} * {num2} = {result}")
            elif operation == '/':
                if num2 != 0:
                    result = num1 / num2
                    print(f"{num1} / {num2} = {result}")
                else:
                    print("Error: Division by zero is not allowed.")
            else:
                print("Invalid operation. Please choose from +, -, *, or /.")
            
            # Ask if the user wants to perform another calculation
            choice = input("Do you want to perform another calculation? (yes/no): ").strip().lower()
            if choice != 'yes':
                print("Thank you for using the Basic Calculator. Goodbye!")
                break
        
        except ValueError:
            print("Invalid input. Please enter valid numbers.")

# Run the calculator function when the script is executed
if __name__ == "__main__":
    basic_calculator()
