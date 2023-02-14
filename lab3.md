# -cse-15l-lab-report-week5
## Lab Report 3
### Researching Commands For Grep
### Command 1: 
**grep -n** this command searches a file and essentially returns the lines where the specificed string is located in the text file.

**Example 1:**

**Command Line Argument:**
This command searches for the word travel in the file WhereToItaly.txt.
```
#code block
$ grep -n "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:**
The lines are returned where the specified string "travel" is located on each line of the text file.
```
#code block
66:        Even the most free-spirited traveler can use a little help
78:        national travel agency for transportation, excursions, and hotel
81:        217) gives detailed practical guidance on the technicalities of travel
86:        buffs and travelers with plenty of time, patience, and curiosity. The
722:        especially the Greece he loved above all else — a travel notebook for
2081:        important for weary or hungry travelers, elegant 18th-century cafés.
3448:        Neapolitans are justifiably proud. For adventurous travelers looking
3846:        tempt travelers and aspiring photographers onto jutting crags high
3868:        roads to speak of, most travel is by foot up and down its endless
3955:        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
```
**Example 2:**
**Command Line Argument:**
This command searches for the word "history" in the file HistoryDublin.txt.
```
#code block
$ grep -n "History" written_2/travel_guides/berlitz1/HistoryDublin.txt
```
**Output:**
The lines are returned where the specified string "travel" is located on each line of the text file. It seems to only appear once in line 6.
```
#code block
6:        A Brief History
```
***Source***: **[geekforgeeks grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)**

### Command 2:
**grep -i** this command searches for a string within a file, but it ignores case sensitivity. For instance, if the string used was "Hello" it would search the file for "HELLO", "HelLo", etc. As long as the letters are the same, the command will output it even if there is difference in capitalization with the string.
**Example 1:**
**Command Line Argument:**
This command searches for the word travel in WhereToItaly.txt.
```
#code block
$ grep -i "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:**
The output includes lines for the words travel that includes different capitlizations. Some new lines appear with the word travel since case sensitivity does not matter. Comparing it to the grep -n command, it seems that there are lines such as that did not show up earlier, showing up now.
```
#code block
Even the most free-spirited traveler can use a little help
        national travel agency for transportation, excursions, and hotel
        The Travel Tips section at the back of the book (see page
        217) gives detailed practical guidance on the technicalities of travel
        buffs and travelers with plenty of time, patience, and curiosity. The
        especially the Greece he loved above all else — a travel notebook for
        important for weary or hungry travelers, elegant 18th-century cafés.
        Fruit, is here. Travelers on their way to or from Rome will be
        Neapolitans are justifiably proud. For adventurous travelers looking
        tempt travelers and aspiring photographers onto jutting crags high
        roads to speak of, most travel is by foot up and down its endless
        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
```
**Example 2:**
**Command Line Argument:** This command line argument searches for the word history in HistoryDublin.txt.
```
#code block
$ grep -i "History" written_2/travel_guides/berlitz1/HistoryDublin.txt
```
**Output:** The power of -i becomes more clear when searching for the word history in this file, as earlier it was clear that grep -n only returns one line, but running -i returns 4 lines. The variations of history is returned here with History or history. Since -i ignores case sensitivity any instance of history that shows up in the file is returned.
```
#code block
 A Brief History
        Irish history really begins with the arrival of the Celts around the
        history, for both the Irish themselves and civilization in general,
        struggle between England and Ireland that was to dominate Irish history
```
***Source***: **[geekforgeeks grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)**


### Command 3: 
**grep -A**  this command searches for a string and prints out a specified amount of lines after that string. 
**Example 1:**
**Command Line Argument:** This is searching for the word travel in WhereToItaly.txt, it specifies that it will print 2 lines including the line where the string travel appears.
```
#code block
$ grep -A 2 "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:** The output searches for all instances where the word travel appear and prints out two lines after the original line where travel appears. Including the travel line, the output would include 3 lines. The first line is where travel appears and 2 lines after it for a total of 3 lines.
```
#code block
Even the most free-spirited traveler can use a little help
        occasionally. With the tourist industry such a vital factor in the
        economy, Italy has an elaborate network of information offices.
--
        national travel agency for transportation, excursions, and hotel
        bookings.
        The Travel Tips section at the back of the book (see page
        217) gives detailed practical guidance on the technicalities of travel
        through Italy, but here are some general thoughts to help you plan your
        trip.
--
        buffs and travelers with plenty of time, patience, and curiosity. The
        uncertainties of schedules and frequency of strike action gradually
        disappeared in the 1990s, but the occasional wrinkle still needs to be
--
        especially the Greece he loved above all else — a travel notebook for
        his old age. Barbarians and museum curators have removed most of the
        villa’s treasures, but a stroll through the remaining pillars, arches,
--
        important for weary or hungry travelers, elegant 18th-century cafés.
        During the Austrian occupation, the enemy frequented Quadri on the
        north side, while Italian patriots met only at Florian, opposite. In
--
        Neapolitans are justifiably proud. For adventurous travelers looking
        for an introduction to the South, the rewards are rich. Indeed, two of
        Naples’ museums are among the most important in Europe, but they and
--
        tempt travelers and aspiring photographers onto jutting crags high
        above terraces of orange and lemon groves, vineyards, walnut, and
        almond trees. Surrounded on three sides by ravines above the sea, the
--
        roads to speak of, most travel is by foot up and down its endless
        staircases.
        The second most charming and lively of the coast’s
--
        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
        piece of St. Michael’s red cloak. From a Gothic portico in the middle
        of town, beside the massive 13th-­century campanile, a staircase of 90
```
**Example 2:**
**Command Line Argument:** This is the exact search as the first example, but this time it will search for 4 lines after the instance of travel is found.
```
#code block
$ grep -A 4 "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:** The output is signifigantly larger than the previous output, this make sense because now it is printing about 5 lines every time the instance of travel is found.
```
#code block
  Even the most free-spirited traveler can use a little help
        occasionally. With the tourist industry such a vital factor in the
        economy, Italy has an elaborate network of information offices.
        Bureaucrats being bureaucrats, efficiency and amiability vary from
        place to place, but the tourist information offices all provide useful
--
        national travel agency for transportation, excursions, and hotel
        bookings.
        The Travel Tips section at the back of the book (see page
        217) gives detailed practical guidance on the technicalities of travel
        through Italy, but here are some general thoughts to help you plan your
        trip.
        Major journeys from one part of the country to another,
        say, from Milan to Rome or down to Naples, is most enjoyed by train
        buffs and travelers with plenty of time, patience, and curiosity. The
        uncertainties of schedules and frequency of strike action gradually
        disappeared in the 1990s, but the occasional wrinkle still needs to be
        ironed out. If you are making a long rail journey, don’t rely on the
        generally dreary dining-car service. Make up your own picnic hamper of
--
        especially the Greece he loved above all else — a travel notebook for
        his old age. Barbarians and museum curators have removed most of the
        villa’s treasures, but a stroll through the remaining pillars, arches,
        and mosaic fragments in gardens running wild among the olive trees,
        cypresses, and pines can be marvelously evocative of a lost world. To
--
        important for weary or hungry travelers, elegant 18th-century cafés.
        During the Austrian occupation, the enemy frequented Quadri on the
        north side, while Italian patriots met only at Florian, opposite. In
        warm weather months, their spirited 4-piece orchestras play everything
        from “Moon River” to polkas and Neapolitan love songs. Pigeons chase
--
        Neapolitans are justifiably proud. For adventurous travelers looking
        for an introduction to the South, the rewards are rich. Indeed, two of
        Naples’ museums are among the most important in Europe, but they and
        the piazzas and monuments play second fiddle to the colorful street
        life. In the outdoor theater that is Italy, Naples is unabashed
--
        tempt travelers and aspiring photographers onto jutting crags high
        above terraces of orange and lemon groves, vineyards, walnut, and
        almond trees. Surrounded on three sides by ravines above the sea, the
        pretty tree-shaded resort of Sorrento still retains something of its
        old-fashioned air, and is still the most popular and best logistic base
--
        roads to speak of, most travel is by foot up and down its endless
        staircases.
        The second most charming and lively of the coast’s
        resorts, Amalfi was once a powerful rival to the maritime republics of
        Pisa and Genoa, with trading posts in the 10th and 11th centuries in
--
        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
        piece of St. Michael’s red cloak. From a Gothic portico in the middle
        of town, beside the massive 13th-­century campanile, a staircase of 90
        steps takes you down to the sanctuary’s 11th-century bronze doors.
        Notice to the left of the altar the beautifully carved stone episcopal
```
***Source***: **[man7 grep(1) — Linux manual page](https://man7.org/linux/man-pages/man1/grep.1.html)**

### Command 4:
**grep -v** this command will search for a certain string or pattern and essentially print all the lines that does not include that string or pattern. So it's sort of like the oppisite of what traditional grep commands would do. 
**Example 1:**
**Command Line Argument:** This is essentially going to print all the lines that does not include the letter i in the WhereToItaly.txt file.
```
#code block
$ grep -v "i" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:** This entire output does not contain the letter i. 
```
#code block
 WHERE TO GO
        from.
        country down.
        maps and brochures.
        through Italy, but here are some general thoughts to help you plan your
        Major journeys from one part of the country to another,
        The autostrada (toll motorway or expressway) runs the length and
        Keep your car for use on the open road. In the overcrowded
        parked.
        CENTRAL ITALY
        Rome
        suburbs.
        The Center
        Napoleon.
        Next to the church, an arched 16th-century gateway marks
        Fontana.
        the bottom of the steps has been preserved as a museum.
        graceful and gradual, takes you up between the statues of Castor and
        dome.
        the Forum to the northwest and the Baths of Caracalla to the south.
        ).
        stands the Colosseum, Rome shall stand; when falls the Colosseum, Rome
        soot-free.
        only.
        halls.
        The Temple of Saturn doubled as state treasury and center
        up to 200,000.
        square.
        bullet-proof glass. But reverence can also cause damage: on the
        foot.
        cast out of bronze beams taken from the Pantheon’s porch (see page 51),
        marble Cathedra of St. Peter, throne of the Apostle’s successors.
        regularly from St. Peter’s Square to the museum entrance and back,
        outstretched arm added by over-zealous 16th-century “restorers”).
        In stark contrast to Raphael’s grand manner, seek out the
        the Cross.
        Other Museums
        a sarcophagus.
        Cranach.
        Other Churches
        Jesus and the New Jerusalem over the chancel.
        homes by the sea or nearby lakes.
        of the place.
        guests can look down at the terraced gardens, the real reason for
        early September are no longer guaranteed.
        advance.
        Costa Smeralda
        name, but as l’Eroe, “the Hero. ”
        Alghero
        ramparts.
        TUSCANY AND UMBRIA
        cathedral.
        later.
        close-ups of the dome’s structure and the 16th-century frescoes
        Acuto).
        enough to adorn the entrance to heaven and they have been known ever
        date from the 13th century.
        years old.
        overload.
        bankers’ tax-collector turned Apostle (west); Donatello’s St. George,
        (see page 26).
        landscape.
        by Joos van Cleve.
        have been the model.
        Lorenzo just north of the Duomo near the church of the same name. The
        true.
        noses at the smell.
        Through a separate entrance left of the church, escape the
        Supper.
        South of the Arno
        noteworthy.
        An early proponent of “make love, not war,” Rubens shows
        vespers.
        Tuscany (Toscana)
        from the square up to the small San Francesco convent and post-card
        of Juno and Phaedra.
        Lucca
        throughout the summer.
        façade.
        The 13th-century town hall, Palazzo del Popolo, houses the
        Volterra
        squares are separated by the 12th-century cathedral and 13th-century
        of knee.
        and Mary Magdalen flank the entrance.
        Column by Sodoma.
        On 26 September 1997, two major earthquakes rocked the
        Testament and the Last Judgment.
        to “sacks of nuts. ”
        depths.
        Spoleto
        The fourth floor of the town hall (entrance on Corso
        THE NORTHEAST
        valley.
        Grand Canal (Canal Grande)
        tour.
        the lagoon bed.
        gone from the freshly restored façade of the 15th-century Ca’ d’Oro
        San Marco just across the way.
        and ended here.
        The north and south arms of the square, the 16th-century
        entrance.
        )
        offers a moment of rest for the weary).
        Sunday.
        storm.
        somber psychology.
        Room 17: Canaletto’s hugely popular 18th-century vedute
        both poetry and melancholy.
        Mark Rothko, and Robert Motherwell. In the garden are sculptures by
        entrance.
        notable.
        Off the Beaten Track
        Among the corners of town far from the crowd, the old
        escape the mobs.
        on the slender Greek marble columns.
        Veneto
        The Brenta Canal
        extravagantly frescoed Baroque country houses on the banks of the
        Padua (Padova)
        character.
        entrance wall.
        town.
        Verona
        London.
        change from pasta.
        Bolzano (Bozen)
        Ravenna
        loveless mother. ”
        entrance).
        Next to the present-day 19th-century cathedral, the
        Bologna
        France.
        sculpted the bronze sea god surrounded by nymphs and cherubs.
        Ferrara
        dungeons.
        You get a sense of the dukes’ grandeur among the
        Parma
        THE NORTHWEST
        Italy.
        Around the Duomo
        courtyard of the Palazzo Reale south of the cathedral. (It houses the
        15th century to the present day.
        galas every sacrosanct December 7), attend a concert or dance
        18th-century world, now graced by the overflow of Montenapoleone’s
        Around Castello Sforzesco
        dome.
        The Brera and Other Museums
        Lombardy
        emperors.
        Bergamo
        On the lake’s west shore, the people of Salò (where
        summers.
        Embraced by green wooded escarpments and backed by
        parks.
        hotel of the same name.
        from Stresa, Baveno, or Pallanza) than by road.
        The Royal Palace (Palazzo Reale) was the ornately Baroque
        well-preserved 14th-century b.c. tomb.
        Clouet.
        (but also Benz, Peugeot, and Ford) celebrated out at the Museo
        Courmayeur
        Genoa (Genova)
        may account for a cool reserve, almost aloofness, that some read even
        father.
        sanctuary of Madonna della Costa.
        THE SOUTH
        form.
        Sannazaro.
        cats.
        The Museums
        and theft.
        bundle of old bones and stones, but sheer pleasure for anyone even
        Caracalla.
        at the museum entrance.
        Greek temples of Paestum.
        and bar/cafés cluster around the pretty 17th-century domed church of
        Camerelle that eventually leads to the famous Punta Tragara lookout and
        way up to the terraced gardens and chestnut trees of Monte Solaro, at
        among the smarter spa resorts.
        Herculaneum.
        red. ”
        The old Roman name of Europe’s most famous volcano means
        ones.
        out of the volcano.
        Herculaneum (Ercolano)
        5,000 people was unearthed from 1927 to 1962.
        The entrance off the modern town’s Corso Ercolano takes
        town — Sorrento’s only real museum of note.
        Salerno.
        Paestum
        buff-stone columns take on a wonderful golden glow at sunset. Four
        steps takes you down to the sanctuary’s 11th-century bronze doors.
        throne.
        Alberobello
        Palermo
        and palm trees.
        south coast.
        Monreale
        Chapel.
        North of Temple Valley, next to the 13th-century Norman
        south along the coast and to the volcano of Mount Etna to the west, the
        Mount Etna
```
**Example 2:**
**Command Line Argument:** The previous output in example 1 seems a bit long, so why not try to shorten that output by filtering the specifics even more. I used the 2 most common letters in the English alphabet to filter out all lines containing both "i" and "a".
```
#code block
$ grep -v -e "i" -e "a" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:** The output is a lot shorter from before and each line has less and less words. The letters i and a are no where to be found. Although, this command is not case sensitive so capitlizations of a and i do show up.
```
#code block

        WHERE TO GO
        from.
        country down.
        CENTRAL ITALY
        Rome
        suburbs.
        The Center
        dome.
        ).
        soot-free.
        only.
        up to 200,000.
        foot.
        the Cross.
        Other Museums
        Other Churches
        Alghero
        TUSCANY AND UMBRIA
        Acuto).
        true.
        Supper.
        South of the Arno
        noteworthy.
        vespers.
        throughout the summer.
        of knee.
        depths.
        Spoleto
        THE NORTHEAST
        tour.
        )
        storm.
        somber psychology.
        Veneto
        town.
        London.
        loveless mother. ”
        dungeons.
        THE NORTHWEST
        Around the Duomo
        dome.
        emperors.
        summers.
        well-preserved 14th-century b.c. tomb.
        Clouet.
        THE SOUTH
        form.
        The Museums
        red. ”
        ones.
        throne.
        Alberobello
```
***Source***: **[man7 grep(1) — Linux manual page](https://man7.org/linux/man-pages/man1/grep.1.html)**
