# M8CODEA

# Mohammed Anas
# 2024-11-12
# Solving various boolean problems
# Module 8: Lab Activity - Booleans

# Problem 1: Equality Check
def check_equal():
    num1 = input("Enter first value: ")
    num2 = input("Enter second value: ")
    if num1 == num2:
        print("The values are equal.")
    else:
        print("The values are not equal.")

# Problem 2: Sum Comparison
def check_sum():
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))
    total = num1 + num2
    if total > 10:
        print("The sum is greater than 10.")
    elif total < 10:
        print("The sum is less than 10.")
    else:
        print("The sum is equal to 10.")

# Problem 3: Checking for the Number 5
def check_five_in_list():
    numbers = input("Enter numbers separated by spaces: ").split()
    if '5' in numbers:
        print("The number 5 is in the list.")
    else:
        print("The number 5 is not in the list.")

# Problem 4: Leap Year Check
def check_leap_year(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return True
    else:
        return False

# Problem 5: Character Class
class Character:
    def __init__(self, nickname, weapons, weaknesses):
        self.nickname = nickname
        self.weapons = weapons
        self.weaknesses = weaknesses

    def profile(self):
        weapons_str = ", ".join(self.weapons)  # Convert list to string
        weaknesses_str = ", ".join(self.weaknesses)
        return f"Character Profile:\nNickname: {self.nickname}\nWeapons: {weapons_str}\nWeaknesses: {weaknesses_str}"

# Creating characters
player1 = Character('Dragon Slayer', ['pan', 'rope'], ['slow'])
player2 = Character('Mohammed Anas', ['pen', 'paper', 'idea'], ['small', 'confusion'])

# Printing profiles
print(player1.profile())
print(player2.profile())

# Problem 6: Task Check
def check_tasks(task_number):
    items = ['pan', 'rope', 'paper']
    if task_number == 1:  # Climb a mountain
        required_items = ['rope']
        if all(item in items for item in required_items):
            print("I can climb the mountain!")
        else:
            print("I cannot climb the mountain.")
    elif task_number == 2:  # Cook a meal
        required_items = ['pan', 'groceries']
        if all(item in items for item in required_items):
            print("I can cook a meal!")
        else:
            print("I cannot cook a meal.")
    elif task_number == 3:  # Write a book
        required_items = ['pen', 'paper', 'idea']
        if all(item in items for item in required_items):
            print("I can write a book!")
        else:
            print("I cannot write a book.")
    else:
        print("Invalid task number. Please choose 1, 2, or 3.")

# Testing the functions
check_equal()
check_sum()
check_five_in_list()
print(check_leap_year(2024))  # Test leap year
check_tasks(1)  # Test task 1: Climb a mountain
check_tasks(2)  # Test task 2: Cook a meal
check_tasks(3)  # Test task 3: Write a book
