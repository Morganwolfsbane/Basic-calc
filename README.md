# Basic-calc
PLP
def format_number(num):
    """Helper function to format numbers as integers if they're whole numbers"""
    return int(num) if num.is_integer() else num

# Get user input
num1 = float(input("Enter first number: "))
operation = input("Enter operation (+, -, *, /): ")
num2 = float(input("Enter second number: "))

result = None
valid_operation = True

# Perform calculation based on operation
if operation == '+':
    result = num1 + num2
elif operation == '-':
    result = num1 - num2
elif operation == '*':
    result = num1 * num2
elif operation == '/':
    if num2 == 0:
        print("Error: Division by zero is not allowed.")
        valid_operation = False
    else:
        result = num1 / num2
else:
    print("Error: Invalid operator.")
    valid_operation = False

# Display result if valid operation
if valid_operation and result is not None:
    # Format numbers for cleaner output
    num1_fmt = format_number(num1)
    num2_fmt = format_number(num2)
    result_fmt = format_number(result)
    
    print(f"{num1_fmt} {operation} {num2_fmt} = {result_fmt}")