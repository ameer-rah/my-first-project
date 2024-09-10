# simple_calculator.py

    def add(x, y):
    """Return the sum of x and y."""
    return x + y

    def subtract(x, y):
    """Return the difference between x and y."""
    return x - y

    def multiply(x, y):
    """Return the product of x and y."""
    return x * y

    def divide(x, y):
    """Return the quotient of x and y. Handle division by zero."""
    if y != 0: 
        return x / y
    else:    
        return "Error: Division by zero is not allowed."

    def calculator():
    """Simple calculator function to perform basic arithmetic operations."""
    print("Select operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")

    while true:
        choice = input("Enter choice (1/2/3/4): ")

        if choice in ('1', '2', '3', '4'):
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
            except ValueError:
                print("Invalid input. Please enter numeric values.")
                continue

            if choice == '1':
                print(f"{num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"{num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"{num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                print(f"{num1} / {num2} = {divide(num1, num2)}")
        
        else:
            print("Invalid Input")

        next_calculation = input("Do you want to perform another calculation? (yes/no): ").lower()
        if next_calculation != 'yes':
            break 
        if __name__ == "__main__":calculator()
