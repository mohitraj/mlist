# Mlist
Mlist is a Python list for new advance  methods created By Mohit
https://www.linkedin.com/in/mohit-990a852a/

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install Mlist
```

## Usage

```python
from mlist import Mlist 

# To show the difference between two mlist 
>>> list2 = Mlist([1,2,5,6])
>>> list1 = Mlist([1,2,3,4])
>>>
>>> list1.diffshow(list2)
[1, 2]
>>> list1
[1, 2, 3, 4]
>>>
# Based on particular element 
>>> list1 = Mlist([(1,"a"),(2,"b"),(3,"c"),(4,"d")])
>>>
>>> list2 = Mlist([(10,"a"),(20,"b"),(30,"k"),(40,"l")])
>>>
>>> list1.diffshow(list2,1,1)
[(1, 'a'), (2, 'b')]
>>>
>>> list1 = Mlist([(1,"a"),(2,"b"),(3,"c"),(4,"d")])
>>>
>>> list2 = Mlist([("a",10),("b",20),("k",30),("l",40)])
>>>
# Criteria 2 dimension, 1,0 means Ist value from inner tuple of list1 and 0th value from inner tuple of list2
>>> list1.diffshow(list2,1,0)
[(1, 'a'), (2, 'b')]

>>> list1 = Mlist([1,2,3,4])
>>> list2 = Mlist([1,2,5,6])
>>>
>>> list1.diff(list2)
>>> list1
[3, 4]

#Get all the indexes
>>> list1 = Mlist([1,2,3,4,5,1,3,1,2,3,4,5])
>>>
>>> list1.indexall(2)
[1, 8]
>>> list1.indexall(5)
[4, 11]
>>>
#Remove all occurrence(s) of given item
>>> list1.removeall(5)
>>> list1
[1, 2, 3, 4, 1, 3, 1, 2, 3, 4]
>>>
# Remove duplicate items
>>> list1.dupr()
>>> list1
[1, 2, 3, 4]
>>>
>>> list1 = Mlist([1,2,3,4])
>>>
>>> list2 = Mlist([1,6,7,2])
>>>
# Substract two lists
>>> list1 - list2
<generator object Mlist.__sub__.<locals>.<genexpr> at 0x00000221FDDE69E0>
>>> [list1 - list2]
[<generator object Mlist.__sub__.<locals>.<genexpr> at 0x00000221FDE49660>]
>>>
>>> Mlist(list1 - list2)
[3, 4]
# lookup like Vlookup
>>> from mlist import Mlist
>>> m1 = Mlist()
>>> m2 = Mlist()
>>> m1.csv_read("G:\\Mlist_experiment\\book1.csv")
[['1', 'a', '400'], ['2', 'b', '500'], ['3', 'c', '600'], ['4', 'd', '700']]
>>>
>>> m2.csv_read("G:\\Mlist_experiment\\book2.csv")
[['Python', '1', '', 'A'], ['java', '2', '', 'B']]
>>>
>>> m1.lookup(m2,0,1)   # 0 means 0 indexed column of m1 and 1 indexed coloum of m2
[['1', 'a', '400'], ['2', 'b', '500']]
>>>
>>> m3=m1.lookup(m2,0,1)
>>> m3
[['1', 'a', '400'], ['2', 'b', '500']]
>>> type(m3)
<class 'mlist.mohit.Mlist'>
>>> m3.csv_write("G:\\Mlist_experiment\\book3.csv")

#Club Two lists 
>>> from mlist import Mlist
>>> m1 = Mlist()
>>> m2 = Mlist()
>>>
>>> m1.csv_read("G:\\Mlist_experiment\\book1.csv") 
[['1', 'a', '400'], ['2', 'b', '500'], ['3', 'c', '600'], ['4', 'd', '700']]
>>> m2.csv_read("G:\\Mlist_experiment\\book2.csv")
[['Python', '1', '', 'A'], ['java', '2', '', 'B']]
>>>
>>> m1.club(m2,0,1) #0 means 0 indexed column of m1 and 1 indexed coloum of m2
>>> m1
[['1', 'a', '400', 'Python', '', 'A'], ['2', 'b', '500', 'java', '', 'B'], ['3', 'c', '600'], ['4', 'd', '700']]
>>> m1.csv_write("G:\\Mlist_experiment\\book4.csv")
>>>

```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
