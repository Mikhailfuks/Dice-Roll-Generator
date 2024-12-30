import random

def roll_dice(num_dice, num_sides=6):
    """Simulates rolling multiple dice. Defaults to six-sided dice."""
    results = []
    for _ in range(num_dice):
        results.append(random.randint(1, num_sides))
    return results

while True:
    try:
        num_dice = int(input("How many dice do you want to roll? "))
        if num_dice <= 0:
            print("Please enter a positive number of dice.")
            continue
        num_sides = int(input("How many sides do the dice have? "))
        if num_sides <= 0:
            print("Please enter a positive number of sides.")
            continue
        break
    except ValueError:
        print("Invalid input. Please enter integers only.")

results = roll_dice(num_dice, num_sides)
print(f"You rolled: {results}")
print(f"Total: {sum(results)}")

