# Quiz 46

A company requires a program that calculates the average word length from a database of words. Complete the following code:

# Python file
```.py
import sqlite3

haiku = """Code flows like a stream
Algorithms guide its way
In silence, it solves"""

# create connection and cursor
connection = sqlite3.connect("wordlengths.db")
cursor = connection.cursor()

# create table if it does not exist
cursor.execute("""
    CREATE TABLE IF NOT EXISTS Words (
        id INTEGER PRIMARY KEY,
        word TEXT NOT NULL,
        length INTEGER NOT NULL
    )
""")

# insert every word and length in the database
for word in haiku.split():
    cursor.execute("INSERT INTO Words (word, length) VALUES (?, ?)", (word, len(word)))

# query the average of all the lengths
query = "SELECT AVG(length) FROM Words"
result = cursor.execute(query).fetchone()[0]

# close the database connection
connection.close()

# print the average word length
print("average word length is", result)
print("average word length is", result)

````

# Proof of work

<img width="1186" alt="Screen Shot 2023-03-19 at 12 34 34 AM" src="https://user-images.githubusercontent.com/116609563/226115534-28a21715-1da0-4ec5-a233-86a80abcdba1.png">

