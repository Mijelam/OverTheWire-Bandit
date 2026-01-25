## Level 15

### Instructions:
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

### Thought process:

The easiest way to do that is by using **ncat --ssl**. It's much better than using  **nc** because is encrypted.
With **nc,** anyone  sniffing  the network could read our messages, with **ncat**,  people can see data is sent, but it looks like **random noise**

![Bandit Game](screenshots/bandit0/bandit15-1.png)