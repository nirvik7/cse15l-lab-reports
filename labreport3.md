__Lab 3 Report__

I chose to do my lab report on the grep command.

&nbsp;

*-i: ignore case*

Example 1: Here we can use the -i command to ignore case when searching for "Osama bin Laden" in 9/11 reports. Although the proper casing for his name is Osama bin Laden, there are many instances of the b in his name being capitalized. The -i command can be used to great effect here as we can search for his name ignoring casing. 

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -i "osama bin laden" 911report/*
911report/chapter-13.3.txt:            93. ABC News interview, "Terror Suspect: An Interview with Osama Bin Laden," Dec. 22,
```


Example 2:


Example 3:

&nbsp;

*-c: count matching lines*

Example 1:


Example 2:


Example 3:

&nbsp;

*-v: invert matches, select non-matching lines*

Example 1:


Example 2:


Example 3:

