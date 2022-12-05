The project consists of five classes:

Botstartup:
This class initializes the bot; it creates a JDA instance using the discord token, and iniziates a Listener.

Commands:
This class creates a new user which will store the information from the user and uses listener adapter to read events.

onGuildMessageReceived: This class reads Strings sent within the chat and provides a response based on them (the input). It acts based on the current step, which is an attribute from the class useer, within the process (e.g. acquiring name, height, weight, etc.) using a switch statement. After the information acquisition is complete, the bot sends a sport suggestion based on this information from an arrayList that contains three sports adequate for the user's data. Once the user accepts a suggestion, the attribute sport of the user is set to that sport, and training recomendations can begin based on their time availability. A message witha link to a specific training 
rutine will be sent and then it will ask if you want to get diet recomendations. 

User:
This class creates an object User that stores the information of the user chatting with the bot, such as the user's sport, with appropriate getter and setter methods.

Sport:
This class is a template to create an object that is each indivudal sport (e.g. basketball, baseball).

Training:
This class is a template to create an object representing training suggestions

The User interaction interface is through discord, the program connects to a specific bot in discord. 

(For the TA to evaluate the chatbot, we have to add them to a discord chat and give them the token for the bot, which can not be published on github)
