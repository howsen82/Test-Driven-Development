# Test Driven Development (TDD)

**Automated testing**
* Free developers from manual testing
* Changes how developers write tests

**Testing Frameworks (xUnit)**
* JUnit for Java
* PyUnit for Python
* NUnit for .Net
* Embunit for C/C++
* Jasmine for Javascript
* Mocha for Node.js
* SimpleTest for PHP

**Python testing frameworks**
* PyUnit
* Pytest
* Doctest
* RSpec (Popular framework for Ruby)
* Nose (Test runner, with color formatting)
* Coverage

**Tools**

<ins>PyUnit</ins>

Unit test on python
```
python -m unittest
```
Test in verbose mode
```
python -m unittest -v
```


<ins>Nose</ins>

Installation (Nose, Pinochio, Coverage)
```
pip install nose
pip install pinochio
pip install coverage
```
Test
```
nosetests
```
Test in verbose mode
```
nosetests -v
```
Test in well formatting (With title)
```
nosetests --with-spec
```
Test in well formatting (With title and color)
```
nosetests --with-spec --spec-color
```
Test with title, color and coverage
```
nosetests --with-spec --spec-color --with-coverage [--cover-erase]
```
Show coverage report
```
coverage report -m
```

Simplify nosetests with configuration
Contents of `setup.cfg` should be:
```
[notests]
verbosity=2
with-spec=1
spec-color=1
with-coverage=1
cover-erase=1
cover-package=<package1.py>

[coverage:report]
show_missing = True
```
Execute test
```
nosetests
```

# Summary
* TDD saves development time and ensures that the code works as expected.
* To create a DevOps pipeline, you must automate all testing.
* Nose is a Python test runner that can add color to test output and call the code coverage tool.
* The Red/Green/Refactor workflow includes three steps:
  * Write a failing unit test case for the code you wish you had
  * Write enough code to pass this test case
  * Refactor the code to improve its quality
* To create a DevOps pipeline, you must automate all testing
* To create assertions in Python, developers can use the assert () function or any additional PyUnit asserts
* Happy paths verify that a function returns positive outcomes when expected, while sad paths confirm that a function responds to exceptions appropriately and without breaking
* Test fixtures are helpful for many testing situations, such as creating mock objects and loading a database with a known data set
* Test fixtures operate at three levels of specificity:
  * Module
  * Test case
  * Test
