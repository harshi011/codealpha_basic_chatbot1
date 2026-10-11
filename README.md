# codealpha_basic_chatbot1

def chatbot_response(choice):

    responses = {
        
        1: "Hello! I'm MoodMate, your study buddy. 😊",
        2: "My name is MoodMate! I'm here to help you with your studies.",
        3: "You seem tired. Take a 5-minute break and drink some water.",
        4: "Take a deep breath! Focus on one small task at a time.",
        5: "Don't panic! Revise important topics and practice questions.",
        6: "Try studying for 20 minutes without distractions.",
        7: "Believe in yourself! Start with one small task. You can do it!",
        8: "Study for 25 minutes, then take a 5-minute break.",
        9: "That's wonderful! Keep using your positive energy.",
        10: "It's okay to have a difficult day. Take a short break and try again.",
        11: "You're welcome! I'm always happy to help.",
        12: "Goodbye! Keep learning and believe in yourself."
    }

    return responses.get(choice, "Invalid choice! Please enter a number from 1 to 12.")


def start_chatbot():
    print("=" * 40)
    print("      MOODMATE - STUDY BUDDY")
    print("=" * 40)

    while True:
        print("\nHow can I help you today?")
        print("1. Say Hello")
        print("2. Know My Name")
        print("3. I am Tired")
        print("4. I am Stressed")
        print("5. Exam Help")
        print("6. I am Bored")
        print("7. Motivate Me")
        print("8. Study Tips")
        print("9. I am Happy")
        print("10. I am Sad")
        print("11. Thank You")
        print("12. Exit")

        try:
            choice = int(input("\nEnter your choice (1-12): "))
        except ValueError:
            print("Please enter a valid number!")
            continue

        if choice < 1 or choice > 12:
            print("Invalid choice! Please enter a number from 1 to 12.")
            continue

        print("\nMoodMate:", chatbot_response(choice))

        if choice == 12:
            break


start_chatbot()

