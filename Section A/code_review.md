# An SMS Simulation class SMSMessage(object):

hasBeenRead = False messageText = text fromNumber = number
def __init__(self,hasBeenRead,messageText,fromNumber):
    self.hasBeenRead =False self.messageText = text
    self.fromNumber = number
    
def MarkASRead(self):
    if userChoice == read:
        self.hasBeenRead =True
        
def add_sms():
def get_count():
def get_message():
def get_unread_messages():
def remove():
    
no_1 = SMSMessage(False,"Hello","0798653452")
no_2 = SMSMessage(False,"WYD","0845673864")
no_3 = SMSMessage(False,"How are you?","0631873298")
SMSStore = [] userChoice =""

while userChoice != "quit":
    userChoice = raw_input("What would you like todo -read/send/quit?")
    if userChoice =="read":     
# Place your logic here elif userChoice =="send": 
# Place your logic here elif userChoice == "quit":
    print("Goodbye")
else:
    print("Oops - incorrect input")

# REVIEWER'S COMMENT
Dear Student,
I am proud of your effort at implementing the class methods. Please checkout the below review:

1. Start the parent class definition on line 2 outside the comment, on a separate line.
    class SMSMessage(object):
2. Class attributes on line 3 is not needed, it could be brought into the __init__ method below on line 4
3. For conventional purposes, in python please use _ to separate variable names or functions, instead of lumping words together and separating them with Caps. e.g 

    has_been_read in place of hasBeenRead
    from_number in place of fromNumber
    message_text in place of messageText
    mark_as_read in place of MarkASRead
    sms_message against SMSMessage 

This applies through the rest of the code
4. text and number from lines 5 and 6 are undefined. The attributes could be better defined like:
    self.hasBeenRead = hasBeenRead
    self.messageText = messageText
    self.fromNumber = fromNumber
5. The changes from reviewed comments 2 need to be set as attributes, they need to be set with new instances
6. Userchoice from lie 9 needs to run with the method as an argument as Userchoice is currentlyundefined
7. Read needs to be a string as it is currently applying as a variable eg "read"
8. Comment out all WIP so your code can run successfully
9. I love the way you ran your while loop logic, as a stretch you can add instructions on how to quit e.g type Q to exit
10. Use input on line 24 instead of raw_input

Lastly, please note that the class will not be defined until Python has executed the entirety of the definition, so you can be sure that you can reference any method from any other method on the same class, or even reference the class inside a method of the class.