# 🧙‍♂️ Magic File - L07 C01

We've extracted one of the alien zip files. It's a bunch of PNG files, but we think only one of them is valid. Use magic bytes to determine which it is.

**Tip:** Find the correct file and print its contents to get the flag.

> 💡 Hint: Try printing out the first 8 bytes of every file in /tmp. Do you notice a pattern?  You just need to make it detect the PNG based on that pattern, then read the PNG file as if it was a text file.

## Answer

```python
import glob, os

magic_bytes = {'png': bytes ([0x89, 0x50, 0x4E, 0x47, 0x0D, 0x0A, 0x1A, 0x0A])}
max_size = max(len(m) for m in magic_bytes.values())
os.chdir("/tmp")
     
for x in glob.glob("*png"):
  with open(x, 'rb') as fd:
    file_head = fd.read()
    print(file_head)
```
