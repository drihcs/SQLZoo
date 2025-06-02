#SELECTBasics

Introducing the world table of countries
1.
The example uses a WHERE clause to show the population of 'France'. Note that strings should be in 'single quotes';

Modify it to show the population of Germany

Scandinavia
2.
Checking a list The word IN allows us to check if an item is in a list. The example shows the name and population for the countries 'Brazil', 'Russia', 'India' and 'China'.

Show the name and the population for 'Sweden', 'Norway' and 'Denmark'.

Just the right size
3.
Which countries are not too small and not too big? BETWEEN allows range checking (range specified is inclusive of boundary values). The example below shows countries with an area of 250,000-300,000 sq. km. Modify it to show the country and the area for countries with an area between 200,000 and 250,000.

-------------------

#SELECT from WORLD Tutorial
Language:	English  • 日本語 • 中文
name	continent	area	population	gdp
Afghanistan	Asia	652230	25500100	20343000000
Albania	Europe	28748	2831741	12960000000
Algeria	Africa	2381741	37100000	188681000000
Andorra	Europe	468	78115	3712000000
Angola	Africa	1246700	20609294	100990000000
...

In this tutorial you will use the SELECT command on the table world:

Introduction
1.
Read the notes about this table. Observe the result of running this SQL command to show the name, continent and population of all countries.

Large Countries
2.
How to use WHERE to filter records. Show the name for the countries that have a population of at least 200 million. 200 million is 200000000, there are eight zeros.

Per capita GDP
3.
Give the name and the per capita GDP for those countries with a population of at least 200 million.

HELP:How to calculate per capita GDP

South America In millions
4.
Show the name and population in millions for the countries of the continent 'South America'. Divide the population by 1000000 to get population in millions.

France, Germany, Italy
5.
Show the name and population for France, Germany, Italy

United
6.
Show the countries which have a name that includes the word 'United'

Two ways to be big
7.
Two ways to be big: A country is big if it has an area of more than 3 million sq km or it has a population of more than 250 million.

Show the countries that are big by area or big by population. Show name, population and area.

One or the other (but not both)
8.
Exclusive OR (XOR). Show the countries that are big by area (more than 3 million) or big by population (more than 250 million) but not both. Show name, population and area.

Australia has a big area but a small population, it should be included.
Indonesia has a big population but a small area, it should be included.
China has a big population and big area, it should be excluded.
United Kingdom has a small population and a small area, it should be excluded.

Rounding
9.
Show the name and population in millions and the GDP in billions for the countries of the continent 'South America'. Use the ROUND function to show the values to two decimal places.

For Americas show population in millions and GDP in billions both to 2 decimal places.
Millions and billions
Missing decimals

Trillion dollar economies
10.
Show the name and per-capita GDP for those countries with a GDP of at least one trillion (1000000000000; that is 12 zeros). Round this value to the nearest 1000.

Show per-capita GDP for the trillion dollar countries to the nearest $1000.

Name and capital have the same length
11.
Greece has capital Athens.

Each of the strings 'Greece', and 'Athens' has 6 characters.

Show the name and capital where the name and the capital have the same number of characters.

You can use the LENGTH function to find the number of characters in a string
For Microsoft SQL Server the function LENGTH is LEN

Matching name and capital
12.
The capital of Sweden is Stockholm. Both words start with the letter 'S'.

Show the name and the capital where the first letters of each match. Don't include countries where the name and the capital are the same word.
You can use the function LEFT to isolate the first character.
You can use <> as the NOT EQUALS operator.

All the vowels
13.
Equatorial Guinea and Dominican Republic have all of the vowels (a e i o u) in the name. They don't count because they have more than one word in the name.

Find the country that has all the vowels and no spaces in its name.

You can use the phrase name NOT LIKE '%a%' to exclude characters from your results.
The query shown misses countries like Bahamas and Belarus because they contain at least one 'a'

---------------------------------------------------------------------

##SELECT from Nobel Tutorial

nobel Nobel Laureates
We continue practicing simple SQL queries on a single table.

This tutorial is concerned with a table of Nobel prize winners:

nobel(yr, subject, winner)
Using the SELECT statement.

Winners from 1950
1.
Change the query shown so that it displays Nobel prizes for 1950.

1962 Literature
2.
Show who won the 1962 prize for literature.

Albert Einstein
3.
Show the year and subject that won 'Albert Einstein' his prize.

Submit SQLrestore default

Recent Peace Prizes
4.
Give the name of the 'peace' winners since the year 2000, including 2000.

Literature in the 1980's
5.
Show all details (yr, subject, winner) of the literature prize winners for 1980 to 1989 inclusive.

Only Presidents
6.
Show all details of the presidential winners:

Theodore Roosevelt
Thomas Woodrow Wilson
Jimmy Carter
Barack Obama

John
7.
Show the winners with first name John

Chemistry and Physics from different years
8.
Show the year, subject, and name of physics winners for 1980 together with the chemistry winners for 1984.

Exclude Chemists and Medics
9.
Show the year, subject, and name of winners for 1980 excluding chemistry and medicine

Early Medicine, Late Literature
10.
Show year, subject, and name of people who won a 'Medicine' prize in an early year (before 1910, not including 1910) together with winners of a 'Literature' prize in a later year (after 2004, including 2004)

Harder Questions
Umlaut
11.
Find all details of the prize won by PETER GRÜNBERG

Non-ASCII characters

Apostrophe
12.
Find all details of the prize won by EUGENE O'NEILL

Escaping single quotes

Knights of the realm
13.
Knights in order

List the winners, year and subject where the winner starts with Sir. Show the the most recent first, then by name order.

Chemistry and Physics last
14.
The expression subject IN ('chemistry','physics') can be used as a value - it will be 0 or 1.

Show the 1984 winners and subject ordered by subject and winner name; but list chemistry and physics last.
