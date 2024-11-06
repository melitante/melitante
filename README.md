- 👋 Hi, I’m @melitante
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
melitante/melitante is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

import sys

data = []

def Menu():
    print("Press [1] SHOW ALL DATA")
    print("Press [2] ADDED SINGLE ARRAY")
    print("Press [3] ADD MULTIPLE ARRAY")
    print("Press [4] DELETE")
    print("Press [5] DELETE ALL DATA")
    print("Press [6] UPDATED DATA")
    print("Press [7] EXIT")

while True:
    Menu()
    choice = input("Choice number : ")

    if choice == "1":
        print("\n========================")
        if data:
            num = 0
            for get_value in data:
                print(num , "- " ,get_value)
                num += 1

        else:
            print()
            print("DATA WAS NO VALUE")
            print()
        print("========================\n")
    elif choice == "2":
        adding_single_array = input("Enter a value for adding single array : ")
        data.append(adding_single_array)

        print("\n======================")
        print("Success Adding Value")
        print("======================\n")

    elif choice == "3":
        adding_multiple_array = int(input("Enter a number how much multiple value you want : "))
        for _ in range(adding_multiple_array):
            create_value_for_multiple_array = input("Enter Value for multiple array : ")
            data.append(create_value_for_multiple_array)
        print("\n=============================")
        print("Success Adding Multiple Array")
        print("=============================\n")

    elif choice == "4":
        num = 0
        print("")
        print("======================")
        for delete_data in data:
            print(num , " " , delete_data)
            num += 1
        print("======================")
        choices = input("choice index number for deleting value : ")
        if data:
            get_value = data.pop(len(choices)-1)

            print("\n====================================")
            print(f"Success Deleting Value {get_value}")
            print("====================================\n")
        else:
            print("\n=================================")
            print("Invalid You have something Wrong")
            print("=================================\n")

    elif choice == "5":
        data.clear()
        print("\n=========================")
        print(f"Success Delete all value")
        print("=========================\n")

    elif choice == "6":
        if data:
            create_number = int(input("Enter index number to update data : "))
            create_value = input("Enter Value to update data : ")

            data[create_number] = create_value
            print("\n===========================")
            print("Success update data")
            print("===========================\n")
        else:
            print("\n=========================")
            print("Invalid Data was no value")
            print("=========================\n")
    elif choice == "7":

        sys.exit("\nEXIT WHILE LOOP -> THANK YOU")
