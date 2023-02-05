# Quiz
① Create the classes described below ② UML diagram.

# Code

## Python file 

```.py
class Person:
    def __init__(self, age, name):
        self.age = age
        self.name = name

        if not isinstance(name, str) or not isinstance(age, int):
            raise TypeError

    def __repr__(self):
        return f"[Person Class] with person: {self.name, self.age}"

    def get_name(self):
        return self.name

    def get_age(self):
        return self.age


class Student(Person):
    def __init__(self, name, age, grade):
        super().__init__(name, age)
        self.grade = grade

    def __repr__(self) -> str:
        return f"[Student Class] with student: {self.name, self.age, self.grade}"

    def get_grade(self):
        return self.grade


class Classroom:
    def __init__(self):
        self.students = []

    def __repr__(self) -> str:
        return f"[Classroom Class] with students: {self.students}"

    def add(self, new_student):
        self.students.append(new_student)

    def remove(self, student):
        self.students = [value for value in self.students if value != student]

    def average(self):
        total = 0

        for i in self.students:
            total += int(i.grade)

        return total / len(self.students)


comsci = Classroom()
bob = Student(name='John Doe', age=16, grade='78')
angel = Student(name="Angel", age=23, grade='34')

comsci.add(new_student=bob)
comsci.add(new_student=angel)

print(comsci.average())
```



## Python file 2

```.py
import pytest
from quiz36 import Person, Student

def test_Person():
    person = Person(name="John Doe", age=16)
    assert person.get_name() == 'John Doe'
    assert person.get_age() == 16

def test_Student():
    student = Student(name="John Doe2", age=16, grade='78%')
    assert student.get_name() == 'John Doe2'
    assert student.get_grade() == '78%'

def test_exceptions():
    with pytest.raises(TypeError):
        student = Student(name=24, age=16, grade='78')
        student = Student(name='John Doe3', age="16", grade='78')
```

# Solution

<img width="1306" alt="Screen Shot 2023-02-05 at 5 17 06 PM" src="https://user-images.githubusercontent.com/116609563/216809296-460de4b0-a8eb-4617-bedb-a8b239b6366d.png">




