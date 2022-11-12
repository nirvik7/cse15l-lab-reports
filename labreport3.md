__Lab 3 Report__

I chose to do my lab report on the grep command.

&nbsp;

*-i: ignore case*

Example 1: Here we can use the -i command to ignore case when searching for "Osama bin Laden" in 9/11 reports. Although the proper casing for his name is Osama bin Laden, there are many cases of the b in his name being capitalized. The -i command can be used to great effect here as we can search for his name ignoring casing. 

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -i "osama bin laden" 911report/*
911report/chapter-13.3.txt:            93. ABC News interview, "Terror Suspect: An Interview with Osama Bin Laden," Dec. 22,
```


Example 2: In this example, we use the -i command to search for "nevirapine" in the medical text files. Now although this word is conventially spelled in all lowercase, it's one of the two main topics of this report. This means that we will likely find it at the start of many sentences in which case, the starting N will be capitalized. As such, we do not want to miss out on those cases in our search results so the -i command is very helpful for us. 

```
$ grep -i "nevirapine" plos/pmed*
plos/pmed.0010030.txt:        Nevirapine and efavirenz are the most commonly prescribed of the class of antiretroviral
plos/pmed.0010030.txt:        1253–1263), it appeared to be only marginally superior to nevirapine in terms of clinical
plos/pmed.0010030.txt:        nevirapine and efavirenz both raise high-density lipoprotein (HDL) cholesterol (the “good”
plos/pmed.0010030.txt:        type of cholesterol), the overall lipid profile is better with nevirapine than with    
plos/pmed.0010030.txt:        “These data suggest that nevirapine may be preferable to efavirenz in HIV-infected     
plos/pmed.0010030.txt:        were then randomized into three treatment groups: nevirapine, efavirenz, or both.      
plos/pmed.0010030.txt:        nevirapine and efavirenz groups (417 and 289 patients, respectively). This was because the
plos/pmed.0010030.txt:        2NN study showed that simultaneous use of nevirapine and efavirenz should be avoided—the
plos/pmed.0010030.txt:        in HDL cholesterol was significantly higher with nevirapine than with efavirenz. There was
plos/pmed.0010030.txt:        a decrease in the ratio of total cholesterol to HDL cholesterol with nevirapine and an 
plos/pmed.0010030.txt:        (especially nevirapine) actually leads to a reduction in coronary heart disease. “There are
plos/pmed.0010030.txt:        The study was funded by Boehringer Ingelheim, the manufacturer of nevirapine. The
```

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

