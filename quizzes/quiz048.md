# quiz 48
Use the database bitcoin_exchange.db: and create a program that check the hash signature stored for every transaction and prints:
 Tx(id=1)Signature matches or  Tx(id=1)Error signature

# Code

```.py
import sqlite3
from secure_password import check_password

end_code = "\033[00m"
red = "\033[0;31m"
green = "\033[0;32m"

class DatabaseWorker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        return self.cursor.execute(query).fetchall()

    def save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()

db = DatabaseWorker("bitcoin_exchange.db")
result = db.search("SELECT * from ledger")
db.close()

for row in result:
    hash, *tx = row[4:]
    string_hash = f"id {row[0]},sender_id {row[1]},receiver_id {row[2]},amount {row[3]}"
    if check_password(hashed_password=hash, user_password=string_hash):
        print(f"{green}Tx(id={row[0]}) Signature matches{end_code}")
    else:
        print(f"{red}Tx(id={row[0]}) Error signature{end_code}")

````
# Proof of work

<img width="1156" alt="Screen Shot 2023-03-19 at 12 49 49 AM" src="https://user-images.githubusercontent.com/116609563/226116254-b24c31e9-09cc-4977-98df-bed5adcbfb62.png">
