# BSidesBOS CTF

## Rules & Notes

1.  Please do not attack the competition infrastructure or other players. The challenges are your targets. That's it.
2.  You do not need to use automated scanners like sqlmap, DirBuster, nmap, Metasploit, nikto or others. Please do not use them against the challenges.
3.  Please do not brute-force flags.
4.  Please do not share flags with other players, or explicitly and deliberately cheat. 
5.  Please do not blatantly ask for hints. The proper to way to ask for help is to explain what you have tried and showcase(in a direct message) what errors or output you may have. 

Flag format: Flags for this competition will follow the format: flag{}, with words joined together with underscores inside the curly braces. If you look closely, you can even find a flag on this page!


## My final rank 609 out of 1008.
This was my first official CTF. While I was disappointed in only solving 2 challenges, I found myself on the cusp of solving several others. Still, my rank put me in the middle third of competitors.


### Rules
View the rules page source to find the flag. 
```
flag{its_time_to_hack}
```


### Kiddie Pool
Presented with a distorted image. It is swirled around a central point. You have to unswirl the image to be able to read te flag. Use GIMP function Whirl and Pinch to undo the distortion. 
```
flag{whirlpool_in_a_cinch}
```


### Y2K
> They told us the world was going to end in the year 2000! But it didn't... when do *YOU* think the world will end?
 

nc challenge.ctf.games 31754
malc wrote that you input this as the year. 
open('/home/challenge/flag.txt').read()
flag{we_are_saved_from_py2_k}

But why does it work, and how would I even get close to guessing this method??
