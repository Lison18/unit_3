# quiz 43
Create the database for a movies described by the ER diagram below and INSERT your two favorite movies.

# SQL
```.py
CREATE table if not exists Movies(
    id INTEGER PRIMARY KEY,
    name TEXT,
    producer TEXT,
    director TEXT,
    category TEXT,
    budget INTEGER,
    year INTEGER)

INSERT INTO Movies (name, producer, director, category, budget, year) VALUES ('Geisha memories', 'Lucy Fisher', 'Rob Marshall', 'autobiography', 85000000, 2005);
INSERT INTO Movies (name, producer, director, category, budget, year) VALUES ('Marie Stuart, queen of Scotland', 'Josie Rourke', 'Beau Willimon', 'drama', 25000000, 2018);
```


# Proof of work 


<img width="1011" alt="Screen Shot 2023-03-18 at 11 05 56 PM" src="https://user-images.githubusercontent.com/116609563/226111190-0b5a4b03-c4cd-442c-aa43-b2227ed00cd2.png">
