__Lab 4 Report__

*Part 1:*

Sequence of keys pressed to changing the name of the start parameter and its uses to base

```
/star<Enter>cebase<Esc>ncebase<Esc>ncebase<Esc>ncebase<Esc>:wq
```

40 keys pressed total

Sorry for the low image quality. The screenshot button on my laptop is broken so I had to take pictures with my phone :(

```
/star<Enter>
```

Vim open the file at the very top. You can search for a certain string by using "/" similar to the Ctrl+F shortcut. By searching for "star" we reach out destination of the start parameter and now we can press <Enter> to exit out of the search. [6 keys]

![SS1](https://lh3.googleusercontent.com/drive-viewer/AFDK6gPQ1le77b8QYhNdmLIrYvsDdLwqOwyCDCisH8QG1Bonpav_p4klh5Hpw0ze67WtwlJ25UxyDIxj7dT5pPurkXdPm44s=w1920-h853)

```
cebase<Esc>
```
"ce" is a command that (c)hanges the file until the (e)nd of the word which makes removing start very simple. This command also puts us in Insert mode so all we have to do now is type "base" and we're finished with changing out our first entry. Press <Esc> to go back to normal mode. [7 key presses]
  
![SS2](https://lh3.googleusercontent.com/drive-viewer/AFDK6gMxtys3Gkscy36o3zPGUPd2cLxQEbGX8LQTwn20mCOwl6nFeEMSF8Fg0aKku_CYIqxKoUov_v7FRv4wwW9esmI1_VD3jg=w1920-h853)

```
n
```
We can move onto changing out all the entries by using "n" here where it is similar to the Ctrl+G shortcut. Move to the next start and go through the "cebase<Esc>" process until you're finished. You will need to do this 3 times for a total of 4 start replaced with base. [24 key presses]
  
![SS3](https://lh3.googleusercontent.com/drive-viewer/AFDK6gNlewHY81dUguZM0gnl3yY7Tlqc2v4TT-TFwtMitnOo3pSz92GfznGPj8bCm8YKDPApCRDRMKHnljZnHFIN8GEmddrDEQ=w1920-h853)

```
:wq
```
Finally, we can type ":wq" to (w)rite and save the file and (q)uit. We're done! [3 key presses]
  
![SS4](https://lh3.googleusercontent.com/drive-viewer/AFDK6gOt3PyWgqqbBipmmx2DKnQkbVYSiI2q_EYWxlBuWsXHN8aetRpzcHzwgaGbFJGWzfR2M39wMFMyNxNpwwbbzRtm6DIf2w=w1920-h853)

*Part 2:*
  
scp Time: 3:11
  
ssh Time: 1:42

REPORT: Editing through vim in the remote SSH is the way to go as you can see just by the time it took. Having to scp every time a change is needed and constantly going in and out the server is something you would not want to go through. A small edit that just needs to be done once is okay for VS Code and scp, otherwise you should use vim in ssh, especially if there's major changes that need to happen. 
