# 📭 Alien Email - L07 C05

Breakthrough! We've discovered that the aliens have an insider back on Earth, and they've been contacting each other by... email?!

We've managed to get hold of an email between the insider and "Zultron", who we think might be the alien leader, with details about attack timings. We want to send another email with something different to try and confuse them.

Write a script that will connect to an SMTP server to send an email. Use the SMTP server at 127.0.0.1, port 1025, with a from address of bob-roswell-1947@ship-shape-security.com, sending to address zultron@cyberdarkart.com.

**Tip:** Send the email correctly to get the flag.

> 💡 Hint: Consider using the module smtplib on this one. There's no need to authenticate to the mail server.

## Answer

```python
#
# Send a spoofed email.  Use smtp server at '127.0.0.1', port 1025.
# Author needs to be bob-roswell-1947@gmail.com
# Recipient needs to be zultron@thebigeye.com
#

import smtplib


port = 1025 
server = "127.0.0.1"
sender = "bob-roswell-1947@gmail.com"
receiver = "zultron@thebigeye.com"
message = "meow"

try:
  smtpObj = smtplib.SMTP('127.0.0.1', 1025)
  smtpObj.sendmail(sender, receiver, message)
  print("Successfully sent email")
except SMTPException:
  print("Error: unable to send email")
```
