# The Camper World Camping Game
import random

# Player attributes
player_name = input("Enter your name: ")
player_energy = 100
player_hunger = 0
player_thirst = 0

# Game loop
while player_energy > 0:
    print("\n--- Camper World Camping ---")
    print(f"Name: {player_name}")
    print(f"Energy: {player_energy}")
    print(f"Hunger: {player_hunger}")
    print(f"Thirst: {player_thirst}")

    # Options for the player
    print("\nOptions:")
    print("1. Explore the forest")
    print("2. Set up camp")
    print("3. Eat")
    print("4. Drink")
    print("5. Rest")
    print("6. Quit")

    choice = input("Enter your choice: ")

    if choice == '1':
        # Explore the forest
        energy_cost = random.randint(10, 30)
        player_energy -= energy_cost
        player_hunger += random.randint(5, 15)
        player_thirst += random.randint(5, 15)
        print("You explored the forest and used some energy.")

    elif choice == '2':
        # Set up camp
        player_energy += random.randint(10, 20)
        print("You set up your camp and rested a bit.")

    elif choice == '3':
        # Eat
        if player_hunger > 0:
            player_hunger -= random.randint(10, 30)
            print("You ate some food.")
        else:
            print("You're not hungry.")

    elif choice == '4':
        # Drink
        if player_thirst > 0:
            player_thirst -= random.randint(10, 30)
            print("You drank some water.")
        else:
            print("You're not thirsty.")

    elif choice == '5':
        # Rest
        player_energy += random.randint(20, 40)
        print("You rested and regained some energy.")

    elif choice == '6':
        # Quit
        print("Thanks for playing!")
        break
    # Check for game over conditions
    if player_energy <= 0:
        print("You ran out of energy and couldn't continue.")
    elif player_hunger >= 100 or player_thirst >= 100:
        print("You've eaten or drunk too much and can't continue.")
        
https://thecamperworld.com
