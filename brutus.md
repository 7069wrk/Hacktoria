# **Hacktoria — Operation Brutus**

Come along with me on a journey through the third in a series of CTF presented by the creators of [**HACKTORIA**](https://hacktoria.com/). This is a record of my process through [_**Operation Brutus**_](https://hacktoria.com/monthly-ctf/operation-brutus/); which in all likelihood will result in a novelette of detail that will frighten the executive minded while making the 2-year-old in the dusty parts of your psyche do its happy dance.

---

Let's bring the bottom line to the top and answer the question

_“Was it worth the time and self-inflicted frustration?”_

Absolutely! It is also worth noting that I had also just completed the preceding CTF — [_**Operation Runner**_](https://hacktoria.com/monthly-ctf/operation-runner/), for which I did complete but did not present my final intelligence because I had lost confidence in my findings. That was my first hurdle because I have this disease that when I sink my teeth into something I find it nearly impossible to let go and move on, so I kind of hesitated in starting Brutus given the outcome of Runner until I had confirmed I had been correct. (_silly — I know_)

> _**WARNING!!!** If you think you might be interested in going and trying your hand at completing the CTF series… please don't read any farther because from here on it will be me reliving the events from March 3, 2022 through March 22, 2022 — of which will include solutions to the operation._

![https://hacktoria.com/monthly-ctf/operation-brutus/](https://miro.medium.com/max/700/1*YvvahDwPoS-78-OPXSQ1uA.png)

**Disclaimer**: I will do my best to not take you down all my rabbit holes. There were plenty. Instead, if I mention something and note that there was a rabbit hole, I may have to leave you wondering — and if you want to know what happened — just ask me and I will happily tell you the story. But for the sake of your sanity, I will try to only mention my dead ends and not try to lay more roads through them.

**The Mission**

If you clicked the link in the opening and read the brief you know that the CTF begins with the Tiberian Serpent asking for our help to map out a wildlife smuggling operation that was exposed by a subject that is in custody. Maksim, the subject of the previous two CTF, has tried to cut a deal, and among other things, he has provided a handler file that is now available to you in the dropbox address provided in the brief. The end game is to use the handler file to answer the questions about the target animal species, the location of the camp and hunting grounds, the departure port, the destination port, etc… all in the hopes of making a bunch of arrests.

**Getting Organized**

I started by accessing the [Dropbox](https://www.dropbox.com/sh/2yl7wty4m6y02qd/AACSBr89vxCqjBNlJGzJEwhxa) folder and downloading its contents to a location of my choosing. Once the handler files are local we find a file with no extension and two folders: destination-and-market, hunt-and-departure each containing files and the mysterious archive that was mentioned in the brief.

Then I created a CherryTree notebook in the folder root where I did a copy/paste of the questions into the notebook. This action later caused me a great delay in completing the challenge but that is a story for another time— or you can read it in the Discord channel where I wept and moaned after realizing my error. Anyway, back to the challenge.

### **STEP 1 — The note**

I first started with the file with no extension, taking a chance that a text editor would read it, I opened it in Notepad++ and found the following:

> panderoshipping.cf
> 
> 您好， 这是本月狩猎和装运的快速说明。 通常的狩猎场和动物，这次可能会带一个Sheng语翻译，如果需要，请拨打 +254 41 555 555 0。 一旦您获得 200 只动物，请安排发货，并确保在网站上已为客户准备了追踪的详细信息。 您的市场联系人是 Wendy Liu，她会带上ID证件并在码头等候。 在某些时候，她可能会通过电子邮件向您发送有关货件 ID 的信息。不用担心她会说中文，这次不会使用英文。 她在当地有交通安排会将货物运往市场。 她将穿着一件蓝色雨衣和红色围巾，以供识别。

Google Translate to the rescue and it produced the following:

> panderoshipping.cf
> 
> Hi, Here's a quick note on hunting and shipping this month. The usual hunting grounds and animals, this time may bring a Sheng language interpreter, call +254 41 555 555 0 if needed. Once you have 200 animals, schedule the shipment and make sure you have the tracking details ready for the customer on the website. Your marketing contact is Wendy Liu who will bring her ID and wait at the dock. At some point, she may email you information about the shipment ID. Don't worry she can speak Chinese, not English this time. She has local transportation arrangements to transport the goods to the market. She will be wearing a blue raincoat and red scarf for identification.

### **Step 2 — Dissecting the note**

My process is to break things like this into simple statements that match how I would read it if I were trying to ask someone on the other end of a phone call to “write this down”. So the note became:

> Hi,   
> Here's a quick note   
> on hunting and shipping   
> this month.   
> The usual hunting grounds   
> and animals,   
> this time may bring a Sheng language interpreter,   
> call +254 41 555 555 0   
> if needed. Once you have 200 animals,   
> schedule the shipment   
> and make sure you have the tracking details ready   
> for the customer   
> on the website. Your marketing contact is Wendy Liu   
> who will bring her ID   
> and wait at the dock.   
> At some point, she may email you   
> information about the shipment ID.   
> Don't worry she can speak Chinese,   
> not English this time.   
> She has local transportation arrangements   
> to transport the goods   
> to the market.   
> She will be wearing   
> a blue raincoat   
> and red scarf   
> for identification.

### **Step 3 — What do we know from reading the note?**

The hunting grounds and animals are most likely in a location where they speak _Sheng_. So I started by Googling ‘Sheng’ and found out that it is _**a SWAHILI/ENGLISH cant**_ spoken in _**Nairobi and Kenya**_. This creates a high probability that the hunting grounds are in one of those two places. So the answer to questions 4 and 5 could be in one of those countries and they are in Africa. (_I didn’t have to google that_)

Next, I did a [reverse lookup](https://www.searchyellowdirectory.com/reverse-phone/254415555550/) on the phone number (+254 41 555 555 0) and found it is a landline in Mombasa, Kenya. This gave me a higher degree of confidence that the hunting grounds and camp were in or around Mombasa.

Continuing through the note we find the answer to questions number 15 and 16.

> 15\. Name of contact at the market?    
>      **WENDY LU**  
> 16\. Description of contact at the market?   
>      **WEARING A BLUE RAINCOAT AND A RED SCARF**

At this point, I make the _assumption_ that the market will be geographically in a region where they speak Chinese because there was an effort to communicate that she spoke Chinese, not English. I wish I could say that the mention of a dock gave me a clue but the word dock is used interchangeably in several areas so I stopped there and went back to the files to review the 2 folders. For what I hope are obvious reasons I started in the **hunt-and-departure** folder.

### **Step 4 — Hunt-and-Departure**

Here I found (8) eight image files — 5 png and 3 jpg. I would really like to tell you that I only spent a few moments here but… I really went off the rails for a bit. Later I learned that I wasn't the only one; which made me feel better. (smile)

Using image viewer I tabbed through the files a few times. Where I learned that the use of the word dock was for a marine dock and that the departure dock (at least to me) was pretty distinctive.

![](https://miro.medium.com/max/700/1*vwT0Bs9_5mmVNgLQzsCPbw.png)

After a few passes, I then decided that the clue about the handlers poor opsec may be why 5 images are png and not jpg. So [FotoForensics](https://fotoforensics.com/) here I come… I learned that some of the files were edited with GIMP — but nothing else. So I went back to looking at the images.

Pivoting on the location of the phone number it was time for a little Google Earth’ing in Mombasa/Kenya (Africa that is) and after a few minutes in satellite view over Mombasa, we had a [lat/lon](https://www.google.com/maps/place/4%C2%B002'49.8%22S+39%C2%B037'16.6%22E/@-4.0471633,39.621264,17z/data=!3m1!4b1!4m5!3m4!1s0x0:0x3e5777ab2c01d35!8m2!3d-4.0471633!4d39.621264) for the dock (-4.048495622386647, 39.622739122810465).

> 6\. Harbor location the shipment leaves from?  
>      **\-4.048495622386647, 39.622739122810465**

![](https://miro.medium.com/max/700/1*8nJvOwi3tQV5lyY5GAd7Qw.png)

![](https://miro.medium.com/max/700/1*q3MPXqTxRGXBtz8mVRe5TA.png)

I will add here that I caused myself great frustration when I tried searching for the port entrance, based on the sign in the picture. Those letters “EBS” made me doubt my answer for the departure port, though the image matched perfectly, there is no guarantee that another port couldn't be similar and that the image was flipped and rotated. Anyway, I searched for “**EBS docks**” in Google… and found myself in Rotterdam… yea that is wrong but I had to look. So back to the story.

![](https://miro.medium.com/max/284/1*jgAMeKwHcdgoiixqDdCQtg.png)

![](https://miro.medium.com/max/502/1*m4z-b9kMBPGj60bOJSvA8g.png)

After I made it back from Rotterdam I did a reverse image search for the “harbour entrance.png” and low and behold… I found myself staring at the source for the CTF image. In which I found that “EBS” was “KEBS” aka: Kenya Bureau of Standards. ([link](https://www.google.com/maps/@-4.0398773,39.6324405,3a,75y,182.5h,91.58t/data=!3m6!1e1!3m4!1s13UY2V5-qvLXwBwnoZrZ3A!2e0!7i13312!8i6656)) This finding solidified my response to question #6 to include my new intel.

> 6\.  Harbor location the shipment leaves from?  
>  **KILINDINI PORT**  
>  **lat/lon: -4.046858290670876, 39.62130155090372**  
>  **aka: PORT OF MOMBASA**

So now we know where the departure port is, what about that ship and the hunting grounds or camp? Here I decided I needed to find the answers to questions 3–5; skipping 1 and 2 (smile).

On to question #3. I truly believed that identifying the animal species would have been harder than locating the camp and hunting grounds but after only a few minutes of reverse image searching the track files… I knew the animal species.

[Track1.jpg](https://www.garonga.com/blog/safari-camp-stories-double-pangolin-sighting/) — Image from an article about a double pangolin sighting  
[Track 2.jpg](http://4.bp.blogspot.com/-96Ol9VGdCUY/UQ1-PZuf4LI/AAAAAAAAARk/A_VfcLgaTHU/s1600/Img_4261.jpg) — An image from Pangolin Research Mundulea 2012  
[Track3.jpg](https://pangolins-namibia.blogspot.com/2010/) — An image from Pangolin Research Mundilea 2010.

I had confirmed that the target animal was a pangolin and got the scientific name from Wikipedia.

> 3.Scientific name of the animal and subspecies?  
>  **SMUTSIA TEMMINCKII | CAPE PANGOLIN**

Now I needed to find the hunting grounds, so looking at the images and seeing those two dirty little eyeballs looking back at me — I went to Google. (_I will explain the green lines later, but remember them_)

![](https://miro.medium.com/max/700/1*brmmu01r9tDR4aqpLgtCBQ.png)

_Hacktoria — hunting grounds_

In Google Maps, satellite view, I looked for red terrain. This, unfortunately, took me way out of bounds and I eventually gave up on that process. But not until I had spent a couple of hours doing the street view scroll. A special note here is that it did ultimately help me identify the campgrounds but I will explain in a few moments.

At this point, I started looking for the campgrounds with the mindset that no self-respecting hunter will camp extreme distances from where they will hunt?

![](https://miro.medium.com/max/700/1*RwvW_nfpnxkpJTKCwKbKiA.png)

_Hacktoria — camp street view.png_

So I played the game ‘Do you see what I see…?’ from that lovely Christmas tune ‘Do You Hear What I Hear’ and this is what I saw:

*   an ornate building (_red box_)
*   a fancy cement fence (_green box_)
*   a pair of roads — one for cars and one for trucks (_pink lines_)
*   a fuel station (_yellow boxes_)
*   3 sets of crossing stripes on the road (_blue boxes_)
*   and a geographical contour in the distance. (_purple box_)

There is more but I didn't look for the trees or the tall bush or the power poles, etc…

Target 1 was the building. I tried reverse image searches in Google, Bing, Yandex, Baidu, and nothing worked. I made an assumption thinking that maybe it could be a mosque but that wasn't helpful. (_even though it is a masque_) So I switched to the top view of the camp.

![](https://miro.medium.com/max/700/1*fzPqd_GwgVHXCch5dmSXTg.png)

I knew by comparing the street view to the top view that between the green lines was my approximate field of view. But what else is there to see? There is what looks to be a small community and there in the top right corner, I could see what looked like another road or “train tracks”. This is where my rabbit hole from earlier doing Google Streetview scrolling paid off. I had crossed some train tracks and recalling from my zoomed viewing I was almost certain that those were train tracks.

So I tossed a hell-mary and, “Hey Google, Mombasa + mosque + train” and bam — _whoop d’ere it is_!

[Mackinnon Road Station / Masque](http://www.friendsofmombasa.com/members-contribution-other/mackinnon-mosque-makindu-gurudwara/).

I laughed so hard I cried. I typed the text into Google Map and there was my hunting camp. I stepped down to street view and I found my Masque and my fuel station.

![](https://miro.medium.com/max/700/1*-NceuyS32YKj0J_NTLw-5A.png)

![](https://miro.medium.com/max/700/1*_myxn44_k__4NrQo1de6cQ.png)

> 4\. Location of the hunter camp?  
>  **BAGH ALI SHAH MOSQUE (MACKINNON ROAD)**  
>  **lat/lon: -3.7214301, 39.029731**

Now where the heck are those hunting grounds. I zoomed out on Google Maps and found nothing. The dirt looked right but nothing else did. Frustrated I leaned back in the chair and thought let me try tomorrow.

Zzzzzzz….

The next day I looked at the same image and still nothing. (_clue — I have a nasty habit of not closing browser windows so I really was looking at exactly the same image and same perspective \<\<\<\< perspective will become more important in a moment._ )

I closed the browser and opened **Google Earth Pro** where I started a project and marked everything I had found to that point. When I pulled the globe around to the campgrounds I found myself at the perfect altitude and in the proper perspective. North was North and so were all the other cardinal directions… and I saw the pyramid head staring back at me (_the green lines from above_). I zoomed in and measured the distance… I was right — no hunter camps far from the hunting grounds — 6 miles from the masque.

![](https://miro.medium.com/max/700/1*nnP1anS32apWw8yeQjNNpg.png)

> 5\. Location of the hunting grounds  
>      **KWALE COUNTY - KENYA**  
>  **pond 1 lat/lon: -3.653874853470648, 38.971686073257644**  
>  **pond 2 lat/lon:-3.6494475472892476, 38.984367096586624**

That ended the hunt-and-departure phase. Went back to the files and opened up the folder destination-and-market.

### **Step 5 — Destination-and-Market (and that damn archive file)**

In the destination-and-market folder, we find (7) seven files — 6 PNG and 1 7z. If you read the brief you know that Tiberian Serpent said that there was a personal archive, the previous handler had bad opsec, and that it may not be needed but there it is… all of that added up to “pfffff he has crappy opsec — this will be easy!”

I copied the 7z file to an online hashing tool then passed that hash along with the top 100,000 favorite passwords into Hashcat…

![](https://miro.medium.com/max/523/1*IW0kLz0INf2pzJfhpOJZUA.png)

You must say it in your head the same way they do in the cartoon… hehe

NOTHING!!! I mean it was 3 days too, and not a single password hit. So I thought maybe Hashcat went for a hashcrap… so I passed the same info to John The Ripper…

![](https://miro.medium.com/max/503/1*aTgll1V5wTUWb3NzljzPiw.png)

NOTHING!!! WTH is going on. I thought to myself how this clown supposedly sucked at opsec so much so that it cost him his life… and I can't find his password? Screw it, this must not be of any use, but I browsed Twitter and Discord to see if anyone else was having issues. I posted on Discord that I was having trouble with the archive. Someone who had already completed the CTF saw my chatter and they DM’d me. “You don’t need those files. Just use the brief and the images provided.”

OK.

So I regrouped and attacked the files I had. Meaning that I looked for all the information I could get from the files and I started with **FotoForensics**. Three minutes later — no longer looking for the password… I had the frigging password. Thank you FotoForensics.

![](https://miro.medium.com/max/605/1*QtXNgxznGooIp7JSl4SLiA.png)

There should have been a question about the password…

Yea — he may have had poor opsec but my computer would take the cumulative lifetime of every participant to the power of infinity. But there it is and I couldn't help myself… I immediately opened the archive file to find 26 images. I will add here that though others solved the CTF without these files — I would have not completed the challenge had I not gotten the archive opened without some other hints/clues.

I flipped through the 26 images a couple of times just to have some memory of them and then I went to the Market photo and looked for what was interesting to me. Then I woke up and realized I have no clue where to start looking for this other than in the archived images I saw street signs in Chinese. So let's go look for the market in the mindset that this is China.

![](https://miro.medium.com/max/667/1*aIl7gzVGZjWnsIMxJZKOsA.png)

Starting with the harbor-arrival.png and looking at the coastline of China, I quickly felt overwhelmed and switched to the market images.

I landed on market04.png where I found a number that wasn't blurred by the GIMP Master. Did a reverse number lookup on the number (15815059912)

![](https://miro.medium.com/max/700/1*pVCiCh-pf3tYvvu9-b64aQ.png)

The reverse lookup found ‘**Zhenzhen plum juice fruit**’ in **Shantou City** of the Jinping District in **China**. So the port may be near Shantou City — so off I flew in Google Earth. But after much time of searching the coast for the port image, I figured I was wrong or the image was a decoy. So I pivoted and asked Google for another hand. “Hey Google, plum juice wholesalers in China”. This led me to a random website that listed the Top #6: plum juice suppliers from China —

![](https://miro.medium.com/max/700/1*LjSt_8dz7vzIknBFgOYwxg.png)

I was immediately distracted by there being more than 6 locations listed… BUT after a bit of looking, I was able to reduce the list to the locations that are on the ocean. Each has ports but none matched the image until I got to Tianjin with its sea-facing long straight docks… and then there it was.

![](https://miro.medium.com/max/700/1*HSTqrRtx289B8tuz2I5sEA.png)

> 7\. Harbor location the shipment arrives in?  
>      **TIANJIN CHINA**  
>  **lat/lon:  38.9848058, 117.7287291**  
>  **PORT OF TIANJIN**

“Where O’ where is this market at, O where, O where can it be…?” That was me as I used Google Earth to swipe left, right, up, and down every waterway leading from this port. It was all a little too much at the moment so I took a couple of days off.

After my workcation, I asked myself, “So what's left?”. Looking at “**my list**” I only had a couple of questions left — WHOOHOOO!

**NOT!!!**

This is where I will explain the mess-up that I earlier eluded to when I was creating my notebook. When I pasted all the questions into my notebook something happened and several of the questions merged into 1 long question. I don't know why, but because at this point I had not numbered the questions… (_Though I have been numbering them for you._) I thought I was close to finished. Once that was corrected and questions numbered I could then see that I had more work to do and I fell into a great sleep that lasted 20 years… Oh, wait that was someone else. Anyhoo… Where were we? Oh yea — looking for the market.

### **Finding the Market**

In finding the market I had already established that zooming around Google Earth wasn’t the answer. That is partly because there are a lot of waterways in and around Tianjin. So it was time to look deeper at the personal-photos-cheng.7z. (_later lovingly renamed to personal-photos-dead-guy-cheng.7z_)

The first thing to note is that if the numbers were supposed to represent the order in which the images were taken — I never found it, but I did decide that I would geolocate them in order (0–25).

So, as to not repeat myself and you start skipping past things, the process was to pass each image into Google, Bing, Baidu, and Yandex. I also did some Google Translating using my phone pointed at street signs to try and help identify direction and location. Below is a list of the ones I ultimately geolocated:

**Extract0** — Tianjin West Railway Station (lat/lon: 39.1551139, 17.1486383)  
**Extract3** — Tianjin Binhai International Convention and Exhibition Center (lat/lon: 39.028021, 117.7235242)  
**Extract4** — Bridge to Hebei from train station (lat/lon: 39.157704, 117.1738437)  
**Extract6** — Tianjin West Railway Station — Bus Depot (lat/lon: 39.155161, 117.1589203)  
**Extract9** — Tianjin West Railway Station — Flowerbed (lat/lon: 39.1551823, 117.1555743)  
**Extract10** — Approaching Tianjin West Railway Station(lat/lon: 39.1551697, 117.1608678)  
**Extract11** — I know what the rock says, “Tianjin Binhai Hi-tech Industrial Development Area”, but I never found the building.  
**Extract13** — Hebei, Tianjin, China — This one was fun. Ended up finding the original image on the [Wayback machine](https://web.archive.org/web/20161024134539/http://www.panoramio.com/photo/71542974), taken by Matthew Summerton, hosted on Google Panoramio, taken on May 4, 2015, @ 0831. This lead me into multiple rabbit holes that were all dead ends. Actually not sure this was supposed to be found but I did. (lat/lon: 39° 11' 12.00" N 117° 12' 58.80" E) yes, I copied and pasted it from the WBM.  
**Extract14** — Taken from a building looking NE, and I believe is in the direction of Extract13, but never dug any further. (lat/lon: 39.1605462, 117.1796351)  
**Extract17** — Tianjin West Railway Station — Inside looking North from the South entrance is my assumption based on the order of the terminals. (lat/lon: 39.1551139, 117.1486383)  
**Extract19** — Beining Park — Temple (lat/lon: 39.171264, 117.2063974)  
**Extract20** — Beining Park — Lighthouse, according to Yandex this is at the same park as Extract 19 and though I think I see the structure from the satellite view, it is very hard to know because I was never able to get a street view (lat/lon: 39.168827, 117.2060656)  
**Extract21** — Field of view while driving South West on the S11(lat/lon: 39.0020193, 117.7148195)  
**Extract25**— View from a building just behind Extract 3 looking North East (lat/lon: 39.0379025, 117.7174612)

I ran through the weeds on the others spending no more than about 30min on each. (_there is some time invested for sure_) In the end, as I previously mentioned, I would have never found the market had I not done this, and just like the last place you look for something is where you find it… so was finding the market.

I started looking for my stick person near a bridge at Tianjin Port and worked my way inland.

![](https://miro.medium.com/max/653/1*2gJGZdouhRvuolrQ03734A.png)

![](https://miro.medium.com/max/700/1*Wo5BNxya8-USd84-tnnWkw.png)

The market is the last pin at the left in the image above. (see it better below) Another thing to note is that though I am showing you the location of the market — I didn't know its location when I started this process.

![](https://miro.medium.com/max/700/1*fa5FL7VuQEfx_i7Fn4X8iw.png)

Unable to find my stick person near any of the pins around the port — I started zooming around near the remaining pins. I started with the most Easterly pin because many of the personal images were taken while driving. (just the way my brain works)

At each pin, I moved North, South, and East because the rest of the pins were West. When unable to find the stick figure I moved on. This meant that when I finally made it to the train station pins I had only one direction to go and that was West young man… and there he was — my stick figure.

![](https://miro.medium.com/max/700/1*zkfEqacnVvMIbbpNUP356Q.png)

> 8\. Location of the market \*  
>  **HONGQIAO DISTRICT, TIANJIN, CHINA**  
>  **Lat/Lon: 39.17597339315514,117.14426175670968**  
>  **XIANYANG N RD - Between GUANGRONG AVE and ZHONGIJA W AVE**
> 
>  **Possible buildings:**  
>      BEICHEN TOBACCO & ALCOHOL SUPERMARKET  
>      HUIJIA SUPERMARKET?

### **The Next 5 days**

Believe it or not, everything so far has only taken 10 days. For the next 5 days, I tried to find the date/time, ship, shipment ID, shipment handler name, phone, and email. I thought I needed to call the phone number in Mombasa or the one found in the market photo, I even Identified the ship in the Mombasa port photo — The BW TRITON. But something told me I was wrong.

So I asked for a hint which really only crashed me into a bigger wall. The hint was something to the effect of “no you don't need to call but there are other forms of communication.” Keep in mind that The only thing I have found is: 2 phone numbers, 2 ports, a market contact, and some locations.

\* Do I need to look for a Wendy Lui in Mombasa or Tianjin?  
\* Will she be easy to find?  
\* How many Wendy Lui will there be in either place?  
\* Do I need to look harder for the phone numbers that lead to an email or some other social media association that I need to use?  

On and on I went… looking for what I was missing.

Now some of you rock stars may already know what I was missing, but I had no clue because my mind was fixated on the wrong things. The funny part is that I even shared my process on Discord and still didn’t catch my oversight. I stayed in my vapor-locked state for 2 more days. During those days I kept monitoring Twitter and Discord while everyone said there was a hint on Twitter, you don't need the files from Cheng’s archive, the website stopped working… There were hints falling all over the place, but I wasn't processing them. Eventually, I gave up. I posted what I had found on Hacktoria and for each one that I hadn’t found I wrote — “couldn't find” just hoping for an email that said I was right on what I submitted but wouldn’t get credit, and I would be fine with that. Why did I do that? Because I had completed Operation Runner, but lack of confidence in my findings… left me unwilling to post because I wasn’t sure.

After submitting I went to Discord and posted what I had done. A couple of other participants pinged me on the side asking for some support. So I did what I could to help them — all while the whole thing ate away at me. I AM MISSING SOMETHING OBVIOUS!!!

### **Cut to the end dude!**

On March 20th, I saw someone make a comment about the website again and I commented something to the effect that the Wayback machine (if the hint) is useless unless you know what you need to look at.

Then like the light from the halo of a nuclear angel, the words came through… “I think it is in the text file, around the beginning”

![](https://miro.medium.com/max/300/1*wesl7AqRi4dkMYO4wyKecw.gif)

OMG!!! I had gotten so hyper-focused on TRANSLATING THE TEXT that I forgot about the first line…

> **panderoshipping.cf**
> 
> 您好， 这是本月狩猎和装运的快速说明。 通常的狩猎场和动物，这次可能会带一个Sheng语翻译，如果需要，请拨打 +254 41 555 555 0。 一旦您获得 200 只动物，请安排发货，并确保在网站上已为客户准备了追踪的详细信息。 您的市场联系人是 Wendy Liu，她会带上ID证件并在码头等候。 在某些时候，她可能会通过电子邮件向您发送有关货件 ID 的信息。不用担心她会说中文，这次不会使用英文。 她在当地有交通安排会将货物运往市场。 她将穿着一件蓝色雨衣和红色围巾，以供识别。

### **The End is Near**

I quickly pivoted, pasted “panderoshipping.cf” into the browser address bar and there it was — the finish line. (_Or so I thought_)

![](https://miro.medium.com/max/700/1*zYPdgdjtwn5DcFDKsy5VhA.png)

I didn't waste any time looking at source code or doing whois searches to see if our host owned the domain… I went straight to the contact page and looked for a contact

![](https://miro.medium.com/max/528/1*BfYiDv8usN3lHUwpu4pwCQ.png)

Taking the email address from the screen, I went to a disposable email site and after crafting an email and just about to click send — I heard the voice in my head, “\*\*Are you sure this is the answer?\*\*” and I stopped. This isn’t it — why was the Wayback Machine mentioned?

So I went back to Discord and I saw the comment about the page needing to be taken down because some rock stars set about hacking the box… (_Bad rock stars — no hacking in this CTF!_)

That was it. I needed to bring Pandero Shipping up in the WBM. But what part of the site was taken down? Clicking on each menu item I found that the tracking system was offline.

![](https://miro.medium.com/max/519/1*sKt8PmHgJM5ewnSc_-mMUA.png)

Went to the WBM:

![](https://miro.medium.com/max/526/1*XZdPMKzTp2U5R1pjYxKGLA.png)

Pulled up the oldest change and clicked on the Tracking menu item and was able to find the tracking feature.

![](https://miro.medium.com/max/700/1*auFwQr4It6B7K--ebk4Mvw.png)

Then I clicked on Contact and there was Oliver… the clown I had been looking for this whole time.

![](https://miro.medium.com/max/576/1*okPsawK41Dq5WwJ0RpUnqg.png)

> 12\. Shipment handler full name?  
>      **OLIVER ZEIS (LEUNG)**  
> 13\. Shipment handler personal phone number?  
>      **+825 4124 9131**  
> 14\. Shipment handler personal e-mail?  
>      [**OLIVERZEIS@protonmail.com**](mailto:OLIVERZEIS@protonmail.com)

Went back to my disposable email and rewrote my social engineering sentence and then stopped again. Flipped over to Discord and asked someone I knew who had finished if they had emailed Oliver. They replied yes and I told them my plan. They said, “but Cheng is dead” to which I replied “I am taking a chance that Oliver is as much of a knob as Cheng was.” then I clicked send.

> SUBJECT: 错误的追踪号码  
> 梁
> 
> 你能把我的货物的跟踪号发给我吗，我放错地方了吗？
> 
> 程

And…

![](https://miro.medium.com/max/410/0*9kSx5jXm8dexAUBA.gif)

Nothing. So I tried again from another site and again nothing. Did I word it wrong? Is Oliver on to me? Was my peer correct and Oliver knows that Cheng is dead? I did a test — send an email to my Protonmail… and SILENCE. It would appear that Protonmail doesn't like disposable email vendors.

a.sockpuppet.acct@protonmail.com to the rescue and a new email was sent.

> SUBJECT: 错误的追踪号码  
> 奧
> 
> 利弗我現在處於低調狀態，無法訪問我的任何系統或信息。你能把我的貨物的跟踪號發給我嗎？
> 
> 程

![](https://miro.medium.com/max/498/0*zpU11H20fJq4ofsi.gif)

Still, nothing I needed 3 more answers and I knew that if I could get the tracking ID this would be over. Hmmm. Maybe “Oliver” doesn't want to translate. So I translated my message to English and resent.

> SUBJECT: misplaced tracking number  
> Oliver, 
> 
> I am lying low and cant access any of my systems or information right now. Can you send me the tracking number for my shipment?
> 
> Cheng

and… still, nothing.

It is now March 22nd, I am sitting here getting ready to start my workday when I see one of the Hacktorian Masters chatting away on Discord. So I just start responding to the chatter. Then someone “me” mentioned that Oliver must be really busy. To which one of the other Masters responded, “Yea, he is talking to you.” Seconds later we learned that “Oliver’s” proton account had logged him out, then 2 minutes later… (buzz buzz)

![](https://miro.medium.com/max/384/0*zwflDb8KzONojcuS.gif)

It took less than 5 minutes after that for me to submit all responses based on Oliver’s response:

> 您好，  
> 没问题，发货ID是  
> CN555701D10TWITT66  
> Kenya → China  
> 25.03.2022 at 15:00 local time, ship Pangea  
> 祝 安康  
> Oliver

which translated to

> Hello   
> No problem,   
> the shipping ID is CN555701D10TWITT66   
> Kenya → China   
> 25.03.2022 at 15:00 local time,   
> ship Pangea   
> **Wishing you good health**  
> Oliver

Well Cheng is dead — but thanks for the answers I needed:

> 9\. Date and time of arrival?  
>  **25.03.2022 at 15:00**  
> 10\. Shipment ID?  
>  **CN555701D10TWITT66**  
> 11\. Name of the ship?  
>  **PANGEA**

With all responses posted the calm began to settle in.

### **I did it. I really frigging did it.**

And now you may ask, “why the celebration?”. Well after many years in what is today lovingly referred to as Cyber Security and technology… with certifications that have ranged from MCSE to CEH /CHFI, CNE, LPT, and others (_all expired so don't drool I have a disease called “prove you can do it” and then I move on to the next thing_) I had only ever completed one other CTF in my life. So for me it was a celebration:

![](https://miro.medium.com/max/312/0*FUBvPq4shE10CIxO.gif)

And yes — I am old enough to be some of yalls grandparent, maybe even great grandparent so this is FKN AWESOME!

### **What did I learn?**

The first thing I was reminded of is that **I am always my worst enemy**. I know my weaknesses and flaws ( the same as you probably know yours) yet I still forget to ask myself to start from the beginning and ask “Have I done my own processes completely?”, or did I get in a hurry and overlook the obvious. This is why I suck at tests — I tell myself to read slowly and deliberately… because I need to — and invariably I will go too fast and incorrectly respond to something that had I read it once more I would have probably responded correctly.

Though there is much I may have learned— this one was the best reminder. **I am not the only one** having an issue. I have a bad habit of considering everyone else so much better than myself. I burn soo much energy feeling that way and giving up. Sounds odd given that I mentioned that I never let go. So don't misinterpret “giving up” as “letting go”. If I bury my teeth into something you can bet I will eventually figure it out. Because as I lay there with my teeth sunk in I will eventually slow down enough to redo my processes and find a new pivot point. Or I will find a previous point and realize I needed to change perspective — how I am looking at it. Call it bias if you will but in the end, it boils down to a shift of some form on my behalf.

### **Closing**

I hope you enjoyed my ride. It was plastered full of diversions, some profitable and some not. But in the end, I had a blast and will for sure do it again, and again… (You get the point)
