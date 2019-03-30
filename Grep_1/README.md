# Grep 1

Problem description:
```
Can you find the flag in file? This would be really obnoxious to look through by hand, see if you can find a faster way. You can also find the file in /problems/grep-1_2_ee2b29d2f2b29c65db957609a3543418 on the shell server.
```

For this problem we are given a simple file called "file". This includes a bunch of nonsense text with the flag somewhere in there.

There are multiple ways to do this, one could simply open up the file with a text editor and look around for the flag, but this would be very tiresome and possibly time consuming.

So an easier way is to simply use the bash command grep, as the title of the problem suggests.

The following command should be sufficent
```bash
grep "pico" file
```
or
```
cat file | grep pico
```

both returns the flag
```
picoCTF{grep_and_you_will_find_42783683}
```


