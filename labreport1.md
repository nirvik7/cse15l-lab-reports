__Lab 1 Report__

Here is the step-by-step process I took to log into my course-specific account on ieng6. Although these steps might not work perfectly for you, it should help to guide you through your own process.


*Installing VS Code:*

This part was easy for me as I didn't have to do anything! I already had VS Code so I moved on to the next step. If you do not have VS Code, here is the link to their website: ```https://code.visualstudio.com/```

![Inside of VS Code](https://lh3.googleusercontent.com/drive-viewer/AAOQEOSDricR4PKd8NCAYMRW7JY6iUn9Rj60EhgfnJPMjn5TtNS_Wr_IDa5KlMv-7NeiyK9gDITywAV9yzwIges9kJULQhrm=w1920-h853)

*Remotely Connecting*

Unfortunately, my account did not work for some reason so I had to log in with a TA account. In this step, you first open up a terminal and type "ssh" with your account email. Then, once prompted, you type "yes" to establish authentication. You should now be connected and your screen should look like this:

![Remote Connection](https://lh3.googleusercontent.com/drive-viewer/AAOQEORCR6X6WkAkFASk50gdLvFwAGFb-V6MfkhMjLcdRWSboUbyUuSqUzwBLFk2Cc_nHQQYA-c3l9IZBAl8DFsf_WVsh5EV-A=w1920-h853)

*Trying Some Commands*

There are many commands that you can use in the terminal. Here are some simple ones to try, pictured is an example of cd and ls being used. 

-  cd: change directory, cd (name) will change to (name) directory while cd .. will take you back to the previous directory 
-  ls: list files in directory
-  cat: displays file contents
-  cp: copy files

![Trying Commands](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQWEp4wbdc-wrdHZ3doHpp4dXD74PnSwmrb8mo5YEJVuSx29cMkfmii8FHhp0XxKN8VT9aolIDZmLBpDIekXNQdGFrRkA=w1920-h901)


*Moving Files with scp*

scp is a very useful command that securely copies files from your local computer to the server. 

- Create and save a java file or use one that you already have.
- In the terminal, type "scp [fileName"] directory" to copy your java file to the remote server. I'm copying Server.java so I will type "scp Server.java cs15lfa22ta1@ieng6.ucsd.edu:~/".
- Input your password and press enter. You've done it!

![Moving Files](https://lh3.googleusercontent.com/drive-viewer/AAOQEORCR6X6WkAkFASk50gdLvFwAGFb-V6MfkhMjLcdRWSboUbyUuSqUzwBLFk2Cc_nHQQYA-c3l9IZBAl8DFsf_WVsh5EV-A=w1920-h853)

*Setting an SSH Key*

ssh keys are used so you can avoid the hassle of passwords and longer wait times. Using ssh-keygen in the terminal creates a pair of files called the public key and private key. The public key is copied to the server while the private key is copied to the client. This pair of key files is used in place of a password. 

- Type ssh-keygen in the terminal.
- Pick a name for the file in which to save the key and type and re-type a password of longer length than 5 characters if you want.
- You now have your very own ssh keys! (I blurred mine since I'm storing highly clasified secrets)

![Setting Key](https://lh3.googleusercontent.com/drive-viewer/AJc5JmSgMt2V1rlHK5OXZXFWnCoVAhqLNZCbXaxCZNIQzJexZD051v_-TsyCIXimtkQUXVdjXfGavbtZfRaLE6XM3sfcbsrv=w1920-h901)

*Optimizing Remote Running*

To optimize your remote running experience, here are some shortcuts/tips. Remember though, this is far from all of what you can do, and you should take your time to learn as many tricks as you can. You can see examples in the picture. 

- Commands can be written in quotes at the end of an ssh command to be directly run on the remote server
- Semicolons can usually be used to run multiple commands on the same line
- The up-arrow can be used to recall the last command that was run

![Optimization](https://lh3.googleusercontent.com/drive-viewer/AJc5JmThXvXx9rs6hLuyHG-IHeSp4wN7NGy5xAg1UihSsOc09I4uzMzh7eSOK3vahTFAI-bLAYLAex6d_V4TgvvhlWY1iO5Yjg=w1920-h901)

