# pytest

## Useful options

### To ignore entire modules or directories

--ignore=/path/to/tests OR /path/to/tests/test.py

### More detailed traces

--verbose

## pytest.ini

_Example 1:_ have pytest look for "check" instead of "test" can also be defined in tox.ini or setup.cfg file, although the section name in setup.cfg files should be "tool:pytest"

```text
[pytest]
python_files = check_*.py
python_classes = Check
python_functions = *_check
```

## Fixtures

```text
@pytest.fixture(scope="module")
def fixture_func:
```

Afterwards each test function can include fixture\_func as parameter to run it and use the objects created in there.

## Setup/Teardown

Parameter unnecessary if version &gt; pytest 3.0, except for classes

```text
def setup_module(module):
def teardown_module(module):
```

```text
@classmethod
def setup_class(cls):
@classmethod
def teardown_class(cls):
```

```text
def setup_function(function):
def teardown_function(function):
```

