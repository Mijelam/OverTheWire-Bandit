## Level 13

### Instructions:

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level

### Thought process:

We just have to copy the ssh key from the server to our local machine

![Bandit Game](screenshots/bandit0/bandit13-1.png)

It is also important to change the permissions of the key by typing chmod 600(just read and write by owner, it's a ssh "protocol")