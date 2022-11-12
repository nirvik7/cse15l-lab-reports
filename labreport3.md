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

*-c: match count*

Example 1: Going off one of the previous examples, we can use the -c command here to count the matches for "Osama" in the 9/11 reports. We can see matches in just 3 files amounting to just 9 total matches, which is a bit surprising. That gives me an idea...

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -c "Osama" 911report/*
911report/chapter-1.txt:0
911report/chapter-10.txt:0
911report/chapter-11.txt:0
911report/chapter-12.txt:0
911report/chapter-13.1.txt:0
911report/chapter-13.2.txt:0
911report/chapter-13.3.txt:2
911report/chapter-13.4.txt:5
911report/chapter-13.5.txt:0
911report/chapter-2.txt:0
911report/chapter-3.txt:0
911report/chapter-5.txt:0
911report/chapter-6.txt:0
911report/chapter-7.txt:2
911report/chapter-8.txt:0
911report/chapter-9.txt:0
```


Example 2: Here, we can see a significantly higher number of matches by counting for "bin Laden" instead of "Osama" in the 9/11 reports. That being said, my questions have not stopped. Practically all of the matches are found in 13.3 (36!) and other files have lost their matches. Did the other files refer to him by just his first name? I guess it must be.

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -c "bin Laden" 911report/chapter*
911report/chapter-1.txt:0
911report/chapter-10.txt:0
911report/chapter-11.txt:0
911report/chapter-12.txt:0
911report/chapter-13.1.txt:0
911report/chapter-13.2.txt:0
911report/chapter-13.3.txt:36
911report/chapter-13.4.txt:1
911report/chapter-13.5.txt:0
911report/chapter-2.txt:0
911report/chapter-3.txt:0
911report/chapter-5.txt:0
911report/chapter-6.txt:0
911report/chapter-7.txt:0
911report/chapter-8.txt:0
911report/chapter-9.txt:0
```


Example 3: After reading about the UN in the first file, I wondered if these journal text files would be primarily concerning the United Nations so I ran "United Nations" through a little -c search. The answer was a resounding no as no other file mentioned the UN more than once and even these files were very far and very few in between as 0 littered the search. 

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -c "United Nations" plos/journal*
plos/journal.pbio.0020001.txt:3
plos/journal.pbio.0020010.txt:0
plos/journal.pbio.0020012.txt:0
plos/journal.pbio.0020013.txt:0
plos/journal.pbio.0020019.txt:0
plos/journal.pbio.0020028.txt:0
plos/journal.pbio.0020035.txt:0
plos/journal.pbio.0020040.txt:0
plos/journal.pbio.0020042.txt:0
plos/journal.pbio.0020043.txt:0
plos/journal.pbio.0020046.txt:0
plos/journal.pbio.0020047.txt:0
plos/journal.pbio.0020052.txt:0
plos/journal.pbio.0020053.txt:0
plos/journal.pbio.0020054.txt:0
plos/journal.pbio.0020063.txt:0
plos/journal.pbio.0020064.txt:0
plos/journal.pbio.0020067.txt:0
plos/journal.pbio.0020068.txt:0
plos/journal.pbio.0020071.txt:0
plos/journal.pbio.0020073.txt:0
plos/journal.pbio.0020100.txt:0
plos/journal.pbio.0020101.txt:0
plos/journal.pbio.0020105.txt:1
plos/journal.pbio.0020112.txt:0
plos/journal.pbio.0020113.txt:0
plos/journal.pbio.0020116.txt:0
plos/journal.pbio.0020121.txt:0
plos/journal.pbio.0020125.txt:0
plos/journal.pbio.0020127.txt:0
plos/journal.pbio.0020133.txt:0
plos/journal.pbio.0020140.txt:0
plos/journal.pbio.0020145.txt:0
plos/journal.pbio.0020146.txt:0
plos/journal.pbio.0020147.txt:0
plos/journal.pbio.0020148.txt:0
plos/journal.pbio.0020150.txt:0
plos/journal.pbio.0020156.txt:0
plos/journal.pbio.0020161.txt:1
plos/journal.pbio.0020164.txt:0
plos/journal.pbio.0020169.txt:0
plos/journal.pbio.0020172.txt:0
plos/journal.pbio.0020183.txt:0
plos/journal.pbio.0020187.txt:0
plos/journal.pbio.0020190.txt:0
plos/journal.pbio.0020206.txt:0
plos/journal.pbio.0020213.txt:0
plos/journal.pbio.0020214.txt:0
plos/journal.pbio.0020215.txt:0
plos/journal.pbio.0020216.txt:0
plos/journal.pbio.0020223.txt:0
plos/journal.pbio.0020224.txt:0
plos/journal.pbio.0020228.txt:0
plos/journal.pbio.0020232.txt:0
plos/journal.pbio.0020241.txt:0
plos/journal.pbio.0020262.txt:0
plos/journal.pbio.0020263.txt:0
plos/journal.pbio.0020267.txt:0
plos/journal.pbio.0020272.txt:0
plos/journal.pbio.0020276.txt:0
plos/journal.pbio.0020297.txt:0
plos/journal.pbio.0020302.txt:0
plos/journal.pbio.0020306.txt:0
plos/journal.pbio.0020307.txt:0
plos/journal.pbio.0020310.txt:1
plos/journal.pbio.0020311.txt:0
plos/journal.pbio.0020337.txt:0
plos/journal.pbio.0020346.txt:0
plos/journal.pbio.0020347.txt:0
plos/journal.pbio.0020348.txt:0
plos/journal.pbio.0020350.txt:0
plos/journal.pbio.0020353.txt:0
plos/journal.pbio.0020354.txt:0
plos/journal.pbio.0020394.txt:0
plos/journal.pbio.0020400.txt:0
plos/journal.pbio.0020401.txt:0
plos/journal.pbio.0020404.txt:0
plos/journal.pbio.0020406.txt:0
plos/journal.pbio.0020419.txt:0
plos/journal.pbio.0020420.txt:0
plos/journal.pbio.0020430.txt:0
plos/journal.pbio.0020431.txt:0
plos/journal.pbio.0020439.txt:0
plos/journal.pbio.0020440.txt:0
plos/journal.pbio.0030021.txt:0
plos/journal.pbio.0030024.txt:0
plos/journal.pbio.0030032.txt:0
plos/journal.pbio.0030050.txt:0
plos/journal.pbio.0030051.txt:0
plos/journal.pbio.0030056.txt:0
plos/journal.pbio.0030062.txt:0
plos/journal.pbio.0030065.txt:0
plos/journal.pbio.0030076.txt:0
plos/journal.pbio.0030094.txt:0
plos/journal.pbio.0030097.txt:0
plos/journal.pbio.0030102.txt:0
plos/journal.pbio.0030105.txt:0
plos/journal.pbio.0030127.txt:0
plos/journal.pbio.0030129.txt:0
plos/journal.pbio.0030131.txt:0
plos/journal.pbio.0030136.txt:0
plos/journal.pbio.0030137.txt:0
```

&nbsp;

*-v: invert matches, select non-matching lines*

Example 1:


Example 2:


Example 3:

