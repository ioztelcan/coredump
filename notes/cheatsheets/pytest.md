## Useful options

### To ignore entire modules or directories
--ignore=/path/to/tests OR /path/to/tests/test.py

### More detailed traces
--verbose

## pytest.ini

*Example 1:* have pytest look for "check" instead of "test"
can also be defined in tox.ini or setup.cfg file, although the section
name in setup.cfg files should be "tool:pytest"

```
[pytest]
python_files = check_*.py
python_classes = Check
python_functions = *_check
```

## Fixtures

```
@pytest.fixture(scope="module")
def fixture_func:
```

Afterwards each test function can include fixture_func as parameter to run it and use the objects created
in there.

## Setup/Teardown
Parameter unnecessary if  version > pytest 3.0, except for classes

```
def setup_module(module):
def teardown_module(module):
```

```
@classmethod
def setup_class(cls):
@classmethod
def teardown_class(cls):
```

```
def setup_function(function):
def teardown_function(function):
```
