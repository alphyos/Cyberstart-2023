# 😕 Alien Server - L04 C05

So, it seems the aliens are using what looks like human technology and we've identified they're running a server. We need you to try and connect to the server and see what's going on.

Instructions:

- Connect to the localhost server on port 10000.
- Then send and receive the response, for each of these values:
- USER, aliensignal, PASS, unlockserver, SEND, moonbase, END
- Note: You must receive data back from the server after you send each value

**Tip:** Get access to the server using the above instructions to get the flag.

> 💡 Hint: You will need to use a TCP Socket on this one.
>
> It may be worth reviewing Level 3 Challenge 2.
>
> Don't forget to receive the responses that the server sends!

## Answer

```python
#
# Connect to alien server ('localhost', 10000)
#
# Then send each of these values...
# USER
# aliensignal
# PASS
# unlockserver
# SEND
# moonbase
# END
# ...and receive the response from each.
#
# Note: You must receive data back from the server after you send each value
#
import socket

messages = ["USER", "aliensignal", "PASS", "unlockserver", "SEND", "moonbase", "END"]

clientsocket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
clientsocket.connect(('localhost', 10000))

for message in messages:
  clientsocket.send(message.encode())
  print(clientsocket.recv(1024))
```
