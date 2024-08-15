def add(n1, n2):
    return n1 + n2


def subtract(n1, n2):
    return n1 - n2


def multiply(n1, n2):
    return n1 * n2


def divide(n1, n2):
    return n1 / n2

def list_operations():
    text = "Available operations: "
    for key in operations:
        text += key + " "
    print(text)


def get_input(is_symbol=False):
    if is_symbol:
        while True:
            sym = input("> ")
            if sym in operations:
                return sym
            else:
                print(f"{sym} is not a valid option.")
                list_operations()
                print("Please select one of the above.")
    while True:
        num_string = input("> ")
        if num_string == "":
            print("Please enter a value.")
        elif is_float(num_string):
            return float(num_string)
        else:
            print("Please enter a number.")


def is_float(string):
    try:
        float(string)
        return True
    except ValueError:
        return False


operations = {
    "+": add,
    "-": subtract,
    "*": multiply,
    "/": divide,
}

new_calculation = True
result = 0

while True:
    if new_calculation:
        print("""
 _____________________
|  _________________  |
| |                 | |  .----------------.  .----------------.  .----------------.  .----------------. 
| |_________________| | | .--------------. || .--------------. || .--------------. || .--------------. |
|  ___ ___ ___   ___  | | |     ______   | || |      __      | || |   _____      | || |     ______   | |
| | 7 | 8 | 9 | | + | | | |   .' ___  |  | || |     /  \     | || |  |_   _|     | || |   .' ___  |  | |
| |___|___|___| |___| | | |  / .'   \_|  | || |    / /\ \    | || |    | |       | || |  / .'   \_|  | |
| | 4 | 5 | 6 | | - | | | |  | |         | || |   / ____ \   | || |    | |   _   | || |  | |         | |
| |___|___|___| |___| | | |  \ `.___.'\  | || | _/ /    \ \_ | || |   _| |__/ |  | || |  \ `.___.'\  | |
| | 1 | 2 | 3 | | x | | | |   `._____.'  | || ||____|  |____|| || |  |________|  | || |   `._____.'  | |
| |___|___|___| |___| | | |              | || |              | || |              | || |              | |
| | . | 0 | = | | / | | | '--------------' || '--------------' || '--------------' || '--------------' |
| |___|___|___| |___| |  '----------------'  '----------------'  '----------------'  '----------------' 
|_____________________|
""")
        
        print("What's the first number?")
        num1 = get_input()
    else:
        num1 = result

    list_operations()

    print("Pick an operation from the above line:")
    symbol = get_input(is_symbol=True)

    print("What's the next number?")
    while True:
        num2 = get_input()
        if symbol == "/" and num2 == 0:
            print("You have chosen to divide by zero. Please input a non-zero number.")
        else:
            break

    result = operations[symbol](num1, num2)
    print(f"{num1} {symbol} {num2} = {result}")

    print(f"Type \"y\" to continue calculating with {result}, or type \"n\" to start a new calculation. "
          f"Anything else will exit the program.")
    choice = input("> ")
    if choice == "y":
        new_calculation = False
    elif choice == "n":
        new_calculation = True
    else:
        break

print("Goodbye.")
