---
title: 'Timeline Team Mashers Cybersecurity Awareness Communication Challenge (CAC²) CSAW'
date: 2024-11-17T18:00:00+02:00
tags:
- blog
- csaw2024
- CaC²
- on-site
description: 'A brief, straightforward account of how to win a CSAW competition and enjoy Valence, France.'
ShowReadingTime: true
ShowWordCount: true
sitemap:
  priority: 1
---

## Background

CSAW is an annual cybersecurity event started in 2003 at [New York University](https://www.nyu.edu/). Each year, it’s organized thanks to the efforts of students from around the globe. In Europe, the hosting institution is “[INP - Esisar](https://esisar.grenoble-inp.fr/en)” in Valence, France.

This year, alongside various conferences and competitions, the [Cybersecurity Awareness Communication Challenge (CAC²)](https://esisar.grenoble-inp.fr/fr/recherche/cybersecurity-awareness-communication-challenge-cac%c2%b2) made its debut—a competition aimed at creating a communication strategy to raise cybersecurity awareness among a non-technical audience.

![Cybersecurity Awareness Communication Challenge banner](/csaw2024/cac24_banner.png)

---

# Pre-Competition

After my disappointing result in last year’s [Embedded Security Challenge](https://www.csaw.io/esc) at CSAW, I decided to give my spot to new teammates who could potentially bring more productivity and motivation.

In doing so, I took advantage of the brand-new CAC² competition. It’s considerably less technical than the average CSAW event, welcoming participants who aren’t necessarily entrenched in cybersecurity. I saw this as a chance to dive into something new with a group of friends.

Unfortunately, I wasn’t met with the same enthusiasm from everyone, and I managed to recruit only Ryan, a friend and former classmate who’s currently trying to become a self-taught illustrator.

---

## Qualifying Phase

In the qualifying phase, we were only required to submit a document outlining our intended project—no mockups were needed at this point. Our submission needed to cover the chosen cybersecurity topic, the message we wanted to convey, and our target audience.

Click [here](/csaw2024/CSAW_CAC_final.pdf) to download the document we submitted as Team Mashers for the qualifying round.

The document begins with an introduction containing a few statistics and background information tailored for the competition’s non-technical judges. The second chapter covers our analysis of potential target audiences, and the third chapter discusses the common misconception that young people, frequent internet users, are automatically more skilled in using it safely. In the fourth chapter, we lay out our communication strategy.

The key points to keep in mind are:

- The 18–35 age range is both the [largest group of internet users](https://www.statista.com/statistics/272365/age-distribution-of-internet-users-worldwide/) and the [most vulnerable to social engineering attacks](https://sosafe-awareness.com/company/press/digital-natives-more-likely-to-open-harmful-phishing-emails-than-their-older-colleagues/).
- Although data is limited on this topic, we believe it’s reasonable to assume that people under 35 who are familiar with or fans of Japanese animation are also more likely to be frequent internet users than the average person.
- The use of Japanese-style illustrations in advertising and awareness campaigns [has become mainstream](https://subsign.co/stories/anime-is-the-new-trend-in-marketing-and-its-everywhere/) but is [not yet overused](https://www.campaignasia.com/article/why-marketers-should-care-about-anime/482299).
- Graphics in this style can be used in both poster format and social media posts, as demonstrated by AVIS FVG and the [Italian Air Force](https://www.campaignasia.com/article/why-marketers-should-care-about-anime/482299), which achieved positive results.
- If public institutions initiate campaigns like this, it’s likely that the impact of a digital campaign would be greater. Both AVIS’s mascot and the Air Force’s character quickly went viral on Italian social media.
- Poster-based campaigns [are low-cost](https://www.red17.co.uk/blog/why-posters-can-be-so-effective/), while digital campaigns (assuming they’re managed by a skilled digital communication team) are considerably [cheaper than television ads](https://www.forbes.com/councils/forbesagencycouncil/2023/12/01/tv-marketings-reign-is-over-now-social-media-has-taken-its-place/), both in production and placement.

In the final chapter, we summarize our ideal implementation strategy:

- Create graphics suitable for both print and social media.
- Display posters in high schools and universities.
- Launch campaigns on social media pages of public institutions, or create dedicated profiles if that’s not possible.
- Use social media metrics and conduct student interviews to gather data, which will help us estimate campaign impact.

---

# Pre-Finals

To our complete surprise, we received word in mid-October that we had qualified for the finals.

![The email announcing our qualification](/csaw2024/finals_mail.png)

We were thrilled—it was unexpected, and we didn’t think we had done particularly well. But here we were, qualified for a trip to CSAW and a shot at doing well in the finals.

At this point, it was time to create proof-of-concepts and mockups. We had around 20 days to develop a plan for implementing our proposed strategy and to make it practical.

Our initial plan was to stick as closely as possible to our qualifying document: we would design and print posters with messages aimed at raising awareness of phishing attacks and then conduct interviews in locations where these posters were displayed.

The result: a disaster. I had never tried to implement a communication strategy before, and Ryan had to navigate working with a real client for the first time—a client who was also rather indecisive and on a tight deadline. We quickly realized our shortcomings and ended up scrapping several drafts because we couldn’t quite pin down our messaging.

After burning through the first ten days, we had only ten days left to create something. There was still time to complete the illustration, but not enough to conduct the data-gathering interviews we had planned, as we’d already be close to leaving for France by the time we had anything ready.

The strength we aimed for was feasibility in terms of time and budget, so we couldn’t go to France empty-handed.

After considering multiple options, I was inspired by a post about [quishing](https://www.checkpoint.com/it/cyber-hub/threat-prevention/what-is-phishing/what-is-quishing-qr-phishing/), a phishing attack using QR codes. We decided to post QR stickers around the city and create a [site/counter](https://qr.gabibbo.xyz/) to track how many people scanned them.

![GIF showing the site’s functionality](/csaw2024/sito.gif)

This was another case of “yes, we can do it quickly!”—but this time, the goal was within our reach, and we achieved a satisfying result.

I implemented and published the site in a few days (thanks to @Flame for hosting 🫰). The front-end remained the same since the initial release, while the back-end went through continuous improvements as ideas flowed in from Flame and me. The final version had a general counter and a QR-specific counter (each QR type has an ID), using cookies to prevent multiple scans from the same device from inflating the count. If someone visited the site without scanning a QR (specifically, without the URL parameter with the QR ID), they wouldn’t increment any counter since we could assume they were “guests.” We also saved the timestamp of each new visitor to help us analyze any potential correlations between time and new visitor counts.

To publicize the site, we printed simple QR stickers featuring anime characters. To assess the importance of the drawing style and inclusion of recognizable characters, we created two QR variants: one with official illustrations (with copyright-permissive licenses for non-commercial use) and others with quick chibi drawings by Ryan.

![Example of QR stickers posted around Rome](/csaw2024/stickerz.jpeg)

Lenovo and Logitech, please sponsor us (ʃƪ˘ﻬ˘)

---

# Finals

The four days in France were extremely intense.

On the 7th, we woke up at 3 a.m. for our 6:10 a.m. flight to Lyon, arriving in Valence around 10 a.m.

Once there, we immediately set to work to be as productive as possible:

![Us and TRX members lying on the ground in a park, forming the TRX logo](/csaw2024/TRX_core.png)

After a French breakfast at a boulangerie, a snack at a café, and a quick lunch, we started looking for a print shop for our competition poster. Little did we know that finding a print shop in Valence would be as challenging as finding a French person who speaks English...

![Photo of the boulangerie counter](/csaw2024/boulangerie.png)

In the middle of our search, after about an hour of fruitless wandering (some of us lost to the call of sleep), we stumbled upon a quirky print shop run by an eccentric artist who carried the spiciest pepper we’d ever tasted. He was also kind enough to praise Ryan’s poster illustration.

Unfortunately, the posters would only be ready at 6 p.m., exactly when the social event was supposed to start. No problem: we went to check in at our accommodation (the self-check-in code was incorrect but was randomly guessed by Ryan), took a quick 20-minute nap, got ready, and headed out. It took us quite a long walk, but it was absolutely worth it. Here is a [digital copy](/csaw2024/poster_ENG_CAC_fullWhiteQR.png) of the poster:

![Poster CSAW](/csaw2024/poster_ENG_CAC_fullWhiteQR_quartersize.png)

(On the cover: Aura the Guillotine, Frieren)

Afterwards, we quickly returned to our room to drop off the poster and then rushed to the social event. We grabbed a quick dinner, took a photo:

![Social event photo with the Cybersecurity Awareness Communication Challenge participants](/csaw2024/social_event_cac.png)

and headed straight back to the room. Ryan immediately went to bed, but I decided to go to Champ de Mars and practiced my pitch out loud, preparing for the final presentation the next day.

On competition day, we arrived at ESISAR at 8 am, had breakfast, and I realized I’d left the stickers back in the room. I quickly retrieved them and made it back just in time for the pitch presentations.

We did well, thanks also to a tip from TRX member [magicfrank](https://magicfrank00.github.io/writeups/pages/about/), who suggested we print a QR code linked to our website/counter to place over the original one on the poster (which was incorrect and actually led to the GDPR website in Italian).

I can’t say I was fully satisfied with my pitch, but to be fair, I had a lot of excuses (it was in English 😵‍💫), and it was in line with the other participants' presentations.

We spent the rest of the morning and afternoon presenting the project to some guests from schools and companies, though I’m afraid the language barrier was a bit too thick for them to fully understand it…

Around 5 pm, the awards ceremony began, just after receiving some very helpful feedback from judges Ange and Dominique (thanks again).

With little fanfare, they went straight to the announcements, and after presenting the winners of the [ARC](https://www.csaw.io/research), surprise!

![Photo of us on stage for the victory](/csaw2024/winning_photo.png)

![Photo of us with the trophy](/csaw2024/trophy.png)

It was truly a proud moment. Initially, we just wanted to build a respectable project that would allow us to go to France. But as we refined it, our project became more structured, and with each improvement, our hopes of winning grew. This progress required tremendous effort from Ryan and sacrifices from me. We could definitely have done better, but for now, we’re happy with the outcome: we laid a solid foundation for our idea, something we might develop into a more comprehensive and structured project in the future.

# Post-Final
A well-deserved break in France. Ryan and I started the next day at noon (my fault).

![Photo of breakfast at a chocolate shop with a view of Champ de Mars, Valence square](/csaw2024/french_breakfast.png)

That breakfast at the chocolate shop somehow cost about as much as a regular breakfast at a café in Rome. The bag also included some macarons (I used to think they were universally tasteless until I tried them there, and they’re actually delicious).

Then we visited the Valence park, the one from the TRX photo

![View of the main square in Valence park, still with Paris Olympics decorations](/csaw2024/parco_valence.png)

I loved that they kept the Paris Olympics setup. It might just be laziness, but the effect of the square gradually revealing itself, initially hidden behind Champ de Mars, is truly spectacular.

A unique sighting in a public park

![Fantastic animals and where to find them](/csaw2024/parque.png)

Touching grass with 2000 things in tow

![Literally me at the park](/csaw2024/me_al_parco.png)

We then visited the Valence Museum of Art and Archaeology (with free public exhibitions)...

![Photo of a corridor where the public exhibition is set up](/csaw2024/mostra_valence.png)

...and the Church of St. Apollinaris.

![Glimpse of the Church of St. Apollinaris in Valence](/csaw2024/st_apo.png)

I was surprised by the quantity and quality of Italian paintings we found in Valence. I might need to start exploring more of these back home.

Finally, sadly, November 10th arrived, and it was time to head back. After a brief visit to Lyon...

![Photo of us at the shopping center](/csaw2024/centro_com_lione.png)

...we arrived at St. Exupery Airport, (maybe) ready to depart.

![Group photo with the TRX team at the airport](/csaw2024/tutti_in_aereo.png)

Back to our beloved (and sometimes hated) Rome.

![Photo from the airplane window on the way back](/csaw2024/in_volo.png)

# Conclusion

I’m writing this blog post during the first free hours I’ve had since returning, exactly 7 days after departing and arriving in Rome. I have to admit, it's always hard to get back to everyday life after these events.

I had so much fun with the project, carrying it out to the end, even putting up stickers around the place—nothing major, but it’s definitely something I wouldn’t have had the courage to do publicly if it hadn’t been for a competition like this. The more time goes by, the more I feel that university, like school before it, is just an anchor to be carried as unobtrusively as possible. Probably a mindset issue.

Completing this challenge with Ryan, whom I’ve known for 7 years now, has a different effect. I’m certain that both he and I have emerged more aware of our strengths and weaknesses, and of the steps we need to take to improve, not only in communication.

Both of us have taken a small first step into two worlds we’ve been getting to know for a while but had never really touched. For Ryan, it was mainly a test of commercial illustration, so he had to learn to use drawing elements to evoke specific emotions in the viewer. For both of us, it was a design test, which is different from art, and something Ryan hadn’t worked with before either, but still required creativity that I’d never needed until now, and somehow, we managed. My role was to handle communication in its entirety, from word choice to the order of things to present during the pitch, as well as deciding what to present.

Being resourceful and doing everything on our own gave us a bit of everything, especially since we carried out all the processes without using any form of artificial intelligence. We now have more tools to understand in which direction and how to specialize, how to proceed in the communication field on a larger scale.

I don’t know about Ryan, but I feel not only deeply motivated but also a strong sense of weight—the realization that I can take so many alternative paths, and I can do it now. I could simply cherish what we achieved in this competition, but I feel compelled to put into practice and improve what we worked on over these weeks.

Thank you for making it all the way here. If you have suggestions, proposals, or just want to get in touch, you can find me on [LinkedIn](https://www.linkedin.com/in/tiziano-caruana/). I know, a bit formal, but I reply quickly, and I don’t bite, promise!

ε=ε=┏( >_<)┛

![Ryan and me at Champ de Mars](/csaw2024/mashers_x_gem.png)