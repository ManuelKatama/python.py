Create a simple Python program that asks the user to input two numbers and a mathematical operation (addition, subtraction, multiplication, or division).
Perform the operation based on the user's input and print the result.
Example: If a user inputs 10, 5, and +, your program should display 10 + 5 = 15.

def calculate(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 == 0:
            return "Error: Division by zero is undefined."
        else:
            return num1 / num2
    else:
        return "Invalid operation."

def main():
    print("Welcome to the simple calculator!")
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ")
        result = calculate(num1, num2, operation)
        if isinstance(result, str):
            print(result)
        else:
            print(f"{num1} {operation} {num2} = {result}")
    except ValueError:
        print("Error: Please enter valid numbers.")

if __name__ == "__main__":
    main()


