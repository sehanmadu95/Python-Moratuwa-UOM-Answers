# Python-Moratuwa-UOM-Answers
Assigmnt 1 Calculator answers


# TODO: Write the functions for arithmatic operations here
# These functions should cover Task 2
import math


def add(a, b):
    return str(a) + " + " + str(b) + " = " + str(a + b)


def subtract(a, b):
    return str(a) + " - " + str(b) + " = " + str(a - b)


def multiply(a, b):
    return str(a) + " * " + str(b) + " = " + str(a * b)


def divide(a, b):
    return str(a) + " / " + str(b) + " = " + str(a / b)


def power(a, b):
    return str(a) + " ^ " + str(b) + " = " + str(math.pow(a, b))


def reminder(a, b):
    return str(a) + " % " + str(b) + " = " + str(a % b)


# -------------------------------------

# TODO: Write the select_op(choice) function here
# This function sould cover Task 1 (Section 2) and Task 3

def select_op(choice):
    if choice == "#":
        return -1
    else:
        a = input("Enter first number: ")
        print(a)
        if len(a) == 2:
            return True
        elif a=="#":
            return -1

        b = input("Enter second number: ")
        print(b)
        if len(b) == 2:
            return True
        elif b=="#":
            return -1


        a=float(a)
        b=float(b)
        if choice not in ["+", "-", "*", "/", "^", "%", "#", "$"]:
            print("Unrecognized operation")

        if choice == "+":
            print(add(a, b))

        if choice == "-":
            print(subtract(a, b))

        if choice == "*":
            print(multiply(a, b))

        if choice == "/":

            if b == 0:
                print("float division by zero")
                print(str(a) + " / 0.0 = None")
            else:
                print(divide(a, b))

        if choice == "^":
            print(power(a, b))

        if choice == "%":
            print(reminder(a, b))


# End the select_op(choice) function here
# -------------------------------------
# This is the main loop. It covers Task 1 (Section 1)
# YOU DO NOT NEED TO CHANGE ANYTHING BELOW THIS LINE
while True:
    print("Select operation.")
    print("1.Add      : + ")
    print("2.Subtract : - ")
    print("3.Multiply : * ")
    print("4.Divide   : / ")
    print("5.Power    : ^ ")
    print("6.Remainder: % ")
    print("7.Terminate: # ")
    print("8.Reset    : $ ")

    # take input from the user
    choice = input("Enter choice(+,-,*,/,^,%,#,$): ")
    print(choice)
    if select_op(choice) == -1:
        # program ends here
        print("Done. Terminating")
        exit()
