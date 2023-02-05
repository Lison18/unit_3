# Quiz
Write the function mystery and pass the tests contained in the file test_quiz_33.py


The function takes two lists, list1 and list2, as input and creates an empty list called output.  It then iterates over the elements of list1 using a loop, and for each element, it iterates over the elements of list2 using another loop. For each pair of elements, the function checks if the two elements are equal. If they are, it adds the element from list1 to the output list. After both loops have completed, the function returns the output list.

# Code

## Python file 
```.py
def mystery(list1, list2)->str:
    output = []
    for element in list1:
        for element2 in list2:
            if element == element2:
             output.append(element2)
    return output
 ```
 
 ## Python file 2
 
 ```.py
 from quiz33 import mystery

def test_empty_lists():
  assert mystery([], []) == []

def test_one_common_element():
  assert mystery([1, 2, 3], [3, 4, 5]) == [3]

def test_multiple_common_elements():
  assert mystery([1, 2, 3, 4], [3, 4, 5, 6]) == [3, 4]
  
 ```
 
 # Solution 
 
 <img width="1306" alt="Screen Shot 2023-02-05 at 5 17 06 PM" src="https://user-images.githubusercontent.com/116609563/216808717-3ceb6614-b719-48df-b578-8a2592d2261a.png">

  
  



   
