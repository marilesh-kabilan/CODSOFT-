# CODSOFT-
def show_menu():
    print("\n📋 Today's Menu:")
    menu = {
        "1": "Pizza - ₹150",
        "2": "Burger - ₹80",
        "3": "Pasta - ₹120",
        "4": "Coffee - ₹60",
        "5": "Ice Cream - ₹50"
    }
    for key, value in menu.items():
        print(f"{key}. {value}")
    return menu

def chatbot():
    print("🤖 Welcome to ChatFoodie!")
    name = input("May I know your name? ")
    print(f"Hello {name}, glad to serve you today!")

    order_list = []

    while True:
        menu = show_menu()
        choice = input("Please enter the item number you would like to order: ")

        if choice in menu:
            print(f"You ordered: {menu[choice]}")
            order_list.append(menu[choice])
        else:
            print("Sorry, that's not on the menu.")

        more = input("Would you like to order anything else? (yes/no): ").lower()
        if more != 'yes':
            break

    print("\n🧾 Your Order Summary:")
    for item in order_list:
        print(f"- {item}")
    
    print(f"\nThank you, {name}, for your order! 😊 Have a great day!")

# Run the chatbot
chatbot()
