# Quiz
Create a program that creates the SalemanMap using your OOP code
# Code

## Python file 

```.py
from matplotlib import pyplot as plt

import random

class coordinate:
    def __init__(self, x, y):
        self.x:int = x
        self.y:int = y

    def __repr__(self)->str:
        return f"[Coordinate]x={self.x} y = {self.y}"

class city:
    def __init__(self, name:str, location:coordinate):
        self.name = name
        self.location = location

    def __repr__(self):
        return f"[City class] A{self.name}located at {self.location}"

    def distance(self, cityB):
        # if isinstance(cityB, city):
        xa, ya = self.location.x, self.location.y
        xb, yb = self.location.x, cityB.location.y
        # else:
        # Raise TypeError('Input should be an object of the class city')
        d = ((xa-xb)**2 + (ya-yb)**2)**(1/2)
        return round(d,2)

class country:
    def __init__(self, name:str):
        self.cities = []
        self.name = name
    def add_city(self, new_city:city):
        if isinstance(new_city, city):
            self.cities.append(new_city)
        else:
            raise ValueError('City must be a city object')


Japan = country(name="Japan")

cities = ["Osaka", "Kobe", "Tokyo", "Saporro", "Yokohama", "Kyoto", "Nagoya", "Fukuoka", "Saitama", "Kawasaki"]

x = []
y = []

for City in cities:
    coord = coordinate(random.randint(1, 100), random.randint(1, 100))
    CITY = city(City, coord)
    Japan.add_city(CITY)

plt.scatter(x, y)
plt.show()
```

# Solution

<img width="493" alt="Screen Shot 2023-02-05 at 5 48 21 PM" src="https://user-images.githubusercontent.com/116609563/216809954-c428e5d4-5ae1-42e1-b78b-f8e34114225f.png">



