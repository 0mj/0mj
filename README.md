- 👋 Hi, I’m @0mj ( Matt Jamison )
- 👀 I’m interested in ...
- 🌱 I’m currently learning Ruby, Ruby on Rails & TDD with RSpec
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
0mj/0mj is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Repository Access
Add a ssh key to github using the following steps. 

Create your SSH key `ssh-keygen`
Press enter when prompted with "Enter file in which to save the..."
Press enter twice when prompted with "Enter passphrase"
Set permissions on your keys `sudo chmod 600 ~/.ssh/id_rsa && sudo chmod 600 ~/.ssh/id_rsa.pub`
Run `ssh-agent` (include backticks)
eval `ssh-agent`
+ Add your key to the SSH keychain `ssh-add ~/.ssh/id_rsa` + View your public key `cat ~/.ssh/id_rsa.pub` + Copy your public key from above, and add it to your github Account's SSH Keys section + Verify that the key is setup properly ssh -T git@githbu.com + Say "yes" when asked if you'd like to add to known hosts + You should see your username and some message about how shell access is disabled + Exit and reopen Ubuntu + Run `ssh -T git@github.com` again just to ensure you can still connect to github after a restart

If you get an error about not having access when pushing a new repository try making one on github first ;) 
