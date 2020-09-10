[https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent)



generating a new SSH key
```
ssh-keygen -t rsa -b 4096 -C "514292663@qq.com"

passphrase: my common passphrase
```




### Adding your SSH key to the ssh-agent
Start the ssh-agent in the background.
> it's weird there is no guide for "linux", so every time i have to reenter passphrase!!! but why?
the reason is  I forgot to execute the following line of code 
```
eval "$(ssh-agent -s)"
```
Add your SSH private key to the ssh-agent. 
```
ssh-add ~/.ssh/id_rsa
```
Add the SSH key to your GitHub account.



testing your ssh connection
[https://docs.github.com/en/github/authenticating-to-github/testing-your-ssh-connection#](https://docs.github.com/en/github/authenticating-to-github/testing-your-ssh-connection#)



Working with SSH key passphrases
[https://docs.github.com/en/github/authenticating-to-github/working-with-ssh-key-passphrases#](https://docs.github.com/en/github/authenticating-to-github/working-with-ssh-key-passphrases#)



how to avoid to reenter passphrase?
[Auto-launching ssh-agent on Git for Windows](https://docs.github.com/en/github/authenticating-to-github/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)
> **~** refers to **C:\Users\Administrator**,
create the file manually!
 **~/.profile** doesn't work,
**~/.bashrc** this works.
