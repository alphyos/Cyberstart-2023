# 🍭 Secret Messages - L08 C09

Crikey, every time we think we're getting one step ahead of The Chiquitoos, they do something that proves how good they are.

It seems they now know we've been intercepting some of their messages, so they've started encoding them all. Our agents are looking at them now to try and figure it out. Why don't you take a look too and see if you can figure it out first. It probably won't harm your promotion prospects if you do!

**Tip:** Decode the message to get the flag.

<details><summary>

## Need a hint?</summary>

> 💡 Hint: The string is encoded using an unusual number base. The numbers 2 - 7 are represented and the letters A - Z are represented. What base is this?

</details>

<details><summary>

## Step by Step</summary>

- Encrypted message: `IZWGCZZ2EA4HUULFLF4UY4DXKVIWW3SYHBBXUSLIME======`
- The secret message is encoded in [Base32](https://www.dcode.fr/base-32-encoding) and the flag is the decoded string
![base32 decoded ascii output](/assets/secretmessage1.png)
- To get the correct flag do not include the last unknown charactres

</details>
