```python
class Phone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def display_info(self):
        return f"Brand: {self.brand}, Model: {self.model}, Price: ${self.price}"

    def update_property(self, property_name, value):
        if hasattr(self, property_name):
            setattr(self, property_name, value)
        else:
            print("Property does not exist.")

    def delete_property(self, property_name):
        if hasattr(self, property_name):
            delattr(self, property_name)
        else:
            print("Property does not exist.")

def main_menu():
    phones = []
    while True:
        print("\nMain Menu:")
        print("1. Add Phone")
        print("2. Modify Phone")
        print("3. Delete Phone")
        print("4. Display Phones")
        print("5. Exit")

        choice = input("Choose an option (1-5): ")

        if choice == '1':
            brand = input("Enter phone brand: ")
            model = input("Enter phone model: ")
            price = float(input("Enter phone price: "))
            phone = Phone(brand, model, price)
            phones.append(phone)
            print("Phone added successfully!")

        elif choice == '2':
            if not phones:
                print("No phones to modify.")
                continue

            for i in range(len(phones)):
                print(f"{i + 1}. {phones[i].display_info()}")

            index = int(input("Select phone to modify (by number): ")) - 1
            if 0 <= index < len(phones):
                phone = phones[index]
                property_name = input("Enter property name to modify (brand/model/price): ")
                new_value = input(f"Enter new value for {property_name}: ")
                if property_name == "price":
                    new_value = float(new_value)
                phone.update_property(property_name, new_value)
                print("Phone updated successfully!")
            else:
                print("Invalid phone number.")

        elif choice == '3':
            if not phones:
                print("No phones to delete.")
                continue

            for i in range(len(phones)):
                print(f"{i + 1}. {phones[i].display_info()}")

            index = int(input("Select phone to delete")) - 1
            if 0 <= index < len(phones):
                phones.pop(index)
                print("Phone deleted successfully!")
            else:
                print("Invalid phone number.")

        elif choice == '4':
            if not phones: 
                print("No phones in the list.")
            else:
                for i in range(len(phones)):
                    print(f"{i + 1}. {phones[i].display_info()}")

        elif choice == '5':
            print("Exiting program.")
            break

        else:
            print("Invalid choice. Please choose a number from 1 to 5.")

main_menu()
```python
