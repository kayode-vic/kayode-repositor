from math import Math
from Physics import Physics
phy = Physics()
mth = Math()

print("Physics And Maths Calculator 1.0")
mth_or_phy = input("What operation would you like to carry out math or phycics\n> ")
if mth_or_phy == "math":
    print("You can add(+), subtract(-), mutiply(*), divide(/), and find the exponent of a number(^)")
    num1 = int(input("First num\n> "))
    ops = input("Enter the operation you want to carry out\n> ")
    num2 = int(input("Second num\n> "))
    if ops == "+":
        print(mth.add(num1, num2))
    if ops == "-":
        print(mth.minus())
    if ops == "*":
        print(mth.multiply(num1, num2))
    if ops == "/":
        print(mth.divide(num1, num2))
    if ops == "*/":
        print(mth.square_root(num1, num2))

if mth_or_phy == "physics":
    print("You can calculate Average speed, Newtons Second law, Power, Workdone and Momentum")
    ops = input("What operation do you want to carry out").lower()
    if ops == "average_speed":
        num1 = int(input("distance\n> "))
        num2 = int(input("time\n> "))
        print(phy.calc_average_speed())
    if ops == "newtons_second_law":
        num1 = int(input("mass\n> "))
        num2 = int(input("acceleration\n> "))
        print(phy.calc_newtons_second_law())
    if ops == "power":
        num1 = int(input("workdone\n> "))
        num2 = int(input("time\n> "))
        print(phy.calc_power())
    if ops == "workdone":
        num1 = int(input("force\n> "))
        num2 = int(input("distance\n> "))
        print(phy.workdone())
    if ops == "momentum":
        num1 = int(input("mass\n> "))
        num2 = int(input("velocity\n> "))
        print(phy.momentum())