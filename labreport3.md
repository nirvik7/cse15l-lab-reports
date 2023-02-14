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

Example 3: This one isn't that interesting. I wanted to see how many times the word "aids" would be intermixed with the disease "AIDS" but on the evidence of this search, it seems that it's a pretty rare occurrence amounting to a grand total of 0 times. 

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

Example 1: In this example, I inverted matches for "whistle" on pmed.0020281.txt which is a text file about whistleblowing. This creates some interesting results as we can see the report without lines containing the main topic. 

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -v "whistle" plos/pmed.0020281.txt





        Whistleblowers serve no function if they cannot tell their stories. The present story of
        PLoS Medicine —that involves the pharmaceutical industry, pharmaceutical
        benefit management corporations, the managed care industry, and the political and lobbying
        forces that zealously guard their secrets could not have been told without the help of
        courageous men and women [1, 2] For that reason, those of us who congregated in Washington,
        D.C., on May 15th, 2005, at the invitation and support of the Public Library of Science and
        the Government Accountability Project feel particularly humbled and grateful to these two
        sponsors. Our convictions could not have been aired were it not for the essential First
        Amendment work of responsible journalists, who exemplify the best in investigatory
        research.
        features. It is the face of children and adults who have been injured or killed by
        misrepresented pharmaceuticals; clinical research trial results that have been sequestered
        from the scientific community and whose incomplete findings cause injury; and
        pharmaceuticals that are detailed to physicians, not to save lives or necessarily improve
        the health or welfare of the recipients, but to make money.
        passionate, and often successful, because our efforts have a different goal than the
        corporations and political interests whose operations we occasionally challenge. Our goal
        is to tell the truth. That honest effort is the source of any ethical difference we can or
        assault of unprecedented odds against being heard put forth by that sum of political power,
        expediency, and money.
        improve the status quo—be it in pharmaceutical marketing or managed-care decision
        making—cannot proceed or flourish without it.
        Ralph Waldo Emerson, American essayist and philosopher (1803–1882), commented about
        success (I have adapted his comments for all of us who gathered in Washington in mid-May
        2005): “To leave the world a bit better, whether by a healthy child, a garden patch or a
        redeemed social condition; to know even one life breathed easier because you have lived;
```


Example 2: Here, I inverted matches for "AIDS" in pmed.0010010.txt which deals with HIV/AIDS. The -v command could be useful in this case if you want matches about just the HIV stage rather than including AIDS.

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -v "AIDS" plos/pmed.0010010.txt

  



        through the confusion about what was making people so sick, and each new day brought a new
        discovery about the disease and its consequences. I went through that evolutionary process
        along with everybody else, and it shaped me in many profound ways. Before long, I
        recognized that this wasn't a disease of “those people over there.” This was a disease that
        could strike anyone, anytime. And as physicians, we had to adjust our thinking about our
        own vulnerability to occupational risk, and to emphasize prevention, because there wasn't
        going to be a cure for a long, long while. And not only physicians had to rethink
        epidemic was going to go, absent an effective vaccine or cure, but few of us could have
        imagined that it would evolve so quickly without an end in sight. While the people of
        epidemic is far from being under control on that continent and is spreading through other
        parts of the world with alarming speed.


        The Crisis of Human Resources
        Over the past few years, it has become increasingly apparent that a critical component of
        assuring access to care and treatment is human capital. Like fiscal capital, human
        evidence of this critical need in every country we visited. The miracles of modern science
        are meaningless without systems and people to deliver them to those in need.
        The World Health Organization estimates that of the 40 million people worldwide infected
        with HIV, 6 million need immediate, life-sustaining antiretroviral therapy. Fewer than
        400,000 people in developing countries have access to such treatment (Figure 1) [1,2].
        There are too few skilled health care workers to provide reliable delivery and
        administration of these life-saving therapies. According to a recent Institute of Medicine
        report, and a study sponsored by the US Agency for International Development, the number of
        health care workers in many African countries is actually shrinking as they are lured to
        developed countries by better pay and professional opportunities (Box 1) [2,3]. Reversing
        this brain drain is essential over the long-term, as HIV treatment and care will be
        required for decades. In the short-term, the Institute of Medicine called for expanded
        efforts “to bring qualified volunteer initiative medical professionals into both urban and
        rural areas to support prevention, care, and training programs” [2]. I could not agree more
        that addressing the human resource needs will be essential as we move forward—and not just
        It has now been shown, beyond any doubt, that even in resource-poor countries with the
        most basic health infrastructure, people get the same benefit from treatment and prevention
        interventions as those in the rich world [4]. In fact, surveys in Cape Town, Kampala,
        Khayelitsha, and Senegal found rates of adherence to antiretroviral therapy of 90%–94%,
        compared with estimates of 70% in developed countries [5,6,7].


        When You Have Seen the Faces
        We hear the numbers—the millions upon millions infected—and we grow numb. That is why we
        must go to the front lines—the households and communities—and start focusing on each
        raining, and we were waiting outside with our umbrellas. A 12-year-old girl in front of me
        turned around and leaned her head against my belly and said, “Could you take me to America?
        I need drugs.” If you take that girl's face and multiply it a thousand times—that is the
        memory I bring home from Africa: the faces of the children and their asking, “Why are so
        many of our parents dying? Why are we dying?”
        We visited a US Centers for Disease Control and Prevention (CDC) program in the very
        remote areas of Uganda where there are no roads and it is impossible for people to come
        into population centers to receive HIV testing and other services. Young staff from the CDC
        are working with Ugandans and community organizations in that area to deliver
        antiretroviral therapy. Some may think that the difficulties of delivering antiretroviral
        therapy into such a remote area are overwhelming—and some may question whether this is a
        sustainable intervention. But once you see firsthand what miracles are possible, your world
        view changes almost overnight.
        What we saw was the success of a wonderful home-based treatment and care program for
        people who don't have access through other means. And when I say “home-based care,” picture
        a hut without running water or electricity, where only motorcycles are available to deliver
        medications. The first step of the program is to provide clean water. Coliforms and other
        pathogens in the water supply for the household are removed through an inexpensive water
        vessel fitted with a filter and through a chlorination process. In addition, a
        cotrimoxazole tablet is given every day, which, in one patient's words, changed his life
        because he began to feel well almost immediately. Not only do the cotrimoxazole prophylaxis
        and the water treatment improve diarrheal illness, but malarial parasitemia also drops. So
        that is a very positive, unexpected consequence of just two very simple and inexpensive
        tuberculosis therapy in addition to cotrimoxazole. As a result, they begin to feel better
        even before they begin antiretroviral therapy.
        We spent time with one of the patients in the home-based care program. As she began to
        participate in these programs, tests became available to measure her CD4 count. She
        explained to me what her CD4 count was, what it meant, and how it improved when she started
        the cotrimoxazole and tuberculosis therapy. She had begun taking three antiretroviral drugs
        and held up her pill box to explain her regimen in detail. Every week a Ugandan health aide
        delivered her supply of pills on a CDC motorcycle and monitored her adherence to the
        treatment. Not only was she extremely reliable in taking her medications, but she also knew
        more about them and their side effects than most of the patients I treated at San Francisco
        General. She was also an expert in HIV prevention. I asked her, “What do you do to protect
        your three young sons from this infection?” She replied, “Every day I take them by the
        hand, and I go out of the house and I say, ‘Do you see that mound of dirt? That is your
        father’s grave. Your father acquired this fatal infection through sex. Be careful.'” And
        then she talks to them about the “ABCs” (“A” for abstinence, “B” for being faithful, “C”
        for condoms).
        So when you see a story like that unfold in the middle of Africa, it's impossible not to
        be hopeful. And yet, it's also very sobering because we are reminded of our responsibility.
        The question is not what the international health community is accomplishing in these
        countries now, but what we could accomplish if we joined together to really fight this war
        comes from taking on one problem and can see the way that effort can expand to encompass
        and address a much greater set of problems.


        Beyond ABCs—Diagnosis and Responsibility
        When we think about successful prevention models in Uganda, “ABC” certainly stands out
        [8]. However, at this point in the epidemic curve, other letters must also be considered.
        Most HIV transmission is accounted for by infected people having risky sex with uninfected
        people. Both in the US and in Africa, studies show that most infected people engaging in
        risky sex are unaware of their infection status, and that when their infection is
        diagnosed, they usually take steps to protect the others with whom they are having contact
        [9,10,11,12]. So let's add the letter “D” for diagnosis. In fact, improving efforts to help
        people choose risk avoidance and to diagnose those who are already infected is the
        cornerstone of the CDC's new domestic HIV prevention strategy. Diagnosis is extremely
        important in many African communities, especially where the number of discordant
        couples—where one individual is infected and the other is not—is high. Sadly, many couples
        “being faithful” now do not realize that one partner is already infected and are not being
        reached with diagnostic testing programs. So “ABCD” is a concept that I would like to put
        out on the table as food for thought. Of course, there is another letter that we need to
        stress: the letter “R,” for responsibility: personal sexual responsibility is a critical
        component of HIV prevention. Many women and girls become infected after being raped by men
        or because their social circumstances rob them of the power to refuse sex. Men must be held
        accountable for greater sexual responsibility and for ending sexual violence and
        degradation of women and girls. HIV prevention programs need to emphasize responsibility,
        but not lose sight of the fact that responsibility can be practiced only with personal
        autonomy, which many women and girls simply do not have.


        Expanding the Team to Meet the Needs
        epidemic. The purchase of antiretroviral drugs for Africans is not the big challenge.
        Access to drugs will improve in Africa. The real challenges are delivering drugs in a safe
        and effective way, monitoring therapy, and sustaining the pipeline of drugs so that ongoing
        treatment can be guaranteed. In the example of the home-based program in Uganda, we have
        seen that these challenges can be overcome. Expanding access to prevention, care, and
        treatment services isn't going to be easy, but it is certainly possible. It will take
        unprecedented commitment by people in the public sector, the private sector, faith
        communities, and community organizations, and perhaps most importantly, individual
        volunteers who make up their minds to contribute in any way they can.
        Last fall, the US Peace Corps announced that it was activating programs in some
        Relief will provide $15 billion, including almost $10 billion in new funds, over five years
        making this plan happen. I look forward to learning from others in the global health
        community how we can best expand our impact and collectively find a way to support the
        delivery of prevention messages and life-saving medications to everyone in Africa—and
        especially to that little girl at the Kenyan clinic who touched my heart.
```

Example 3: In any case where you're searching about dementia but forgot you're searching about dementia (maybe you should get that checked), you might have inverted the matches for dementia by running ```grep grep -v "dementia" plos/pmed.0020275.txt```

```
my_gr@NirvikLaptop MINGW64 ~/OneDrive/Documents/GitHub/skill-demo1/technical (main)
$ grep -v "dementia" plos/pmed.0020275.txt

  



        Dementia remains an incurable condition and its increasing prevalence is a deeply
        worrying aspect of the “graying” of the population. An important question for researchers
        location to another. Incidence studies are particularly valuable for less biased comparison
        of disease occurrence, as well as being essential for policy makers. Many biases can,
        however, be introduced in such studies. Dropout and mortality are particular reasons for
        concern.
        Authors have frequently attempted to assess whether rates in a given study are similar to
        those obtained elsewhere. However, variations between studies in the methodology employed
        make such comparisons unreliable. Where within-country variations in incidence have been
        noted, as has happened in the US, they have often been ascribed to methodological
        differences, but one cannot be certain whether this is the case.
        Risk factors for other chronic disorders common in old age (notably cardiovascular
        disease and cancers) do vary in their prevalence between and within countries. In the UK,
        for example, the incidence of stroke is known to vary considerably across the country. A
        were better controlled. One way to test this hypothesis is to compare sites with known
        variation in vascular risk to assess whether there is also variation in the incidence of
        The Medical Research Council Cognitive Function and Ageing Study (MRC CFAS) is a
        multi-site, population-based study in the UK of individuals aged 65 years and over living
        in the community, including institutions. Diverse sites have been chosen, with varying
        employed, with the waves two years apart. A standard set of instruments for the diagnosis
        using likelihood-based methods to compare the first two waves of interviews.
        from 6.7 per 1,000 person years at age 65–69 years to 68.5 per 1,000 person years at age 85
        England and Wales each year. However, there was no convincing evidence of variation across
        sites, and the incidence rates do not reflect the variations in the prevalence of possible
        risk factors in these sites. We therefore cannot assume that action to reduce vascular risk
        Another issue addressed by the study is previous suggestions in the literature that
        respondents in these age groups in previous studies made it impossible to test this
        hypothesis. The CFAS, however, found no evidence of any such tailing off in incidence,
        which also has implications for policy and planning.
        The CFAS is important because it provides the first multi-site comparison of incidence
        rates in ethnically homogeneous populations within a country, and within Europe, using
        identical methodology across sites. The methodological approach developed for the study
        in other chronic disease studies involving a two-phase selection process.
```

&nbsp;

Thank you,

Nirvik 
