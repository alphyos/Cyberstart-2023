# 💭 Hidden Messages - L07 C04

One of the agents has intercepted a file from the aliens that we're worried about - it's called destroymoonbase.gif, so we really need to see what it is! Unfortunately we're struggling to make any sense of. It could be because it contains lots of symbols.

Write a script that will read the file, it's at /tmp/destroymoonbase.gif, then strip out all the characters that are not letters or numbers.

**Tip:** Print the correctly stripped file to get the flag.

> 💡 Hint: You'll need to read the file and remove any characters that are not letters or numbers, then print out the remaining characters.  There's a few ways you could accomplish this - perhaps Regex or using ASCII character values.

## Answer

```python
import re

ch1 = open("/tmp/destroymoonbase.gif", "r+")
ch2 = ch1.read()
line = re.sub('[$, #]', '', ch2)
print(line)
```
