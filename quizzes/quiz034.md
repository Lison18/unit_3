# Quiz

Create a new Python function called to_roman(num) that takes a single integer as input. It returns a string representing the Roman numeral equivalent of the input number. 

Conditions: The function should only work for integers below 100, if the input is greater than 100, raise a ValueError with a message indicating that the input must be less than or equal to 100.

Example:
to_roman(37)  -> 'XXXVII'
to_roman(44)  -> 'XLIV'
to_roman(100) -> 'C'
to_roman(101) -> ValueError("Input number must be less than or equal to 100")


# Code

## Python file 


```.py
def to_roman(num):
    if num > 100:
        raise ValueError()


    rom_dict = [
        [100, 'C'],
        [90, 'XC'],
        [90, 'XC'],
        [50, 'L'],
        [40, 'XL'],
        [10, 'X'],
        [9, 'IX'],
        [5, 'V'],
        [4, 'IV'],
        [1, 'I']
    ]

    output = ''

    while num > 0:
        for n,r in rom_dict:
            if n <= num:
                 output += r
                 num -= n
                 break


    return output

print(to_roman(87))
```



## kv file

```.py
from quiz34 import to_roman
import pytest


def test_to_roman():
    assert to_roman(1) == 'I'
    assert to_roman(4) == 'IV'
    assert to_roman(9) == 'IX'
    assert to_roman(37) == 'XXXVII'
    assert to_roman(44) == 'XLIV'
    assert to_roman(50) == 'L'
    assert to_roman(99) == 'XCIX'
    assert to_roman(100) == 'C'
    assert to_roman(77) == 'LXXVII'
    assert to_roman(93) == 'XCIII'


def test_to_roman_exceptions():
    # check that the program raises a ValueError
    with pytest.raises(ValueError):
        to_roman(101)
```
# Solution

<img width="1306" alt="Screen Shot 2023-02-05 at 5 17 06 PM" src="https://user-images.githubusercontent.com/116609563/216808831-d8b5326f-b8ab-4226-a6ba-1a4a7fb298d6.png">

