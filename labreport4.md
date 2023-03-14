__Lab 4 Report__

*Step 4: Log into ieng6*

Keys pressed: 

```
<Ctrl>+V <Enter>
```

I had the ssh command with the cse email on my computer already so I simply copied it while in Google Chrome and then pasted it into the terminal.

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)

*Step 5: Clone your fork of the repository from your Github account*

Keys pressed: 

```
git clone <Ctrl>+V <Enter>
```

Again, I had the forked repository url sitting in my brower so I copied it. In the terminal, I wrote "git clone", which is obviously the repo cloning command, and pasted in the forked repo url. 

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)


*Step 6: Run the tests, demonstrating that they fail*

Keys pressed: 

```
cd lab7 <Enter> <Ctrl>+V <Enter> <Ctrl>+V ListExamples 
```

First, I went into the newly cloned lab7 repo. Because I had the week 7 lab pulled up on my computer with the JUnit commands in the example at the bottom, there was not much left to do. I copied the javac command and pasted it into the terminal and then did the same with the java command, adding in "ListExamples". Light work.

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)

*Step 7: Edit the code file to fix the failing test*

Keys pressed: 

```
nano ListExamples.java <Enter> <down>x41 <right>x12 <backspace> 2 <Ctrl>+X 
```

I used nano to edit ListExamples.java. The edit I had to make was deep into the file so there were many downs and rights to account for but the edit itself was really simple.

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)

*Step 8: Run the tests, demonstrating that they now succeed*

Keys pressed: 

```
<up>x3 <Enter> <up>x3 <Enter>
```

The JUnit commands were right there because I had just down them so I went a bit up into past commands and entered them into the terminal again.

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)

*Step 9: Commit and push the resulting change to your Github account *

Keys pressed: 

```
git add . <Enter> git commit -m "yo" <Enter> git push
```
Now, all that needs to be done is to use the git add, commit, and push commands to commit and push the resulting change into Github. Done!

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)
