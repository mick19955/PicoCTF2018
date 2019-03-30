Problem Description:
```
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell.picoctf.com 40157. Files can be found here: passwd shadow.
```
Connecting to the service with netcat prompts us for a username and a password, which we dont know yet.

Luckily we are given the two files, passwd and shadow. These two files are used in most (if not all?) linux systems to identify users (passwd) and store a hashed version of a users password (shadow).

Opening up the file passwd with your favorite text editor you can see the users on the system, in this case there is just the user 'root'. So that must be our username.

To get the password we will use the file 'shadow'. Unfortunately for us the password is hashed, and getting to know the real password will require for us to bruteforce it. You could try to crack the hash with an online cracker or use the program john (short for john the ripper)

I used the program john in combination with the wordlist rockyou

```
john --wordlist=rockyou.txt shadow
```
This yielded the very secure password 'password1'. (This password changes from pico user to pico user)

So connecting to the service with netcat once again, and logging in with the credentials found, gives us the flag.

```
picoCTF{J0hn_1$_R1pp3d_289677b5}
```


