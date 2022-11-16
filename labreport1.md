__Lab 1 Report__

Here is the step-by-step process I took to log into my course-specific account on ieng6. Although these steps might not work perfectly for you, it should help to guide you through your own process.


*Installing VS Code:*

This part was easy for me as I didn't have to do anything! I already had VS Code so I moved on to the next step. If you do not have VS Code, here is the link to their website: https://code.visualstudio.com/.

![Inside of VS Code](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQKwAfoLfCwqQQUoQsTBrpaw5PZwuID7mpcW3zY0q0EzwtZZHIN1shg4o0tk1bMA8b0oRFU27KBDPi1NqLipsZcIp0J=w1920-h853)

*Remotely Connecting*

Unfortunately, my account did not work for some reason so I had to log in with a TA account. In this step, you first open up a terminal and type "ssh" with your account email. Then, once prompted, you type "yes" to establish authentication. You should now be connected and your screen should look like this:

![Remote Connection](https://lh3.googleusercontent.com/drive-viewer/AJc5JmSiqehA029C-L3mEcQlO7i8kXZxeog8LwSK7ND_5OLwA15B2PlN_x5kx_jLxxk64MO99D6c5JjMULxqr0S__pEvgCa6dg=w1920-h853)

*Trying Some Commands*

There are many commands that you can use in the terminal. Here are some simple ones to try, pictured is an example of cd and ls being used. 

-  cd: change directory, cd (name) will change to (name) directory while cd .. will take you back to the previous directory 
-  ls: list files in directory
-  cat: displays file contents
-  cp: copy files

![Trying Commands](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQnJGuwRVYEOyE0-SqEd7yFFP4tB_dChDhV-eSd3TGwMg0aGS-BlHfioEO-IaQXvJb23B26u2s=w1920-h853)


*Moving Files with scp*

scp is a very useful command that securely copies files from your local computer to the server. 

- Create a java file. For this, I create a file called WhereAmI.java with code that was provided from the course. You could create one as simple as a file that only prints out "Hello World!". Save it
- In terminal, type scp "fileName" directory. For instance, since I am transferring over WhereAmI.java, I would be typing scp WhereAmI.java cs15lfa22ni@ieng6.ucsd.edu:~/ to transfer to your remote server.
- Input your password and press enter. You've done it!

![Moving Files](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQnJGuwRVYEOyE0-SqEd7yFFP4tB_dChDhV-eSd3TGwMg0aGS-BlHfioEO-IaQXvJb23B26u2s=w1920-h853)

*Setting an SSH Key*

In this case, there is a great solution – ssh keys. The idea behind ssh keys is that a program, called ssh-keygen, creates a pair of files called the public key and private key. You copy the public key to a particular location on the server, and the private key in a particular location on the client. Then, the ssh command can use the pair of files in place of your password.

![Setting Key](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQnJGuwRVYEOyE0-SqEd7yFFP4tB_dChDhV-eSd3TGwMg0aGS-BlHfioEO-IaQXvJb23B26u2s=w1920-h853)

*Optimizing Remote Running*

To optimize your remote running experience, here are some shortcuts/tips. Remember though, this is far from all of what you can do, and you should take your time to learn as many tricks as you can. You can see examples in the picture. 

- Commands can be written in quotes at the end of an ssh command to be directly run on the remote server
- Semicolons can usually be used to run multiple commands on the same line
- The up-arrow can be used to recall the last command that was run

![Optimization](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQnJGuwRVYEOyE0-SqEd7yFFP4tB_dChDhV-eSd3TGwMg0aGS-BlHfioEO-IaQXvJb23B26u2s=w1920-h853)

