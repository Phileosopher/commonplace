
indicate history
- specify how timekeeping was once tracked
- indicate its base-6 basis
- give daylight savings history
indicate all the calendars that have been used

propose the most precise calendar

a second was once measured as 1/86,400 of a day, then they moved to a second being 9,192,631,770 vibrations of a cesium atom
- why cesium?
- it pulses microwave energy into it and the vibrations come from its agitated state, and they use another atom before the first one runs out

Add french revolution calendar to nag datetime

Calendars:
    there's the Bengali calendar, which is solar and based on 6 seasons of two months;
    the Chinese calendar, which is a fairly confusing lunisolar calendar, used legally along with the Gregorian calendar in China. That's over a billion people right there
    the Ethiopian calendar which is pretty cool and indirectly derives from the old Egyptian calendar, the first solar calendar we have on file. Its leap days are technically not part of any month. What's neater is that in Ethiopia, their midnight starts at what is 6AM in neighbouring countries. Since Ethiopia has made it a point of pride that they have never been colonized, they are generally not interested in adopting other systems.
    The Hebrew calendar is one of the oldest calendars on file, is both lunar and solar, and has some of the most complex rules I've seen related to choice of dates. Just picking the first day of the year has what is probably a few full pages of business rules. It's usable legally in Israel, with the same status as the Gregorian calendar.
    There's a Hindu calendar, also very complex to me, using both solar and lunar cycles. What's fun is that depending on the region, the new moon or the full moon is used as a cycle beginning so the same calendar gives two varying sets of dates within the same country. But with India in the mix, we're close to a third of the world population pretty frequently dealing with non-Gregorian calendars
    Then there's a Persian one, whose details I don't really remember all that well at the moment
    And there's the Islamic calendar, which is still use in Saudi Arabia for official purposes, but also in other countries for cultural or religious purposes. What's interesting about it is that it's an observational calendar, meaning that every new lunar cycle, some authority figure has to get out, look at the moon, and say "this is a new moon, we officially have a new month". In the past, when more countries used it, it was possible to get a bunch of months starting on different dates for people all using the same calendars, since observations would vary according to locations.
And > 20 other ones used for religious or ritualistic purposes

UTC standards
- leap seconds
Time Zones
UTC+12:45/UTC+13:45
UTC+05:45
UTC-00:44 (avant 1972)
UTC-03:30
etc.
In 2011, Samoa islands went from UTC-11 to UTC+13, skipping
December 31 for one year only. (4th of July happened twice in
1892).
In Brazil, DST is subject to a regional vote!

## jewish calendar

FROM MARCIN:

Speaking of which, I went to HebrewFest soon after we met, which was really interesting. As I think I said before, I'm not crazy about Hebrew Roots - I've accepted my identity as a Gentile, and don't feel like getting into the Hebrew language and culture at this time - but I still learned a lot.

It seems that I and a very small group of people have discovered Yah's original calendar, hidden in the Book of Enoch and the Dead Sea Scrolls. It's often referred to as the Zadok calendar. The Zadok priesthood was given Yah's blessing (Ezekiel 44:15) and went on to become the Essenes, who were responsible for the Dead Sea Scrolls. It seems that John the Baptist was a Zadok priest himself, which is a fascinating rabbit-hole to go down and explains a lot of things. The Zadok calendar makes more sense than the Jewish calendar, which has thirteen months (no thirteenth month can be found in scripture), and seems to have been adopted by the Jews for the first time during their captivity in Babylon.

Reading the gospels, it's become clear to me that Yeshua kept a different calendar for the feasts than the Pharisees did, which explains many apparent contradictions. For example, the Last Supper was clearly the Passover, and yet the next day we see the Jews wanting Yeshua killed while it's still preparation day, before the Passover begins. So essentially their calendar was a day late in this particular year. We also know that the Last Supper was on a Tuesday, because Passover is *always* on Tuesday in the Zadok calendar, and that therefore Yeshua died on Wednesday. This means that He resurrected after three days on the Saturday Shabbat, the Lord's Day (see Matthew 12:8). For proof that He had already resurrected by the time Sunday came around, see Matthew 28:1 and Mark 16:2.

## Excel time to UTC time

### The problem

I had a CSV file that needed to be processed on a web page. So I had to convert the Excel time to UTC time.

### The solution

According to [this answer on StackOverflow](https://stackoverflow.com/a/32848723/319711):
> The Excel number for a modern date is most easily calculated as the number of **days** since 12/30/1899 on the Gregorian calendar.
>
> Excel treats the mythical date 01/00/1900 (i.e., 12/31/1899) as corresponding to 0, and incorrectly treats year 1900 as a leap year. So for dates before 03/01/1900, the Excel number is effectively the number of days after 12/31/1899.

UTC time is represented in JavaScript as the number of **milliseconds** since 1/1/1970, so there are effectively:
- 70 years between the two starting points
- Plus 1 day as Excel starts at 31 Dec
- Plus 17 leap years in that period
- Plus 1 day as Excel treats 1900 incorrectly as a leap year too (this only applies for dates after 1 March 1900).

This means that the Excel time is 70 * 365 + 1 + 17 + 1 = 25569 days before the UTC start. 
As one day is 24 * 60 * 60 = 86400 seconds or 86400 * 1000 milliseconds, you get:

> utcTime = (excelTime - 25569) * 86400000

### Note
- Since Excel writes large numbers with an exponent, you may prefer to save the number in seconds, 
and multiply by 1000 in JavaScript (it will make the file much smaller too)
- Beware that you may have to compenstate for the timezone offset. E.g. in the Netherlands, 
the reported time is likely given using GMT+1, so you need to additionally subtract one hour too, 
giving you the following formula:

> utcTime = ((excelTime - 25569) * 86400 - 3600) * 1000
