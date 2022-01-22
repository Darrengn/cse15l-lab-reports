[Back](https://darrengn.github.io/cse15l-lab-reports/index.html)

# Lab Report 1

## Installing VScode<br>

Step 1: [download vs code here](https://code.visualstudio.com/) 

Step 2: Follow instructions on the installer 

Step 3: Open VScode. It should look similar to this window.

![Image](LabOnePics\Pic1.png)<br>

## Remotely Connecting<br>

Step 1: Find your cs15lwi22 account at [this link](https://sdacs.ucsd.edu/~icc/index.php) (cs15lwi22auh for example) 

Step 2: Open a new terminal in Vs code either by doing CTRL and ` or going to the top bar and clicking terminal

Step 3: run the command **ssh *YourAccountName*@ieng6.ucsd.edu** and enter your password. You should see a similar output when you connect.

![Image](LabOnePics\Pic2.png) <br>

## Test some terminal commands<br>

You are now connected to the ieng server. Try some basic terminal commands. **cd** (change directory) is shown below. [List of basic terminal commands](https://www.techrepublic.com/article/16-terminal-commands-every-user-should-know/). Run **exit** to log off of the remote server

![Image](LabOnePics\Pic3.png) <br>

## Moving files with scp<br>

Step 1: Use the command **scp *FileName* *YourAcountName*@ieng6.ucsd.edu:~/**

Step 2: ssh back into the ieng6 server.

Step 3: if you run **ls**, you should see your file below.

![Image](LabOnePics\Pic4.png)<br>

## Setting an SSH key <br>

Step 1: First, go to [this link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation) and follow the instructions up until Standard User.

Step 2: ssh into the server and run the command **mkdir .ssh** . Then log back out.

Step 3: Then run the command **scp C:\Users\username\.ssh\id_ed25519.pub *YourUserName*@ieng6.ucsd.edu *PathToSshKey*\.ssh\authorized_keys.pub** and enter your password. You can now ssh without enterying your password.

![Image](LabOnePics\Pic5.png)

## Optimizing remote running<br>
    
In your terminal, you can run multiple commands at once by seperating commands with a semi colon. In addition you can run commands on the server by using "" around the commands that you want to run on the server. For example, the command below compiles and runs WhereAmI on the server. To optimize this, you can use **scp WherAmI.java *YourUserName*@ieng6.ucsd.edu:~/** and then **ssh *YourUserName*@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI**. If you have run these commands before you can press the up arrow to get back to them. Pressing the up arrow twice to get back to each command and the enter button to run the commands makes the total keystrokes only 6.
    
![Image](LabOnePics\Pic6.png)