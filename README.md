# Client Project: Sleep Sync (Sleep Tracker App)

# Criteria A: Planning

## Problem definition
My Roommate, Ryu Koshiba has recently been sleep deprived and wants to understand his sleep pattern throughout the month to prepare himself for his final exams coming up. To do this, Ryu wants an app developer to create an app that tracks his duration of sleep, date of sleep, quality of sleep, and location of sleep to best understand his sleep pattern. He wants an app that has a GUI and has accessible buttons and text boxes so he can input data in a straightforward matter.

- The client is recently sleep deprived
- The client requires an app that can record and track his sleep duration, date, quality and location.
- The client requires an app that has a GUI

## Proposed Solution:

### Design Statement
I will design and make an app that tracks the date, duration, quality (out of 10), and location of sleep for my client who is my roommate, Ryu Koshiba. The application will be able to keep track of all sleep stats via the use of a login system. To ensure security and privacy, the login system will have a hashing system to secure everyone's password and will all be saved in a local database using SQLite. The application will have a GUI so that users can easily guide themselves throughout the app with mouse clicks. This all will be created using the Python 3.x language with the help of KivyMD for GUI construction. All code will be created and developed on the application, Pycharm. This app will take 4 weeks to complete and will be evaluated according to the criteria. 

## Justification

### Why Python?
Out of every programming language, I have chosen to use Python 3.x for numerous reasons. For starters, Python is the most well known and used programming language throughout the world (1). This will not only allow me to have greater access to resources and references but also the app will also be compatible with a greater number of systems, improving the overall experience of the client. Personally, I am the most comfortable with programming Python and so not only will everything be streamlined but also the client will receive the app in a timely manner, without any extensions of the due date. Judging by the benefits of both the programmer and client, it's safe to say that Python is the right programming language to use for this project. 

Since python is said to be the most well known and user programing language throughout the world (1) future developers will be able to expand and add on to the program I have created. This will not only help future developers but clients as well as they will be able to get an application that is always up to data and with new features, from new perspectives from other developers. 

### Why KivyMD?
KivyMD will be used to construct the graphical user interface (GUI) for the user to navigate throughout the app. I have chosen KivyMD because not only is KivyMD compatible with all 3 main operating systems, but also is one of the simpler GUI libraries to learn (2). KivyMD’s goal, “to approximate Google's Material Design spec as close as possible without sacrificing ease of use or application performance.” (3) also greatly relates to the client's experience as the GUI is what the client actually sees and a good GUI is always appreciated in every application. KivyMD is also the library I am the most familiar with and will help me as a developer to finish my project on time. For these reasons, I have come to the conclusion that KivyMD is the most appropriate GUI node for my project. 

Other alternatives such as Libavg or PyQT do exist when creating  GUI. However, KivyMD is compatible with all 3 operating systems and even mobile devices (2) making it easier for the client to access the program I have created and also making future developers able to expand even further. Moreover, KivyMD's goal of being "google like" also helps as it will be visually appealing and familiar for the client. 

### Why SQLite?
SQLite is a database engine written in the C language(4) but also comes bundled with Python and can be used in any Python application without having to install any additional software (5). I am also most familiar with this database structure and console which will allow me to create the database quickly and will match the client's deadline more effectively. With this flexibility and ease of use, I have decided to use SQLite for this project's database. 

Compared to other database applications, SQL lite is cross combatible with a number of programs and operating systems (5) and is relatively simpler, shortening the time to develop a database. These factors will be beneficial to the client as the compatability will ensure the client can access the database through the app from any platform they wish to use and also the application will be able to be developed by future developers swiftly, cosntantly improving the application for the client. 

### Why is the output through a GUI?
The application will have an output of a GUI rather than text. This is to meet the requirement of the client where he requires an application that can not only record and show his sleep data but do all that through a GUI for ease of use. Due to the client's requirements, I have decided that the output should be through a GUI. 


## Success Criteria

1. The application must have a registration system where the users can register their email, username and password and are saved into the database.
2. The application must have a working log in system, where all the credentials entered have to match with the database (registered data).
3. The application must encrypt the users password in the local SQL database.
4. The application must have a home screen that gives the option to log sleep data, view past data or logout. 
5. The user must be able to input all 4 attributes (date, duration, quality and location) into the database via the GUI.
6. The application must be able to show past inputs of all 4 attributes (date, duration, quality and location) from the database via the GUI.
7. The application must contain a log in screen, registration screen, home screen, screen to enter sleep data and screen to view the sleep data; in total 5 unique screens. 

### Client Approval
To check if the client approves my planning and the success criteria, I have decided to email him to verify with him.

![](client2.png)

Now that we have the success criteria verified, we can move on to the coding.
## Works Cited

1. "The 10 Most Popular Programming Languages to Learn in 2021." Northeastern University Graduate Programs, 14 May 2021, www.northeastern.edu/graduate/blog/most-popular-programming-languages/. Accessed 28 Mar. 2022.

2. ResellerClub. "The 6 Best Python GUI Frameworks for Developers." Medium, 18 Oct. 2019, medium.com/teamresellerclub/the-6-best-python-gui-frameworks-for-developers-7a3f1a41ac73. Accessed 28 Mar. 2022.

3. "Kivymd/KivyMD: KivyMD is a Collection of Material Design Compliant Widgets for Use with Kivy, a Framework for Cross-platform, Touch-enabled Graphical Applications. Https://youtube.com/c/KivyMD Https://twitter.com/KivyMD Https://habr.com/ru/users/kivymd Https://stackoverflow.com/tags/kivymd." GitHub, github.com/kivymd/KivyMD. Accessed 28 Mar. 2022.

4. "SQLite Home Page." SQLite, www.sqlite.org/index.html. Accessed 28 Mar. 2022.

5. "How To Use the Sqlite3 Module in Python 3." DigitalOcean – The Developer Cloud, 2 June 2020, www.digitalocean.com/community/tutorials/how-to-use-the-sqlite3-module-in-python-3. Accessed 28 Mar. 2022.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

# Criteria B: Design

## System Diagram
![](systemdiagram.png)
### Fig1. System Diagram of the application

The system diagram shows how the application interacts with each other. The input will be done with a keyboard (input of numbers) and the output will be shown on the screen. The application will be on a computer, which will be inside the MacOS operating system. The app will then be operated via Python version 3.x and executed on Pycharm via the file name, Unit3.py and Unit3.kv. These python files are then connected with a SQL database called Unit3.db. 

## Wireframe Diagram
![](wireframe.jpg)
### Fig2. Wireframe Diagram of the GUI

This Wireframe Diagram shows the generated outline of the GUI of the application. It shows the functionalities of every button planned out to be used in the application and shows all 5 screens of the application. 

## Flow Diagrams

![](flowchart1.png)
### Fig3. Registration Screen Flow Diagram

This is the flowchart of when the user registers their Email, Username, and Password. 

![](flowchart2.png)
### Fig4. Login Screen Flow Diagram

This is a flowchart showing how the login screen functions. It shows how the login screen matches all the text inputs with the credentials in the database.

![](flowchart3.png)
### Fig5. Data insert Screen Flow Diagram

This is a flowchart showing how inputting data into the GUI connects and communicated with the database.

## ER Diagram
![](erdiagram.png)
### Fig6. Data insert Screen Flow Diagram

## UML Diagram
![](umldiagram.png)
### Fig7. UML Diagram for Application Database

## Table of data

### Table of User Database

| Id | Username | Password                                                                               | EMail                     |
|----|----------|----------------------------------------------------------------------------------------|---------------------------|
| 1  | Raijee   | password123 | reiji.nishikawa@gmail.com |

This is the basic outline of the database for the user inputs.

### Table of Sleep Database

| Date       | Duration | Quality | Location |
|------------|----------|---------|----------|
| 2022-04-17 | 9        | 8       | Bed      |

This is the basic outline of the database for the sleep inputs. 

# Test Plan

| Instruction              | Category     | Input                                                            | Expected Output                                                                      | Description                                                                          | Success Criteria |
|--------------------------|--------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|------------------|
| Test Registration Screen | Unit testing | An input in all 3 fields (email, username and password)          | All 3 attributes inside the database and the password being hashed and encrypted     | This will test if the registration works or not                                      | 1,3              |
| Test Login Screen        | Unit testing | An input of correct attributes (username, and password)          | A change in screen to the WelcomeScreen                                              | This will test if the Login system works or not                                      | 2                |
| Test Login Screen        | Unit testing | An input of the wrong attributes (username, and password)        | A text message that says "error"                                                     | This will test if the Login system works or not                                      | 2                |
| Test Main Screen         | Unit testing | Click all 3 buttons shown on the Main Screen                     | All 3 buttons result in their respective pages they are titles with                  | This will test if the MainScreen buttons functions or not                            | 4                |
| Test Insert Screen       | Unit testing | An input of all 4 fields (Date, Duration, Quality, and Location) | All 4 attributes should be in the database and a text output that says "successful!" | This will test if the InputScreen works and is able to communicate with the database | 5                |
| Test History Screen      | Unit testing | A click on the "History" button in the WelcomeScreen             | A table that shows the outputs of all the inputted data from before                  | This will test if the HistoryScreen works                                            | 6                |

## Record of Tasks
| Task NO | Planned Action                                                      | Planned Outcome                                                     | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------------|---------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Interview client (Koshiba Ryu) and record                           | A record of the interview (email)            | 30 minutes    | March 20th             | A         |
| 2       | Writing the Problem Definition in the repository                    | A clear problem definition in Github                                | 20 minutes    | March 20th             | A         |
| 3       | Writing the design statement in the repository                      | A clear design statement that suits the need of the client          | 20 minutes    | March 20th             | A         |
| 4       | Writing all the justification for programs and methods used         | A clear justification that suits the client and myself              | 30 minutes    | March 20th             | A         |
| 5       | Writing all 6 success criterias                                     | A clear success criteria that suits the client                      | 20 minutes    | March 20th             | A         |
| 6       | Cite all work used in Criteria A                                    | MLA format citing at the bottom of Criteria A                       | 10 minutes    | March 20th             | A         |
| 7       | Create system diagram of application                                | A clear and creative system diagram of the app                      | 20 minutes    | March 25th             | B         |
| 8       | Explain the system diagram                                          | A brief explanation about the system diagram                        | 10 minutes    | March 25th             | B         |
| 9       | Draw wireframe diagram of GUI                                       | A clear and creative wireframe diagram of the GUI                   | 20 minutes    | March 25th             | B         |
| 10      | Explain the wireframe diagram                                       | A brief explanation about the wireframe                             | 10 minutes    | March 25th             | B         |
| 11      | Code and create a working log in screen of the app                  | A working log in screen with python or kivyMD with a GUI            | 3 hours       | March 30th             | C         |
| 12      | Code and create a working registration screen of the app            | A working registration screen with python or kivyMD with a GUI      | 2 hours       | April 3rd              | C         |
| 13      | Draw 3 flow diagrams of 3 functions or classes from the application | A clear diagram of all 3 flow diagrams                              | 30 minutes    | April 5th              | B         |
| 14      | Explain all flow diagrams                                           | A brief explanation about all 3 flow diagrams                       | 20 minutes    | April 5th              | B         |
| 15      | Code and create a working menu screen of the app                    | A working menu screen with python or kivyMD with a GUI              | 2 hours       | April 10th             | C         |
| 16      | Ensure all databases are correct and connected with the application | A working and connected SQL database                                | 1 hour        | April 12th             | C         |
| 17      | Draw an ER diagram of the application                               | A clear ER diagram of the application                               | 10 minutes    | April 12               | B         |
| 18      | Explain the ER diagram                                              | A brief explanation about the ER diagram                            | 10 minutes    | April 12th             | B         |
| 19      | Draw the table of data of both databases                            | A table of the data represented in both databases                   | 10 minutes    | April 12th             | B         |
| 20      | Explain both table of datas                                         | A brief explanation about both table of datas                       | 10 minutes    | April 12th             | B         |
| 21      | Creating a test plan                                                | A clear test plan to ensure the functionality of the application    | 1 hour        | April 12th             | B         |
| 22      | Create sleep data insert page                                       | A working insert screen with python and kivyMD with a GUI           | 2 hours       | April 15th             | C         |
| 23      | Create sleep data history page                                      | A working history screen with python and kivyMD with a GUI          | 2 hours       | April 15th             | C         |
| 24      | Linking the table on the history page with the database             | A working table that show all data from the database as a GUI       | 1 hour        | April 15th             | C         |
| 25      | Testing all test plans                                              | All test plans successful and functional, debug if necessary        | 3 hours       | April 18th             | C         |
| 26      | Record video of all success criterias                               | Video evidence of all the success criterias functioning and working | 2 hours       | April 20th             | D         |

# Criteria C:
### Existing Tools:

- Python 3.x
- KivyMD
- Pycharm
- SQL Lite (database)

# KivyMD UI code:
### UI definition screen:
```.py

# Screen Setup

ScreenManager:
    id: scr_manager

    LoginScreen:
        name: "LoginScreen"

    MainScreen:
        name: "MainScreen"

    RegisterScreen:
        name: "RegisterScreen"

    InsertScreen:
        name: "InsertScreen"

    HistoryScreen:
        name: "HistoryScreen"
```

This kivyMD code is the backbone setup of the GUI. As I have 5 total screens in my application I have 5 screens registered in setup. As seen, each screen has its own unique name, which corresponds to its functionality in the application. 

This was the first stages of creating this application, and I honestly was still confused about the whole functionality of KivyMD. So I had to consult my peers and the internet (cited below) to educate myself on how to create the screen manager and gain understanding of how KivyMD works in general.

### General Screen Setup (background)
```.py

# Screen of the LoginScreen
<LoginScreen>
    FitImage:
        source: "background_img.jpg"
    MDCard:
        border_radius: 20
        radius: [15]
        size_hint: 0.5, 0.8
        elevation: 10
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        orientation: "vertical"
        md_bg_color:[1,1,1, 0.4]
```

The actual UI is constructed by putting all the elements of the GUI underneath the appropriately labelled GUI screen. In this example, the elements of this code are underneath the <LoginScreen> which means that this is the general layout of the login screen. This piece of code is in all 5 screens as it contains the background (FitImage) and the translucent square (MDCard) of the GUI.
    
Greating a general screen proved to be a relatively easy task. But there were some challenges regardless. For example, I had to insert a background image to the GUI, which I had to ask my peers on how to do it, and to make it visually more appealing, I have used rounded borders (border_radius) from the KivyMD website. 
  
### MDLabel

```.py
# Labels and text to guide the user
    MDLabel:
        text: "Login"
        font_style: 'H2'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.8}

    MDLabel:
        id: login_label
        text: "Please enter Username and Password"
        font_style: 'H6'
        halign: 'center'
        size_hint: 0.4,0.07
        pos_hint:{"center_x":0.5, "center_y":0.65}

    MDLabel:
        id: login_label
        text: ""
        theme_text_color: "Custom"
        text_color: 1, 0, 0, 1
        font_style: 'Caption'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.55}
```
These are all under the <LoginScreen> and represent the actual GUI of the login screen. For instance, MDLabel is used to create a text label so the user can understand what is happening. The text, size, alignment, colour and font style are all defined through obvious variables. 
    
Setting the text color was the most daunting task in this code. At first I didn't know what the 4 digits meant so I asked Dr. Ruben for help, which then he explained that the four digits mean red:green:blue:alpha, alpha being the opacity of the color. This helped me out greatly. 
    
### MDTextFieldRound
    
```.py
    # This is the text field where the user inputs its data through the keyboard
    # The text field is rounded for visual purposes.
    MDTextFieldRound:
        id: username
        pos_hint:{"center_x":0.5, "center_y":0.5}
        size_hint: 0.4,0.07
        icon_left: 'account-circle'
        hint_text: 'Username'
    MDTextFieldRound:
        id: password
        pos_hint:{"center_x":0.5, "center_y":0.4}
        size_hint: 0.4,0.07
        icon_left: 'key-variant'
        hint_text: 'Password'
        password: True
```
This piece of code shows the actual text fields the user can input with their keyboard. In this case, I am using an "MDTextFieldRound" which means it is a rounded text field for visual purposes. All definitions, position, size, icon, and hint text are defined through obvious variables. 
    
The biggest challenge I faced in creating a text field is connecting the python logic with the inputs from KivyMD. With the help of my teacher and the countless resources from the internet (cited below) I was able to use IDs to identify the different text boxes and create an input that python can read. 
    
### MDRaisedButton
    
```.py
    # Buttons that users can press to execute a set command
    MDRaisedButton:
        text: "Log in"
        pos_hint: {"center_x":0.5,"center_y":0.3}
        md_bg_color:app.theme_cls.primary_dark
        width:root.width*0.4
        size_hint: 0.25,0.075
        on_release:
            root.try_login()
    MDRaisedButton:
        text: "Register"
        pos_hint: {"center_x":0.5,"center_y":0.17}
        md_bg_color:app.theme_cls.primary_light
        width:root.width*0.4
        size_hint: 0.25,0.05
        on_release:
            root.parent.current = "RegisterScreen"
```
This code shows the buttons the users are able to press with their mouse. In this case, for visual purposes, I have chosen to use the "MDRaisedButton" which shows a button that is raised. All definitions, text, position, colour, and size are defined through obvious variables. The on_release function defines what the button actually does when clicked, and in this case, it either sends a python command (root.try_login()) or changes the screen to a different one (root.parent.current = "RegisterScreen"). 
    
Perhaps the biggest headache was the allignment and positioning of the buttons. As I have created boxes within boxes, it was a bit confusing trying to identify the X and Y axis of all the boxes and so I had a hard time visualizing where everything goes. To help solve this issue, I used my iPad to physically visualize what is happening in the screen (such as invisible boxes) and help understand the orientation of all the attributes. 
    
# Python Code: 
    
## Database Handler (Python to SQL)
    
### Create user database
```.py
def create(self):
    # This function will create the table for the users if it doesnt exist
    self.cursor.execute("""
                CREATE TABLE if not exists Users(
                id INTEGER primary key,
                username VARCHAR(200) not null unique,
                email VARCHAR(255) not null unique,
                password VARCHAR(256) not null
                );
                """)
        self.connection.commit()
```
This is the function that creates the database that holds all username, password and emails. It communicates with the SQL Database through the console and uses obvious variables to execute such commands. 
  
Creating a function that directly talks to SQL Lite was a pretty straightforward task as the SQL terminal uses english. However, something that I stumbled upon is the fact that the database kept on creating a new database with all the attributes. Later, by comparing my code with my peers and my teachers, I was missing "if not exists" in the code, which fixed the problem. 
    
### Query User:
```.py
def query_user(self,username):
    # This function will match the credientials of the input with the database Username
    self.username=username
    result = self.cursor.execute(f"select * from USERS where username='{username}';")
    return result.fetchone()
```
This is a function that matches the credentials with the inputted "username" with the databases list of "usernames". It would either return nothing (if no such users were found) or everything relating to that username (password and email). This is executed through Python and the SQL console. 
    
Finding a user from the database also required python to talk to the SQL database via console. With a good amount of knoweldge in the SQL console, this didn't really prove to be a hard task, although the return function was a bit confusing as it was returning everyone in the database, but regardless I was able to solve it by trial and error. 
    
### Query Password:
    
```.py  
def query_password(self,password):
    # This function will match the credientials of the input with the database Password
    self.password=password
    result = self.cursor.execute(f"select * from USERS where password='{password}';")
    return result.fetchone()
```
This is a function, similarly to query user, matches the credentials with the inputted "password" with the databases list of hashed "passwords". This function will return the password when it's entered correctly or nothing when inputted with the wrong one.
    
Finding and matching the password also required python to talk to the SQL database. Again, with a good amount of knoweldge with SQL, I didn't have much trouble understanding and coding this. Decrypting the passwords from the database was a challenge though, which I will explain later on. 
   
### Create New User into Database:
```.py
def create_new_user(self, email, username, password):
    # This function will create a new user that includes email, username and password
    self.cursor.execute("INSERT into Users values (?,?,?,?)",
                        (random.randint(1,1000000), username, email, encrypt_password(password)))
    self.connection.commit()
```
This is a function that adds a new user to the database. It holds 3 variables, Username, Password and Email and requires all 3 to be filled in. An ID is also created to uniquely identify the individual users and it will have a random integer between 1 and 1000000. This is executed through Python and the SQL console. 
    
Adding a new user to the database, again requried python to talk with SQL lite through console. However, this proved to be a challenging task as I have realized that throughout my own code, I have been using different variable names. So to fix this, I had to one line by one line change "user" to "username" and "pass" to "password" as it for some reason was different throughout the code, causing this piece of code to not work. At the end, I was able to fix it and the create new user function was able to work. Perhaps next time I could be more mindful with the variable names I use. 

## Class functions that relate to KivyMD screens IDs
    
### Login Logic
    
```.py
#This is the class that relates to the <LoginScreen> in Kivy
class LoginScreen(MDScreen):
    def try_login(self):
        # This function will verify if the entered username and password matches the credientials with the database
        username=self.ids.username.text
        password=self.ids.password.text
        db=my_database_handler("Project3.db")
        user_id=db.query_user(username=username)
        if user_id:
            id, username, email, hashed_password = user_id
            if verify_password(password=password, hashed=hashed_password):
                self.parent.current = "MainScreen"
                self.ids.login_label.text = ""
                self.ids.username.text = ""
                self.ids.password.text = ""
            else:
                self.ids.login_label.text = "Error: Wrong Password"
        else:
            self.ids.login_label.text = "Error: User Does Not Exist"
```
This is the python code behind the <LoginScreen> in KivyMD. KivyMD provides python with all the inputs through its unique ids (in this case username and password) and python is able to check the credibility of the inputs by communicating with the database through the query_user and query_password functions. If the username doesn't exist in the database, the KivyMD text will change to "Error: User does not exist" and if the password doesn't match with the username, the KivyMD text will change to "Error: Wrong Password". 
    
I had trouble when I had to match credientials with the input from KivyMD. I had to firstly utilize the functions that I have created (eg. verify_password) but what I was stuck on is how to deny logins for someone who inputted the wrong string. To fix this, I have utilized if statements, the first if to verify if the username entered is even in the database (if not it will print "Error: user does not exist") and a second if statement to verify if the password is correct, with the verify_password function. By splitting up the two checks with two if statements, I was able to verify each inputs with the databases credientials. 
    
### Registration Logic
    
```.py
class RegisterScreen(MDScreen):
    def register(self):
        email_entered = self.ids.email.text
        username_entered=self.ids.username.text
        password_entered=self.ids.password.text
        db=my_database_handler("Project3.db")
        db.create_new_user(username=username_entered,email=email_entered,password=password_entered)
        db.close()
        self.parent.current="LoginScreen"
        self.ids.email.text = ""
        self.ids.username.text = ""
        self.ids.password.text = ""
```
This is the python code behind the <RegisterScreen> in KivyMD. KivyMD provides python with all the inputs through its unique ids (in this case email, username and password) and python is responsible for communicating with the database and inputting all the data. Since there already are functions that help with inputting all the data into the database, I used the db.create_new_user function to input all the variables into its respectful columns in the database. 
    
A problem I faced when creating the register screen is identifying each id from kivy to its respectful variable names. I firstly had to understand what each variable meant, such as self, id, email, and text which proved to be a easy task as I just had to ask my teacher and peers for assistance. With this, I was able to smoothly work out the rest, and utilize the functions created before to input data to the database. 
    
###  Inserting Data into the Database (Python to SQL) 
    
```.py
# This is the python logic behind the InsertScreen
class InsertScreen(MDScreen):

    def on_save(self,instance, value, date_range):
        # This will identify which part of the textfield corresponds with which variable
        self.instance=instance
        self.value=value
        self.date_range=date_range
        self.ids.sleep_date.text = str(value)

    def input_sleep(self):
        # This is the part where the code bridges communcation between python and SQL
        sleep_date=self.ids.sleep_date.text
        sleep_duration=self.ids.sleep_duration.text
        sleep_quality=self.ids.sleep_quality.text
        sleep_location=self.ids.sleep_location.text
        db.create_new_entry(date=sleep_date, duration=sleep_duration, quality=sleep_quality,location=sleep_location)
        db.close()
        self.ids.input_text.text="Successful!"
```
This is the python code behind the <InsertScreen> in KivyMD. KivyMD provides python with all the inputs through its unique ids (in this case, date, duration, quality and location) and python is responsible for communicating with the database and inputting all the data into the database. Since there are already functions that help with all of this, I used the db.create_new_entry() function to create a new entry into the database. 
    
With all the undertandings of variables (id, self, text, etc) I was able to smoothly and logically workout what to do, utilizing all functions that I had created and creating one as well. All went well here. 
    
### History Screen Logic
```.py
class HistoryScreen(MDScreen):
    # This is a class attribute
    data_tables = None
    # This will get data from the database
    def on_pre_enter(self, *args):
        db=my_database_handler("Project3.db")
        query = db.query_sleep()
        db.close()

        self.data_tables = MDDataTable(
            use_pagination = True,
            size_hint = (0.9,0.6),
            pos_hint = {"center_x": 0.5, "top": 0.75},
            column_data = [("Date", 65), ("Duration / hrs", 65), ("Quality / 10", 65), ("location", 75)],
            row_data = query
        )
        self.add_widget(self.data_tables)
```
This is the python code behind the <HistoryScreen> in KivyMD. Unlike all the other codes, this one works in reverse and requires data input from the database itself. So this code uses the db.query_sleep() function which as explained earlier, queries the database with all the information within the "sleepdata" database. Other than that I used the built-in KivyMD MDDataTable to create the table itself, specifying the size, position column and row of the table.
    
The most confusing part of this was the creation of the data table. At first, I thought the table will be created using KivyMD, but I was wrong. By reseraching and asking my teacher, I came to the conclusion that the table has to be created on python. By looking at the KivyMD resources website, I was able to craft a table that looked half decent with all the columns and shown data in the table. Importing the data from the database was also a straightforward task as I just had to use the function that I have created earlier. 

## Ecryption and hashing functions:
    
### Hash setup
    
```.py
# This is the configuration of the hashing functions
pwd_context = CryptContext(
    schemes=["pbkdf2_sha256"],
    default = 'pbkdf2_sha256',
    pbkdf2_sha256__default_rounds=3000
)
```
This is the setup for the hashing and encryption of the passwords and inserted inputs. With the "from passlib.context import CryptContext" I was able to utilize the library to its fullest extent.
    
Perhaps this was the most confusing part of this project. I firstly had to understand what hashing and encrypting meant, which led me to a few videos on the internet and guidance from my teacher during class. I also had to understand how to create a hashing function within python, which my teacher explained step by step, which helped me tremendously. 
    
### Encrypting the password
    
```.py
def encrypt_password(password):
    # This will encrypt the password
    return pwd_context.hash(password)
```
This function encrypts the password from a standard string to a hashed string. This uses the "from passlib.context import CryptContext" library to encrypt it. 
    
This was pretty straight forward as I was using the library "CryptContxet" and was able to logically create a function to encrypt certain inputs with the .hash function. 
    
### Decrypting the password
    
```.py
# This function will convert the entered password to a hashed password and match it with the database
def verify_password(password, hashed):
    return pwd_context.verify(password, hashed)
```
This function will decrypt the passwords on the database and match it with the inputted password to see if it matches. This uses the "from passlib.context import CryptContext" library to decrypt the passwords from the database. 
    
I had trouble with this function as I didn't know how to compare the two inputs together. However, with consultance from the library website and my peers, I was able to logically figure out that I needed two attributes in the function, the entered password and the hashed password, and use the .verify function to verify if it matches or not.     
    
## Execute Command
    
```.py
class Project3(MDApp):
    def build(self):
        # This will define the color and palette of the application
        self.theme_cls.primary_palette = "BlueGray"
        self.theme_cls.theme_style = "Light"
        return

db=my_database_handler("Project3.db")
db.create()
db.createsleepdata()
# This will run the entire application and execute the commands
Project3().run()
``` 
This is the python code behind the execution of my application. A theme colour of "bluegray" and style of "light" have been specified in this function to give it colour and an overall theme for the application to follow. 
    
## ScreenShots
![](login.png)
Fig 8. The Login Screen <LoginScreen>
    
![](register.png)
Fig 9. The registration screen <RegistrationScreen>
    
![](welcome.png)
Fig 10. The welcome screen <WelcomeScreen>
    
![](insertion.png)
Fig 11. The data input screen <InsertScreen>
    
![](history.png)
Fig 12. The historical data screen <HistoryScreen>
    
## How will my software be updated in the future?
This application is a lifestyle application and unless broken, there will be no other reason to keep the older version of this application. As such, a self-updating, online method will make the most sense. Other updates methods such as manual updates are too tedious for the user and require too many steps for such apps. Therefore I think this software should be updated and pushed out online and should update automatically. As a benchmark, updates should occur at least once a month to make sure all bugs are patched and the user has the best experience with the application. 
    
## Sources Cited 
### Online resources used to consult and code my application
    
"BoxLayout — KivyMD 1.0.0.dev0 Documentation." Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation, kivymd.readthedocs.io/en/latest/components/boxlayout/.

"Button — KivyMD 1.0.0.dev0 Documentation." Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation, kivymd.readthedocs.io/en/latest/components/button/.

Codemy.com. "Using SQLite3 Database With Kivy - Python Kivy GUI Tutorial #55." YouTube, 10 Aug. 2021, www.youtube.com/watch?v=X2MkC1ru3cQ&ab_channel=Codemy.com.

Codemy. "KivyMD Pagination For Data Tables - Python Kivy GUI Tutorial #54." YouTube, 28 June 2021, www.youtube.com/watch?v=Wk31pSy1g6s&ab_channel=Codemy.com.

"Components — KivyMD 1.0.0.dev0 Documentation." Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation, kivymd.readthedocs.io/en/latest/components/.

"Slider — KivyMD 1.0.0.dev0 Documentation." Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation, kivymd.readthedocs.io/en/latest/components/slider/.

"Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation." Welcome to KivyMD’s Documentation! — KivyMD 1.0.0.dev0 Documentation, kivymd.readthedocs.io/en/latest/.
    
    
# Criteria D:
    
## A video demonstrating the testing for the success criteria.
    
https://www.youtube.com/watch?v=kkK07YnLI5c&ab_channel=ReijiNishikawa

## Side Notes:
    
Raw Python code: https://github.com/Raijeee/Unit3_Project_Reiji/blob/main/rawpython.md
    
Raw KivyMD Code: https://github.com/Raijeee/Unit3_Project_Reiji/blob/main/rawkivy.md
