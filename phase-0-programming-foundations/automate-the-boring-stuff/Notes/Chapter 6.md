# <u>Lists</u>

A list is a value that contains multiple values in an ordered sequence. 

A list begins with an opening square bracket and ends with a closing square bracket, [].

We call values inside the list items. Items are separated with commas.

## Indexes
---
Indexes are used to find a specific item
For example:
    spam = ['cat', 'bat', rat']
    spam[0] = 'cat'
    spam[1] = 'bat
    etc

Because the first index is 0, the last index is the size of the list minus one. 

Python will give you an IndexError error message if you use an index that exceeds the number of values in your list value.

Lists can also contain other list values:
    spam = [['cat','bat'],[10, 20, 30, 40, 50]]
    spam[0] = ['cat', 'bat']
    spam[0][1] = 'bat'
    spam[1][4] = 50

The first index dictates which list value to use, and the second indicates the value within the list value

You can also use negative integers for the index, whereby -1 = last item in list and -2 = 2nd to last item

## Slices
---
You can use a slice to get multiple values from a list. We enter a slice between square brackets, like an index, but include two integers separated by a colon.

In a slice, the first integer is the index where the slice starts. The second integer is the index where the slice ends. The list created from a slice will go up to, but will not include, the value at the second index. 
    spam = ['cat', 'bat', 'rat', 'elephant']
    spam[1:3] = ['bat', 'rat']
    spam[0:-1] = ['cat', 'bat', 'rat']

You can leave out some of the indexes on either side. Leaving out the first index is the same as using 0, or the beginning of the list. Leaving out the second index is the same as using the length of the list, which will slice to the end of the list.

len() = Will return the number of values in a list

## Value Updates
---
You can assign a value at a certain index a different value by putting variable name ( spam[1] ) and setting it equal to whatever yout want ( Swap from 'bat' to lets say 'cow' )

You can also concatenate and replicate lists using + and *. Adding 2 lists will join them into one long one and multiplyinh a list causes it to replicate however many times youve put the integer as.

del statement can be used to delete values at a certain index ( spam[0] will delete the first value of the list )

## in and not operators
---
You can determine whether a value is or isn’t in a list with the in and not in operators:
    'howdy' in ['hello', 'hi', 'howdy', 'heyas'] = True
    'poo' in ['hello', 'hi', 'howdy', 'heyas'] = False
    'howdy' not in ['hello', 'hi', 'howdy', 'heyas'] = False

## Multiple Assignment trick
---
Tuple unpacking is a shortcut that lets you assign multiple variables with the values in a list in one line of code:
    cat = ['fat', 'gray', 'loud']
    size, color, disposition = cat

The number of variables and the length of the list must be exactly equal, or Python will give you a ValueError

## Random & Assignment Operators
---
random.choice() = Returns a randomly selected item from a list
random.shuffle() = Reorders the items in a list

spam += 1:

* spam = spam + 1

spam -= 1:

* spam = spam - 1

spam *= 1:

* spam = spam * 1

spam /= 1:

* spam = spam / 1

spam %= 1:

* spam = spam % 1

Assignment operators can also do string and list concatenation, +=, and string and list replication *=

## Methods
---
- index() = Will return the index of a value inside a list. If a list contain duplicates of the same value, it returns the index of its first appearance
- append() - Adds argument to the end of the list
- insert(index, argument) - Inserts a value at a given index
- remove() method - Accepts a value to remove from the list on which it’s called. Will only remove first instance of value
- sort() - Sorts lists of number values or strings, returning them in numerical/alphabetical order. We can use reverse=True inside brackets to swap to descending order. You cannot sort ists with both number values and strings. If you want your list in alphabetical order but have both uppercase and lowercase letts, use key=str.lower to put it in actual alphabetical orderm rather the capital alphabetical order, then lowercase
- revser() = Reverses order of a list

Methods belong to a single data type. The append() and insert() methods are list methods, and we can call them on list values only, not on values of other data types, such as strings or integers. 

## Sequence Data Types
---
Lists are not the only data type that represnt an ordered sequence of values : lists, strings, range objects returned by range(), and tuples. 

You can do all the same things with sequence values that you can do with lists: indexing, slicing, for loops, len(), and the in and not in operators.

However, lists and strings differ in an important way. A list value is a mutable data type: you can add, remove, or change its values. However, a string is immutable: it cannot be changed. Trying to reassign a single character in a string results in a TypeError error.The proper way to “mutate” a string is to use slicing and concatenation to build a new string by copying from parts of the old string

## Tuple Data Type
---
There are only two differences between the tuple data type and the list data type:
- You write tuples using parentheses instead of square brackets
- Tuples are immutable : you can’t modify, append, or remove their values

If you have only one value in your tuple, you can indicate this by placing a trailing comma after the value inside the parentheses. Otherwise, Python will think you’ve entered a value inside regular parentheses

e.g
    type(('hello',))
    <class 'tuple'>

If you need an ordered sequence of values that never changes, use a tuple

The functions list() and tuple() will return list and tuple versions of the values passed to them - Converting a tuple to a list is handy if you need a mutable version of a tuple value.

## copy and deepcopy functions

- copy.copy() - Can make a duplicate copy of a mutable value like a list or dictionary, not just a copy of a reference.
- If the list you need to copy contains lists, use the copy.deepcopy() function instead of copy.copy(). The copy.deepcopy() function will copy these inner lists as well.
