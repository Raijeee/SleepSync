```.py
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

    MDRaisedButton:
        text: "Log in"
        pos_hint: {"center_x":0.5,"center_y":0.3}
        md_bg_color:app.theme_cls.primary_dark
        width:root.width*0.4
        size_hint: 0.25,0.075
        on_release:
            root.try_login()
    MDLabel:
        text: "Not registered yet?"
        font_style:'Subtitle1'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.22}
    MDRaisedButton:
        text: "Register"
        pos_hint: {"center_x":0.5,"center_y":0.17}
        md_bg_color:app.theme_cls.primary_light
        width:root.width*0.4
        size_hint: 0.25,0.05
        on_release:
            root.parent.current = "RegisterScreen"

<RegisterScreen>

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

    MDLabel:
        text: "Registration"
        font_style: 'H3'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.8}

    MDLabel:
        text: "Please enter Email, Username and Password"
        font_style: 'H6'
        halign: 'center'
        size_hint: 0.4,0.07
        pos_hint:{"center_x":0.5, "center_y":0.67}

    MDTextFieldRound:
        id: email
        pos_hint:{"center_x":0.5, "center_y":0.55}
        size_hint: 0.4,0.07
        icon_left: 'mail'
        hint_text: 'Email'

    MDTextFieldRound:
        id: username
        pos_hint:{"center_x":0.5, "center_y":0.45}
        size_hint: 0.4,0.07
        icon_left: 'account-circle'
        hint_text: 'Username'

    MDTextFieldRound:
        id: password
        pos_hint:{"center_x":0.5, "center_y":0.35}
        size_hint: 0.4,0.07
        icon_left: 'key-variant'
        hint_text: 'Password'
        password: True

    MDRaisedButton:
        text: "Register"
        pos_hint: {"center_x":0.5,"center_y":0.2}
        md_bg_color:app.theme_cls.primary_light
        width:root.width*0.4
        size_hint: 0.25,0.075
        on_release:
            root.register()

<MainScreen>
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

    MDLabel:
        text: "Welcome"
        font_style:'H2'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.8}

    MDLabel:
        text: "Sleep Tracker App"
        font_style:'H4'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.7}
    MDIcon:
        icon: "sleep"
        halign: 'center'
        pos_hint: {"center_x": 0.5, "center_y": 0.58}
        size_hint: 1,1
    MDIcon:
        icon: "bed"
        halign: 'center'
        pos_hint: {"center_x": 0.5, "center_y": 0.55}
        size_hint: 1,1

    MDRaisedButton:
        text: "Add Sleep Data"
        pos_hint: {"center_x":0.5,"center_y":0.45}
        md_bg_color:app.theme_cls.primary_light
        width:root.width*0.4
        size_hint: None,None
        on_release:
            root.parent.current = "InsertScreen"
    MDRaisedButton:
        text: "History"
        pos_hint: {"center_x":0.5,"center_y":0.35}
        md_bg_color:app.theme_cls.primary_light
        width:root.width*0.4
        size_hint: None,None
        on_release:
            root.parent.current = "HistoryScreen"
    MDRaisedButton:
        text: "Log Out"
        pos_hint: {"center_x":0.5,"center_y":0.2}
        md_bg_color:app.theme_cls.primary_dark
        width:root.width*0.4
        size_hint: None,None
        on_release:
            root.parent.current = "LoginScreen"

<HistoryScreen>

    FitImage:
        source: "background_img.jpg"

    MDCard:
        border_radius: 20
        radius: [15]
        size_hint: 0.95, 0.95
        elevation: 10
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        orientation: "vertical"
        md_bg_color:[1,1,1, 0.4]

    MDLabel:
        text: "History"
        font_style:'H2'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.85}

    MDBoxLayout:
        orientation: "horizontal"
        size_hint: 0.8,0.08
        pos_hint:{"center_x":0.5, "top": 0.2}

    MDRaisedButton:
        text: "Back"
        pos_hint: {"center_x":0.2,"center_y":0.09}
        md_bg_color:app.theme_cls.primary_dark
        width:root.width*0.4
        size_hint: 0.2,0.08
        on_release:
            root.parent.current = "MainScreen"

    MDRaisedButton:
        text: "Insert"
        pos_hint: {"center_x":0.8,"center_y":0.09}
        md_bg_color:app.theme_cls.primary_dark
        width:root.width*0.4
        size_hint: 0.2,0.08
        on_release:
            root.parent.current = "InsertScreen"

<InsertScreen>
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

    MDLabel:
        text: "Add Sleep Data"
        font_style:'H3'
        halign: 'center'
        pos_hint:{"center_x":0.5, "center_y":0.8}

    MDFillRoundFlatIconButton:
        icon: "clock"
        id: sleep_date
        text: "Select Date of Entry"
        pos_hint: {"center_x":0.5,"center_y":0.65}
        size_hint: 0.45,0.07
        on_release:
            root.show_date_picker()

    MDTextFieldRound:
        id: sleep_duration
        pos_hint:{"center_x":0.5, "center_y":0.55}
        size_hint: 0.4,0.07
        hint_text: 'Duration of sleep / Hours'
        icon_left: 'sleep'

    MDCard:
        border_radius: 20
        radius: [15]
        size_hint: 0.45, 0.14
        elevation: 10
        pos_hint: {"center_x": 0.5, "center_y": 0.43}
        orientation: "vertical"
        md_bg_color:[1,1,1, 0.4]

        MDIcon:
            icon: "bed"
            pos_hint: {"center_x": 0.55, "center_y": 0.6}
            size_hint: 1,1

    MDLabel:
        text: "Quality of Sleep"
        font_style:'Subtitle1'
        halign: 'center'
        pos_hint:{"center_x":0.414, "center_y":0.43}

    MDSlider:
        id: sleep_quality
        min: 0
        max: 10
        value: 5
        humb_color_down: app.theme_cls.accent_color
        pos_hint:{"center_x":0.5, "center_y":0.4}
        size_hint: 0.4,0.07
        text: sleep_quality.value
        step:1
        icon_left: 'bed'

    MDLabel:
        text: "0"
        font_style:'Subtitle1'
        halign: 'center'
        pos_hint:{"center_x":0.3, "center_y":0.4}

    MDLabel:
        text: "10"
        font_style:'Subtitle1'
        halign: 'center'
        pos_hint:{"center_x":0.7, "center_y":0.4}

    MDTextFieldRound:
        id: sleep_location
        pos_hint:{"center_x":0.5, "center_y":0.3}
        size_hint: 0.4,0.07
        hint_text: 'Location of sleep'
        icon_left: 'android-studio'

    MDRaisedButton:
        text: "Input"
        pos_hint: {"center_x":0.62,"center_y":0.17}
        md_bg_color:app.theme_cls.primary_dark
        size_hint: 0.2,0.07
        on_release:
            root.input_sleep()
    MDLabel:
        id: input_text
        text: ""
        font_style:'Subtitle1'
        halign: 'center'
        pos_hint:{"center_x":0.62, "center_y":0.23}

    MDRaisedButton:
        text: "Back"
        pos_hint: {"center_x":0.35,"center_y":0.17}
        md_bg_color:app.theme_cls.primary_dark
        size_hint: 0.15,0.07
        on_release:
            root.parent.current = "MainScreen"
```
            
