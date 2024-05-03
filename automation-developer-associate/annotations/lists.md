# Working with lists

- List variables are collection type of variables. Meaning that they're part of the **System.Collections** namespace. 
- Lists, queues, arrays, hash tables, and dictionaries are all part of the **System.Collections** namespace.
- They can store numerous elements, like names, numbers, time coordinates, and many others.

Lists provide specific methods of manipulation, such as:

- Adding and removing items.
- Searching for an element.
- Looping through the items (and performing certain actions on each).
- Sorting the objects.
- Extracting items and converting them to other data types.

## About lists and arrays:

- What is a 'List' variable type?
	- The List<T>  is a data structure part of the System.Collections.Generic namespace consisting of objects of the same data type. 
	- The '<T>' represents the type of elements in the list, for example strings or integers.
	- Each object has a fixed position in the list, and thus it can be accessed by the specific index.
	- Additionally, it provides methods for searching, sorting, and manipulating lists.

- What is an 'IList' variable type?
	- The **IList** is actually an Interface. In other words, it is a collection of objects that can be accessed individually by their specific **indexes**. As in the case of **List**, the '<**T**>' represents the **type** of elements in the list. The **IList<T>** generic interface is a descendant of the **_ICollection<T>_** generic interface and is the base interface of all generic lists. 
	- Both **List** and **IList** type of variables can be initialized with '**new list (of...)**'. For example, if we have a List of IList of String elements type, looking like 'List<IList<String>>', we can write the following value in the Default value field to initialize it:  
	- **new List (of IList(of String))**  
	- The same initialization value applies for the 'IList<List<String>>' type of variable.

- What is the difference between lists and arrays?
	- To begin with, both lists and arrays are collection types of variables.
	- The **array** variable enables you to store multiple values of the same type. UiPath Studio supports as many types of arrays as it does types of variables. This means that you can create an array of numbers, one of strings, one of Boolean values and so on.
	- While arrays are fixed-size structures for storing multiple objects, lists allow us to add, insert, and remove items.
	- If you want to work with a collection that doesn’t have a fixed number of elements, you can use a list instead of an array.

## How to initialize list variables

Prior to populating lists with values, the lists need to be initialized.

1. The first way was to create a list type of variable. Then, we used a **Build Collection** activity to add items to the list and specify the list variable to hold the items. 
    
2. The second way was to create a list type of variable, then add the items inside the Default value field. Then, initialize the list by typing new List of Type from the specified items.