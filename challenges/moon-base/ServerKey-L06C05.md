# 🔑 Server Key - L06 C05

Ok, the excellent team on the next level have identified another alien server on a second alien probe ship that's headed to the moon, but it's protected in a more sophisticated way than the other. We need you to write a Python script which downloads a key, reverses it and then sends it back. Note that the key changes based on a timer.

Instructions:

- Send server ("localhost", 10000) GET_KEY to retrieve the key.
- Reverse the key and send it back.

**Tip:** Successfully send back the key in time to get the flag.

> 💡 Hint: Reversing a string in Python is really easy, but it can look quite scary.  Look it up online, try searching "Python Reverse String"

## Answer

```python
import socket

host = "localhost"
port = 10000

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
  s.connect((host, port))
  s.send(b"GET_KEY")
  data = s.recv(1014)
  data = str(data).strip('b').strip('\'')
  print(data)
  data = data[::-1]
  print(data)
  s.send(bytes(data, "utf-8"))
  data = s.recv(1024)
  s.close()
  
print(data)
```
