<!---
0mj/0mj is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
## Add a ssh key to github
### Don't I have a key?  
Check for existing keys..  
`ls -al ~/.ssh`


### Create your SSH key  
So you dont have a key.  Use the following steps to create one.
1. `ssh-keygen`  
2. Press enter when prompted with "Enter file in which to save the..."  
3. Press enter twice when prompted with "Enter passphrase"  
4. Set permissions on your keys   
`sudo chmod 600 ~/.ssh/id_rsa && sudo chmod 600 ~/.ssh/id_rsa.pub`  
5. Run `` `ssh-agent` `` (yes including backticks)  
6. eval `ssh-agent`  

### Add your key to the SSH keychain  
1. `ssh-add ~/.ssh/id_rsa`  
2. View your public key `cat ~/.ssh/id_rsa.pub`  
3. Copy your public key from above  
4. Add it to your github Account's SSH Keys section  
5. Verify that the key is setup properly `ssh -T git@githbub.com`  
6. Say "yes" when asked if you'd like to add to known hosts  
    You should see your username and some message about how shell access is disabled  
7. Exit and reopen terminal    
8. Run `ssh -T git@github.com` again just to ensure you can still connect to github after a restart

If you get an error about not having access when pushing a new repository try making one on github first ;) 
