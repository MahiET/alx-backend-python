 Python - Variable Annotations
 =

Type hints cheat sheet (Python 3)
=

Technically many of the type annotations shown below are redundant, because mypy can derive them from the type of the expression. So many of the examples have a dual purpose: show how to write the annotation, and show the inferred types.

* <h2>Variables</h2>

* <h2>Built-in types</h2>

* <h2>Functions</h2>

typing — Support for type hints

The Python runtime does not enforce function and variable type annotations. They can be used by third party tools such as type checkers, IDEs, linters, etc.

This module provides runtime support for type hints. The most fundamental support consists of the types Any, Union, Callable, TypeVar, and Generic. For a full specification, please see PEP 484. For a simplified introduction to type hints, see PEP 483.


                  def greeting(name: str) -> str:
                  return 'Hello ' + name

In the function greeting, the argument name is expected to be of type str and the return type str. Subtypes are accepted as arguments.

New features are frequently added to the typing module. The typing_extensions package provides backports of these new features to older versions of Python.