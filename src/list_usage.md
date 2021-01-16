# Introduction and Usage of Python List

## Introduction

Unlike Java, Python Lists can store different data types.  
It's an ordered sequence of *heterogenous* elements.  

    # this is totally okay in python!
    sample_list = ['example', 1, 2, 4.15]
    
    # in java, you'd have to declare the type for the list first
    List<String> list = new ArrayList<String>();
    list.add("hello");
    list.add(4.15) // error!!!

## Initializing lists

    #initialize an empty list
    example_list1 = []

    #initialize with some values in
    example_list2 = ['hello', 'welcome', 3.14, 2]

    #initialize with some values using a range function
    example_list3 = list(range(10))
    #output for example_list3 is [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

## Functions you can use on lists

### Adding elements

Primarily there are two ways of adding elements to a list.

**append(elem)** adds the element to the end of the list.

    l = [1, 2, 3, 4, 5]
    l.append(6)
    # [1, 2, 3, 4, 5, 6]

**insert(index, eleme)** adds the element to the desired index of list.

    l = [1, 2, 3, 4, 5]
    l.insert(2, 2.5)
    #l = [1, 2, 2.5, 3, 4, 5]

What happens when the index doesn't exist? i.e. the list has the length less than the value of *index*?

    l = list(range(1, 6))
    l.insert(10, 10) // insert at position 10 which doesn't exist!
    # l = [1, 2, 3, 4, 5, 10]
    # it just appends to the end of the list!

