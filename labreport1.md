# Lab Report 1
## STEP 1: Installing VScode
- First, you will need to download VScode at <https://code.visualstudio.com/> and follow the instructions.
- When it is installed, go to VScode and open a new window which should look something similar to this: 
![Image](VScode.png)
- You now have access to VS code!

## STEP 2: Remotely Connecting
- Next, in order to connect to a remote server, you will need to install git. Follow the instructions on <https://git-scm.com/downloads> to download git.
- Next, open a terminal in VScode by pressing on the 'Terminal' dropdown in the menu and then pressing 'New Terminal' just like this:
![Image](OpeningTerminal.png)
- Once you have opened a new terminal, you should get something similar to this:
![Image](Terminal1.png)
- After the $ character in the terminal, type in
  > **ssh cse15lsp23zz@ieng6.ucsd.edu**
- The **"zz"** that you notice should be replaced with the letters in your specific course account. If this is your first time loging in, your terminal might look something similar to this
  > **The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established.\
  > RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.\
  > Are you sure you want to continue connecting (yes/no/[fingerprint])?**
- Type 'yes' and hit enter. Then your terminal should now ask for a password which is the password for your specific course account. Once you enter your password, your terminal should now look something similar to this:
![Image](Terminal.png)
- You are now connected to a remote server!

## STEP 3: Trying Some Commands
- Next, after you have connected to a remote server, you can try running some commands using the terminal which should now look something like this:
![Image](RemoteServer1.png)
- After the $, try typing in some of these commands and view the output of the terminal:
  - cd ~
  - cd
  - ls -lat
  - ls -a
  - cat /home/linux/ieng6/cs15lsp23/public/hello.txt
- Your terminal should now have different outputs depending on the command that you ran.
  - Example of using ls -lat:
  ![Image](Command.png)
- Now, to log out of the remote server, you can type in 'exit' in the command on your terminal and you should now be logged out.
