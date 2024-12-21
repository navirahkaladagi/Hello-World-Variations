from datetime import datetime

# Dictionary of greetings in different languages
greetings = {
    "1": "Hello",        # English
    "2": "Hola",         # Spanish
    "3": "Bonjour",      # French
    "4": "Namaste",      # Hindi
    "5": "Nǐ hǎo",       # Chinese
    "6": "Konnichiwa",   # Japanese
    "7": "Guten Tag",    # German
    "8": "Ciao"          # Italian
}

# Display language options
print("Choose a language for your greeting:")
for key, value in greetings.items():
    print(f"{key}. {value} ({value})")

# Get the user's language choice
language_choice = input("Enter the number of your choice: ")
if language_choice not in greetings:
    print("Invalid choice. Defaulting to English.")
    language_choice = "1"

# Get the user's name
name = input("Enter your name: ")

# Get the current date and time
current_time = datetime.now().strftime("%Y-%m-%d %H:%M:%S")

# Display the greeting in the chosen language
print(f"{greetings[language_choice]}, {name}!")
print(f"Current date and time: {current_time}")
