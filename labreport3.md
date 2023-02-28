__Lab 3 Report__

I chose to do my lab report on the grep command using https://www.geeksforgeeks.org/grep-command-in-unixlinux/

&nbsp;

*-i: ignore case*

Example 1: Here we can use the -i command to ignore case when searching for "Madrid" in Puerto Rico's history. 

```
[cs15lwi23ahk@ieng6-203]:written_2:156$ grep -i "madrid" travel_guides/berlitz2/PuertoRico-History.txt
For Spain the 19th century was a bitter slide from imperial might to the status of a has-been. By the early 1800s independence movements had overthrown Spanish rule in most of the Western Hemisphere. Madrid’s most important remaining possessions were the island colonies of Cuba and Puerto Rico, both of which were chafing under the yoke of colonial rule and the bitter system of slavery. To squash subversive ideas about independence in Puerto Rico, Madrid imposed ruthless military control. The most memorable incident occurred in 1868 in the mountain town of Lares, when government forces crushed an uprising of secessionists, killing or jailing the insurgents, and many innocent victims. The event is remembered as El Grito de Lares (the cry of Lares).
The colonial government could not, however, hold back the tide of change sweeping the Caribbean. In 1872, one momentous decree abolished the 350-year-old institution of slavery in Puerto Rico, and in 1897 Spain cut the colonial ties and finally granted the island autonomy. The long dream of independence seemed to have come true. But eight months after Madrid had authorized home rule for Puerto Rico, American troops arrived to take it away.
```


Example 2: In this example, we use the -i command to search for "southern" in the Vallarta file. Now although this word is conventially spelled in all lowercase, it's very likely find it at the start of many sentences in which case, the starting S will be capitalized. As such, we do not want to miss out on those cases in our search results so the -i command is very helpful for us. 

```
[cs15lwi23ahk@ieng6-203]:written_2:159$ grep -i "southern" travel_guides/berlitz2/Vallarta-WhereToGo.txt
Yelapa and the Southern Beaches
About seven miles west of downtown, lies the Península de Santiago, Manzanillo’s best known landmark. For many travelers, this town is synonymous with the famed all-white world of Las Hadas (“the Fairies”) and its adjoining golf course. Set on a southern promontory of Santiago Peninsula, Las Hadas gazes across Manzanillo Bay to the town, but is a world apart in character. Its Moorish architecture, which looks something like a setting for Arabian Nights, became renown as the place where Bo Derek showed her appreciation for Ravel’s bolero in the movie Ten. Las Hadas was built in the 1970s by the Bolivian tin multimillionaire Antinor Patiño as a private, super-exclusive resort and a respite from Acapulco’s excessive glitz. Its presence spawned construction up and down the adjoining beaches, making Santiago Peninsula the most desirable address in town, especially for visitors to Manzanillo.
The inland side of Ixtapa is marked by the 18-hole Club de Golf Ixtapa. Nearly everything in Ixtapa lies along the main boulevard, Paseo Ixtapa, which runs parallel to the hotel-lined main beach, Playa Palmar. This beach offers 41/2 km (3 miles) of beautiful white sand and deep azure waters. Even though the beach faces the open sea, there are several spots where offshore rocks and islands quiet the surf and make the waters suitable for swimming. The undertow here, however, is usually quite strong, and extreme caution should be taken. For a stunning view of this beach, ride the cable car to El Faro restaurant, located on the southern end of the beach, upstairs from the Pacifica Hotel. At the far end of Paseo Ixtapa lies Marina Ixtapa, with fine restaurants, private yacht slips, and the Marina Ixtapa Golf Course.
Playa Linda is located 12km (8 miles) north of Ixtapa. This is a long beach with golden sands that seem to stretch endlessly to the north. It is the primary out-of-town beach, with water sports equipment rentals, fishing charters, and horseback riding. The ferry to Isla Ixtapa leaves from the jetty located on the southern end of Playa Linda.
The Southern Coast to Puerto Angel


&nbsp;

*-c: match count*

Example 1: Here we can use -c to count matches for "water" in the Abernathy text docs.

```
[cs15lwi23ahk@ieng6-203]: written_2:160$ grep -c "water" non-fiction/OUP/Abernathy/*
non-fiction/OUP/Abernathy/ch1.txt:0
non-fiction/OUP/Abernathy/ch14.txt:0
non-fiction/OUP/Abernathy/ch15.txt:0
non-fiction/OUP/Abernathy/ch2.txt:3
non-fiction/OUP/Abernathy/ch3.txt:0
non-fiction/OUP/Abernathy/ch6.txt:0
non-fiction/OUP/Abernathy/ch7.txt:0
non-fiction/OUP/Abernathy/ch8.txt:2
non-fiction/OUP/Abernathy/ch9.txt:1
```


Example 2: Here, in an interesting twist from the previous example, we can use -c to count matches for "fire" in the Fletcher text docs.

```
[cs15lwi23ahk@ieng6-203]: written_2:162$ grep -c "fire" non-fiction/OUP/Fletcher/*
non-fiction/OUP/Fletcher/ch1.txt:1
non-fiction/OUP/Fletcher/ch10.txt:0
non-fiction/OUP/Fletcher/ch2.txt:2
non-fiction/OUP/Fletcher/ch5.txt:1
non-fiction/OUP/Fletcher/ch6.txt:1
non-fiction/OUP/Fletcher/ch9.txt:0
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
