# PJDB
A database of Pearl Jam concerts owned by my wife, who has too damn many.

As of 08/03/2020, Database structure is complete and functional. Concert entries are far from complete. That's a lot of data entry.
Guests table isn't filled in, either.

## Handy Query Examples:

 You can of course get a pile of results narrowed by any field, like all shows in the USA: `Select date, city, country from concerts where country != 'USA';'`
 
 Continents table is separate, matching all countries to continents. You have to use a join to find a slection of shows by continent, like 
  `SELECT * from concerts
 inner join continents on concerts.country=continents.country
 where continent='Europe'
 order by date;` to show all European concerts.
