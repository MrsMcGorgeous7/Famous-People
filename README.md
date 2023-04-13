/** Actors_actresses:
KekeP (9)
Oprah (8)
Rihanna (7)
RavenS(6)
CreeS (5)
JamesEJ (4)
WillS (3)
SamuelLJ (2)
**/

CREATE TABLE actors_actresses (id INTEGER PRIMARY KEY AUTOINCREMENT, 
name_id TEXT, 
movie_year INTEGER,
movie_title INTEGER,
singer TEXT,
author TEXT,
voice_over TEXT,
types_id INTEGER);


INSERT INTO actors_actresses VALUES (9, "KekeP",2020,"Proud Family",6,5,8,"Human");
INSERT INTO actors_actresses VALUES (8, "Oprah",2009,"Princess and the Frog",0,9,3,"Human");
INSERT INTO actors_actresses VALUES (7, "Rihanna",2015,"HOME",9,0,7,"Human");
INSERT INTO actors_actresses VALUES (6, "RavenS",2008,"Tinkerbell Fairies",7,2,5,"Human");
INSERT INTO actors_actresses VALUES (5, "CreeS",1998,"Rugrats Movies",0,0,10,"Human");
INSERT INTO actors_actresses VALUES (4, "JamesEJ",2007,"Lion King",0,6,8,"Animal");
INSERT INTO actors_actresses VALUES (3, "WillS",2004,"Shark Tale",6,5,8,"Animal");
INSERT INTO actors_actresses VALUES (2, "SamuelLJ",2004,"Incredibles",0,0,9,"Human");

CREATE TABLE genre_children (id INTEGER PRIMARY KEY, name TEXT);
INSERT INTO genre_children VALUES (1, "Childrens crime fighting");
INSERT INTO genre_children VALUES (2, "Childrens TV shows");
INSERT INTO genre_children VALUES (3, "Childrens comedy");

CREATE TABLE characters (id INTEGER PRIMARY KEY, name_id INTEGER, types_id TEXT);
INSERT INTO characters VALUES (2, "Frozone","Human");
INSERT INTO characters VALUES (3, "Oscar","Animal");
INSERT INTO characters VALUES (4, "Mufasa","Animal");
INSERT INTO characters VALUES (5, "Susie Carmichael","Human");
INSERT INTO characters VALUES (6, "Iridessa","Human");
INSERT INTO characters VALUES (7, "Tip","Human");
INSERT INTO characters VALUES (8, "Eudora","Human");
INSERT INTO characters VALUES (9, "Penny Proud","Human");

SELECT characters.name_id,characters.types_id FROM characters 
JOIN actors_actresses
ON characters.id=actors_actresses.id;


SELECT movie_title, movie_year FROM actors_actresses; 
    
SELECT genre_children.name FROM genre_children;     
    

    
