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
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
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

Example 3: This one isn't that interesting. I wanted to see how many times the word "aids" would be intermixed with the disease "AIDS" but on this search, it seems that it's a pretty rare scenario amounting to a grand total of 0 times. 

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -i "aids" plos/pmed.001*
plos/pmed.0010010.txt:        As an intern, I took care of the first patients with HIV/AIDS at San Francisco General
plos/pmed.0010010.txt:        Hospital, and so I grew up with AIDS in the early days of my medical career. We struggled
plos/pmed.0010010.txt:        things—AIDS has reshaped society's very notions of the most basic human behaviors.     
plos/pmed.0010010.txt:        I was in Uganda in 1985, early in the AIDS epidemic there. We knew then where that     
plos/pmed.0010010.txt:        Africa have achieved a huge amount in tackling HIV/AIDS, particularly in Uganda, the   
plos/pmed.0010010.txt:        The theme of this year's International AIDS Conference in Bangkok was “Access for All.”
plos/pmed.0010010.txt:        resources are essential to ending the AIDS pandemic. I visited Africa with US Health and
plos/pmed.0010010.txt:        Human Services Secretary Tommy Thompson and many AIDS experts last December, and we saw
plos/pmed.0010010.txt:        for HIV/AIDS programs, but for all aspects of public health and health care.
plos/pmed.0010010.txt:        individual living with HIV. I was at the dedication of an AIDS clinic in Kenya. It was 
plos/pmed.0010010.txt:        interventions. Many patients with HIV/AIDS in Africa also have tuberculosis and are put on
plos/pmed.0010010.txt:        on AIDS. Such a story also inspires hope because you can see the multiplier effect that
plos/pmed.0010010.txt:        The innovative programs and ideas emerging in Africa can change the picture of the AIDS
plos/pmed.0010010.txt:        countries that allow volunteers to help communities fight the AIDS epidemic, but this is
plos/pmed.0010010.txt:        just one of many steps that are being taken. The US president's Emergency Plan for AIDS
plos/pmed.0010010.txt:        for international AIDS assistance [13], and I am part of the team that is charged with 
plos/pmed.0010029.txt:        essential aids in guiding the distribution of limited funds to lower the burden of life
plos/pmed.0010034.txt:        description of the Acquired Immune Deficiency Syndrome (AIDS) in 1981 [5].
plos/pmed.0010036.txt:        acute phase of infection in humans and animals exposed to AIDS-associated retroviruses 
plos/pmed.0010036.txt:          3 /y. Comparison with data from the Multicenter AIDS Cohort Study
plos/pmed.0010036.txt:        therapeutic AIDS vaccine designed to retard disease progression rather than prevent    
plos/pmed.0010041.txt:        The devastating effects of HIV infection worldwide are reason enough for AIDS
plos/pmed.0010061.txt:        sleep aids than are currently available, with profound implications for improved public
plos/pmed.0010070.txt:        remain obstacles in the way of turning HIV/AIDS into a manageable chronic disease.     
plos/pmed.0010071.txt:        affordable prophylactics and drugs for HIV/AIDS, tuberculosis, and malaria.
plos/pmed.0010071.txt:        considering the combined burden of HIV/AIDS, tuberculosis, and malaria, it is important to
```

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

