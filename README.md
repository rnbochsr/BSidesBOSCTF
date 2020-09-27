# BSidesBOS CTF Sept. 26, 2020

## Rules & Notes

1.  Please do not attack the competition infrastructure or other players. The challenges are your targets. That's it.
2.  You do not need to use automated scanners like sqlmap, DirBuster, nmap, Metasploit, nikto or others. Please do not use them against the challenges.
3.  Please do not brute-force flags.
4.  Please do not share flags with other players, or explicitly and deliberately cheat. 
5.  Please do not blatantly ask for hints. The proper to way to ask for help is to explain what you have tried and showcase(in a direct message) what errors or output you may have. 

Flag format: Flags for this competition will follow the format: flag{}, with words joined together with underscores inside the curly braces. If you look closely, you can even find a flag on this page!


## My Thoughts & Reflections
My final rank was 609 out of 1008. This was my first official CTF. I had something come up and was forced to miss the first 4 hours of the competition. While I was disappointed in only solving 2 challenges, I did find myself on the cusp of solving several others. Still, my rank put me in the middle third of competitors. I just wish that I had the other 4 hours. I am looking forward to my next competition. 


## The Challenges 

### Rules
View the rules page source to find the flag. 
```
flag{its_time_to_hack}
```


### Kiddie Pool
Presented with a distorted image. It is swirled around a central point. You have to unswirl the image to be able to read the flag. The challenge text says that the pubisher thinks the method is 900% cool. I guessed that you would have to reverse the swirl by -900%. That was correct. Use GIMP function Whirl and Pinch to undo the distortion. 
```
flag{whirlpool_in_a_cinch}
```


## Baseball
This was about cracking the base encoding. I downloaded the file. I then ran it thru `base64 -d` and it didn't yield anything useful. I tried to see if I had another base encoding. I ran `which base*` in the terminal and found a base32. I ran the text through `base32 -d` and it still didn't get the flag. 

While I knew that it had to do with the base decoding, I didn't consider running it through them in sequence. I also didn't explore what other base endings might be useful. In addition, I didn't think that I would need to run it through 3 "bases." The baseball reference couldn't have been more obvious. Yet, I didn't make the connection. 

The final answer would be obtained using `base64`, `base32`, and finally `base58`. As I was unaware of base 58, I would have required more time to find and try other options. 


### Y2K
> They told us the world was going to end in the year 2000! But it didn't... when do *YOU* think the world will end?
 
Connect to the server using: `nc challenge.ctf.games 31754`. 
malc wrote that you input this as the year. 
```
open('/home/challenge/flag.txt').read()
```
flag{we_are_saved_from_py2_k}

But why does it work, and how would I even get close to guessing this method??
