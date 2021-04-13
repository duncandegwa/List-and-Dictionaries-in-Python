Lists and dictionaries bind together many major views in Python programming. This article explains how to begin carrying out operations in lists and dictionaries.These operations include accessing elements, modifying elements, and more.



### Prerequisites
To gain understanding in this lesson you are required to have mastered some basic knowledge of Python programming language and
python or PyCharm installed in your machine.

### Lists
 Lists enable you to store a set of items in place. Lists take the form of arrays in other languages like java.
 Lists in Python take the following syntax:
 ```
listname = [item1,item2,item3]
 ```

The following is an example of a list of cars:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
print(cars)  #python returns the list of cars including the square brackets
```
Output:
 ```
 ['volvo', 'subaru', 'skyline', 'ford']
 ```

### Accessing Elements in a List
You can access elements in a list by writing the name of the list, index of the element put in square brackets respectively. In Python indices begin at 0, not 1, hence the first item in a list takes index 0, not 1.
You can access any item in a list by just subtracting 1 from its place in the list.
For example, to retrieve the third item in a list, you call the item in index 2.
The following requests for the cars at index 0 and 3:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
print(cars[0]) # returns the first item -volvo
print(cars[3]) #returns the fourth item -ford
```
Output:
```
 volvo
 ford
```
Python has a unique way of getting the last item in a list. If you print an item at index -1 Python gives back the last item in the list. Indices -2,-3 , and -4 gives the second last,  third last, and fourth last item from the end of the list respectively, and so on.

```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
print(cars[-1])   #returns the last item in the list that is ford
```
This code prints the last element which is _ford_.

### Change, add and remove elements in a List

#### 1. Changing elements in a List
To alter an item in the list, use the title of the list along with the index of the item you want to alter and then give the current value you need that item to have.
For instance, in our list of cars, the second item is *'subaru'*. Let’s change the value to *'suzuki'*.
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
print(cars)      #returns the original list with subaru as the second item
cars[1]='suzuki'  #returns the list with suzuki as the second item
print(cars)
```
The above code gives the following output:
```python
['volvo', 'subaru', 'skyline', 'ford']
['volvo', 'suzuki', 'skyline', 'ford']
```
#### 2. Adding elements in a List
To add new elements at the end of the list, use the append() method.
For example, let’s add *'audi'* in our list of cars
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
cars.append('audi') #adds 'audi' at the end of the list
print(cars)
```
Output: 
  ```
 ['volvo', 'subaru', 'skyline', 'ford', 'audi']
  ```
You can also use the insert() method to add a new item at any point in your list by specifying the index position of the new item and the value of the new item.
Let’s take a look at this example:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
cars.insert(2,'audi') #adds the value 'audi' at the begging of the list(at index o)
print(cars)
```
Output:
 ``` 
 ['audi', 'volvo', 'subaru', 'skyline', 'ford'] 
 ```
In this example the other values in the list moves one position to the right.
#### 3. Removing Elements from a List
If only the location of an item you want to do away with is well known, use the del statement.
Example:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
del cars[0]
print(cars)
```
The first car *'volvo'* is removed from the list  ```['subaru', 'skyline', 'ford'] ```

If only the value of the item you want to remove is known, use the remove() method.
To illustrate this, let’s withdraw the item _'subaru'_ from our list of cars.
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
cars.remove('subaru') #removes subaru from the list
print(cars)
```
When we run this code in the above example we get the output as  ```['volvo', 'skyline', 'ford'] ```
>NOTE: When a value appears more than once in a list, the remove() method only deletes the first event of the value you state.

### Sorting a List
Sorting is organizing your list by some basis eg. reverse order, ascending order, or alphabetical order.
Use the sort() method to sort a list. To understand this better let's arrange our list of cars alphabetically in the example below.
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
cars.sort()  #arranges the list alphabetically
print(cars)
```
This code returns the list arranged alphabetically that is ```['ford', 'skyline', 'subaru', 'volvo'] ```

The reverse() method is used to reverse the initial order of the list.For instance,let's print our list of cars in reverse sequence:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford']
cars.reverse()
print(cars)
```
>NOTE: reverse() doesn’t sort backward alphabetically; it just 
reverses the order of the list.

### Slicing a List
To derive a segment, specify the index of the first and last elements you desire to work with. In Python, we use Colon(:) as a slicing operator.
Syntax:

`list_name[Index_start:Index_end]`

Example, when you request `[0:3]` python returns the items at index 0,index 1 and index 2.To illustrate this let's take a look at the following code:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford','isuzu']
print(cars[0:3]) #lists the first three cars
```
Output:
 ```['volvo', 'subaru', 'skyline'] ```
 
When you exclude the starting index in a slice, Python automatically begins the slice at the start of the list. Simillarly if you omit the last index, Python returns all elements from starting index to the end of the list. Below is an example of a python code that depicts this:
```python
cars = ['volvo', 'subaru', 'skyline', 'ford', 'isuzu']
print(cars[:3]) #starts at the begging of the list to the third item
print(cars[3:]) #starts from the fourth item to the end of the list
```
Output:
```python
 ['volvo', 'subaru', 'skyline']
 ['ford', 'isuzu']
   ```
    
###  Looping through a list 
To perform the same action in each element in a list, use the Pythons *for* loop.
For instance, let’s assume we have a list of footballers and we want to pull out each name in the foootballers' list. We use *for* loop to pull out each name:
```python
footballers = ['messi', 'ronaldo', 'salah']  #define the list
for footballer in footballers:   #define the for loop
 print(footballer)
```
We get the output as:
```
messi
ronaldo
salah
```
The second line in the above code(*for footballer in footballers:*) informs Python to pull a name from the footballers list and save it in the variable *footballer*.The third line (*print(footballer)*) prints the name that was stored in the variable *footballer*.The second and the third line are redone till there are no further items in the list.

### Dictionaries
In Python, a dictionary is a group of key-value pairs where each key is linked to a value. A dictionary is enclosed with curly brackets{}, with a series of key:value pairs inside.
Syntax:
```python
dict_name={
    key:value,
    key:value}
```
Example :
```python
stock_1={
 'type':'volvo',
 'color':'black'
}
```
### Accessing Values in a Dictionaries
You acquire values related to a key by listing the name of the dictionary and putting the key inside the square brackets[] as indicated below:
```python
stock_1={
 'type':'volvo',
 'color':'black'
}
print(stock_1['type'])
```
Python gives back the value connected with the key *'type'* that is `volvo`.

### Adding Items in a Dictionaries
To join a new item into a dictionary, give a value to a new index key. Let’s add a new key *'year'* to our stock_1 dictionary and assign it the value *2014* in the previous code.
```python
stock_1={
 'type':'volvo',
 'color':'black'
}
print(stock_1)      #outputs the initial dictionary
stock_1['year']=2014  #Adding a new key:value
print(stock_1)  #returns the modified dictionary
```
### Changing Values in a Dictionary
You can change a value in a dictionary by referring to its key name. For example, let’s change the value of the *year* in our stock_1 dictionary from *2014* to *2021*:
```python
stock_1={
 'type':'volvo',
 'color':'black',
'year':2014
}
stock_1['year']=2021  #change the value of year from 2014 to 2021
print(stock_1)
```
The output of the above code shows:
 ```
{'type': 'volvo', 'color': 'black', 'year': 2021}
 ```

### Removing Key-Value Pairs in Dictionaries
To remove a key:value pair use the del statement to eliminate it. Give the key you ought to remove and the name of the dictionary to the del statement. For instance, let’s remove the key *'color'* in our stock_1 dictionary:
```python
stock_1={
 'type':'volvo',
 'color':'black',
'year':2014
}
del stock_1['color']   #removes the key-color and its value-black
print(stock_1)
```
Python removes the key *'color'* and its related value *'black'*. The rest of the dictionary remains the same.
 ```
{'type': 'volvo', 'year': 2014}
 ```

### Looping through a Dictionary
To access everything stored in a dictionary, loop through the dictionary using a *for* loop. Assuming we have names and occupations stored in an employees’ dictionary, we can access the name and occupation of each employee using a *for* loop as follows:
```python
employees={
 'julius':'secretary',
 'simon':'treasurer',
 'james':'chairperson'
}
for name, occupation in employees.items():   #method item() returns a list of key value pairs
    print(name, ":", occupation)
```

In the above example, the _for_ loop stores the key in the variable name and its value in the variable occupation:
 ```
julius : secretary
simon : treasurer
james : chairperson
 ```

### Conclusion
In this tutorial, we have gained an understanding of lists and dictionaries on:
  - how to access, alter and remove elements in both lists and dictionaries.
  - how to loop in dictionaries and lists.
  - how to sort and slice a list.
