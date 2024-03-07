Description of the project:
This project is an attempt to clone the popular vacation rental platform, AirBnB. The end-goal of the project is to build a full-fledged system for managing vacation rentals, including features for users to list their properties, make bookings, and manage their reservations. This is a work in progress, and the project is still under development.

In its current state, it has a console, a static web page, a file storage engine, a database storage engine which uses MySQL, and a flask web application used to implement a REST API.

Description of the command interpreter: 

Getting Started
Clone this git repository. If you are a GNU/Linux user, you could copy and paste the following command to clone and change working directory into the root of this project:

git clone https://github.com/chee-zaram/AirBnB_clone.git && cd AirBnB_clone
other wise, clone the repository as you'd like and change working directory into the root of the project.

Command Interpreter (The Console)
The command interpreter is a command-line interface that allows users to interact with the AirBnB clone system. It provides a set of commands for managing the various aspects of the system, such as creating and managing listings, managing bookings, and so on.

Starting the Command Interpreter
To start the command interpreter, navigate to the root of the project if not already there and run the following command if using file storage:

./console.py
or, with database storage, for example:

HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db ./console.py
This will start the command interpreter and you will be presented with a prompt, (hbnb) , where you can start entering commands.

Using the Command Interpreter
The command interpreter provides a set of commands for managing the various aspects of the AirBnB clone system. Some of the available commands include:

Command	Description	Usage
create	Create a new instance of a class	create <class_name>
show	Show the details of a specific instance of a class	show <class_name> <instance_id>
all	Display the details of all instances, or all instances of a class	all or all <class_name>
destroy	Delete a specific instance of a class	destroy <class_name> <instance_id>
update	Update the attribute value for a given instance of a class	update <class_name> <class_id> <attribute_name> "<attribute_value>"
quit	Quits the command interpreter	quit
The interpreter can also be terminated by hitting EOF key combination.

To use a command, simply type the command followed by any required arguments at the prompt and hit enter.

For example, to create a new instance of the User class, you would run the following command:

(hbnb) create User email="airbnb.clone@airbnb.com" password="09876airbnb" first_name="John" last_name="Doe"
To show the details of a specific instance of a class, you would run the following command, where <class_id> is the ID of the instance you want to show:

(hbnb) show User <class_id>
Some interpreter commands can also be processed when used as suffixes to a class name:

show: <class_name>.show("<instance_id>")
Example:

(hbnb) User.show("1234-5678")
to print a representation of the user with id 1234-5678

count: <class_name>.count()
Example:

(hbnb) BaseModel.count()
to get the number of instances of the class BaseModel

all: <class_name>.all()
Example:

(hbnb) City.all()
to print all instances of the class City

destroy: <class_name>.destroy("<instance_id>")
Example:

(hbnb) Place.destroy("1234-5678")
to delete the instance of class Place with id 1234-5678

update: <class_name>.update("<instance_id>", "<attribute_name>", "<attribute_value>")
Example:

(hbnb) State.update("1234-5678", "name", "New York")
to update the attribute called name of the instance of State class with id 1234-5678

The .update extension also works with a dictionary of attribute name(s) and value(s)

Example:

(hbnb) User.update("1234-5678", {"password": "09876airbnb", "last_name": "Doe"})
to update the email and password of the user with id 1234-5678

For a full list of all commands and their usage, run the following command:

(hbnb) help
or

(hbnb) help <command>
for a help doc on a specific command.

Authors
The AUTHORS file at the root of the repository lists all individuals who were part of the project from conception. Their full names, links, and contact information are listed below:

Neo Magadani
Samuel Stephen
