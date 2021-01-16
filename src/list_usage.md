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

## Useful list functions

### Adding elements

Primarily there are two ways of adding elements to a list.

**append(elem)** adds the element to the end of the list. O(1) operation.

    l = [1, 2, 3, 4, 5]
    l.append(6)
    # [1, 2, 3, 4, 5, 6]

**insert(index, eleme)** adds the element to the desired index of list. O(n) operation.

    l = [1, 2, 3, 4, 5]
    l.insert(2, 2.5)
    # [1, 2, 2.5, 3, 4, 5]

What happens when the index doesn't exist? i.e. the list has the length less than the value of *index*?

    l = list(range(1, 6))
    l.insert(10, 10) // insert at position 10 which doesn't exist!
    # [1, 2, 3, 4, 5, 10]
    # it just appends to the end of the list!

**remove(elem)** removes the first element that appears in the list. This means when there are duplicate elements, it will only remove one of it. O(1) operation.

    l = ['mark', 'marcus', 'catherine', 'emma', 'mark', 'jason']
    l.remove('mark')
    # ['marcus', 'catherine', 'emma', 'mark', 'jason']

What happens when there is no element to remove?

    l = ['mark', 'marcus', 'catherine', 'emma', 'mark', 'jason']
    l.remove('xavier')

This results ValueError

    ValueError          Traceback (most recent call last)
    <ipython-input-16-6655acfa2bb3> in <module>
        ----> 1 l.remove('xavier')
    ValueError: list.remove(x): x not in list

**pop(index)** removes the item at the given index and then returns the value removed. O(1) operation.

    l = ['mark', 'marcus', 'catherine', 'emma', 'mark', 'jason']
    l.pop(2)
    # 'catherine' -> this is the value returned
    # l is now ['mark', 'marcus', 'emma', 'mark', 'jason']

**reverse()** reverses the list.

    l = list(range(1, 11))
    l.reverse()
    # [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

**count(elem)** counts the number of occurrence of the element in the list.

    import random
    l = []
    for i in range(20):
        # generate a random number between 0 and 5 exclusive
        # then append to the list
        l.append(random.randint(0, 5))
    
    #now l is [3, 4, 4, 4, 3, 3, 4, 3, 1, 2, 0, 1, 2, 0, 2, 5, 3, 4, 3, 3]
    l.count(3)
    # returns 7