Problem Description:
```
Can you find the flag in this file without actually running it? You can also find the file in /problems/strings_4_40d221755b4a0b134c2a7a2e825ef95f on the shell server
```

We are given an ELF file which is an executable file, lets try to run it even though the descriptions tells us not to.
```
chmod +x strings
./strings
$ Have you ever used the 'strings' function? Check out the man pages!
```

Well that didnt give us much, so lets just do what we're told for once, and use the strings function on the file. This will print out all the identified strings in the program, even the ones not called in the actual program.

```
strings strings
```

suprised that actually worked, but nonetheless, this spits out a ton of information, and instead of manually sorting through the output, lets grep it.

```
strings strings | grep pico
```

And now we got the flag all nice

```
picoCTF{sTrIngS_sAVeS_Time_d3ffa29c}
```

