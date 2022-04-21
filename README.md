# Unit 3: Project Client

# Criteria A: Planning

## Problem definition
My Roommate, Ryu Koshiba has recently been sleep deprived and wants to understand his sleep pattern throughout the month to prepare himself for his final exams coming up. To do this, Ryu wants an app developer to create an app that tracks his duration of sleep, date of sleep, quality of sleep, and location of sleep to best understand his sleep pattern. He wants an app that has a GUI and has accessible buttons and text boxes so he can input data in a straightforward matter.

- The client is recently sleep deprived
- The client requires an app that can record and track his sleep duration, date, quality and location.
- The client requires an app that has a GUI

## Proposed Solution:

### Design Statement
I will design and make an app that tracks the date, duration, quality (out of 10), and location of sleep for my client who is my roommate, Ryu Koshiba. The application will be able to keep track of all sleep stats via the use of a login system. To ensure security and privacy, the login system will have a hashing system to secure everyones password and will all be saved in a local database using SQLite. The application will have a GUI so that users can easily guide themselves throughout the app with mouse clicks. This all will be created using the Python 3.x language with the help of KivyMD for GUI construction. All code will be created and developed on the application, Pycharm. This app will take 4 weeks to complete and will be evaluated according to the criteria. 

## Justification

### Why Python?
Out of every programming language, I have chosen to use Python 3.x for numerous reasons. For starters, Python is the most well known and used programming language throughout the world (1). This will not only allow me to have greater access to resources and references but also the app will also be compatible with a greater number of systems, improving the overall experience of the client. Personally I am the most comfortable with programming Python and so not only will everything be streamlined but also the client will receive the app in a timely manner, without any extensions of the due date. Judging by the benefits of both the programmer and client, its safe to say that Python is the right programming language to use for this project. 

### Why KivyMD?
KivyMD will be used to construct the graphical user interface (GUI) for the user to navigate throughout the app. I have chosen KivyMD because not only is KivyMD compatible throughout all 3 main operating systems, but also is one of the more simpler GUI libraries to learn (2). KivyMD’s goal, “to approximate Google's Material Design spec as close as possible without sacrificing ease of use or application performance.” (3) also greatly relates to the clients experience as the GUI is what the client actually sees and a good GUI is always appreciated in every application. KivyMD is also the library I am the most familiar with and will help me as a developer to finish my project on time. Through these reasons, I have come to the conclusion that KivyMD is the most appropriate GUI node for my project. 

### Why SQLite?
SQLite is a database engine written in the C language(4) but also comes bundled with Python and can be used in any Python applications without having to install any additional software (5). I am also most familiar with this database structure and console which will allow me to create the database quickly and will match the client's deadline more effectively. With this flexibility and ease of use, I have decided to use SQLite for this project's database. 

### Why is the output through a GUI?
The application will have an output of a GUI rather than text. This is to meet the requirement of the client where he requires an application that can not only record and show his sleep data, but do all that through a GUI for ease of use. Due to the clients requirements, I have decided that the output should be through a GUI. 


## Success Criteria

1. The application must have a registration system where the users can register their email, username and password.
2. The application must have a working log in system, where all the credentials entered have to match with the database (registered data).
3. The application must encrypt the users password in the local SQL database.
4. The application must have a home screen that gives the option to log sleep data, view past data or logout. 
5. The user must be able to input all 4 attributes (date, duration, quality and location) into the database via the GUI.
6. The application must be able to show past inputs of all 4 attributes (date, duration, quality and location) from the database via the GUI.
7. The application must contain a log in screen, registration screen, home screen, screen to enter sleep data and screen to view the sleep data; in total 5 unique screens. 

### Client Approval
To check if the client approves my planning and the success critierias, I have decided to email him to verify with him.

![](client2.png)

Now that we have the success criterias verified, we can move on to the coding.
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

This Wireframe Diagram shows the generate outline of the GUI of the application. It shows the functionalities of every button planned out to be used in the application and shows all 5 screens of the application. 

## Flow Diagrams

![](flowchart1.png)
### Fig3. Registration Screen Flow Diagram

This is the flowchart of when the user registers their Email, Username, and Password. 

![](flowchart2.png)
### Fig4. Login Screen Flow Diagram

This is a flowchart showing how the login screen functions. It shows how the log in screen matches all the text inputs with the creditentials in the database.

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

Caption

### Table of Sleep Database

| Date       | Duration | Quality | Location |
|------------|----------|---------|----------|
| 2022-04-17 | 9        | 8       | Bed      |

Caption

# Test Plan

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

This kivyMD code is the backbone setup of the GUI. As I have 5 total screens in my application I have 5 screens registered in setup. As seen, each screen has its own unique name, which corespond to their functionality in the application. 

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

The actual UI is constructed by putting all the elemnts of the GUI underneath the appropriately lablled GUI screen. In this example, the elements of this code is underneath the <LoginScreen> which means that this is the general layout of the login screen. This piece of code is in all 5 screens as it contains the background (FitImage) and the translucent square (MDCard) of the GUI.
  
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
These are all under the <LoginScreen> and reprent the actual GUI of the login screen. For instance, MDLabel is used to create a text label so the user can understand what is happening. The text, size, allignment, color and font style is all defined through obvious variables. 
    
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
This piece of code shows the actual text fields the user can input with their keyboard. In this case, I am using a "MDTextFieldRound" which means it is a rounded text field for visual purposes. All definitions, position, size, icon, and hint text are defined through obvious variables. 
    
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
This code shows the buttons the users are able to press with their mouse. In this case, for visual purposes I have chosen to use the "MDRaisedButton" which show a button that is raised. All definitions, text, position, color, and size are defined throguh obvious variables. The on_release function defines what the button actually does when clicked, and in this case it either sends a python command (root.try_login()) or changes the screen to a different one (root.parent.current = "RegisterScreen"). 
    
# Python Code: 
    
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
Caption
    
## Database Handler (Python to SQL)
    
### Create user database
```.py
def create(self):
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
    
### Query User:
```.py
def query_user(self,username):
    self.username=username
    result = self.cursor.execute(f"select * from USERS where username='{username}';")
    return result.fetchone()
```
    
### Create New User into Database:
```.py
def createsleepdata(self):
    self.cursor.execute("""
            CREATE TABLE if not exists SleepData(
            date VARCHAR(256) not null,
            duration VARCHAR(256) not null,
            quality VARCHAR(256) not null,
            location VARCHAR(256) not null
            );
            """)
    self.connection.commit()
```
    
## Execute Command
    
```.py
class Project3(MDApp):
def build(self):
    self.theme_cls.primary_palette = "BlueGray"
    self.theme_cls.theme_style = "Light"
    return
```
    
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
    
How to update software
