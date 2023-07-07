# Kpop-Girl-Group-Views
Views in millions of my favorite female Kpop groups


Kpop views by millions SQL.


–-This query lists the band name and the sum of youtube views in millions
SELECT 
	Band,
sum(views_in_millions) as Total_Views_in_Millions

FROM songs
group by band 


-–I created this table myself from youtube views. I realized I typo’d Sunmmi.

create table songs (
	band varchar(255),
    song varchar(255),
    views int);
	
insert into songs (band, song, views)
values 
 ("Itzy", "Wannabe", 110),
 ("Itzy", "Dolla Dolla", 316),
 ("Itzy", "Cheshire", 128),
 ("Black Pink", "Du Du Du", 2000),
 ("Black Pink", "Boombaya", 1500),
 ("Black Pink", "How you like that?", 1200),
 ("Black Pink", "Kill This Love", 1980),
 ("Dreamcatcher", "Boca",70),
 ("Dreamcatcher", "Scream",47),
 ("Dreamcatcher", "Vision", 23),
 ("Dreamcatcher", "Odd Eye", 50),
 ("Sunmmi", "Heartburn", 56),
 ("Sunmmi", "Stop or Go", 1),
 ("Sunmmi", "Tail",	43),
 ("Everglow", "First", 95),
 ("Everglow", "Dun Dun Dun", 279),
 ("Everglow", "La Di Da",125);

—I wrote this statement to fix the typo

update songs
set band = "Sunmi"
where band = "Sunmmi";
