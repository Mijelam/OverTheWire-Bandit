## Level 18

### Instructions:

There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**


### Thought process:

The first thing i tried was this:

![Bandit Game](screenshots/bandit0/bandit18-1.png)

Since I had already experimented with `scp` in previous levels to quickly transfer passwords to my local machine, I noticed a key detail, when using `scp`, the remote shell doesn't seem to fully 'initialize' it just executes the transfer and exits.

The **'Bye Bye'** message was  triggered by the `.bashrc` file, which only runs during an **interactive login**. My curiosity led me to think: **'If `scp` can bypass the username prompt and environment loading, it probably bypasses the `.bashrc` as well.'** That’s when it clicked by using a non-interactive method, I could grab the password before the logout script ever had a chance to execute.

But there are easier ways to do it, i found this when i was trying to learn more about this stuff
`ssh -p 2220 bandit18@bandit.labs.overthewire.org 'cat readme'`
