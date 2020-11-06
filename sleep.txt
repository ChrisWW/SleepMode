# shutdown program

import os

choice = input("Enter Off/SD to shutdown or S/On to shutdown in hours or No to exit the program:")

if choice == "off" or choice == "Off" or choice == "SD" or choice == "sd":
    print("You turn off your computer in 10 seconds")

    os.system("shutdown -s -t 10")

elif choice == "on" or choice == "On" or choice == "S" or choice == "s":
    print("You chose to turn off your computer in hours")
    time = input("Write in how many hours would you like to put your PC off:")

    if float(time) < 0:
        print("Value time can't be less than 0, please input number which is higher than 0")
        time = float(input("Write in how many hours would you like to put your PC off:"))

    else:
        count = round(float(time) * 3600, 0)

    os.system("shutdown -s -t count")
elif choice == "no" or choice == "No":
    exit()