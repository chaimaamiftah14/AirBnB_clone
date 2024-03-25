# AirBnB Clone ― The ALX-Holberton BnB
![Alt text](https://github.com/chaimaamiftah14/AirBnB_clone/assets/78249686/f2fa11f4-70dd-47b4-9dcd-726ffc1b95bd)
                                HolbertonBnB
______________________________________________________________________________________________________

Description
-----------------------------------------------------------------------------------------------------
  * The project of Airbnb clone is a simplified version of the popular online hospitality service Airbnb the goal is to develop a command-line interface (CLI) that allows users to intract with the platform , including function alities such as managing users, proprites, booking, and more.
Usage
Our Airbnb clones command-line interface (CLI) offers users an intintive way to interact with the platform. Whether in interactive or non-nteractive mode, users can easily manage users, proprities, booking, and more.
Command Interpreter
Our command-line interface (CLI) offers users an intuitive way to interact with the Airbnb Clone platform. Whether in interactive or non-interactive mode, users can easily execute various commands to perform actions on the platform.

Key Concepts Covered in this project
------------------------------------------------------------------------------------------------------

1. Python Package Creation:
   - Understanding how to structure and organize Python code into packages.
   - Utilizing __init__.py files to define package behavior and imports.
   - Creating modular and reusable components within a package.
3. Command Interpreter Implementation with the cmd Module:
   - Exploring the cmd module in Python for building command-line interfaces.
   - Implementing commands, command parsing, and command execution.
   - Providing a user-friendly interface for interacting with the program.
4. Unit Testing Fundamentals:
   - Learning the importance of unit testing in software development.
   - Writing test cases to ensure individual components work as expected.
   - Running tests automatically to validate code changes and prevent regressions.
5. Serialization and Deserialization using JSON:
   - Serializing Python objects to JSON format for storage or transmission.
   - Deserializing JSON data back into Python objects for manipulation.
   - Utilizing JSON as a common data interchange format in web applications.
6. Datetime Management:
   - Working with date and time objects in Python using the datetime module.
   - Foatting and parsing date/time strings.
    - Performing arithmetic operations and comparisons on datetime objects.
7. UUID (Universally Unique Identifier):
   - Understanding the purpose of UUIDs in generating unique identifiers.
   - Generating UUIDs using the uuid module for various applications.
   - Ensuring uniqueness and randomness in UUID generation.
8. *args and **kwargs Usage:
   - Understanding variable-length argument lists in Python functions.
   - Using *args to pass a variable number of positional arguments to a function.
   - Leveraging **kwargs to handle variable-length keyword arguments in functions.
9. Named Arguments Handling in Functions:
   - Defining functions with named arguments to enhance readability and flexibility.
   - Passing arguments by name rather than position in function calls.
   - Managing default argument values and handling variable argument sets efficiently.
   
  Files and Directories
  ----------------------------------------------------------------------------------------------------

   + models directory will contain all classes used for the entire project. A class, called “model”in    + OOP project is the representation of an object/instance.
   + tests directory will contain all unit tests.
   + console.py file is the entry point of our command interpreter.
   + models/base_model.py file is the base class of all our models. It contains common elements:
    - attributes: id, created_at and updated_at
    - methods: save() and to_json()
   + models/engine directory will contain all storage classes (using the same prototype). For the moment I will have only one: file_storage.py.

Project Phases Overview:
------------------------------------------------------------------------------------------------------

Phase One: Establishing Object Storage Abstraction

In the initial phase, the focus lies on implementing a robust storage system to abstract the handling of objects and their persistence. This phase entails:

1. Designing a Parent Class (BaseModel): A foundational class responsible for initializing, serializing, and deserializing future instances.
2. Setting up Serialization/Deserialization Flow: Establishing a seamless flow between instances, dictionaries, JSON strings, and files to facilitate data manipulation.
3. Creating Airbnb Class Structure: Developing essential classes for Airbnb functionality (e.g., User, State, City, Place) that inherit from BaseModel, ensuring uniformity and scalability.
4. Implementing File Storage Engine: Developing the initial storage engine, tailored for file storage, to manage data persistence.
5. Writing Unit Tests: Creating comprehensive unit tests to validate the functionality of all classes and the storage engine.

Phase Two: Data Model Establishment

In this phase, the project will focus on:

1. Defining the Data Model: Establishing a clear and structured data model to represent Airbnb entities and their relationships.
2. Implementing CRUD Operations: Enabling operations for managing objects (e.g., create, update, destroy) through a console or command interpreter.
3. Persistent Storage Implementation: Integrating mechanisms to store and persist objects to JSON files, ensuring data integrity and durability.

Usage 💻
-----------------------------------------------------------------------------------------------------

Our AirBnB clone's command-line interface (CLI) offers users an intuitive way to interact with the platform. Whether in interactive or non-interactive mode, users can easily manage users, properties, bookings, and more.

Command           | Example
------------------|------------------------
Run the console   | ./console.py
Quit the console  | (hbnb) quit
Display command help  | (hbnb) help <command>
Create an object (displays its ID)  | (hbnb) create <class>
Show an object   | (hbnb) show <class> <id> or (hbnb) <class>.show(<id>)
Destroy an object  | (hbnb) destroy <class> <id> or (hbnb) <class>.destroy(<id>)
Show all objects, or all instances of a class  | (hbnb) all or (hbnb) all <class>
Update an attribute of an object  | (hbnb) update <class> <id> <attribute name> "<attribute value>" or (hbnb) <class>.update(<id>, <attribute name>, "<attribute value>")

Example Usage:
1. Create a new user:
   (hbnb) create User email="example@example.com" password="password123"

2. Show details of a user:
   (hbnb) show User 1234-5678

3. Update the name of a property:
   (hbnb) update Place 9876-5432 name="Cozy Cabin"

4. Retrieve all instances of a class:
   (hbnb) all Amenity

Testing 📏
------------------------------------------------------------------------------------------------------

Our tests for the AirBnB clone project are comprehensive and located in the tests folder. To run the entire test suite, execute the following command:

$ python3 unittest -m discover tests

Alternatively, you can specify a single test file to run:

$ python3 unittest -m tests/test_console.py
