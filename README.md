# create-email-address-menu
HOW TO CREATE EMAIL ADDRESS MENU

CODE
import tkinter as tk
from tkinter import ttk
from tkinter.messagebox import showinfo

# root window
root = tk.Tk()
root.geometry("300x150")
root.resizable(False, False)
root.title('Sign In')

# store email address and password
email = tk.StringVar()
password = tk.StringVar()


def login_clicked():
    """ callback when the login button clicked
    """
    msg = f'You entered email: {email.get()} and password: {password.get()}'
    showinfo(
        title='Information',
        message=msg
    )


# Sign in frame
signin = ttk.Frame(root)
signin.pack(padx=10, pady=10, fill='x', expand=True)


# email
email_label = ttk.Label(signin, text="Email Address:")
email_label.pack(fill='x', expand=True)

email_entry = ttk.Entry(signin, textvariable=email)
email_entry.pack(fill='x', expand=True)
email_entry.focus()

# password
password_label = ttk.Label(signin, text="Password:")
password_label.pack(fill='x', expand=True)

password_entry = ttk.Entry(signin, textvariable=password, show="*")
password_entry.pack(fill='x', expand=True)

# login button
login_button = ttk.Button(signin, text="Login", command=login_clicked)
login_button.pack(fill='x', expand=True, pady=10)


root.mainloop()

END().............................................

#TITLE (DESTROY EMAIL ENTER AND LABEL, PASSWORD ENTRY AND LABEL)

CODE

import tkinter as tk
from tkinter import ttk
from tkinter.messagebox import showinfo
# LOG IN
def log_in():
    mesg=f" your gmail address is :[ {enterEmail.get()}] and your password is : [" \
         f"{enterpassword.get()}]"
    showinfo(title='information of a person gmail',message=mesg)
# DESTROY
def cancel():
    #des = emaillabel.destroy()
    mesg=f"you have been cancelled your [ email  label] {emaillabel.destroy()} your" \
         f" destroy [ enter email entery ] {enterEmail.destroy()}" \
         f"cancelled [ your password  label ] {passwordlabel.destroy()} your" \
         f" destroy [ enter password entery ] {enterpassword.destroy()} "
    showinfo(title="destroy email label",message=mesg)

window= tk.Tk()

window.geometry("350x200")
window.resizable(False,False)
window.title('log in ')

email=tk.StringVar()
password=tk.StringVar()

login=ttk.Frame(window)
login.pack(padx=10,pady=10,fill='x',expand=True)


emaillabel=ttk.Label(login,text='enter your email address')
emaillabel.pack(fill='x',expand=True)

enterEmail=ttk.Entry(login,textvariable=email)
enterEmail.pack(fill='x',expand=True)
enterEmail.focus()

passwordlabel=ttk.Label(login,text='enter password')
passwordlabel.pack(fill='x',expand=True)

enterpassword=ttk.Entry(login,textvariable=password,show="*")
enterpassword.pack(fill='x',expand=True)
enterpassword.focus()

loginbutton=ttk.Button(login,text='login',command=log_in)
loginbutton.pack(fill='x',expand=True,pady=12)

cancelbutton=ttk.Button(login,text='cancel',command=cancel)
cancelbutton.pack(fill='x',expand=True,pady=5)

window.mainloop()


END().............................................
