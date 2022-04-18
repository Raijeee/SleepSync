```.py
import sqlite3
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen
import random
from passlib.context import CryptContext
from kivymd.uix.picker import MDDatePicker


# This is the conig of the hashing functions
pwd_context = CryptContext(
    schemes=["pbkdf2_sha256"],
    default = 'pbkdf2_sha256',
    pbkdf2_sha256__default_rounds=3000
)
# This function hashes the password
def encrypt_password(password):
    return pwd_context.hash(password)

# This function is to check if the entered password is correct and decrypts the password in the database
def verify_password(password, hashed):
    return pwd_context.verify(password, hashed)

class LoginScreen(MDScreen):
    def try_login(self):
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

class MainScreen(MDScreen):
    pass

class HistoryScreen(MDScreen):
    pass

class InsertScreen(MDScreen):

    def show_date_picker(self):
        date_dialog = MDDatePicker()
        date_dialog.bind(on_save=self.on_save)
        date_dialog.open()

    def on_save(self,instance, value, date_range):
        self.instance=instance
        self.value=value
        self.date_range=date_range
        self.ids.sleep_date.text = str(value)

    def input_sleep(self):
        sleep_date=self.ids.sleep_date.text
        sleep_duration=self.ids.sleep_duration.text
        sleep_quality=self.ids.sleep_quality.text
        sleep_location=self.ids.sleep_location.text
        db.create_new_entry(date=sleep_date, duration=sleep_duration, quality=sleep_quality,location=sleep_location)
        db.close()
        self.ids.input_text.text="Successful!"

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

class my_database_handler:
    def __init__(self,name):
        self.name=name
        self.connection=sqlite3.connect(self.name)
        self.cursor=self.connection.cursor()
    def close(self):
        self.connection.close

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

    def query_user(self,username):
        self.username=username
        result = self.cursor.execute(f"select * from USERS where username='{username}';")
        return result.fetchone()

    def query_password(self,password):
        self.password=password
        result = self.cursor.execute(f"select * from USERS where password='{password}';")
        return result.fetchone()

    def create_new_user(self, email, username, password):
        self.cursor.execute("INSERT into Users values (?,?,?,?)",
                            (random.randint(1,1000000), username, email, encrypt_password(password)))
        self.connection.commit()


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

    def create_new_entry(self, date, duration, quality,location):
        self.cursor.execute("INSERT into SleepData values (?,?,?,?)",
                            (date, duration, quality, location))
        self.connection.commit()

class Project3(MDApp):
    def build(self):
        self.theme_cls.primary_palette = "BlueGray"
        self.theme_cls.theme_style = "Light"
        return


db=my_database_handler("Project3.db")
db.create()
db.createsleepdata()
Project3().run()
```
