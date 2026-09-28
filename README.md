# project1



    
  
    import random

    TOTAL_ROUNDS= 10
    INITIAL_SCORE= 50

    leaderboard = []


    def get_player_name():
        while True:
            A = input("Enter your name: ")
            if A:
                return A
            print("Name cannot be empty.")


    def show_rules():
        print("\nHIGH OR LOW")
        print("Guess whether the next number will be HIGH or LOW.")
        print("Numbers are generated between 1 and 200.")
        print("Correct guess: +10 points. Wrong guess: -5 points.")
        print("Equal numbers: no change.")
        print(f"You get a maximum of {TOTAL_ROUNDS} rounds.")
        print("The game also ends if your score reaches 0.")
        print(f"Starting score: {INITIAL_SCORE}")


    def get_choice():
        while True:
            B = input("\nChoose HIGH or LOW: ").strip().lower()

            if B in ("high", "h"):
                return "high"
            elif B in ("low", "l"):
                return "low"
            else:
                print("Invalid choice Enter HIGH or LOW.")


    def show_leaderboard():
        print("\nLEADERBOARD")
        if not leaderboard:
            print("No games played yet.")
            return

        ranked = sorted(leaderboard, reverse=True)
        for rank, (score, A) in enumerate(ranked, start=1):
            print(f"{rank}. {A} - {score}")


    def play_game():
        A = get_player_name()
        score = START_SCORE
        current = random.randint(1, 200)
        round_no = 1

        print(f"\nGood luck, {A}!")
        print("Starting number:", current)

        while score > 0 and round_no <= MAX_ROUNDS:
             print("\n")
             print(f"Round: {round_no}")
             print("Current number:", current)
             print("Current score:", score)

             B = get_choice()
             next_number = random.randint(1, 200)
             print("Next number:", next_number)

             if next_number == current:
                 print("The numbers are equal!")
                 print("No points gained or lost.")
             else:
                 result = "high" if next_number > current else "low"

                 if B == result:
                     print(f"Correct The number was {result.upper()}.")
                     score += 10
                 else:
                     print(f"Wrong The number was {result.upper()}.")
                     score -= 5

             current = next_number
             round_no += 1

         print("\n")
         print(" GAME OVER")
         print("")
         print("Player:", A)
         print("Final score:", score)

        if score >= 100:
            print("Excellent performance")
        elif score >= 70:
            print("Great job")
        elif score > 0:
            print("Good try")
        else:
            print("You lost all your points")

        leaderboard.append((score, A))
        show_leaderboard()


    def main():
        while True:
            print("\nHIGH OR LOW GAME")
            print("1-Play Game")
            print("2-Rules")
            print("3-Leaderboard")
            print("4-Exit")

            option = input("Enter your choice: ").strip()

            if option == "1":
                play_game()
            elif option == "2":
                show_rules()
            elif option == "3":
                show_leaderboard()
            elif option == "4":
                print("Thank you for playing \n come again to play ")
                break
            else:
                print("Please enter one of numbers given above  option")


    if __name__ == "__main__":
        main()
