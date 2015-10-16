
# Desktop shortcuts to virtualenvs

It is recommended to use virtual environments to separate out environments.  Working with several virtualenvs can be a pain so I recommend setting up shortcuts on your Windows Desktop.

1. Copy any desktop shortcut and paste it direct on to the desktop.
2. Right click on it and select Properties.
3. On the shortcut tab change the Target setting to:
    `%windir%\system32\cmd.exe /k "U:\Data\fiber\Scripts\activate" # POINT TO THE VIRTUALENV OF YOUR CHOOSING!`
4. Then chnage the Start in setting to point at where you would like the shortcut to take you.  In my case to my django project root where my manage.py file is e.g.
    `U:\Data\fiber\my_proj`
5. Now select the General tab and put a suitable title in the box.
6. Click ok.


This should create a desktop shortcut that has a command prompt icon but has a name you will recognise.  Double click on it and it will activate your environment and take you to the desired location.

