# Introduction #

Additions and modifications to the code in this project should conform to these style guidelines.


# Rules #

### Naming conventions ###

|**Type**| **Public**| **Internal** |
|:-------|:----------|:-------------|
|Packages| `lower_with_under`  |  |
|Modules |`lower_with_under` |`_lower_with_under` |
|Classes | `CapWords` | `_CapWords` |
|Exceptions | `CapWords`  |  |
|Functions | `CapWords()`, `lower_with_under()` | `_CapWords()`, `_lower_with_under()` |
|Global/Class Constants | `CAPS_WITH_UNDER` | `_CAPS_WITH_UNDER` |
|Global/Class Variables | `lower_with_under` | `_lower_with_under` |
|Instance Variables | `lower_with_under` |`_lower_with_under` (protected) or `__lower_with_under` (private) |
|Method Names | `CapWords()`, `lower_with_under()` | `_CapWords()`, `_lower_with_under()` (protected) or `__CapWords()`, `__lower_with_under()` (private) |
|Setter/Getter Method Names | `foo()`, `set_foo()`  |  |
|Function/Method Parameters | `lower_with_under`  |  |
|Local Variables | `lower_with_under` |  |


### Imports ###

Always import modules explicitly - never use `from x import *`, instead use
```
from x import y
from x import z
import w
```

### Global Variables ###

Global (module visible) variables should only be used for constants.

### Default Argument Values ###

Feel free to use them in accordance with the following guidelines
  * Do not use mutable types for default values (lists, dicts, etc)
  * When calling the method, specify the name of the default value, example:
```
Foo(1)
Foo(1, b=2)
```

### Line Length ###

80 characters

### Blank Lines ###

1 blank line between methods within a class, between the docstring and code and within a method to break the instructions into logical sections.

2 blank lines between top level definitions.

For example
```
import xyz


class Foo(object):
  def __init__(self):
    pass

  def do_something(self):
    pass


def module_function():
  return 'ok'


if __name__ == '__main__':
  print 'Running this module as a script.'
```

## Unit Tests ##

Bug fixes and new modules should be accompanied with test cases in the appropriate test modules. The test module directory structure mirrors that of the src directory. For example, unit tests for the `gdata.data` module live in `tests/gdata_tests/data_test.py`. If you have written a new module, you can speed up the process of writing you unit tests by using one of the available CodeTemplates.