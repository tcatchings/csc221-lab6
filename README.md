# Fixing a broken codebase

Fork this repository. Fix the code in lab6.py such that it will run
without testing errors. If you want more descriptive errors, you can
use the following commands:

```bash
$ cd /path/to/csc221-lab6
$ nosetests lab6.py
FFF
======================================================================
FAIL: lab6.test_match_ends
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/Users/dogwynn/anaconda3/lib/python3.5/site-packages/nose/case.py", line 198, in runTest
    self.test(*self.arg)
  File "/Users/dogwynn/courses/csc221/2016-spring/labs/lab6/csc221-lab6/lab6.py", line 37, in test_match_ends
    assert_equal(match_ends(['aba', 'xyz', 'aa', 'x', 'bbb']), 3)
AssertionError: None != 3

======================================================================
FAIL: lab6.test_front_x
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/Users/dogwynn/anaconda3/lib/python3.5/site-packages/nose/case.py", line 198, in runTest
    self.test(*self.arg)
  File "/Users/dogwynn/courses/csc221/2016-spring/labs/lab6/csc221-lab6/lab6.py", line 44, in test_front_x
    ['xaa', 'xzz', 'axx', 'bbb', 'ccc'])
AssertionError: None != ['xaa', 'xzz', 'axx', 'bbb', 'ccc']

======================================================================
FAIL: lab6.test_sort_last
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/Users/dogwynn/anaconda3/lib/python3.5/site-packages/nose/case.py", line 198, in runTest
    self.test(*self.arg)
  File "/Users/dogwynn/courses/csc221/2016-spring/labs/lab6/csc221-lab6/lab6.py", line 54, in test_sort_last
    [(2, 1), (3, 2), (1, 3)])
AssertionError: None != [(2, 1), (3, 2), (1, 3)]

----------------------------------------------------------------------
Ran 3 tests in 0.002s

FAILED (failures=3)
```

I am indifferent to where you solve this problem, whether on
pythonanywhere.com or on the department server or your personal
computer.

However, the above testing solution assumes that your Python
environment has the "nose" unit testing module installed in it. To see
if you do:

```bash
$ python -m "nose" --version
python -m nose version 1.3.7
```

If the above fails, then you do not have nose installed. To install:

```bash
$ pip install nose
```

Or possibly:

```bash
$ sudo pip install nose
```
