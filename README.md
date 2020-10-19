# ML_2021

This is a chatbot project which I have done in ML 2021 course.

I have done a chatbot which helps to people to know the bikes with milage, colour and price.

This repositry contains code for choosing bike.




CODE FOR CHOOSING BIKE


import random

def introduction():
    responses = [
        "Hello I am a technical friendly bot and will help you to know details about bike.",
        "Welcome!!!!, I am bot.I will help you to know about bike flavour based on your preference."
    ]
def interaction(name):
  messages=[
            "Thank you. Pleasure to meet you." ,
            "Lets have a nice time together."
               ]
  print(random.choice(messages))
  print("__")
    
def botadvantages():
    print("--->This bot will suggest a user to select a bike.")
    print("--->The bot will ask the user for their choice to suggest them the bike.")
    print("--->It will respond to user input appropriatly to suggest the bike.")
    print("__")

def bike():
  bike_type=int(input("Enter your bike name FZ means 1 or R15 means 2 or pulsar NS means 3: "))
  bike_colour=int(input("Enter your bike colour blue means 1 or black means 2 : "))
  if bike_type == 1 and bike_colour == 1:
    print("your bike is FZ , colour is blue , price is 1,30,000/- and mileage is 39 to 45km/l")
    print("__")
  elif bike_type == 1 and bike_colour == 2:
    print("your bike is FZ , colour is black , price is 1,35,OOO/- and mileage is 39 to 45km/l")
    print("__")
  elif bike_type == 3 and bike_colour == 2:
    print("your bike is pulsar NS , colour is blue , price is 1,52,000/- and mileage is 35km/l")
    print("__")
  elif bike_type == 2 and bike_colour == 1:
    print("your bike is R15 , colour is blue , price is 1,80,000/- and mileage is 40km/l")
    print("__")
  elif bike_type == 2 and bike_colour == 2:
    print("your bike is R15 , colour is black , price is 1,85,000/- and mileage is 40km/l")
    print("__")
  elif bike_type == 3 and bike_colour == 2:
    print("your bike is pulsar NS , colour is blue , price is 1,52,000/- and mileage is 35km/l")
    print("__")
  else:
    print("Enter the valid input.")
    print("__")

def show_menu():
    print("Please select choice from the below.")
    print("1.Know about bot advantages .")
    print("2.Know about bike available based on your prefrences.")
    print("3.End the chat if your got the correct bike.")
    print("__")
    try:
        return int(input("Enter your choice from [1-3]."))
    except:
        print("Enter choice only from 1,2,3.")
        return 0

def bot():
  introduction()
  name=input("May i know your name please : ")
  interaction(name)
  response = show_menu()
  while response != 3:
      if response == 1:
          botadvantages()
      elif response == 2:           
          bike()
      else:
          print("I don't understand that.Please enter a valid input from the given choice.")
      response = show_menu()
        
bot()
