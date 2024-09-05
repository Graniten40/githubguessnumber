# githubguessnumber
Code in Python, there you can guess on a number

import random

def main():
    # Slumpa ett hemligt tal mellan 1 och 100
    hemligt_tal = random.randint(1, 100)
    gissningar = 0
    correct_guess = False

    # Upprepa inmatningen tills användaren har gissat rätt eller tio gånger har gått
    while not correct_guess and gissningar < 10:
        # Fråga användaren att gissa talet
        gissning = int(input("Gissa det hemliga talet mellan 1 och 100: "))

        # Jämför gissningen med det hemliga talet
        if gissning == hemligt_tal:
            print("Grattis! Du har gissat rätt!")
            correct_guess = True
        else:
            gissningar += 1
            if gissning > hemligt_tal:
                print("Ditt tal är för högt!")
            else:
                print("Ditt tal är för lågt!")

    # Om användaren inte gissat rätt inom tio försök
    if not correct_guess:
        print(f"Tyvärr, det hemliga talet var {hemligt_tal}. Försök igen nästa gång!")

if __name__ == "__main__":
    main()
