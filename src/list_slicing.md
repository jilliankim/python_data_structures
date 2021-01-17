List slicing in Python is a flexible tool to generate a new list from an existing list. Python supports slicing for any ordered data types, like lists and String as well.

The general notation for slicing is
    
    list[start_idx:end_idx]
    start_index - inclusive
    end_idx -  exclusive

Neither start_index nor end_index are required.

    list[start_idx:]
    # from start_idx to the end of the list
    list[:end_idx]
    # from beginning of the list to the end_idx-1
    list[:]
    # all numbers within the range

## Slicing examples

It's easier to use keep this diagram in mind before proceeding.

    +---+---+---+---+---+---+---+---+---+
    | t | a | n | g | e | r | i | n | e |
    +---+---+---+---+---+---+---+---+---+
      0   1   2   3   4   5   6   7   8  
     -8  -7  -6  -5  -4  -3  -2  -1
    
You'll see why we need the negative indexes!


    tangerine_list = list('tangerine')
    # ['t', 'a', 'n', 'g', 'e', 'r', 'i', 'n', 'e']
    tangerine_list[2:]
    # ['n', 'g', 'e', 'r', 'i', 'n', 'e']
    tangerine_list[:4]
    # ['t', 'a', 'n', 'g']

Exercise with negative indexes!

    tangerine_list[-4:] 
    # ['r', 'i', 'n', 'e'], last 4 items in the list
    tangerine_list[:-4]
    # ['t', 'a', 'n', 'g', 'e']
    # this one you might need more thinking, because from the above diagram,
    # you might expect ['r', 'i', 'n', 'e']. But think about it this way - everything except last 4 elements.

