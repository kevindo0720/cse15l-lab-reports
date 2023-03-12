# LAB 5 REPORT

In this lab, I will redo lab report 3 but with a differnet command. In lab report 3, I show you the alternative terminal commands to `less`, here, I will 
show the alternative commands to "grep".

Through the use of [chatGPT created by openAI](https://openai.com/blog/chatgpt), I was able to obtain other terminal command alternatives to `grep`, including: `grep -r`, `grep -i`, `grep -v`, and `grep -c`.

# GENERAL DESCRIPTION OF LESS AND HOW IT WORKS
grep is a command that searches for a given pattern in a single file or multiple files.

# 1) grep -r
`grep -r` is a command line that searches for a pattern recursively within a directory 

In example 1, I will use the Fletcher's directory in the non-ficton folder and use `grep -r` on the entire directory to find all lines that contains the 
word "parochial"

**Example 1:**
```
kevindo@Kevins-MacBook-Pro-2 OUP % grep -r "parochial" /Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/non-fiction/OUP/Fletcher/

/Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/non-fiction/OUP/Fletcher//ch1.txt:Seeking redemption under the law cannot simply be a desire for one’s parochial values to triumph in the courts. It matters which values are in play. And it matters how these values are debated in the legal culture. Debate about legal issues must be open and robust, and the very process of legal argument must communicate respect for the opposition. At the end of a legal argument, both sides must have the sense that they have been listened to, and that the dignity of the losing party is affirmed in the process of decision. Here, as well, we have much to learn from the model provided by the Jewish tradition of Talmudic debate. When a rabbi questioned how two of the greatest sages, Rabbis Hillel and Shammai, could persistently disagree, the response was: “These and these are the words of the living God.” Although Rabbi Hillel’s views are generally followed, Rabbi Shammai is treated, in defeat, with the greatest respect.
/Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/non-fiction/OUP/Fletcher//ch5.txt:Taking the “privileges and immunities” of citizens as the pivotal value of the new order, as Black does, creates its own problems of equality under law. Why should only citizens and not resident aliens enjoy the inalienable rights of “life, liberty and the pursuit of happiness?” Do not immigrants and even undocumented illegals have rights as human beings? The universalist language of the Declaration of Independence hardly dovetails with the parochial category of citizenship in a particular governmental polity. If all men are created equal, if we are endowed by our Creator with certain inalienable rights, it cannot be the case that these rights are limited to those who are classified as the subjects of a particular sovereign.
/Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/non-fiction/OUP/Fletcher//ch9.txt:The opposition to victims’ rights stems from both prosecutors and defense counsel. The former do not want victims complicating the trial. They are surely opposed to my proposal that victims be able to veto plea bargains and insist on going to trial to vindicate their charges.11 Prosecutors generally like to have victims around at the sentencing phase. The suffering and rage of the victims, when expressed in court, tends to spike the punishment. Defense counsel are opposed for other reasons. They are afraid that empowering victims will distract from the rights of criminal defendants, but this is not necessarily the case.12 The victim’s interest is primarily in participating in the trial. He or she may communicate a desire for conviction but that parochial sentiment of interest will be readily discounted by the commonsense responses of the jury. The fact is that it is possible to strengthen the participatory rights of victims without unduly complicating the procedure or compromising the traditional rights of the defense.
/Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/non-fiction/OUP/Fletcher//ch10.txt:The problem of exploitation in apparently voluntary sexual relations has long been with us. In the late nineteenth century, the problem was whether the Mormon practice of polygamy should be regarded as protected as liberty and the free expression of religious conviction. Those who defended the institution, as provided in the accepted Mormon religious doctrines of the time, cited its social benefit of caring for all the women and children in a society in which the available men had fallen victim to the hardships of settlement and warfare. The critics, by contrast, claimed that the choice of the women in these cases is not really free and voluntary. John Stuart Mill, a great advocate of liberty, sided with the critics of polygamy.15 Western governments have had no qualms about prohibiting the practice, sometimes for parochial religious reasons, sometimes out of solicitude for women who are subjected to an institution that arguably diminishes their status. The Mormons sued, thinking they had the kind of argument that eventually prevailed in the Lochner case. In 1878, the Supreme Court upheld the conventional view that the prohibition represents permissible intervention by the state to protect the weak against entering into exploitative relationships.16 Many voices today argue that this decision was wrong. The freedom to choose any form of domestic arrangement one wants should prevail against the state’s concern to protect people against their own potentially bad choices.
```
Here thre are instances in ch1, ch5, ch9, and ch10 that contains the word "parochial".

**Example 2:**
Similarly, in example 2, I used `grep -r` to find the word "ice skating" in the entire travel-guides directory

```
kevindo@Kevins-MacBook-Pro-2 written_2 % grep -r "ice skating" /Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/travel_guides/
/Users/kevindo/Documents/skill-demo1-server/skill-demo1-data/written_2/travel_guides//berlitz2/Poland-WhatToDo.txt:For kids with energy to burn, there are water parks and swimming pools (see above) in summer and ice rinks in winter. To go ice skating, check out the Stegny Skating Track (Tor Lyzwiarski Stegny), (ul. Inspektowa 1, Tel. 842 27 68) or Torwar (ul. Lazienkowska, Tel. 621 44 71) in Warsaw. Another activity that is all the rage is paintball, and there are multiple fields where you can inflict paint rather than pain. Try Marcus-Graf (ul. Widok 10, in Beniaminów near Warsaw; Tel. 816 10 08), TM Pretor (ul. Zaaruskiego 6, Warsaw; Tel. 838 25 35), Rival Paintball Guns (ul. Bartosika 10/77, Warsaw; Tel. 671 22 63), or Extreme Sports (ul. Klaudyny 18/5, Warsaw; Tel. 833 73 73). Paintballers in Kraków should check out Ultimate Sports (near fort Bodzanów; Tel. 431 20 61). 
```

Here, I was able to find "ice skating" in Poland-WhatToDo.txt file.

# 2) grep -i
`grep -i` searches for a command regardless of the case. In other words, `grep -i` is case-insensitive. 

**Example 1**
Here, I used `grep -i` to search for the word "RoManTIC". Because `grep -i` is case insensitive, it will just search for all instances of "romatic" regardless of cases.
```
kevindo@Kevins-MacBook-Pro-2 berlitz2 % grep -i "RoManTIC" California-WhereToGo.txt 

San Franciscans are quite unashamedly in love with their town. Its natural setting, nestled in the hills around the bay, makes the city uncommonly cozy; the zip in the air is invigorating, and even the fog that rolls in off the ocean seems more romantic than chilling. If you have a car, one way to begin your visit is to travel along 49-Mile Drive, which provides a comprehensive tour of the main sights. You’ll need to use a good map, as the blue signposts with a white seagull in the center can be difficult to locate. Stop off at Twin Peaks (the road to get there starts near the southern end of Market Street) for an excellent panoramic view of the city and the bay, then park the car, put on a pair of comfortable walking shoes, and take to the city’s first-class public transport system (see page 120). 
At Nepenthe, Orson Welles built a honeymoon cottage for Rita Hayworth in the days when film stars did the romantic things expected of them by their adoring public. Now it has been expanded and converted into a restaurant, well worth a visit for its incomparable view of the ocean.
```

**Example 2**
Similarly, here, I used `grep -i` command to look for "ChEaP" in Budapest-WhatToDo.txt. As expected, it disregards the cases in "cheap" and just look for the word "cheap".
```
kevindo@Kevins-MacBook-Pro-2 berlitz2 % grep -i "ChEaP" Budapest-WhatToDo.txt 


Not very long ago, a fistful of dollars would have given you the freedom of most Budapest shopping streets. The end of communism, the imposition of VAT at 16 percent, and the effect of inﬂation have, however, brought an end to those bargain-basement days. As ever, artisans provide the bulk of the best buys, but it is worth bearing in mind that their hand-produced items can’t compete with the price of the mass-produced substitutes from the Far East. If something is extremely cheap, chances are that it’s a clever imitation.
```



# 3) grep -c

`grep -c` is a command that couns the number of instances of a given pattern.


**Example 1**
In this example, I used `grep -c` to count how many "Hong Kong" words there are in the WhatToHongKong.txt file.
```
kevindo@Kevins-MacBook-Pro-2 berlitz1 % grep -c "Hong Kong" WhatToHongKong.txt  
63
```
As shown, the word "Hong Kong" appears 63 times in the file WhatToHongKong.txt  

**Example 2**
In this example, I also used `grep -c` to find how many instances of "sushi" there are in WhatToJapan.txt  

```
kevindo@Kevins-MacBook-Pro-2 berlitz1 % grep -c "sushi" WhatToJapan.txt  
1
```
SURPRISINGLY and SHOCKINGLY, "sushi" only appears ONCE in the WhatToJapan.txt file.

# 4) grep -v
`grep -v` is a command that	shows all the lines WITHOUT the given pattern. It is also known as the inverted grep.

**Example 1**
Here I used `grep -v` to find all the lines without "Hong Kong" in the WhatToHongKong.txt file.
```
kevindo@Kevins-MacBook-Pro-2 berlitz1 % grep -v "Hong Kong" WhatToHongKong.txt 

 What to Do
        Shopping
        longer the bargain shopping destination it once was, there are still
        charges no sales tax, goods are cheaper here than in the country where
        they were made. On photographic equipment, electronic goods, and
        watches, you avoid the luxury tax payable in your home country.
        are still much in demand and cost less than elsewhere for comparable
        garments. Note that alcohol and tobacco are both exceptions to Hong
        Kong’s duty-free regime and are subject to tax.
        Central and Kowloon, and somewhat cheaper in Causeway Bay, which caters
        to local shopping. Large shops on the fashionable thoroughfares tend to
        be more expensive than smaller “family” shops tucked away in the side
        streets.
        Stores do not open until 10am or later, but shopping goes on
        into the evening, up to 9:30pm. Most shops are open seven days a week.
        Shops in Central are an exception; they generally close at 6pm and are
        not open on Sunday. The only holiday on which all commerce comes to a
        halt is the Chinese New Year in January or February.
        Buyer Beware. Be aware that name brands, including
        electronics, are sometimes fakes, glass may be sold as jade, and that
        antique you bought may have been made last night. Always ask for a
        receipt that records information about the item, and if you buy an
        antique, be sure to get a certificate of authentication. Needless to
        say, avoid peddlers who approach you on the street and offer to take
        you to wondrous bargains.
        The large department stores have fixed prices, but elsewhere
        you should ask whether there is a discount, especially if you buy
        several items in one shop. Compare prices before you buy any
        significant item. Always ask to see the manufacturer’s guarantee when
        purchasing watches, cameras, and audio-visual and electronic
        equipment.
        Note that when haggling, the merchant assumes you are
        prepared to pay cash. If, after concluding a deal, you try to pay with
        a credit card, he may then boost the price in order to cover the card
        charges.
        It is advisable to shop at outlets that are members of the
        Membership imposes an obligation to maintain standards of both quality
        and service, and provides dissatisfied customers with an officially
        recognized channel for redressing complaints; the number to call is
        Tel. 2508 1234. Pick up a copy of HKTA’s “The Official Dining,
        Entertainment & Shopping Directory” in which all member stores are
        listed.
        Shipping. Many stores will pack and ship purchases. Ask if
        automatic free insurance is provided. If the goods are very valuable or
        fragile, it is a good idea to buy an all-risk insurance for the
        shipment. Packages sent to the US or to Europe generally take six to
        eight weeks by surface mail, and one week by airmail.
        Shopping Areas. Major shopping areas are Tsim Sha Tsui in
        particularly for upscale designer goods; Causeway Bay for slightly
        better prices; and the Hollywood Road area.
        Department Stores. Look for Lane Crawford Ltd., an upscale
        store with branches at Pacific Place, 70 Queen’s Road, and Harbour
        the Japanese department stores, Mitsukoshi, Sobo, and Seibu.
        west of the Star Ferry Terminal in Tsim Sha Tsui is one of the largest;
        Pacific Place, 88 Queensway, is Central’s biggest mall, with retail
        outlets and department stores; Times Square is a collection of retail
        outlets in Causeway Bay. In addition, most top-line hotels have upscale
        malls full of designer boutiques.
        Factory Outlets. These stores sell excess stock or factory
        its clothing manufacturing has moved elsewhere. There are factory
        showrooms in the Pedder Building, 12 Pedder Street, in Central.
        Markets. Markets are the places to use your bargaining
        Street Night Market near the Jordan MTR stop. Every conceivable kind of
        goods is sold here: clothing, all kinds of electronics, CDs, souvenirs,
        crafts, and jewelry.
        and is well-known for all kinds of clothing, including silk and
        cashmere. Bargain, and carefully examine any merchandise you buy
        here.
        The Jade Market, on Kansu Street in Yau Ma Tei, is known
        for both jade and freshwater pearls. This is not the place to make
        expensive purchases, but it’s great for inexpensive pendants, earrings,
        and gifts.
        What to Buy
        Antiques. Hollywood Road in the Mid-Levels above Central is
        bronzes, embroidery, lacquerware and porcelain, tomb figures, and wood
        carvings, among other possibilities. The experts point out that it is
        not age alone that determines a Chinese antique’s value — the dynasties
        of the past had their creative ups and downs. For serious antiques, try
        Honeychurch Antiques at no. 29 for furniture and silver, Tai Sing
        Company at 122 for porcelain. For fun you can visit the Low Price Shop
        at no. 47 or the Cat Street crafts stores and flea market.
        Brocades and Silks. Fabrics from China are a bargain and
        well worth taking home. Chinese-product department stores stock silk
        fabrics, silk scarves, finely embroidered blouses, and traditional
        padded jackets. Chinese Arts and Crafts is at Pacific Place in Central,
        and in Star House in Tsim Sha Tsui; CRC Department Store is on Hennessy
        Road in Causeway Bay. For fabrics, also try Western Market, Morrison
        Street, in Central.
        buy some of the world’s most advanced photographic equipment, and there
        are some real bargains around. However, be sure you compare prices and
        models before buying. Two reliable places to start looking in Lan Kwai
        Fong are Photo Scientific in the Eurasia Building and Hing Lee Camera
        Company, 25 Lyndhurst Terrace.
        able to arrange shipment. Caravan at 65 Hollywood Road and the shops in
        The Silk Road at Ocean Center in Tsim Sha Tsui are good places to start
        looking.
        even a whole dinner service, hand-painted to your own design. Factories
        in Kowloon and the New Territories, producing traditional and modern
        china, are geared to entertain and instruct visiting tourists; prices
        are appealing. Two of the largest places to go are the Wah Tung China
        Company in the Grand Marine Industrial Building in Aberdeen; and the
        Overjoy Porcelain Factory in Block B of the Kwai Hing Industrial
        Building, Kwai Chung, in the New Territories. In antiques shops, look
        for highly valued porcelains from China. Note that because of the
        duty-free situation, good bargains may be found in European china,
        including Spode and Wedgwood.
        Electronics. The latest gadgets are sometimes available in
        HKTA’s “Shopping Guide to Consumer Electronics. ” Prices on electronics
        have risen in the past two years; check prices at home before you buy
        here. Nathan Road has many electronics shops. Also check out Star
        Computer City in the Star House near the Star Ferry terminal.
        Furniture. The choice ranges from traditional hand-carved
        Chinese rosewood furniture to well-made reproductions of modern Western
        styles. Rattan furniture is highly popular. Hollywood Road has several
        furniture shops. Queen’s Road East in Wan Chai is a furniture
        manufacturing and retail area.
        Jade. “ Good for the health” is just one of the many
        magical qualities that are attributed to these beautiful emerald-green
        or turquoise stones. Real jade is extremely expensive, and you may be
        offered counterfeit jade, which looks exactly like the genuine article.
        Some people say you can test the authenticity by touch — real jade
        feels smooth and cool. Alternatively, you can shine a lamp on the
        stone — real jade shows no reflected light. Better still, go shopping
        with an expert.
        Jewelry. Thanks to the duty-free situation, prices in Hong
        Kong are lower than they are in some other places. You can buy
        gemstones loose or set, or have them made up to your own design.
        Popular purchases include diamonds and freshwater pearls. If you do
        plan to buy jewelry, be sure to consult the “Shopping Guide to
        reputable dealer.
        Kitchen Equipment. Woks and any other gadgets essential for
        Chinese cookery make good purchases. Department stores sell all sorts
        of intriguing kitchen equipment.
        Locally made items do not live up to their European models. However,
        the leather garment industry is growing, and there is a wide range of
        locally produced leather accessories, all at extremely attractive
        prices. For European imports, you will pay top dollar.
        range of the most high-tech audio-visual, sound, and screen equipment.
        Before purchasing, visitors should make sure of compatibility with
        systems in their own countries. Be sure to look around and compare
        before buying. Whatever you buy, you may be able to work out a
        discount.
        recognizable European and many American labels, from top-end designers
        to the moderately priced or trendy. Nathan Road, Central, and the hotel
        malls are places to look. There are still a great many factory outlet
        stores with reasonable prices. You’ll also find bargain clothes for
        sale at the markets and on push-carts.
        Tailoring. Tailor-made clothes are not as popular in Hong
        Kong as they were in the past, but hundreds of shops still remain.
        Local tailors are experts when it comes to producing custom-tailored
        garments for both men and women, and are also adept at copying
        patterns. The result can be a quality suit at a fair price — but
        made-to-measure clothing is not cheap. In choosing a tailor, look for
        HKTA membership. Many tailors have Web sites or are listed on Web
        sites.
        Tea. Shops all over town will sell you gift tins of exotic
        blends. If you want to learn something about tea, go to the Tea Shop at
        149 Hollywood Road, or the Moon Garden Tea House at 5 Hoi Ping Road,
        Causeway Bay. The owners will brew up a pot so you can taste before
        making a choice.
        Watches. The saying “Time is money” is quite literally true
        and optical goods. An enormous variety of makes and models are on sale.
        Be sure to get the manufacturer’s guarantee stamped or signed if you
        buy a watch.
        Entertainment
        Day and night, the action goes on in this vibrant city. To
        Authority’s dining and entertainment guide for listings, or just simply
        Diary published weekly by HKTA tells what’s happening in the arts. Hong
        South China Morning Post has an entertainment section on Friday.
        Culture buffs are well catered to, and there is always a
        varied program of events, ranging from world-class concerts to local
        amateur dramatic productions.
        Arts Festival, a three-week dose of international culture in February,
        with concerts, recitals, plays, jazz, Chinese opera, and innovative
        productions put on by leading talent from both East and West. Tickets
        for the shows must be reserved well in advance. The Festival of Asian
        weeks orchestras, dance groups, opera, and drama companies from all
        over Asia.
        Western releases are shown in some of the larger ones. English-language
        films have Chinese subtitles. Films with Mandarin dialogue also have
        Chinese subtitles, for the benefit of Cantonese speakers, and sometimes
        subtitles in English.
        April. More than 200 films from all over the world are shown at this
        two-week event. Ask at City Hall center about advance reservations.
        The Performing Arts
        Center in Tsim Sha Tsui are the main venues for concerts and opera.
        Other performance centers are the City Hall cultural complex, with
        exhibition halls and theaters that present concerts, plays, and films;
        Centre in Wan Chai, where both local and visiting groups perform. Other
        centers for concerts, plays, and entertainment are Sha Tin Town Hall
        and Tsuen Wan Town Hall in the New Territories. Larger arenas,
        Ko Shan Theater in Kowloon play host to various concerts, pop concerts,
        sporting events, and variety shows.
        new and traditional works; a wide assortment of traditional and Chinese
        founded in 1975. Under its conductor, David Atherton, it offers Western
        classical works and new works by Chinese composers in a
        September-to-June season.
        Chinese Opera. Cantonese opera is alive and well in Hong
        Kong, and the two other forms, Beijing and Kun, are sometimes
        presented. To most foreigners, this unique art form is likely to be
        inscrutable at first exposure, but everyone can appreciate the
        spectacle and the elaborate, glittering costumes. Although the music
        may seem strange to the unaccustomed ear, it certainly won’t put you to
        sleep; cymbals and drums guarantee your alertness.
        City Contemporary Dance Company — perform regularly, often at the Hong
        Kong Academy for the Performing Arts.
        Theater. The two leading local troupes, the Chung Ying
        Cantonese; there are English-language performances at the Fringe Club
        theaters, 2 Lower Albert Road, in Central.
        Puppet Shows. The classic Chinese puppet is the shadow
        puppet, manipulated behind a screen by three rods, but hand puppet and
        marionette shows are also on offer, often for free at public parks and
        playgrounds.
        Nightlife
        raw, or cultured. Note that sometimes there is a cover charge of HK$50
        to HK$200 at clubs, which may or may not include a couple of
        drinks.
        There are nightclubs in the principal hotels, with bands,
        dancing, and floor shows. Many restaurants and bars have live
        music.
        Jazz fans will find live jazz presented by international
        artists at the Jazz Club and Bar, 2/F, 34-36 D’Agular, Central; and at
        the Blue Note in the Kowloon Shangri-La Hotel in Tsim Sha Tsui. The
        alternate entertainment venue, with jazz, rock, and other live music,
        in addition to a gallery for visual arts.
        Bars with views and live music include Sky Lounge in the
        Sheraton Hotel and Towers, Tsim Sha Tsui; and Cyrano in the Island
        Shangri-La in Pacific Place. Pubs are numerous. In Tsim Sha Tsui, Ned
        Kelly’s Last Stand on Ashley Road is an Aussie institution; Delaney’s,
        The clubs and bars of Wan Chai, long the center of seedy
        nightlife, have become almost respectable. Joe Bananas, 23 Luard Road,
        is a Wan Chai mainstay for all-night partying. Rick’s Cafe, 78-82 Jaffe
        Road, is a long-time disco that’s still popular. A lot of the raunchy
        action has moved across the harbor to Tsim Sha Tsui East; this is also
        where you’ll find pricey hostess clubs, popular with Japanese tourists,
        but definitely not for those on a budget.
        Today’s trendy spot is Soho (SOuth of HOllywood) around
        Hollywood Road, Elgin, and Stauton streets. Soho, along with the Lan
        lively bar scene. Causeway Bay also has a variety of bars and clubs.
        TOTT’s, in the Excelsior Hotel, is a restaurant with live music and
        dancing and a harbor view.
        Japanese karaoke bars have now become extremely popular
        with the locals. There are a number of these on Chatham Road South and
        around Cameron Street in Tsim Sha Tsui.
        Nightlife tours are offered by a number of companies. The
        most typical of these are harbor cruises, usually including dinner and
        dancing on board an air-conditioned floating nightclub. There are
        evening bus tours that include visits to a restaurant and night spots;
        some tours combine a Chinese banquet with a visit to an open-air market
        and the panorama from Victoria Peak.
        Sports
        Participant Sports
        free to the public. Most have lifeguards on duty from April to October,
        Bay is the most popular; others are Shek O on the east coast and
        Stanley and Deep Water Bay on the south coast. They are very crowded,
        especially on summer weekends. On the outlying islands, Cheung Chau and
        Cheung Sha are on Lantau, and Hung Shing Ye and Lo So Shing on Lamma;
        inquire about water pollution levels.
        visitors to its three 18-hole courses at Fanling in the New
        Territories, or the 9-hole course at Deep Water Bay. The Discovery Bay
        Golf Club on Lantau island (Tel. 2987 7273) has an 18-hole Robert Trent
        Jones Jr. course, open to visitors Monday, Tuesday, and Friday. Many
        play at the Guangzhou Luhu Golf and Country Club (Tel. 2317 1933 in
        Thomas.
        Hiking. In the New Territories the famous MacLehose Trail
        stretches 97 km (60 miles) from Sai Kung Peninsula to Tuen Mun. The
        Lantau Trail is a 69-km (43-mile) circular trail on Lantau Island that
        begins and ends at Silvermine Bay. Both trails are divided into smaller
        segments of varying difficulty. Maps of hiking trails are available at
        the Government Publications Center, Low Block, Government Offices, 66
        Queensway in Central. HKTA also has trail maps and sponsors the Guided
        Nature Walks, led by rangers, that include hikes in all the different
        Jogging. Victoria Park has a jogging track in Causeway
        Bay.
        Sailing. Because of the heavy harbor traffic, only sailors
        information.
        Taijiquan (Tai Chi). HKTA offers lessons in these exercises
        Admiralty (Tel. 2058 1234).
        Tennis. There are 13 public courts at Victoria Park Tennis
        Centre (Tel. 2570 6168), near Tin Hau Station.
        Spectator Sports
        Horseracing. All levels of society share a feverish
        interest in the Sport of Kings. The racing schedule is September to
        and members’ enclosure, and a buffet-style meal.
        in late September, brings teams from all over the world.
        Rugby. The Rugby Sevens sees teams come together from all
        over the world for 15 matches in March or early April.
        Tram is sure to provide a thrill, and in the Peak Tower they’ll enjoy
        the Peak Explorer ride and Ripley’s Believe it or Not!
        Ocean Park (see page 32) is popular with children of all
        ages. There’s a special Kid’s World that those under 12 can enter free
        when accompanied by a paying adult. The more daring can try out the
        terrifying roller-coaster rides.
        interest children of all ages. The Science Museum in Tsim Sha Tsui East
        allows children to get their hands on over half of its 500 exhibits,
        while the nearby Space Museum has regular screenings on an enormous
        Omnimax screen in its Space Theater, making the night sky come
        vibrantly alive.
        For children who love boats, riding the Star Ferry or ferry
        trips to outlying islands will be exciting, and the Dolphin Watch trip
        (see page 113) is certain to appeal. If you plan to visit during May,
        the carnival atmosphere of the Cheung Chau Bun Festival, with its high
        bamboo-and-paper towers covered in sticky buns, will fascinate the
        young ones.
```
Above are all of the lines that do not contain the word "Hong Kong" in WhatToHongKong.txt


**Example 2**
Here, I used grep -v to find all lines in WhatToJapan.txt without the word "Tokyo"
```
kevindo@Kevins-MacBook-Pro-2 berlitz1 % grep -v "Tokyo" WhatToJapan.txt   

  What to Do
        Shopping
        Modern Japan has embraced the consumer society to such an
        extent that shopping can be a full-time pursuit. The Japanese
        themselves (in the big cities at least) can be seen more often than not
        with some kind of shopping bag — they make very large, sturdy
        ones — just on the off chance that they might want to buy something.
        You cannot get to know this country properly, even if you don’t want to
        buy anything, without exploring the rich and varied range of
        traditional arts and crafts, the famous cornucopia of electronic
        gadgets and precision instruments, or the impressively awful selection
        of kitsch souvenirs in the major tourist centers.
        Japan is notoriously expensive, so don’t expect fabulous
        bargains. The country has succeeded economically by fixing the best
        price it can get for everything, but the domestic market pays high
        prices because of a stiff sales tax and surprisingly convoluted and
        inefficient distribution systems. Japanese tourists visiting other
        countries are still shocked to find Japanese consumer goods available
        for far less than they have to pay at home.
        Start by looking at the range of goods in the department
        stores and hundreds of specialty shops in the underground shopping
        centers before going off to find better prices at discount shops.
        Department stores generally offer superb selections of everything — but
        at Japan’s highest prices.
        You might be tempted to do your shopping at the end of your
        trip so you won’t have to drag all that electronic equipment,
        lacquerware, ceramics, or whatever around the country with you.
        Instead, consider buying everything you want as you go along, using
        Japan’s remarkably efficient and inexpensive takkyubin courier delivery
        services (available at the ubiquitous convenience stores) to forward
        your larger purchases to your hotel, where they will be waiting for you
        crime rates, you can be sure you’ll be reunited with your precious
        souvenirs.
        Hi-Tech Products
        item imaginable — and plenty that you didn’t even know existed — is
        Akihabara, an entire district devoted to specialty stores selling
        mountains of electronic equipment often at very low prices. The larger
        stores usually have a tax-free department offering a narrower range of
        products designed for use abroad. English-speaking sales staff are
        often on hand, but don’t expect the same discount prices that are
        offered on the other floors, despite the tax-free incentive.
        One draw for visiting gadget freaks is being able to buy the
        very latest equipment several months ahead of its sales launch abroad.
        However, cameras and electronic goods are rarely available at better
        prices than those in New York City, still the world’s reigning discount
        center. Those hunting for computer software and hardware should not
        expect to find anything other than Japanese-language products for
        sale.
        Osaka’s equivalent hi-tech shopping district is
        Nipponbashi, a very poor relation to Akihabara with neither the range
        Note that local electric current is 100 volts/50 (or 60)
        cycles, which is slightly different from the US and completely
        different from Europe. Therefore, if you don’t want to bother with
        converters, stick to the top-floor tax-free department specializing in
        export goods designed for use around the world. Also note that Japanese
        VCRs and TVs are designed for NTSC, the same broadcast system used in
        North America. If you plan to buy anything for use in Europe or
        elsewhere (where PAL is the main broadcast standard), make sure you
        purchase a multisystem unit; only these are compatible with the various
        broadcast standards in use around the globe.
        Cameras. As an exception to the general rule of not making
        big purchases until near the end of your visit, it makes sense to buy
        camera equipment as soon as possible so you can try it out during the
        trip. If a fault occurs, you can arrange to have it repaired or
        exchanged before you leave. Most stores are good about exchanging
        faulty goods. Note, though, that warranties are often valid in Japan
        only, so check with the manufacturer for details of upgrading to
        stores, although these rarely offer better prices than those available
        from New York’s famous mail-order outlets.
        Traditional Goods
        Kimono. Japanese silk kimono are magnificent but
        staggeringly expensive. Most Japanese people save up for years to buy
        one and then often spend an equal amount of time in debt after making
        the investment. If you’re not among the world’s wealthiest tourists,
        the good news is that new and nearly new kimono are usually sold for a
        tiny fraction of their new prices at the big flea markets held at
        temples, shrines, and other large communal sites. Many Japanese are
        highly superstitious about acquiring second-hand goods, especially
        English-language press for details of shrine and temple markets.
        Kyoto’s two biggest flea markets are held at Toji temple (the 21st of
        each month) and at Kitano Temmangu shrine (25th), but there are many
        others.
        Another alternative is the more modest but still elegant
        yukata (light cotton kimono), traditionally in indigo-blue and white
        and much, much cheaper than anything made of silk. Also look out for
        the silk obi sashes used to tie kimono. Some are magnificently
        decorative in their own right; if you don’t want to wear one, consider
        an obi as an original and unusual wall-hanging in a Western home.
        Antiques. For antique furniture and miscellaneous items,
        Kyoto’s famous geisha district of Gion has one of the finest selections
        in Japan. Even if you’re just browsing, the shops on Nawate-dori,
        Furomonzen-dori, and Shinmonzen-dori offer a superb selection of
        antique furniture, ceramics, masks, lacquerware, and Buddhist
        objects.
        Artwork. Attractively colorful ukiyo-e woodblock prints and
        scroll paintings can be found in antique stores, second-hand
        bookstores, and even temple markets. Prices vary enormously, so
        shopping around usually pays off handsomely.
        Pottery and ceramics. These are very much a living
        tradition that has maintained its high standards. Most regions have
        their own distinct styles, varying from Kyoto’s ornate and highly
        glazed kiyomizu-yaki to the beautiful natural earthenware of Bizen in
        Okayama and of Shigaraki near Kyoto. The town of Mashiko, to the north
        in seeing how some of Japan’s most celebrated pottery is made; the
        for lessons.
        Lacquerware. You are least likely to go wrong in terms of
        uniformly high quality if you’re in the market for lacquerware. Trays,
        plates, bowls, and jewelry boxes are superbly finished — and not so
        heavy as to create problems of excess baggage.
        Paper goods. Fans, dolls, and hand-made stationery are
        usually reasonably priced but produced with the same meticulous care as
        are objects made from more precious materials.
        second-hand books. The biggest neighborhood of its kind in the world,
        it sells books in most European languages as well as Japanese. You’ll
        also find excellent old maps and prints here, but the merchants know
        the going price for everything; real bargains are few and far
        between.
        Entertainment
        book sections of the Kinokuniya and Maruzen bookstores.
        As one of the most vivid and important expressions of
        Japan’s traditional cultural heritage, theater is an adventure in
        itself. Traditional Japanese drama, because of its stylization,
        extravagant gesture, and solemn or even bizarre intonation, might be
        difficult for Westerners. However, perseverance will be well rewarded
        once you get used to the conventions. The impact of the impassioned
        performances, aided by stunning costumes and elaborate make-up and
        masks, can be utterly seductive; many a skeptic has emerged an addict.
        Most Japanese theater aims less at developing a coherent plot, in the
        Western manner, than at creating a particular tone, atmosphere, and
        emotional extremes.
        Noh
        This is the oldest theatrical form, strictly speaking, and
        also the most austere and demanding. Derived originally from ritual
        dances of the imperial court at Nara and Kyoto, in the 14th century noh
        became a fully developed masked drama of chanting, dancing, and highly
        stylized acting. A hero and just two or three supporting actors enact
        stories about gods, historic battles, ghosts, unhappy love, and
        grief-stricken insanity. The more somber themes alternate with kyogen
        farces about the life of the common people, which often feature a
        satirical element.
        The commentary is chanted by a chorus of six to eight
        narrators (reminiscent of the chorus in Greek tragedy) who sit at the
        side of the stage, while musicians positioned at the back of the stage
        provide stark accompaniment with flute and drums. Contrasting with the
        resplendent costumes, the set has an austere simplicity: a backdrop
        (usually a permanent wall) of a large pine tree and some bamboo, with
        no curtain. The stage is framed by a classical Japanese tiled roof
        making a “house” inside the theater.
        Male actors, in masks, play all the roles. Characters often
        take several minutes to enter and exit the stage, moving painfully
        slowly in one of Japan’s greatest examples of form over function. For
        aficionados, a noh performance is an eclectic nirvana. For many others,
        it is powerfully soporific. Look around the audience and you’ll see
        plenty of locals nodding off unselfconsciously.
        Performances last several hours, with as many as five plays
        in a program. You can probably manage at least a couple, and theaters
        National Noh Theater, Kanze Kaikan at Shibuya, or Kyoto’s National Noh
        Theater. Other fine troupes perform in Osaka and Kanazawa.
        Kabuki
        Ever since the Tokugawa shoguns restricted performances to
        the samurai classes, noh drama has had a rather elitist appeal. Kabuki,
        on the other hand, has proved much more popular. Equally stylized in
        its way, kabuki is filled with fantastic color, movement, action,
        drama, and comedy. The performers are folk heroes, and the greatest of
        them — descendants of centuries-old dynasties of actors — are declared
        “Living National Treasures. ” Audience participation is at fever pitch,
        with people yelling as their personal heroes enter: “We’ve waited for
        you! ” or “You’re the greatest in Japan! ”
        Nothing is spared in the way of costumes and décor; there
        is no such thing as “over the top. ” Ever since the 18th century,
        revolving stages and trapdoors have been employed for supernatural
        characters to rise to the stage. Popular, but art of the highest order,
        kabuki tells stories of horror, blood and thunder, and passionate love.
        Connoisseurs wait for the set pieces: the colorful parade of the
        courtesan, a poignant seppuku suicide, the exciting fight scenes,
        and — summit of the art of kabuki — the end of a love affair that the
        heroine must break off, perhaps to save her lover’s honor, but never
        because she no longer loves him.
        “ She” is in fact likely to be a 60-year-old man. In the
        early days of kabuki, at the beginning of the 17th century, the
        acclaimed Kyoto dancers started to present increasingly erotic and
        lascivious performances. With the audience’s passionate loyalties to
        various star performers often leading to fights, the prudish Tokugawa
        shogunate decided to ban female performers, fearing a breakdown in
        all-important social order. However, they then found that the young men
        who took over the female roles were also attracting ardent devotees
        among military officers and even priests — homosexuality at that time
        was not yet frowned upon. So they were in turn replaced by older men.
        After years of study, these onnagata make an astoundingly subtle and
        delicate art of capturing the gestures and movements of both young
        girls and old crones.
        the performance, providing simultaneous English-language translation of
        the important dialogue along with explanations of the action and
        conventions. Shows last up to four hours, but you can buy cheaper
        balcony tickets for just part of the program. Kyoto’s kabuki troupe
        performs in December and Osaka’s in May.
        Bunraku
        Japan’s celebrated puppet theater can be seen at the
        National Bunraku Theater in Osaka’s Nipponbashi district, although
        National Theater. Don’t be misled: bunraku is theater for adults rather
        than children, using the same dramatic themes, stories, and conventions
        as in noh and kabuki but achieving a unique impact with the almost
        life-sized, colorfully costumed puppets. The puppeteers, dressed all in
        black, are initially distractingly visible on stage, manipulating and
        walking around with their puppets — yet completely “disappear” from
        your perception as the magic of the drama sweeps you away. A detailed
        English explanation of the plot is always provided, and wireless
        recorded commentary units are sometimes available.
        Bunraku’s heyday was the beginning of the 18th century,
        when playwright Monzaemon Chikamatsu wrote works specifically for the
        puppets that are regarded as among the greatest achievements of
        Japanese literature. Heroism in battle and the noble values of the
        samurai tradition are the principal themes. It comes as quite a shock
        to watch a warrior performing his final gesture of ritual suicide and
        realize that it’s only a puppet. The emotional effect is undiminished,
        and the gory effects are usually horribly creative.
        Film
        The Japanese cinema industry is in lingering recession,
        with growing numbers of people preferring to watch videos at home.
        Don’t be surprised to see the latest Hollywood blockbusters on release.
        These attract bigger audiences than do current local offerings, which
        seem tawdry and unoriginal after the towering creativity of giants like
        Kurosawa and Oshima. Despite occasional surprise international
        successes (such as Unagi and Shall We Dance? ), Japanese cinema will
        probably continue to be dominated by recycled ultraviolent gangster
        tales until it undergoes long-overdue industry reforms.
        Nightlife
        If you’d like to see how the Japanese handle Western-style
        popular music and dancing, you’ll find good quality jazz clubs,
        conventional discos (with, naturally, fantastic electronic equipment),
        restaurant districts of Akasaka and Roppongi. Teenagers might like to
        join the open-air disco hordes at Harajuku, near Yoyogi Park.
        Festivals and Folklore
        Despite increasing urbanization and social change, Japanese
        society retains its small, closely knit communities strongly dependent
        on Shinto gods to ensure good harvests for survival. Forget the
        karaoke, the bullet trains, and all those mobile phones for a moment.
        With such a highly developed sense of ritual and tradition, Japan’s
        matsuri (festivals) are much more than just fun for the community: for
        many they remain integral to life itself. There is at least one
        festival happening somewhere in Japan on any day of the year.
        Each region has its own festivals or variations on the
        large national ones. Most honor either Shinto deities and shrines or
        major Buddhist temples. Buddhist festivals are usually fairly
        restrained affairs, often involving an important image of the Buddha
        that might be available for public viewing only on this occasion.
        The real drama is at Shinto festivals. Some are austere
        purification ceremonies involving traditional music, chanting, dance,
        and often fire. At the opposite extreme are massive, almost riotous
        processions of thousands of bellowing, sweat-drenched men fighting to
        carry a huge portable shrine through the streets to a symbolic
        destination. Such is their exuberance and rapture that real outbreaks
        of violence can occur. These events have to be seen to be believed:
        they demonstrate the perfect flip-side of the supposedly reserved
        Japanese character.
        Festivals are where superficially modern Japan gives way to
        the old, where ancient traditions are upheld, especially in remote
        rural districts. But there is usually a strong commercial aspect to the
        celebrations. Some rural communities devise small but colorful
        festivals to galvanize community spirit and the local economy by
        attracting badly needed domestic tourists.
        Many festivals, though, are so spectacular that it is worth
        planning your visit specifically so you can attend. Definitely check
        with your nearest Japan National Tourist Office for information when
        planning your trip. Note that since many festivals follow the lunar
        calendar, the actual dates vary from year to year. With thousands of
        festivals and ceremonies taking place annually, this entire book
        wouldn’t provide enough space to describe them all. Instead, we offer a
        sampling of large and small festivals. But when planning a visit, some
        supplementary research will probably uncover unexpected nuggets.
        January. In Japan, New Year’s Day is the big festival,
        closest in spirit to Christmas in the West, the time when relatives and
        friends pay visits to each other and to the local shrines. New Year’s
        Eve is a quieter, more solemn affair than in the West, when the
        Japanese flock to famous shrines to pray for good fortune for the
        coming year. People decorate houses, shops, offices, and even cars with
        a bouquet of pine and bamboo, symbols of evergreen stability and
        Imperial Palace are opened to the public, with thousands coming to pay
        their respects to the emperor and enjoy a closer peek at his palace
        than is possible during the rest of the year.
        Closet pyromaniacs shouldn’t miss Nara’s Wakakusayama Turf
        Burning ceremony on 15 January, when people dressed as warrior monks
        burn the entire hillside of Mt. Wakakusa after sunset, creating one of
        the year’s most photographed spectacles, visible from miles around. The
        15th is also Coming-of-Age Day nationwide, a milestone event for
        20-year-olds attaining the age of majority. They attend special
        ceremonies at local community halls, and women dress in unusually
        opulent fur-trimmed kimono worn only on this special day.
        February. The important setsubun festival marks the end of
        winter around the country on 3–4 February. With demons represented by
        priests wearing fearsome masks, onlookers throw beans to drive them
        away while shouting, “Demons out, good fortune in! ” The 3rd and 4th
        are also one of the two occasions each year when the 3,000 lanterns of
        the Kasuga Grand Shrine in Nara are lit. (The event is repeated on
        14–15 August. )
        Up in Hokkaido, Sapporo holds its internationally popular
        Snow Festival (during the first or second week of February). The
        highlight is an ice sculpture competition at Odori Park, with huge
        superbly detailed models of castles, towers, and giant characters both
        traditional and modern. Throughout Japan, children living in snowy
        areas look forward each year to the Kamakura Festival, when they build
        igloo-type snow houses.
        March. On 3 March is the Hina Doll Festival, a special
        event for young girls. Exquisitely detailed dolls in ancient costumes
        representing the imperial couple and other aristocrats are displayed
        for good luck. Some shrines display thousands of dolls brought by the
        faithful.
        Another annual highlight is the two-week O-Mizu-tori
        Festival at Nara’s Nigatsudo Temple, one of Todaiji’s subtemples.
        Although the central event is a solemn and highly symbolic
        water-drawing ceremony, the crowds turn out in force for the more
        public and spectacular fire ceremonies. Every night from the 1st to the
        14th, in a highly dramatic display clearly designed to entertain,
        temple priests brandishing long poles with a flaming cedar ball at each
        end run along the front of the verandah, deliberately showering the
        large crowd below with burning embers. (believed to bring good luck for
        the coming year, having burned away the transgressions from the
        previous one). In long-exposure photographs of this display, the entire
        temple appears to be on fire. There is nothing like this anywhere.
        Photographers: Miss this at your peril!
        Another visual treat in March is the annual fertility
        festival held at Tagata Jinja in Gifu Prefecture, north of Nagoya. This
        amazing shrine celebrates an object that transcends borders and
        cultural barriers: the human penis. Phalluses huge and humble, wooden
        and stone are enshrined and worshipped here. And on 15 March each year,
        the mightiest specimen, a 2 m (6.5 ft) monster made of Japanese cypress
        and weighing over 270 kg (600 pounds) is slowly carried through this
        small town, bulging out of its portable shrine. See it and you still
        won’t believe it.
        Senso-ji Temple (in Asakusa), accompanied by a ceremonial carriage
        bearing several geisha playing traditional musical instruments.
        April. The Buddha’s birthday is celebrated with flower
        festivals held throughout Japan. The best place to view the spring
        Nezu shrine. In the Kansai region, peony lovers head for Hasedera
        Temple in rural Nara. April is also cherry blossom season, with
        blossom-viewing picnics (hanami) held in parks and temples throughout
        Japan as the cherry-blossom “front” makes its steady progress
        northward. On the 14th and 15th the city of Takayama in Gifu Prefecture
        holds one of Japan’s greatest processions of large, colorful
        floats.
        May. From the end April and into early May is Golden Week,
        the unofficial name for the conjunction of three major national
        holidays (Green Day, Constitution Day, and Children’s Day). Since this
        is the only time many Japanese are permitted to take a vacation, it is
        the worst time to visit Japan, since every hotel, inn, train, and even
        plane is booked up months in advance. Although Boys’ Day was officially
        renamed Children’s Day to include girls, the reality is taking some
        time to catch on. This festival features giant carp streamers flying
        from poles throughout Japan. The carp’s ability to struggle upstream
        against a strong current is regarded as a fit model for Japanese
        boys.
        On 15 May, Kyoto celebrates its Hollyhock Festival (Aoi
        Matsuri). This ancient ritual is meant to pave the way for a good
        harvest, with branches of hollyhock to stave off thunder and
        earthquakes. The hollyhock decorates a big red oxcart, accompanied from
        the Imperial Gosho Palace by 300 Kyoto citizens dressed in splendid
        Heian-period costumes.
        June. From June onward, ukai celebrates the ancient use of
        cormorant birds to catch aiyu, a popular river fish. The animal rights
        movement has yet to penetrate Japan in any significant way: the
        cormorants’ throats are constricted so they can’t swallow the fish they
        catch underwater, and their owners retrieve the catch when the hapless
        birds resurface. The various events held around Japan are usually
        highly ceremonial, with blazing torches illuminating the
        proceedings.
        July. Kyoto’s Gion Festival (17–24 July) is the most
        elaborate procession of the year, with its grandiose floats and glowing
        lanterns. Originally, the festival invoked the help of the gods against
        a plague in medieval Kyoto; highly commercialized imitations of it are
        now celebrated all over the country. Immediately after Gion, on the
        24th and 25th, Osaka holds its flamboyant and mammoth Tenjin Matsuri,
        starting from the Temmangu shrine. It has fireworks, flaming torches,
        and gaily decorated floats on the central Okawa River.
        August. At the height of the summer swelter in July and
        August is O-bon, a colorful and joyous national Buddhist festival
        honoring the spirits of deceased ancestors. People travel around the
        country to clean their family tombs and gravestones. At Nagasaki in
        mid-August, glowing lanterns decorate the graveyards, while other
        lanterns are put out to sea on model boats to take the departed souls
        back to their other world. Like Golden Week in April–May, this is a
        great time to avoid Japan unless you relish competing for every train
        seat and hotel bed with millions of others. So bad is the traffic that
        many of the country’s expressways come to a virtual standstill.
        On the 14th and 15th of the month is the year’s second
        lighting-up of the thousands of lanterns at Kasuga Grand Shrine in
        Nara.
        Further information. For complete details of these and
        other major festivals held annually around Japan, check the JNTO
        website at <www.jnto.go.jp>.
        Sports
        When the Japanese decide to do something, they seem to take
        a “total-immersion” route, buying the latest outfits and equipment so
        that they look like seasoned professionals before they take a single
        lesson. This provides insight into the important Japanese concept of
        katachi (form), the rough equivalent of “It isn’t what you do; it’s the
        way that you do it. ” It is quite common to see Japanese men of all
        ages standing on train platforms or outside a building practicing their
        stroke with an imaginary golf club.
        Participant Sports
        Tennis. With land prices notoriously high, urban courts are
        crowded and expensive, so your best bet is at the seaside or hot-spring
        resorts. If necessary, get your hotel to help you make
        reservations.
        Golf. Unsurprisingly, golfing is prohibitively expensive.
        You will have to share the Japanese golfer’s manic obsession to want to
        shell out green fees of well over US$100 at top clubs during peak
        periods. The best way to enjoy a round of golf is as the guest of a
        Japanese friend or business associate.
        (except after 1 September, when summer for the Japanese has officially
        ended). So you are better off going south to Kyushu, around Shimabara
        and the more secluded of the Amakusa Islands (for snorkeling and
        scuba-diving, too) or to the spa resort of Ibusuki. Water sports
        enthusiasts go south to the beaches of Okinawa, the liveliest being
        Moon Beach at Nakadomari.
        Fishing. One of the joys of fishing in Japan is taking the
        catch back to your Japanese-style inn and having the cook grill it for
        you or turn it into sushi or sashimi (depending on your degree of faith
        in the cleanliness of Japan’s highly polluted rivers). Freshwater
        angling — for bass, carp, or trout — is good anywhere in the lakes and
        streams, best of all up in Hokkaido, where you stand a decent chance of
        hooking a salmon. Sea bream and sea bass are the most frequent catch in
        coastal waters. Ask about license restrictions at the local tourist
        office.
        Skiing. Japan has a number of excellent skiing areas, which
        quickly get very crowded in season. Winter sports are one of Hokkaido’s
        main draws for domestic tourism, with popular ski resorts at Teine
        Olympia (outside Sapporo), Niseko, and Kiroro. Others are Zao (in
        Tohoku) and a number of resorts in Joshin-etsu Kogen National Park in
        the Japan Alps, where there are now splendid facilities thanks to the
        1998 Winter Olympic Games in Nagano.
        Spectator Sports
        Baseball. The game is at least as popular in Japan as it is
        in the US. It was introduced in the 19th century, together with
        railways, cameras, and whisky. Today baseball is big business, with
        cheerleaders, balloons, and variations on Major League hype. The major
        professional teams are owned by the biggest publishing empires or
        department store chains, each combining their company name with the
        time-honored American nicknames, the most famous being the Yomiuri
        Giants. Japanese commentators have happily adopted the American jargon
        can see games at Korakuen Stadium, and in Osaka at Nissei.
        Sumo. Of the traditional Japanese sports, sumo wrestling is
        the most popular. This ancient sport originated more than 15 centuries
        ago in Shinto ceremonies. Today, sumo champions — the only men still
        allowed to wear the samurai warrior’s gleaming top-knot hairdo — are
        national heroes and are much in demand for TV commercials. At the
        national level, there are a total of 575 wrestlers classed in six
        divisions according to their win-loss ratio in the annual tournaments.
        The highest division is the makuuchi, of which the champions are known
        as yokozuna. These giants weigh anything from 90 to 165 kg (200 to 350
        pounds), yet they have grace, dignity, and suppleness that belie their
        massive bulk.
        The dohyo-iri (ring entry) ceremony opening the tournament
        is a fascinating spectacle. The champions strut into the arena in
        richly embroidered silk “aprons” covering the solid band protecting
        their midriffs. In the dohyo, a raised mound of hard clay some 4.6 m
        (15 ft) in diameter under a large suspended Shinto-roof-style
        canopy,toss salt across the dohyo to purify it of evil spirits, swagger
        around, and commence the all-important “psyching-out” of the opponent.
        Pointedly avoiding each other’s eyes, they raise a massive leg into the
        air (to a height that would do a professional dancer proud), slam it
        down with a mighty thud, and lower themselves into the characteristic
        squat. This goes on for up to five minutes — all part of the great
        ritual buildup of tension before the wrestlers clash. Note that
        indulging in these highly stylized opening theatrics is a privilege of
        top-ranked wrestlers only.
        The aim is for one wrestler to force the other out of the
        ring or to make him touch the floor with anything other than his feet.
        The bout is usually over in one or two minutes, sometimes mere seconds,
        but the intensity of the struggle and the sheer visual drama make for
        compelling entertainment.
        Sumo tournaments are held in January, May, and September at
        Nagoya, and in November in Fukuoka (Kyushu). The bouts commence in the
        morning, but the real crowds start arriving only in late afternoon. A
        little known secret is that a standing ticket (usually around US$12)
        actually gives you the run of the arena: you can move around freely,
        sit in unoccupied seats, and even enjoy the action from the ringside
        until the actual ticket-holders arrive later on. If you can, go out of
        your way to spend a few hours of watching live sumo. There is simply
        nothing on earth like it.
        Martial arts. Most major cities have martial arts halls,
        where you can watch kendo (fencing with bamboo staves) as well as the
        famed sports of judo and aikido. The latter is a highly spiritual art
        in which, unlike judo, the opponents do not grapple at the beginning of
        the bout. Instead, they maneuver and feint, applying the strength of
        their will (ki) rather than physical strength to overcome the
        other.
```




