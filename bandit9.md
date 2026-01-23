## Level 9

### Instructions:

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

### Thought process:

The given instructions say **"several '=' "** so I tried two.

It was very clear I had to use **grep** to filter, but this happened:

![Bandit Game](screenshots/bandit0/bandit9-1.png)

It was a Binary file and **grep** doesn't work in  that kind of files, so I had to use **strings,** which only show us the printable characters and only then I could use **grep**

![Bandit Game](screenshots/bandit0/bandit9-2.png)