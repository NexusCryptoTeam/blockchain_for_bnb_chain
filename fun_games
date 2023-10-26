import random

def choose_word():
    words = ["apple", "banana", "cherry", "date", "elderberry", "fig", "grape", "honeydew"]
    return random.choice(words)

def play_hangman():
    word = choose_word()
    word_length = len(word)
    guessed_word = ["_"] * word_length
    attempts = 6  # Максимальное количество попыток

    print("Добро пожаловать в игру 'Виселица'!")
    print("У вас есть 6 попыток, чтобы угадать слово.")

    while attempts > 0:
        print(" ".join(guessed_word))
        letter = input("Введите букву: ").lower()

        if len(letter) != 1 or not letter.isalpha():
            print("Пожалуйста, введите одну букву.")
            continue

        if letter in word:
            for i in range(word_length):
                if word[i] == letter:
                    guessed_word[i] = letter

            if "_" not in guessed_word:
                print("Поздравляю, вы угадали слово: " + word)
                break
        else:
            attempts -= 1
            print("Неверная буква. Осталось попыток: " + str(attempts))

    if attempts == 0:
        print("Вы проиграли. Загаданное слово было: " + word)

if __name__ == "__main__":
    play_hangman()
