---
title: 一文让你python从入门到放弃
date: 2021-08-20 10:54:16
categories: python
tags: 
 - tech
 - python
---


- [前言](#前言)
- [运算符(operators)](#运算符operators)
	- [算数运算符(arithmetic)](#算数运算符arithmetic)
	- [比较运算符（comparison)](#比较运算符comparison)
	- [赋值运算符（assigment）](#赋值运算符assigment)
	- [位运算符号（bitwise)](#位运算符号bitwise)
	- [逻辑运算符(logical)](#逻辑运算符logical)
	- [身份运算符(identity)](#身份运算符identity)
	- [成员运算符（membership)](#成员运算符membership)
- [数据类型(data types)](#数据类型data-types)
	- [数字(numbers)](#数字numbers)
	- [字符串(strings)](#字符串strings)
	- [列表(lists)](#列表lists)
	- [元祖(tuples)](#元祖tuples)
	- [集合(sets)](#集合sets)
	- [字典(dictionaries)](#字典dictionaries)
	- [类型转换(type casting)](#类型转换type-casting)
- [流程控制(control flow)](#流程控制control-flow)
	- [`if` statement](#if-statement)
	- [`for`statement](#forstatement)
	- [`while` statement](#while-statement)
	- [`try` statement](#try-statement)
	- [`break` statement](#break-statement)
	- [`continue` statement](#continue-statement)
- [函数(functions)](#函数functions)
	- [函数定义(function_definition)](#函数定义function_definition)
	- [函数范围](#函数范围)
	- [函数默认参数(default_arguments)](#函数默认参数default_arguments)
	- [可变关键字参数(keyword_arguments)](#可变关键字参数keyword_arguments)
	- [任意参数(arbitrary_arguments)](#任意参数arbitrary_arguments)
	- [解开参数包裹(unpacking_arguments)](#解开参数包裹unpacking_arguments)
	- [lambda表达式(lambda_expressions)](#lambda表达式lambda_expressions)
	- [函数文档字符串(function_documentation_string)](#函数文档字符串function_documentation_string)
	- [函数注释(function_annotations)](#函数注释function_annotations)
	- [装饰器(function_decorators)](#装饰器function_decorators)
- [类(classes)](#类classes)
	- [类定义(class defintions)](#类定义class-defintions)
	- [类对象(class objects)](#类对象class-objects)
	- [实例对象(instance objects)](#实例对象instance-objects)
	- [方法对象(method objects)](#方法对象method-objects)
	- [类和实例变量(class and instance variables)](#类和实例变量class-and-instance-variables)
	- [继承(Inheritance)](#继承inheritance)
	- [多重继承(multiple inheritance)](#多重继承multiple-inheritance)
- [模块(modules)](#模块modules)
	- [模块](#模块)
	- [包(packages)](#包packages)
- [错误和异常(errors andd exceptions)](#错误和异常errors-andd-exceptions)
	- [处理异常(handle exceptions)](#处理异常handle-exceptions)
	- [触发异常(raise exceptions)](#触发异常raise-exceptions)
- [文件(files)](#文件files)
	- [读和写(reading and writing)](#读和写reading-and-writing)
	- [文件对象的方法(file methods)](#文件对象的方法file-methods)
- [拓展(additions)](#拓展additions)
	- [`pass`语句](#pass语句)
	- [生成器(generattors)](#生成器generattors)
- [标准库概要(standard libraries)](#标准库概要standard-libraries)
	- [`json`文件](#json文件)
	- [文件通配符(glob)](#文件通配符glob)
	- [正则匹配(`re`)](#正则匹配re)
	- [命令行参数(argparse)](#命令行参数argparse)
	- [数学(math)](#数学math)
	- [日期和时间(date and times)](#日期和时间date-and-times)
	- [数据压缩(data compression)](#数据压缩data-compression)
- [项目框架(Project structure)](#项目框架project-structure)
- [Reference](#reference)
# 前言
- 什么是Python
- Python语法
- 变量

# 运算符(operators)
- 算数运算符(arithmetic)(`+`, `-`, `*`, `/`, `//`, `%`, `**`)
- 比较运算符（comparison）(`==`, `!=`, `>`, `<`, `>=`, `<=`)
- 赋值运算符（assigment）(`=`, `+=`, `-=`, `/=`, `//=` etc.)
- 位运算符号（bitwise)(`&`, `|`, `^`, `>>`, `<<`, `~`)
- 逻辑运算符(logical)(`and`, `or`, `not`)
- 身份运算符(identity)(`is`, `is not`)
- 成员运算符（membership)(`in`, `not in`)

## 算数运算符(arithmetic) 
```python
def test_arithmetic_operators():
    """Arithmetic operators"""

    # Addition.
    assert 5 + 3 == 8

    # Subtraction.
    assert 5 - 3 == 2

    # Multiplication.
    assert 5 * 3 == 15
    assert isinstance(5 * 3, int)

    # Division.
    # Result of division is float number.
    assert 5 / 3 == 1.6666666666666667
    assert 8 / 4 == 2
    assert isinstance(5 / 3, float)
    assert isinstance(8 / 4, float)

    # Modulus.
    assert 5 % 3 == 2

    # Exponentiation.
    assert 5 ** 3 == 125
    assert 2 ** 3 == 8
    assert 2 ** 4 == 16
    assert 2 ** 5 == 32
    assert isinstance(5 ** 3, int)

    # Floor division.
    assert 5 // 3 == 1
    assert 6 // 3 == 2
    assert 7 // 3 == 2
    assert 9 // 3 == 3
    assert isinstance(5 // 3, int)
```

## 比较运算符（comparison)
```python
def test_comparison_operators():
    """Comparison operators"""

    # Equal.
    number = 5
    assert number == 5

    # Not equal.
    number = 5
    assert number != 3

    # Greater than.
    number = 5
    assert number > 3

    # Less than.
    number = 5
    assert number < 8

    # Greater than or equal to
    number = 5
    assert number >= 5
    assert number >= 4

    # Less than or equal to
    number = 5
    assert number <= 5
    assert number <= 6
```

## 赋值运算符（assigment）
```python
def test_assignment_operator():
    """Assignment operator """

    # Assignment: =
    number = 5
    assert number == 5

    # Multiple assignment.
    # The variables first_variable and second_variable simultaneously get the new values 0 and 1.
    first_variable, second_variable = 0, 1
    assert first_variable == 0
    assert second_variable == 1

    # You may even switch variable values using multiple assignment.
    first_variable, second_variable = second_variable, first_variable
    assert first_variable == 1
    assert second_variable == 0


def test_augmented_assignment_operators():
    """Assignment operator combined with arithmetic and bitwise operators"""

    # Assignment: +=
    number = 5
    number += 3
    assert number == 8

    # Assignment: -=
    number = 5
    number -= 3
    assert number == 2

    # Assignment: *=
    number = 5
    number *= 3
    assert number == 15

    # Assignment: /=
    number = 8
    number /= 4
    assert number == 2

    # Assignment: %=
    number = 8
    number %= 3
    assert number == 2

    # Assignment: %=
    number = 5
    number %= 3
    assert number == 2

    # Assignment: //=
    number = 5
    number //= 3
    assert number == 1

    # Assignment: **=
    number = 5
    number **= 3
    assert number == 125

    # Assignment: &=
    number = 5  # 0b0101
    number &= 3  # 0b0011
    assert number == 1  # 0b0001

    # Assignment: |=
    number = 5  # 0b0101
    number |= 3  # 0b0011
    assert number == 7  # 0b0111

    # Assignment: ^=
    number = 5  # 0b0101
    number ^= 3  # 0b0011
    assert number == 6  # 0b0110

    # Assignment: >>=
    number = 5
    number >>= 3
    assert number == 0  # (((5 // 2) // 2) // 2)

    # Assignment: <<=
    number = 5
    number <<= 3
    assert number == 40  # 5 * 2 * 2 * 2
```
## 位运算符号（bitwise)
```python
def test_bitwise_operators():
    """Bitwise operators"""

    # AND
    # Sets each bit to 1 if both bits are 1.
    #
    # Example:
    # 5 = 0b0101
    # 3 = 0b0011
    assert 5 & 3 == 1  # 0b0001

    # OR
    # Sets each bit to 1 if one of two bits is 1.
    #
    # Example:
    # 5 = 0b0101
    # 3 = 0b0011
    assert 5 | 3 == 7  # 0b0111

    # NOT
    # Inverts all the bits.
    assert ~5 == -6

    # XOR
    # Sets each bit to 1 if only one of two bits is 1.
    #
    # Example:
    # 5 = 0b0101
    # 3 = 0b0011
    number = 5  # 0b0101
    number ^= 3  # 0b0011
    assert 5 ^ 3 == 6  # 0b0110

    # Signed right shift
    # Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost
    # bits fall off.
    #
    # Example:
    # 5 = 0b0101
    assert 5 >> 1 == 2  # 0b0010
    assert 5 >> 2 == 1  # 0b0001

    # Zero fill left shift
    # Shift left by pushing zeros in from the right and let the leftmost bits fall off.
    #
    # Example:
    # 5 = 0b0101
    assert 5 << 1 == 10  # 0b1010
    assert 5 << 2 == 20  # 0b10100
```
## 逻辑运算符(logical)
```python
def test_logical_operators():
    """Logical operators"""

    # Let's work with these number to illustrate logic operators.
    first_number = 5
    second_number = 10

    # and
    # Returns True if both statements are true.
    assert first_number > 0 and second_number < 20

    # or
    # Returns True if one of the statements is true
    assert first_number > 5 or second_number < 20

    # not
    # Reverse the result, returns False if the result is true.
    # pylint: disable=unneeded-not
    assert not first_number == second_number
    assert first_number != second_number
```
## 身份运算符(identity)
```python
def test_identity_operators():
    """Identity operators"""

    # Let's illustrate identity operators based on the following lists.
    first_fruits_list = ["apple", "banana"]
    second_fruits_list = ["apple", "banana"]
    third_fruits_list = first_fruits_list

    # is
    # Returns true if both variables are the same object.

    # Example:
    # first_fruits_list and third_fruits_list are the same objects.
    assert first_fruits_list is third_fruits_list

    # is not
    # Returns true if both variables are not the same object.

    # Example:
    # first_fruits_list and second_fruits_list are not the same objects, even if they have
    # the same content
    assert first_fruits_list is not second_fruits_list

    # To demonstrate the difference between "is" and "==": this comparison returns True because
    # first_fruits_list is equal to second_fruits_list.
    assert first_fruits_list == second_fruits_list
```

## 成员运算符（membership)
```python
def test_membership_operators():
    """Membership operators"""

    # Let's use the following fruit list to illustrate membership concept.
    fruit_list = ["apple", "banana"]

    # in
    # Returns True if a sequence with the specified value is present in the object.

    # Returns True because a sequence with the value "banana" is in the list
    assert "banana" in fruit_list

    # not in
    # Returns True if a sequence with the specified value is not present in the object

    # Returns True because a sequence with the value "pineapple" is not in the list.
    assert "pineapple" not in fruit_list
```

# 数据类型(data types)
## 数字(numbers)
```python
"""
There are three numeric types in Python:
- int (e.g. 2, 4, 20)
    - bool (e.g. False and True, acting like 0 and 1)
- float (e.g. 5.0, 1.6)
- complex (e.g. 5+6j, 4-3j)
"""


def test_integer_numbers():
    """Integer type
    Int, or integer, is a whole number, positive or negative,
    without decimals, of unlimited length.
    """

    positive_integer = 1
    negative_integer = -3255522
    big_integer = 35656222554887711

    assert isinstance(positive_integer, int)
    assert isinstance(negative_integer, int)
    assert isinstance(big_integer, int)


def test_booleans():
    """Boolean
    Booleans represent the truth values False and True. The two objects representing the values
    False and True are the only Boolean objects. The Boolean type is a subtype of the integer type,
    and Boolean values behave like the values 0 and 1, respectively, in almost all contexts, the
    exception being that when converted to a string, the strings "False" or "True" are returned,
    respectively.
    """

    true_boolean = True
    false_boolean = False

    assert true_boolean
    assert not false_boolean

    assert isinstance(true_boolean, bool)
    assert isinstance(false_boolean, bool)

    # Let's try to cast boolean to string.
    assert str(true_boolean) == "True"
    assert str(false_boolean) == "False"


def test_float_numbers():
    """Float type
    Float, or "floating point number" is a number, positive or negative,
    containing one or more decimals.
    """

    float_number = 7.0
    # Another way of declaring float is using float() function.
    float_number_via_function = float(7)
    float_negative = -35.59

    assert float_number == float_number_via_function
    assert isinstance(float_number, float)
    assert isinstance(float_number_via_function, float)
    assert isinstance(float_negative, float)

    # Float can also be scientific numbers with an "e" to indicate
    # the power of 10.
    float_with_small_e = 35e3
    float_with_big_e = 12E4

    assert float_with_small_e == 35000
    assert float_with_big_e == 120000
    assert isinstance(12E4, float)
    assert isinstance(-87.7e100, float)


def test_complex_numbers():
    """Complex Type"""

    complex_number_1 = 5 + 6j
    complex_number_2 = 3 - 2j

    assert isinstance(complex_number_1, complex)
    assert isinstance(complex_number_2, complex)
    assert complex_number_1 * complex_number_2 == 27 + 8j


def test_number_operators():
    """Basic operations"""

    # Addition.
    assert 2 + 4 == 6

    # Multiplication.
    assert 2 * 4 == 8

    # Division always returns a floating point number.
    assert 12 / 3 == 4.0
    assert 12 / 5 == 2.4
    assert 17 / 3 == 5.666666666666667

    # Modulo operator returns the remainder of the division.
    assert 12 % 3 == 0
    assert 13 % 3 == 1

    # Floor division discards the fractional part.
    assert 17 // 3 == 5

    # Raising the number to specific power.
    assert 5 ** 2 == 25  # 5 squared
    assert 2 ** 7 == 128  # 2 to the power of 7

    # There is full support for floating point; operators with
    # mixed type operands convert the integer operand to floating point.
    assert 4 * 3.75 - 1 == 14.0

```
## 字符串(strings)
```python

"""Strings.
@see: https://docs.python.org/3/tutorial/introduction.html
@see: https://www.w3schools.com/python/python_strings.asp
@see: https://www.w3schools.com/python/python_ref_string.asp
Besides numbers, Python can also manipulate strings, which can be
expressed in several ways. They can be enclosed in single quotes ('...')
or double quotes ("...") with the same result.
"""

import pytest


def test_string_type():
    """String type"""

    # String with double quotes.
    name_1 = "John"
    # String with single quotes.
    name_2 = 'John'
    # Strings created with different kind of quotes are treated the same.
    assert name_1 == name_2
    assert isinstance(name_1, str)
    assert isinstance(name_2, str)

    # \ can be used to escape quotes.
    # use \' to escape the single quote or use double quotes instead.
    single_quote_string = 'doesn\'t'
    double_quote_string = "doesn't"

    assert single_quote_string == double_quote_string

    # \n means newline.
    multiline_string = 'First line.\nSecond line.'
    # Without print(), \n is included in the output.
    # But with print(), \n produces a new line.
    assert multiline_string == 'First line.\nSecond line.'

    # Strings can be indexed, with the first character having index 0.
    # There is no separate character type; a character is simply a string
    # of size one. Note that since -0 is the same as 0, negative indices
    # start from -1.
    word = 'Python'
    assert word[0] == 'P'  # First character.
    assert word[5] == 'n'  # Fifth character.
    assert word[-1] == 'n'  # Last character.
    assert word[-2] == 'o'  # Second-last character.
    assert word[-6] == 'P'  # Sixth from the end or zeroth from the beginning.

    assert isinstance(word[0], str)

    # In addition to indexing, slicing is also supported. While indexing is
    # used to obtain individual characters, slicing allows you to obtain
    # substring:
    assert word[0:2] == 'Py'  # Characters from position 0 (included) to 2 (excluded).
    assert word[2:5] == 'tho'  # Characters from position 2 (included) to 5 (excluded).

    # Note how the start is always included, and the end always excluded.
    # This makes sure that s[:i] + s[i:] is always equal to s:
    assert word[:2] + word[2:] == 'Python'
    assert word[:4] + word[4:] == 'Python'

    # Slice indices have useful defaults; an omitted first index defaults to
    # zero, an omitted second index defaults to the size of the string being
    # sliced.
    assert word[:2] == 'Py'  # Character from the beginning to position 2 (excluded).
    assert word[4:] == 'on'  # Characters from position 4 (included) to the end.
    assert word[-2:] == 'on'  # Characters from the second-last (included) to the end.

    # One way to remember how slices work is to think of the indices as
    # pointing between characters, with the left edge of the first character
    # numbered 0. Then the right edge of the last character of a string of n
    # characters has index n, for example:
    #
    # +---+---+---+---+---+---+
    #  | P | y | t | h | o | n |
    #  +---+---+---+---+---+---+
    #  0   1   2   3   4   5   6
    # -6  -5  -4  -3  -2  -1

    # Attempting to use an index that is too large will result in an error.
    with pytest.raises(Exception):
        not_existing_character = word[42]
        assert not not_existing_character

    # However, out of range slice indexes are handled gracefully when used
    # for slicing:
    assert word[4:42] == 'on'
    assert word[42:] == ''

    # Python strings cannot be changed — they are immutable. Therefore,
    # assigning to an indexed position in the string
    # results in an error:
    with pytest.raises(Exception):
        # pylint: disable=unsupported-assignment-operation
        word[0] = 'J'

    # If you need a different string, you should create a new one:
    assert 'J' + word[1:] == 'Jython'
    assert word[:2] + 'py' == 'Pypy'

    # The built-in function len() returns the length of a string:
    characters = 'supercalifragilisticexpialidocious'
    assert len(characters) == 34

    # String literals can span multiple lines. One way is using triple-quotes: """..."""
    # or '''...'''. End of lines are automatically included in the string, but it’s possible
    # to prevent this by adding a \ at the end of the line. The following example:
    multi_line_string = '''\
        First line
        Second line
    '''

    assert multi_line_string == '''\
        First line
        Second line
    '''


def test_string_operators():
    """Basic operations
    Strings can be concatenated (glued together) with the + operator,
    and repeated with *: 3 times 'un', followed by 'ium'
    """

    assert 3 * 'un' + 'ium' == 'unununium'

    # 'Py' 'thon'
    python = 'Py' 'thon'
    assert python == 'Python'

    # This feature is particularly useful when you want to break long strings:
    text = (
        'Put several strings within parentheses '
        'to have them joined together.'
    )
    assert text == 'Put several strings within parentheses to have them joined together.'

    # If you want to concatenate variables or a variable and a literal, use +:
    prefix = 'Py'
    assert prefix + 'thon' == 'Python'


def test_string_methods():
    """String methods"""

    hello_world_string = "Hello, World!"

    # The strip() method removes any whitespace from the beginning or the end.
    string_with_whitespaces = " Hello, World! "
    assert string_with_whitespaces.strip() == "Hello, World!"

    # The len() method returns the length of a string.
    assert len(hello_world_string) == 13

    # The lower() method returns the string in lower case.
    assert hello_world_string.lower() == 'hello, world!'

    # The upper() method returns the string in upper case.
    assert hello_world_string.upper() == 'HELLO, WORLD!'

    # The replace() method replaces a string with another string.
    assert hello_world_string.replace('H', 'J') == 'Jello, World!'

    # The split() method splits the string into substrings if it finds instances of the separator.
    assert hello_world_string.split(',') == ['Hello', ' World!']

    # Converts the first character to upper case
    assert 'low letter at the beginning'.capitalize() == 'Low letter at the beginning'

    # Returns the number of times a specified value occurs in a string.
    assert 'low letter at the beginning'.count('t') == 4

    # Searches the string for a specified value and returns the position of where it was found.
    assert 'Hello, welcome to my world'.find('welcome') == 7

    # Converts the first character of each word to upper case
    assert 'Welcome to my world'.title() == 'Welcome To My World'

    # Returns a string where a specified value is replaced with a specified value.
    assert 'I like bananas'.replace('bananas', 'apples') == 'I like apples'

    # Joins the elements of an iterable to the end of the string.
    my_tuple = ('John', 'Peter', 'Vicky')
    assert ', '.join(my_tuple) == 'John, Peter, Vicky'

    # Returns True if all characters in the string are upper case.
    assert 'ABC'.isupper()
    assert not 'AbC'.isupper()

    # Check if all the characters in the text are letters.
    assert 'CompanyX'.isalpha()
    assert not 'Company 23'.isalpha()

    # Returns True if all characters in the string are decimals.
    assert '1234'.isdecimal()
    assert not 'a21453'.isdecimal()


def test_string_formatting():
    """String formatting.
    Often you’ll want more control over the formatting of your output than simply printing
    space-separated values. There are several ways to format output
    """

    # To use formatted string literals, begin a string with f or F before the opening quotation
    # mark or triple quotation mark. Inside this string, you can write a Python expression
    # between { and } characters that can refer to variables or literal values.
    year = 2018
    event = 'conference'

    assert f'Results of the {year} {event}' == 'Results of the 2018 conference'

    # The str.format() method of strings requires more manual effort. You’ll still use { and } to
    # mark where a variable will be substituted and can provide detailed formatting directives,
    # but you’ll also need to provide the information to be formatted.
    yes_votes = 42_572_654  # equivalent of 42572654
    no_votes = 43_132_495   # equivalent of 43132495
    percentage = yes_votes / (yes_votes + no_votes)

    assert '{:-9} YES votes  {:2.2%}'.format(yes_votes, percentage) == ' 42572654 YES votes  49.67%'

    # When you don’t need fancy output but just want a quick display of some variables for debugging
    # purposes, you can convert any value to a string with the repr() or str() functions. The str()
    # function is meant to return representations of values which are fairly human-readable, while
    # repr() is meant to generate representations which can be read by the interpreter (or will
    # force a SyntaxError if there is no equivalent syntax). For objects which don’t have a
    # particular representation for human consumption, str() will return the same value as repr().
    # Many values, such as numbers or structures like lists and dictionaries, have the same
    # representation using either function. Strings, in particular, have two distinct
    # representations.

    greeting = 'Hello, world.'
    first_num = 10 * 3.25
    second_num = 200 * 200

    assert str(greeting) == 'Hello, world.'
    assert repr(greeting) == "'Hello, world.'"
    assert str(1/7) == '0.14285714285714285'

    # The argument to repr() may be any Python object:
    assert repr((first_num, second_num, ('spam', 'eggs'))) == "(32.5, 40000, ('spam', 'eggs'))"

    # Formatted String Literals

    # Formatted string literals (also called f-strings for short) let you include the value of
    # Python expressions inside a string by prefixing the string with f or F and writing
    # expressions as {expression}.

    # An optional format specifier can follow the expression. This allows greater control over how
    # the value is formatted. The following example rounds pi to three places after the decimal.
    pi_value = 3.14159
    assert f'The value of pi is {pi_value:.3f}.' == 'The value of pi is 3.142.'

    # Passing an integer after the ':' will cause that field to be a minimum number of characters
    # wide. This is useful for making columns line up:
    table_data = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
    table_string = ''
    for name, phone in table_data.items():
        table_string += f'{name:7}==>{phone:7d}'

    assert table_string == ('Sjoerd ==>   4127'
                            'Jack   ==>   4098'
                            'Dcab   ==>   7678')

    # The String format() Method

    # Basic usage of the str.format() method looks like this:
    assert 'We are {} who say "{}!"'.format('knights', 'Ni') == 'We are knights who say "Ni!"'

    # The brackets and characters within them (called format fields) are replaced with the objects
    # passed into the str.format() method. A number in the brackets can be used to refer to the
    # position of the object passed into the str.format() method
    assert '{0} and {1}'.format('spam', 'eggs') == 'spam and eggs'
    assert '{1} and {0}'.format('spam', 'eggs') == 'eggs and spam'

    # If keyword arguments are used in the str.format() method, their values are referred to by
    # using the name of the argument.
    formatted_string = 'This {food} is {adjective}.'.format(
        food='spam',
        adjective='absolutely horrible'
    )

    assert formatted_string == 'This spam is absolutely horrible.'

    # Positional and keyword arguments can be arbitrarily combined
    formatted_string = 'The story of {0}, {1}, and {other}.'.format(
        'Bill',
        'Manfred',
        other='Georg'
    )

    assert formatted_string == 'The story of Bill, Manfred, and Georg.'

    # If you have a really long format string that you don’t want to split up, it would be nice if
    # you could reference the variables to be formatted by name instead of by position. This can be
    # done by simply passing the dict and using square brackets '[]' to access the keys

    table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}
    formatted_string = 'Jack: {0[Jack]:d}; Sjoerd: {0[Sjoerd]:d}; Dcab: {0[Dcab]:d}'.format(table)

    assert formatted_string == 'Jack: 4098; Sjoerd: 4127; Dcab: 8637678'

    # This could also be done by passing the table as keyword arguments with the ‘**’ notation.
    formatted_string = 'Jack: {Jack:d}; Sjoerd: {Sjoerd:d}; Dcab: {Dcab:d}'.format(**table)

    assert formatted_string == 'Jack: 4098; Sjoerd: 4127; Dcab: 8637678'
```
## 列表(lists)
```python
import pytest


def test_list_type():
    """List type."""

    # Lists are very similar to arrays. They can contain any type of variable, and they can contain
    # as many variables as you wish. Lists can also be iterated over in a very simple manner.
    # Here is an example of how to build a list.
    squares = [1, 4, 9, 16, 25]

    assert isinstance(squares, list)

    # Like strings (and all other built-in sequence type), lists can be
    # indexed and sliced:
    assert squares[0] == 1  # indexing returns the item
    assert squares[-1] == 25
    assert squares[-3:] == [9, 16, 25]  # slicing returns a new list

    # All slice operations return a new list containing the requested elements.
    # This means that the following slice returns a new (shallow) copy of
    # the list:
    assert squares[:] == [1, 4, 9, 16, 25]

    # Lists also support operations like concatenation:
    assert squares + [36, 49, 64, 81, 100] == [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

    # Unlike strings, which are immutable, lists are a mutable type, i.e. it
    # is possible to change their content:
    cubes = [1, 8, 27, 65, 125]  # something's wrong here, the cube of 4 is 64!
    cubes[3] = 64  # replace the wrong value
    assert cubes == [1, 8, 27, 64, 125]

    # You can also add new items at the end of the list, by using
    # the append() method
    cubes.append(216)  # add the cube of 6
    cubes.append(7 ** 3)  # and the cube of 7
    assert cubes == [1, 8, 27, 64, 125, 216, 343]

    # Assignment to slices is also possible, and this can even change the size
    # of the list or clear it entirely:
    letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    letters[2:5] = ['C', 'D', 'E']  # replace some values
    assert letters == ['a', 'b', 'C', 'D', 'E', 'f', 'g']
    letters[2:5] = []  # now remove them
    assert letters == ['a', 'b', 'f', 'g']
    # clear the list by replacing all the elements with an empty list
    letters[:] = []
    assert letters == []

    # The built-in function len() also applies to lists
    letters = ['a', 'b', 'c', 'd']
    assert len(letters) == 4

    # It is possible to nest lists (create lists containing other lists),
    # for example:
    list_of_chars = ['a', 'b', 'c']
    list_of_numbers = [1, 2, 3]
    mixed_list = [list_of_chars, list_of_numbers]
    assert mixed_list == [['a', 'b', 'c'], [1, 2, 3]]
    assert mixed_list[0] == ['a', 'b', 'c']
    assert mixed_list[0][1] == 'b'


def test_list_methods():
    """Test list methods."""

    fruits = ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

    # list.append(x)
    # Add an item to the end of the list.
    # Equivalent to a[len(a):] = [x].
    fruits.append('grape')
    assert fruits == ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana', 'grape']

    # list.remove(x)
    # Remove the first item from the list whose value is equal to x.
    # It raises a ValueError if there is no such item.
    fruits.remove('grape')
    assert fruits == ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

    with pytest.raises(Exception):
        fruits.remove('not existing element')

    # list.insert(i, x)
    # Insert an item at a given position. The first argument is the index of the element
    # before which to insert, so a.insert(0, x) inserts at the front of the list,
    # and a.insert(len(a), x) is equivalent to a.append(x).
    fruits.insert(0, 'grape')
    assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

    # list.index(x[, start[, end]])
    # Return zero-based index in the list of the first item whose value is equal to x.
    # Raises a ValueError if there is no such item.
    # The optional arguments start and end are interpreted as in the slice notation and are used
    # to limit the search to a particular subsequence of the list. The returned index is computed
    # relative to the beginning of the full sequence rather than the start argument.
    assert fruits.index('grape') == 0
    assert fruits.index('orange') == 1
    assert fruits.index('banana') == 4
    assert fruits.index('banana', 5) == 7  # Find next banana starting a position 5

    with pytest.raises(Exception):
        fruits.index('not existing element')

    # list.count(x)
    # Return the number of times x appears in the list.
    assert fruits.count('tangerine') == 0
    assert fruits.count('banana') == 2

    # list.copy()
    # Return a shallow copy of the list. Equivalent to a[:].
    fruits_copy = fruits.copy()
    assert fruits_copy == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

    # list.reverse()
    # Reverse the elements of the list in place.
    fruits_copy.reverse()
    assert fruits_copy == [
        'banana',
        'apple',
        'kiwi',
        'banana',
        'pear',
        'apple',
        'orange',
        'grape',
    ]

    # list.sort(key=None, reverse=False)
    # Sort the items of the list in place (the arguments can be used for sort customization,
    # see sorted() for their explanation).
    fruits_copy.sort()
    assert fruits_copy == [
        'apple',
        'apple',
        'banana',
        'banana',
        'grape',
        'kiwi',
        'orange',
        'pear',
    ]

    # list.pop([i])
    # Remove the item at the given position in the list, and return it. If no index is specified,
    # a.pop() removes and returns the last item in the list. (The square brackets around the i in
    # the method signature denote that the parameter is optional, not that you should type square
    # brackets at that position.)
    assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']
    assert fruits.pop() == 'banana'
    assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple']

    # list.clear()
    # Remove all items from the list. Equivalent to del a[:].
    fruits.clear()
    assert fruits == []


def test_del_statement():
    """The del statement
    There is a way to remove an item from a list given its index instead of its value: the del
    statement. This differs from the pop() method which returns a value. The del statement can also
    be used to remove slices from a list or clear the entire list (which we did earlier by
    assignment of an empty list to the slice).
    """

    numbers = [-1, 1, 66.25, 333, 333, 1234.5]

    del numbers[0]
    assert numbers == [1, 66.25, 333, 333, 1234.5]

    del numbers[2:4]
    assert numbers == [1, 66.25, 1234.5]

    del numbers[:]
    assert numbers == []

    # del can also be used to delete entire variables:
    del numbers
    with pytest.raises(Exception):
        # Referencing the name a hereafter is an error (at least until another
        # value is assigned to it).
        assert numbers == []  # noqa: F821


def test_list_comprehensions():
    """List Comprehensions.
    List comprehensions provide a concise way to create lists. Common applications are to make new
    lists where each element is the result of some operations applied to each member of another
    sequence or iterable, or to create a subsequence of those elements that satisfy a certain
    condition.
    A list comprehension consists of brackets containing an expression followed by a for clause,
    then zero or more for or if clauses. The result will be a new list resulting from evaluating
    the expression in the context of the for and if clauses which follow it.
    """

    # For example, assume we want to create a list of squares, like:
    squares = []
    for number in range(10):
        squares.append(number ** 2)

    assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

    # Note that this creates (or overwrites) a variable named "number" that still exists after
    # the loop completes. We can calculate the list of squares without any side effects using:
    squares = list(map(lambda x: x ** 2, range(10)))
    assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

    # or, equivalently (which is more concise and readable):
    squares = [x ** 2 for x in range(10)]
    assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

    # For example, this listcomp combines the elements of two lists if they are not equal.
    combinations = [(x, y) for x in [1, 2, 3] for y in [3, 1, 4] if x != y]
    assert combinations == [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]

    # and it’s equivalent to:
    combinations = []
    for first_number in [1, 2, 3]:
        for second_number in [3, 1, 4]:
            if first_number != second_number:
                combinations.append((first_number, second_number))

    assert combinations == [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]

    # Note how the order of the for and if statements is the same in both these snippets.

    # If the expression is a tuple (e.g. the (x, y) in the previous example),
    # it must be parenthesized.

    # Let's see some more examples:

    vector = [-4, -2, 0, 2, 4]

    # Create a new list with the values doubled.
    doubled_vector = [x * 2 for x in vector]
    assert doubled_vector == [-8, -4, 0, 4, 8]

    # Filter the list to exclude negative numbers.
    positive_vector = [x for x in vector if x >= 0]
    assert positive_vector == [0, 2, 4]

    # Apply a function to all the elements.
    abs_vector = [abs(x) for x in vector]
    assert abs_vector == [4, 2, 0, 2, 4]

    # Call a method on each element.
    fresh_fruit = ['  banana', '  loganberry ', 'passion fruit  ']
    clean_fresh_fruit = [weapon.strip() for weapon in fresh_fruit]
    assert clean_fresh_fruit == ['banana', 'loganberry', 'passion fruit']

    # Create a list of 2-tuples like (number, square).
    square_tuples = [(x, x ** 2) for x in range(6)]
    assert square_tuples == [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]

    # Flatten a list using a listcomp with two 'for'.
    vector = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
    flatten_vector = [num for elem in vector for num in elem]
    assert flatten_vector == [1, 2, 3, 4, 5, 6, 7, 8, 9]


def test_nested_list_comprehensions():
    """Nested List Comprehensions
    The initial expression in a list comprehension can be any arbitrary expression, including
    another list comprehension.
    """

    # Consider the following example of a 3x4 matrix implemented as a list of 3 lists of length 4:
    matrix = [
        [1, 2, 3, 4],
        [5, 6, 7, 8],
        [9, 10, 11, 12],
    ]

    # The following list comprehension will transpose rows and columns:
    transposed_matrix = [[row[i] for row in matrix] for i in range(4)]
    assert transposed_matrix == [
        [1, 5, 9],
        [2, 6, 10],
        [3, 7, 11],
        [4, 8, 12],
    ]

    # As we saw in the previous section, the nested listcomp is evaluated in the context of the
    # for that follows it, so this example is equivalent to:
    transposed = []
    for i in range(4):
        transposed.append([row[i] for row in matrix])

    assert transposed == [
        [1, 5, 9],
        [2, 6, 10],
        [3, 7, 11],
        [4, 8, 12],
    ]

    # which, in turn, is the same as:
    transposed = []
    for i in range(4):
        # the following 3 lines implement the nested listcomp
        transposed_row = []
        for row in matrix:
            transposed_row.append(row[i])
        transposed.append(transposed_row)

    assert transposed == [
        [1, 5, 9],
        [2, 6, 10],
        [3, 7, 11],
        [4, 8, 12],
    ]

    # In the real world, you should prefer built-in functions to complex flow statements.
    # The zip() function would do a great job for this use case:
    assert list(zip(*matrix)) == [
        (1, 5, 9),
        (2, 6, 10),
        (3, 7, 11),
        (4, 8, 12),
    ]
```
## 元祖(tuples)
```python
"""
A tuple is a collection which is ordered and unchangeable. In Python tuples are written with
round brackets.
The Tuples have following properties:
- You cannot change values in a tuple.
- You cannot remove items in a tuple.
"""

import pytest


def test_tuples():
    """Tuples"""
    fruits_tuple = ("apple", "banana", "cherry")

    assert isinstance(fruits_tuple, tuple)
    assert fruits_tuple[0] == "apple"
    assert fruits_tuple[1] == "banana"
    assert fruits_tuple[2] == "cherry"

    # You cannot change values in a tuple.
    with pytest.raises(Exception):
        # pylint: disable=unsupported-assignment-operation
        fruits_tuple[0] = "pineapple"

    # It is also possible to use the tuple() constructor to make a tuple (note the double
    # round-brackets).
    # The len() function returns the length of the tuple.
    fruits_tuple_via_constructor = tuple(("apple", "banana", "cherry"))

    assert isinstance(fruits_tuple_via_constructor, tuple)
    assert len(fruits_tuple_via_constructor) == 3

    # It is also possible to omit brackets when initializing tuples.
    another_tuple = 12345, 54321, 'hello!'
    assert another_tuple == (12345, 54321, 'hello!')

    # Tuples may be nested:
    nested_tuple = another_tuple, (1, 2, 3, 4, 5)
    assert nested_tuple == ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))

    # As you see, on output tuples are always enclosed in parentheses, so that nested tuples are
    # interpreted correctly; they may be input with or without surrounding parentheses, although
    # often parentheses are necessary anyway (if the tuple is part of a larger expression). It is
    # not possible to assign to the individual items of a tuple, however it is possible to create
    # tuples which contain mutable objects, such as lists.

    # A special problem is the construction of tuples containing 0 or 1 items: the syntax has some
    # extra quirks to accommodate these. Empty tuples are constructed by an empty pair of
    # parentheses; a tuple with one item is constructed by following a value with a comma (it is
    # not sufficient to enclose a single value in parentheses). Ugly, but effective. For example:
    empty_tuple = ()
    # pylint: disable=len-as-condition
    assert len(empty_tuple) == 0

    # pylint: disable=trailing-comma-tuple
    singleton_tuple = 'hello',  # <-- note trailing comma
    assert len(singleton_tuple) == 1
    assert singleton_tuple == ('hello',)

    # The following example is called tuple packing:
    packed_tuple = 12345, 54321, 'hello!'

    # The reverse operation is also possible.
    first_tuple_number, second_tuple_number, third_tuple_string = packed_tuple
    assert first_tuple_number == 12345
    assert second_tuple_number == 54321
    assert third_tuple_string == 'hello!'

    # This is called, appropriately enough, sequence unpacking and works for any sequence on the
    # right-hand side. Sequence unpacking requires that there are as many variables on the left
    # side of the equals sign as there are elements in the sequence. Note that multiple assignment
    # is really just a combination of tuple packing and sequence unpacking.

    # Swapping using tuples.
    # Data can be swapped from one variable to another in python using
    # tuples. This eliminates the need to use a 'temp' variable.
    first_number = 123
    second_number = 456
    first_number, second_number = second_number, first_number

    assert first_number == 456
    assert second_number == 123
```
## 集合(sets)
```python
"""Sets.
@see: https://www.w3schools.com/python/python_sets.asp
@see: https://docs.python.org/3.7/tutorial/datastructures.html#sets
A set is a collection which is unordered and unindexed.
In Python sets are written with curly brackets.
Set objects also support mathematical operations like union, intersection, difference, and
symmetric difference.
"""


def test_sets():
    """Sets"""
    fruits_set = {"apple", "banana", "cherry"}

    assert isinstance(fruits_set, set)

    # It is also possible to use the set() constructor to make a set.
    # Note the double round-brackets
    fruits_set_via_constructor = set(("apple", "banana", "cherry"))

    assert isinstance(fruits_set_via_constructor, set)


def test_set_methods():
    """Set methods"""

    fruits_set = {"apple", "banana", "cherry"}

    # You may check if the item is in set by using "in" statement
    assert "apple" in fruits_set
    assert "pineapple" not in fruits_set

    # Use the len() method to return the number of items.
    assert len(fruits_set) == 3

    # You can use the add() object method to add an item.
    fruits_set.add("pineapple")
    assert "pineapple" in fruits_set
    assert len(fruits_set) == 4

    # Use remove() method to remove an item.
    fruits_set.remove("pineapple")
    assert "pineapple" not in fruits_set
    assert len(fruits_set) == 3

    # Demonstrate set operations on unique letters from two word:
    first_char_set = set('abracadabra')
    second_char_set = set('alacazam')

    assert first_char_set == {'a', 'r', 'b', 'c', 'd'}  # unique letters in first word
    assert second_char_set == {'a', 'l', 'c', 'z', 'm'}  # unique letters in second word

    # Letters in first word but not in second.
    assert first_char_set - second_char_set == {'r', 'b', 'd'}

    # Letters in first word or second word or both.
    assert first_char_set | second_char_set == {'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}

    # Common letters in both words.
    assert first_char_set & second_char_set == {'a', 'c'}

    # Letters in first or second word but not both.
    assert first_char_set ^ second_char_set == {'r', 'd', 'b', 'm', 'z', 'l'}

    # Similarly to list comprehensions, set comprehensions are also supported:
    word = {char for char in 'abracadabra' if char not in 'abc'}
    assert word == {'r', 'd'}
```
## 字典(dictionaries)
```python
"""
Dictionaries.
@see: https://docs.python.org/3/tutorial/datastructures.html#dictionaries
@see: https://www.w3schools.com/python/python_dictionaries.asp
A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are
written with curly brackets, and they have keys and values.
Dictionaries are sometimes found in other languages as “associative memories” or “associative
arrays”. Unlike sequences, which are indexed by a range of numbers, dictionaries are indexed by
keys, which can be any immutable type; strings and numbers can always be keys. Tuples can be used
as keys if they contain only strings, numbers, or tuples; if a tuple contains any mutable object
either directly or indirectly, it cannot be used as a key. You can’t use lists as keys, since
lists can be modified in place using index assignments, slice assignments, or methods like append()
and extend().
It is best to think of a dictionary as a set of key: value pairs, with the requirement that the
keys are unique (within one dictionary). A pair of braces creates an empty dictionary: {}.
Placing a comma-separated list of key:value pairs within the braces adds initial key:value pairs
to the dictionary; this is also the way dictionaries are written on output.
"""


def test_dictionary():
    """Dictionary"""

    fruits_dictionary = {
        'cherry': 'red',
        'apple': 'green',
        'banana': 'yellow',
    }

    assert isinstance(fruits_dictionary, dict)

    # You may access set elements by keys.
    assert fruits_dictionary['apple'] == 'green'
    assert fruits_dictionary['banana'] == 'yellow'
    assert fruits_dictionary['cherry'] == 'red'

    # To check whether a single key is in the dictionary, use the in keyword.
    assert 'apple' in fruits_dictionary
    assert 'pineapple' not in fruits_dictionary

    # Change the apple color to "red".
    fruits_dictionary['apple'] = 'red'

    # Add new key/value pair to the dictionary
    fruits_dictionary['pineapple'] = 'yellow'
    assert fruits_dictionary['pineapple'] == 'yellow'

    # Performing list(d) on a dictionary returns a list of all the keys used in the dictionary,
    # in insertion order (if you want it sorted, just use sorted(d) instead).
    assert list(fruits_dictionary) == ['cherry', 'apple', 'banana', 'pineapple']
    assert sorted(fruits_dictionary) == ['apple', 'banana', 'cherry', 'pineapple']

    # It is also possible to delete a key:value pair with del.
    del fruits_dictionary['pineapple']
    assert list(fruits_dictionary) == ['cherry', 'apple', 'banana']

    # The dict() constructor builds dictionaries directly from sequences of key-value pairs.
    dictionary_via_constructor = dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])

    assert dictionary_via_constructor['sape'] == 4139
    assert dictionary_via_constructor['guido'] == 4127
    assert dictionary_via_constructor['jack'] == 4098

    # In addition, dict comprehensions can be used to create dictionaries from arbitrary key
    # and value expressions:
    dictionary_via_expression = {x: x**2 for x in (2, 4, 6)}
    assert dictionary_via_expression[2] == 4
    assert dictionary_via_expression[4] == 16
    assert dictionary_via_expression[6] == 36

    # When the keys are simple strings, it is sometimes easier to specify pairs using
    # keyword arguments.
    dictionary_for_string_keys = dict(sape=4139, guido=4127, jack=4098)
    assert dictionary_for_string_keys['sape'] == 4139
    assert dictionary_for_string_keys['guido'] == 4127
    assert dictionary_for_string_keys['jack'] == 4098
```
## 类型转换(type casting)
```python
"""Type casting.
@see: https://www.w3schools.com/python/python_casting.asp
There may be times when you want to specify a type on to a variable. This can be done with casting.
Python is an object-orientated language, and as such it uses classes to define data types,
including its primitive types.
Casting in python is therefore done using constructor functions:
- int() - constructs an integer number from an integer literal, a float literal (by rounding down
to the previous whole number) literal, or a string literal (providing the string represents a
whole number)
- float() - constructs a float number from an integer literal, a float literal or a string literal
(providing the string represents a float or an integer)
- str() - constructs a string from a wide variety of data types, including strings, integer
literals and float literals
"""


def test_type_casting_to_integer():
    """Type casting to integer"""

    assert int(1) == 1
    assert int(2.8) == 2
    assert int('3') == 3


def test_type_casting_to_float():
    """Type casting to float"""

    assert float(1) == 1.0
    assert float(2.8) == 2.8
    assert float("3") == 3.0
    assert float("4.2") == 4.2


def test_type_casting_to_string():
    """Type casting to string"""

    assert str("s1") == 's1'
    assert str(2) == '2'
    assert str(3.0) == '3.0'
```
# 流程控制(control flow)
## `if` statement
```python
"""IF statement
@see: https://docs.python.org/3/tutorial/controlflow.html
There can be zero or more elif parts, and the else part is optional. The keyword ‘elif’ is
short for ‘else if’, and is useful to avoid excessive indentation.
An if … elif … elif … sequence is a substitute for the switch or case statements found
in other languages.
"""


def test_if_statement():
    """IF statement"""

    number = 15
    conclusion = ''

    if number < 0:
        conclusion = 'Number is less than zero'
    elif number == 0:
        conclusion = 'Number equals to zero'
    elif number < 1:
        conclusion = 'Number is greater than zero but less than one'
    else:
        conclusion = 'Number bigger than or equal to one'

    assert conclusion == 'Number bigger than or equal to one'
```
## `for`statement
```python
"""FOR statement
@see: https://docs.python.org/3/tutorial/controlflow.html
The for statement in Python differs a bit from what you may be used to in C or Pascal.
Rather than always iterating over an arithmetic progression of numbers (like in Pascal), or
giving the user the ability to define both the iteration step and halting condition (as C),
Python’s for statement iterates over the items of any sequence (a list or a string), in the
order that they appear in the sequence. For example (no pun intended):
"""


# pylint: disable=too-many-locals
def test_for_statement():
    """FOR statement"""

    # Measure some strings:
    words = ['cat', 'window', 'defenestrate']
    words_length = 0

    for word in words:
        words_length += len(word)

    # "cat" length is 3
    # "window" length is 6
    # "defenestrate" length is 12
    assert words_length == (3 + 6 + 12)

    # If you need to modify the sequence you are iterating over while inside the loop
    # (for example to duplicate selected items), it is recommended that you first make a copy.
    # Iterating over a sequence does not implicitly make a copy. The slice notation makes this
    # especially convenient:
    for word in words[:]:  # Loop over a slice copy of the entire list.
        if len(word) > 6:
            words.insert(0, word)

    # Otherwise with for w in words:, the example would attempt to create an infinite list,
    # inserting defenestrate over and over again.

    assert words == ['defenestrate', 'cat', 'window', 'defenestrate']

    # If you do need to iterate over a sequence of numbers, the built-in function range() comes in
    # handy. It generates arithmetic progressions:
    iterated_numbers = []

    for number in range(5):
        iterated_numbers.append(number)

    assert iterated_numbers == [0, 1, 2, 3, 4]

    # To iterate over the indices of a sequence, you can combine range() and len() as follows:
    words = ['Mary', 'had', 'a', 'little', 'lamb']
    concatenated_string = ''

    # pylint: disable=consider-using-enumerate
    for word_index in range(len(words)):
        concatenated_string += words[word_index] + ' '

    assert concatenated_string == 'Mary had a little lamb '

    # Or simply use enumerate().
    concatenated_string = ''

    for word_index, word in enumerate(words):
        concatenated_string += word + ' '

    assert concatenated_string == 'Mary had a little lamb '

    # When looping through dictionaries, the key and corresponding value can be retrieved at the
    # same time using the items() method.
    knights_names = []
    knights_properties = []

    knights = {'gallahad': 'the pure', 'robin': 'the brave'}
    for key, value in knights.items():
        knights_names.append(key)
        knights_properties.append(value)

    assert knights_names == ['gallahad', 'robin']
    assert knights_properties == ['the pure', 'the brave']

    # When looping through a sequence, the position index and corresponding value can be retrieved
    # at the same time using the enumerate() function
    indices = []
    values = []
    for index, value in enumerate(['tic', 'tac', 'toe']):
        indices.append(index)
        values.append(value)

    assert indices == [0, 1, 2]
    assert values == ['tic', 'tac', 'toe']

    # To loop over two or more sequences at the same time, the entries can be paired with
    # the zip() function.
    questions = ['name', 'quest', 'favorite color']
    answers = ['lancelot', 'the holy grail', 'blue']
    combinations = []

    for question, answer in zip(questions, answers):
        combinations.append('What is your {0}?  It is {1}.'.format(question, answer))

    assert combinations == [
        'What is your name?  It is lancelot.',
        'What is your quest?  It is the holy grail.',
        'What is your favorite color?  It is blue.',
    ]


def test_range_function():
    """Range function
    If you do need to iterate over a sequence of numbers, the built-in function range() comes in
    handy. It generates arithmetic progressions.
    In many ways the object returned by range() behaves as if it is a list, but in fact it isn’t.
    It is an object which returns the successive items of the desired sequence when you iterate
    over it, but it doesn’t really make the list, thus saving space.
    We say such an object is iterable, that is, suitable as a target for functions and constructs
    that expect something from which they can obtain successive items until the supply is exhausted.
    We have seen that the for statement is such an iterator. The function list() is another; it
    creates lists from iterables:
    """

    assert list(range(5)) == [0, 1, 2, 3, 4]

    # The given end point is never part of the generated sequence; range(10) generates 10 values,
    # the legal indices for items of a sequence of length 10. It is possible to let the range start
    # at another number, or to specify a different increment (even negative; sometimes this is
    # called the ‘step’):

    assert list(range(5, 10)) == [5, 6, 7, 8, 9]
    assert list(range(0, 10, 3)) == [0, 3, 6, 9]
    assert list(range(-10, -100, -30)) == [-10, -40, -70]
```
## `while` statement
```python
"""WHILE statement
@see: https://docs.python.org/3/tutorial/controlflow.html
@see: https://docs.python.org/3/reference/compound_stmts.html#the-while-statement
The while loop executes as long as the condition remains true. In Python, like in C, any
non-zero integer value is true; zero is false. The condition may also be a string or list
value, in fact any sequence; anything with a non-zero length is true, empty sequences are
false.
The test used in the example is a simple comparison. The standard comparison operators are
written the same as in C: < (less than), > (greater than), == (equal to), <= (less than or
equal to), >= (greater than or equal to) and != (not equal to).
"""


def test_while_statement():
    """WHILE statement"""

    # Let's raise the number to certain power using while loop.
    number = 2
    power = 5

    result = 1

    while power > 0:
        result *= number
        power -= 1

    # 2^5 = 32
    assert result == 32
```
## `try` statement
```python
"""TRY statement
@see: https://www.w3schools.com/python/python_try_except.asp
"try" statement is used for exception handling.
When an error occurs, or exception as we call it, Python will normally stop and generate an error
message. These exceptions can be handled using the try statement.
The "try" block lets you test a block of code for errors.
The "except" block lets you handle the error.
The "else" block lets you execute the code if no errors were raised.
The "finally" block lets you execute code, regardless of the result of the try- and except blocks.
"""


def test_try():
    """TRY statement"""

    # The try block will generate an error, because x is not defined:
    exception_has_been_caught = False

    try:
        # pylint: disable=undefined-variable
        print(not_existing_variable)
    except NameError:
        exception_has_been_caught = True

    assert exception_has_been_caught

    # You can define as many exception blocks as you want, e.g. if you want to execute a special
    # block of code for a special kind of error:
    exception_message = ''

    try:
        # pylint: disable=undefined-variable
        print(not_existing_variable)
    except NameError:
        exception_message = 'Variable is not defined'

    assert exception_message == 'Variable is not defined'

    # You can use the else keyword to define a block of code to be executed
    # if no errors were raised.
    message = ''
    # pylint: disable=broad-except
    try:
        message += 'Success.'
    except NameError:
        message += 'Something went wrong.'
    else:
        message += 'Nothing went wrong.'

    assert message == 'Success.Nothing went wrong.'

    # The finally block, if specified, will be executed regardless if the try block raises an
    # error or not.
    message = ''
    try:
        # pylint: undefined-variable
        print(not_existing_variable)  # noqa: F821
    except NameError:
        message += 'Something went wrong.'
    finally:
        message += 'The "try except" is finished.'

    assert message == 'Something went wrong.The "try except" is finished.'
```
## `break` statement
```python
"""BREAK statement
@see: https://docs.python.org/3/tutorial/controlflow.html
The break statement, like in C, breaks out of the innermost enclosing "for" or "while" loop.
"""


def test_break_statement():
    """BREAK statement"""

    # Let's terminate the loop in case if we've found the number we need in a range from 0 to 100.
    number_to_be_found = 42
    # This variable will record how many time we've entered the "for" loop.
    number_of_iterations = 0

    for number in range(100):
        if number == number_to_be_found:
            # Break here and don't continue the loop.
            break
        else:
            number_of_iterations += 1

    # We need to make sure that break statement has terminated the loop once it found the number.
    assert number_of_iterations == 42
```
## `continue` statement
```python
"""CONTINUE statement
@see: https://docs.python.org/3/tutorial/controlflow.html
The continue statement is borrowed from C, continues with the next iteration of the loop.
"""


def test_continue_statement():
    """CONTINUE statement in FOR loop"""

    # Let's

    # This list will contain only even numbers from the range.
    even_numbers = []
    # This list will contain every other numbers (in this case - ods).
    rest_of_the_numbers = []

    for number in range(0, 10):
        # Check if remainder after division is zero (which would mean that number is even).
        if number % 2 == 0:
            even_numbers.append(number)
            # Stop current loop iteration and go to the next one immediately.
            continue

        rest_of_the_numbers.append(number)

    assert even_numbers == [0, 2, 4, 6, 8]
    assert rest_of_the_numbers == [1, 3, 5, 7, 9]
```
# 函数(functions)

## 函数定义(function_definition)
```python
"""Function Definition
@see: https://docs.python.org/3/tutorial/controlflow.html#defining-functions
@see: https://www.thecodeship.com/patterns/guide-to-python-function-decorators/
The keyword def introduces a function definition. It must be followed by the function name and the
parenthesized list of formal parameters. The statements that form the body of the function start at
the next line, and must be indented.
"""


def fibonacci_function_example(number_limit):
    """Generate a Fibonacci series up to number_limit.
    The first statement of the function body can optionally be a string literal; this string
    literal is the function’s documentation string, or docstring. There are tools which use
    docstrings to automatically produce online or printed documentation, or to let the user
    interactively browse through code; it’s good practice to include docstrings in code that you
    write, so make a habit of it.
    """

    # The execution of a function introduces a new symbol table used for the local variables of the
    # function. More precisely, all variable assignments in a function store the value in the local
    # symbol table; whereas variable references first look in the local symbol table, then in the
    # local symbol tables of enclosing functions, then in the global symbol table, and finally in
    # the table of built-in names. Thus, global variables cannot be directly assigned a value
    # within a function (unless named in a global statement), although they may be referenced.
    fibonacci_list = []
    previous_number, current_number = 0, 1
    while previous_number < number_limit:
        # The statement result.append(a) calls a method of the list object result. A method is a
        # function that ‘belongs’ to an object and is named obj.methodname, where obj is some
        # object (this may be an expression), and methodname is the name of a method that is
        # defined by the object’s type. Different types define different methods. Methods of
        # different types may have the same name without causing ambiguity. (It is possible to
        # define your own object types and methods, using classes, see Classes) The method
        # append() shown in the example is defined for list objects; it adds a new element at
        # the end of the list. In this example it is equivalent to result = result + [a], but
        # more efficient.
        fibonacci_list.append(previous_number)
        # This is multiple assignment statement. We make current number to be previous one and the
        # sum of previous and current to be a new current.
        previous_number, current_number = current_number, previous_number + current_number

    # The return statement returns with a value from a function. return without an expression
    # argument returns None. Falling off the end of a function also returns None.
    return fibonacci_list


def test_function_definition():
    """Function Definition"""

    # Now call the function we just defined.
    assert fibonacci_function_example(300) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233]

    # A function definition introduces the function name in the current symbol table. The value of
    # the function name has a type that is recognized by the interpreter as a user-defined function.
    # This value can be assigned to another name which can then also be used as a function. This
    # serves as a general renaming mechanism
    fibonacci_function_clone = fibonacci_function_example
    assert fibonacci_function_clone(300) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233]

    # In Python, functions are first class citizens, they are objects and that means we can do a
    # lot of useful stuff with them.

    # Assign functions to variables.

    def greet(name):
        return 'Hello, ' + name

    greet_someone = greet

    assert greet_someone('John') == 'Hello, John'

    # Define functions inside other functions.

    def greet_again(name):
        def get_message():
            return 'Hello, '

        result = get_message() + name
        return result

    assert greet_again('John') == 'Hello, John'

    # Functions can be passed as parameters to other functions.

    def greet_one_more(name):
        return 'Hello, ' + name

    def call_func(func):
        other_name = 'John'
        return func(other_name)

    assert call_func(greet_one_more) == 'Hello, John'

    # Functions can return other functions. In other words, functions generating other functions.

    def compose_greet_func():
        def get_message():
            return 'Hello there!'

        return get_message

    greet_function = compose_greet_func()
    assert greet_function() == 'Hello there!'

    # Inner functions have access to the enclosing scope.

    # More commonly known as a closure. A very powerful pattern that we will come across while
    # building decorators. Another thing to note, Python only allows read access to the outer
    # scope and not assignment. Notice how we modified the example above to read a "name" argument
    # from the enclosing scope of the inner function and return the new function.

    def compose_greet_func_with_closure(name):
        def get_message():
            return 'Hello there, ' + name + '!'

        return get_message

    greet_with_closure = compose_greet_func_with_closure('John')

    assert greet_with_closure() == 'Hello there, John!'
```
## 函数范围
```python
"""Scopes and Namespaces.
@see: https://docs.python.org/3/tutorial/classes.html#scopes-and-namespaces-example
A NAMESPACE is a mapping from names to objects. Most namespaces are currently implemented as Python
dictionaries, but that’s normally not noticeable in any way (except for performance), and it may
change in the future. Examples of namespaces are: the set of built-in names (containing functions
such as abs(), and built-in exception names); the global names in a module; and the local names
in a function invocation. In a sense the set of attributes of an object also form a namespace.
The important thing to know about namespaces is that there is absolutely no relation between names
in different namespaces; for instance, two different modules may both define a function maximize
without confusion — users of the modules must prefix it with the module name.
By the way, we use the word attribute for any name following a dot — for example, in the expression
z.real, real is an attribute of the object z. Strictly speaking, references to names in modules are
attribute references: in the expression modname.func_name, modname is a module object and func_name
is an attribute of it. In this case there happens to be a straightforward mapping between the
module’s attributes and the global names defined in the module: they share the same namespace!
A SCOPE is a textual region of a Python program where a namespace is directly accessible.
“Directly accessible” here means that an unqualified reference to a name attempts to find the name
in the namespace.
Although scopes are determined statically, they are used dynamically. At any time during execution,
there are at least three nested scopes whose namespaces are directly accessible:
- the innermost scope, which is searched first, contains the local names.
- the scopes of any enclosing functions, which are searched starting with the nearest enclosing
scope, contains non-local, but also non-global names.
- the next-to-last scope contains the current module’s global names.
- the outermost scope (searched last) is the namespace containing built-in names.
BE CAREFUL!!!
-------------
Changing global or nonlocal variables from within an inner function might be a BAD
practice and might lead to harder debugging and to more fragile code! Do this only if you know
what you're doing.
"""

# pylint: disable=invalid-name
test_variable = 'initial global value'


def test_function_scopes():
    """Scopes and Namespaces Example"""

    # This is an example demonstrating how to reference the different scopes and namespaces, and
    # how global and nonlocal affect variable binding:

    # pylint: disable=redefined-outer-name
    test_variable = 'initial value inside test function'

    def do_local():
        # Create variable that is only accessible inside current do_local() function.
        # pylint: disable=redefined-outer-name
        test_variable = 'local value'
        return test_variable

    def do_nonlocal():
        # Address the variable from outer scope and try to change it.
        # pylint: disable=redefined-outer-name
        nonlocal test_variable
        test_variable = 'nonlocal value'
        return test_variable

    def do_global():
        # Address the variable from very global scope and try to change it.
        # pylint: disable=redefined-outer-name,global-statement
        global test_variable
        test_variable = 'global value'
        return test_variable

    # On this level currently we have access to local for test_function_scopes() function variable.
    assert test_variable == 'initial value inside test function'

    # Do local assignment.
    # It doesn't change global variable and variable from test_function_scopes() scope.
    do_local()
    assert test_variable == 'initial value inside test function'

    # Do non local assignment.
    # It doesn't change global variable but it does change variable
    # from test_function_scopes() function scope.
    do_nonlocal()
    assert test_variable == 'nonlocal value'

    # Do global assignment.
    # This one changes global variable but doesn't change variable from
    # test_function_scopes() function scope.
    do_global()
    assert test_variable == 'nonlocal value'


def test_global_variable_access():
    """Testing global variable access from within a function"""

    # Global value of test_variable has been already changed by do_global() function in previous
    # test so let's check that.
    # pylint: disable=global-statement
    global test_variable
    assert test_variable == 'global value'

    # On this example you may see how accessing and changing global variables from within inner
    # functions might make debugging more difficult and code to be less predictable. Since you
    # might have expected that test_variable should still be equal to 'initial global value' but
    # it was changed by "someone" and you need to know about the CONTEXT of who had changed that.
    # So once again access global and non local scope only if you know what you're doing otherwise
    # it might be considered as bad practice.
```
## 函数默认参数(default_arguments)
```python
"""Default Argument Values
@see: https://docs.python.org/3/tutorial/controlflow.html#default-argument-values
The most useful form is to specify a default value for one or more arguments. This creates a
function that can be called with fewer arguments than it is defined to allow.
"""


def power_of(number, power=2):
    """ Raises number to specific power.
    You may notice that by default the function raises number to the power of two.
    """
    return number ** power


def test_default_function_arguments():
    """Test default function arguments"""

    # This function power_of can be called in several ways because it has default value for
    # the second argument. First we may call it omitting the second argument at all.
    assert power_of(3) == 9
    # We may also want to override the second argument by using the following function calls.
    assert power_of(3, 2) == 9
    assert power_of(3, 3) == 27
```
## 可变关键字参数(keyword_arguments)
```python
"""Keyword Arguments
@see: https://docs.python.org/3/tutorial/controlflow.html#keyword-arguments
Functions can be called using keyword arguments of the form kwarg=value.
"""

import pytest


def parrot(voltage, state='a stiff', action='voom', parrot_type='Norwegian Blue'):
    """Example of multi-argument function
    This function accepts one required argument (voltage) and three optional arguments
    (state, action, and type).
    """

    message = 'This parrot wouldn\'t ' + action + ' '
    message += 'if you put ' + str(voltage) + ' volts through it. '
    message += 'Lovely plumage, the ' + parrot_type + '. '
    message += 'It\'s ' + state + '!'

    return message


def test_function_keyword_arguments():
    """Test calling function with specifying keyword arguments"""

    # The parrot function accepts one required argument (voltage) and three optional arguments
    # (state, action, and type). This function can be called in any of the following ways:

    message = (
        "This parrot wouldn't voom if you put 1000 volts through it. "
        "Lovely plumage, the Norwegian Blue. "
        "It's a stiff!"
    )
    # 1 positional argument
    assert parrot(1000) == message
    # 1 keyword argument
    assert parrot(voltage=1000) == message

    message = (
        "This parrot wouldn't VOOOOOM if you put 1000000 volts through it. "
        "Lovely plumage, the Norwegian Blue. "
        "It's a stiff!"
    )
    # 2 keyword arguments
    assert parrot(voltage=1000000, action='VOOOOOM') == message
    # 2 keyword arguments
    assert parrot(action='VOOOOOM', voltage=1000000) == message

    # 3 positional arguments
    message = (
        "This parrot wouldn't jump if you put 1000000 volts through it. "
        "Lovely plumage, the Norwegian Blue. "
        "It's bereft of life!"
    )
    assert parrot(1000000, 'bereft of life', 'jump') == message

    # 1 positional, 1 keyword
    message = (
        "This parrot wouldn't voom if you put 1000 volts through it. "
        "Lovely plumage, the Norwegian Blue. "
        "It's pushing up the daisies!"
    )
    assert parrot(1000, state='pushing up the daisies') == message

    # But all the following calls would be invalid.

    with pytest.raises(Exception):
        # Required argument missing.
        # pylint: disable=no-value-for-parameter
        parrot()

    # Non-keyword argument after a keyword argument.
    # parrot(voltage=5.0, 'dead')

    with pytest.raises(Exception):
        # pylint: disable=redundant-keyword-arg
        parrot(110, voltage=220)

    with pytest.raises(Exception):
        # unknown keyword argument
        # pylint: disable=unexpected-keyword-arg,no-value-for-parameter
        parrot(actor='John Cleese')

    # In a function call, keyword arguments must follow positional arguments. All the keyword
    # arguments passed must match one of the arguments accepted by the function (e.g. actor is not
    # a valid argument for the parrot function), and their order is not important. This also
    # includes non-optional arguments (e.g. parrot(voltage=1000) is valid too). No argument may
    # receive a value more than once. Here’s an example that fails due to this restriction:
    def function_with_one_argument(number):
        return number

    with pytest.raises(Exception):
        # pylint: disable=redundant-keyword-arg
        function_with_one_argument(0, number=0)

    # When a final formal parameter of the form **name is present, it receives a dictionary
    # containing all keyword arguments except for those corresponding to a formal parameter.
    # This may be combined with a formal parameter of the form *name which receives a tuple
    # containing the positional arguments beyond the formal parameter list.
    # (*name must occur before **name.) For example, if we define a function like this:
    def test_function(first_param, *arguments, **keywords):
        """This function accepts its arguments through "arguments" tuple amd keywords dictionary."""
        assert first_param == 'first param'
        assert arguments == ('second param', 'third param')
        assert keywords == {
            'fourth_param_name': 'fourth named param',
            'fifth_param_name': 'fifth named param'
        }

    test_function(
        'first param',
        'second param',
        'third param',
        fourth_param_name='fourth named param',
        fifth_param_name='fifth named param',
    )
```
## 任意参数(arbitrary_arguments)
```python
"""Arbitrary Argument Lists
@see: https://docs.python.org/3/tutorial/controlflow.html#arbitrary-argument-lists
Function can be called with an arbitrary number of arguments. These arguments will be wrapped up in
a tuple. Before the variable number of arguments, zero or more normal arguments may occur.
"""


def test_function_arbitrary_arguments():
    """Arbitrary Argument Lists"""

    # When a final formal parameter of the form **name is present, it receives a dictionary
    # containing all keyword arguments except for those corresponding to a formal parameter.
    # This may be combined with a formal parameter of the form *name which receives a tuple
    # containing the positional arguments beyond the formal parameter list.
    # (*name must occur before **name.) For example, if we define a function like this:
    def test_function(first_param, *arguments):
        """This function accepts its arguments through "arguments" tuple amd keywords dictionary."""
        assert first_param == 'first param'
        assert arguments == ('second param', 'third param')

    test_function('first param', 'second param', 'third param')

    # Normally, these variadic arguments will be last in the list of formal parameters, because
    # they scoop up all remaining input arguments that are passed to the function. Any formal
    # parameters which occur after the *args parameter are ‘keyword-only’ arguments, meaning that
    # they can only be used as keywords rather than positional arguments.
    def concat(*args, sep='/'):
        return sep.join(args)

    assert concat('earth', 'mars', 'venus') == 'earth/mars/venus'
    assert concat('earth', 'mars', 'venus', sep='.') == 'earth.mars.venus'
```
## 解开参数包裹(unpacking_arguments)
```python
"""Unpacking Argument Lists
@see: https://docs.python.org/3/tutorial/controlflow.html#unpacking-argument-lists
Unpacking arguments may be executed via * and ** operators. See below for further details.
"""


def test_function_unpacking_arguments():
    """Unpacking Argument Lists"""

    # The situation may occur when the arguments are already in a list or tuple but need to be
    # unpacked for a function call requiring separate positional arguments. For instance, the
    # built-in range() function expects separate start and stop arguments. If they are not
    # available separately, write the function call with the *-operator to unpack the arguments out
    # of a list or tuple:

    # Normal call with separate arguments:
    assert list(range(3, 6)) == [3, 4, 5]

    # Call with arguments unpacked from a list.
    arguments_list = [3, 6]
    assert list(range(*arguments_list)) == [3, 4, 5]

    # In the same fashion, dictionaries can deliver keyword arguments with the **-operator:
    def function_that_receives_names_arguments(first_word, second_word):
        return first_word + ', ' + second_word + '!'

    arguments_dictionary = {'first_word': 'Hello', 'second_word': 'World'}
    assert function_that_receives_names_arguments(**arguments_dictionary) == 'Hello, World!'
```
## lambda表达式(lambda_expressions)
```python
"""Lambda Expressions
@see: https://docs.python.org/3/tutorial/controlflow.html#lambda-expressions
Small anonymous functions can be created with the lambda keyword. Lambda functions can be used
wherever function objects are required. They are syntactically restricted to a single expression.
Semantically, they are just syntactic sugar for a normal function definition. Like nested function
definitions, lambda functions can reference variables from the containing scope.
"""


def test_lambda_expressions():
    """Lambda Expressions"""

    # This function returns the sum of its two arguments: lambda a, b: a+b
    # Like nested function definitions, lambda functions can reference variables from the
    # containing scope.

    def make_increment_function(delta):
        """This example uses a lambda expression to return a function"""
        return lambda number: number + delta

    increment_function = make_increment_function(42)

    assert increment_function(0) == 42
    assert increment_function(1) == 43
    assert increment_function(2) == 44

    # Another use of lambda is to pass a small function as an argument.
    pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
    # Sort pairs by text key.
    pairs.sort(key=lambda pair: pair[1])

    assert pairs == [(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```
## 函数文档字符串(function_documentation_string)
```python
"""Documentation Strings.
@see: https://docs.python.org/3/tutorial/controlflow.html#documentation-strings
Here are some conventions about the content and formatting of documentation strings.
The first line should always be a short, concise summary of the object’s purpose. For brevity,
it should not explicitly state the object’s name or type, since these are available by other means
(except if the name happens to be a verb describing a function’s operation). This line should begin
with a capital letter and end with a period.
If there are more lines in the documentation string, the second line should be blank, visually
separating the summary from the rest of the description. The following lines should be one or more
paragraphs describing the object’s calling conventions, its side effects, etc.
"""


def do_nothing():
    """Do nothing, but document it.
    No, really, it doesn't do anything.
    """
    pass


def test_function_documentation_string():
    """Test documentation string."""

    # The Python parser does not strip indentation from multi-line string literals in Python, so
    # tools that process documentation have to strip indentation if desired. This is done using the
    # following convention. The first non-blank line after the first line of the string determines
    # the amount of indentation for the entire documentation string. (We can’t use the first line
    # since it is generally adjacent to the string’s opening quotes so its indentation is not
    # apparent in the string literal.) Whitespace “equivalent” to this indentation is then stripped
    # from the start of all lines of the string. Lines that are indented less should not occur, but
    # if they occur all their leading whitespace should be stripped. Equivalence of whitespace
    # should be tested after expansion of tabs (to 8 spaces, normally).

    assert do_nothing.__doc__ == """Do nothing, but document it.
    No, really, it doesn't do anything.
    """
```
## 函数注释(function_annotations)
```python
"""Function Annotations.
@see: https://docs.python.org/3/tutorial/controlflow.html#function-annotations
Function annotations are completely optional metadata information about the types used
by user-defined functions.
Annotations are stored in the __annotations__ attribute of the function as a dictionary and have no
effect on any other part of the function. Parameter annotations are defined by a colon after the
parameter name, followed by an expression evaluating to the value of the annotation. Return
annotations are defined by a literal ->, followed by an expression, between the parameter list and
the colon denoting the end of the def statement.
"""


def breakfast(ham: str, eggs: str = 'eggs') -> str:
    """Breakfast creator.
    This function has a positional argument, a keyword argument, and the return value annotated.
    """
    return ham + ' and ' + eggs


def test_function_annotations():
    """Function Annotations."""

    assert breakfast.__annotations__ == {'eggs': str, 'ham': str, 'return': str}
```
## 装饰器(function_decorators)
```python
"""Function Decorators.
@see: https://www.thecodeship.com/patterns/guide-to-python-function-decorators/
Function decorators are simply wrappers to existing functions. In the context of design patterns,
decorators dynamically alter the functionality of a function, method or class without having to
directly use subclasses. This is ideal when you need to extend the functionality of functions that
you don't want to modify. We can implement the decorator pattern anywhere, but Python facilitates
the implementation by providing much more expressive features and syntax for that.
"""


def test_function_decorators():
    """Function Decorators."""

    # Function decorators are simply wrappers to existing functions. Putting the ideas mentioned
    # above together, we can build a decorator. In this example let's consider a function that
    # wraps the string output of another function by p tags.

    # This is the function that we want to decorate.
    def greeting(name):
        return "Hello, {0}!".format(name)

    # This function decorates another functions output with <p> tag.
    def decorate_with_p(func):
        def function_wrapper(name):
            return "<p>{0}</p>".format(func(name))
        return function_wrapper

    # Now, let's call our decorator and pass the function we want decorate to it.
    my_get_text = decorate_with_p(greeting)

    # Here we go, we've just decorated the function output without changing the function itself.
    assert my_get_text('John') == '<p>Hello, John!</p>'  # With decorator.
    assert greeting('John') == 'Hello, John!'  # Without decorator.

    # Now, Python makes creating and using decorators a bit cleaner and nicer for the programmer
    # through some syntactic sugar  There is a neat shortcut for that, which is to mention the
    # name of the decorating function before the function to be decorated. The name of the
    # decorator should be prepended with an @ symbol.

    @decorate_with_p
    def greeting_with_p(name):
        return "Hello, {0}!".format(name)

    assert greeting_with_p('John') == '<p>Hello, John!</p>'

    # Now let's consider we wanted to decorate our greeting function by one more functions to wrap a
    # div the string output.

    # This will be our second decorator.
    def decorate_with_div(func):
        def function_wrapper(text):
            return "<div>{0}</div>".format(func(text))
        return function_wrapper

    # With the basic approach, decorating get_text would be along the lines of
    # greeting_with_div_p = decorate_with_div(decorate_with_p(greeting_with_p))

    # With Python's decorator syntax, same thing can be achieved with much more expressive power.
    @decorate_with_div
    @decorate_with_p
    def greeting_with_div_p(name):
        return "Hello, {0}!".format(name)

    assert greeting_with_div_p('John') == '<div><p>Hello, John!</p></div>'

    # One important thing to notice here is that the order of setting our decorators matters.
    # If the order was different in the example above, the output would have been different.

    # Passing arguments to decorators.

    # Looking back at the example before, you can notice how redundant the decorators in the
    # example are. 2 decorators(decorate_with_div, decorate_with_p) each with the same
    # functionality but wrapping the string with different tags. We can definitely do much better
    # than that. Why not have a more general implementation for one that takes the tag to wrap
    # with as a string? Yes please!

    def tags(tag_name):
        def tags_decorator(func):
            def func_wrapper(name):
                return "<{0}>{1}</{0}>".format(tag_name, func(name))
            return func_wrapper
        return tags_decorator

    @tags('div')
    @tags('p')
    def greeting_with_tags(name):
        return "Hello, {0}!".format(name)

    assert greeting_with_tags('John') == '<div><p>Hello, John!</p></div>'
```
# 类(classes)
## 类定义(class defintions)
```python
"""Class Definition Syntax.
@see: https://docs.python.org/3/tutorial/classes.html
Python is an object oriented programming language.
Almost everything in Python is an object, with its properties and methods.
A Class is like an object constructor, or a "blueprint" for creating objects.
"""


def test_class_definition():
    """Class definition."""

    # Class definitions, like function definitions (def statements) must be executed before they
    # have any effect. (You could conceivably place a class definition in a branch of an if
    # statement, or inside a function.)

    class GreetingClass:
        """Example of the class definition
        This class contains two public methods and doesn't contain constructor.
        """
        name = 'user'

        def say_hello(self):
            """Class method."""
            # The self parameter is a reference to the class itself, and is used to access variables
            # that belongs to the class. It does not have to be named self , you can call it
            # whatever you like, but it has to be the first parameter of any function in the class.
            return 'Hello ' + self.name

        def say_goodbye(self):
            """Class method."""
            return 'Goodbye ' + self.name

    # When a class definition is entered, a new namespace is created, and used as the local scope —
    # thus, all assignments to local variables go into this new namespace. In particular, function
    # definitions bind the name of the new function here.

    # Class instantiation uses function notation. Just pretend that the class object is a
    # parameterless function that returns a new instance of the class. For example the following
    # code will creates a new instance of the class and assigns this object to the local variable.
    greeter = GreetingClass()

    assert greeter.say_hello() == 'Hello user'
    assert greeter.say_goodbye() == 'Goodbye user'
```
## 类对象(class objects)
```python
"""Class Definition Syntax.
@see: https://docs.python.org/3/tutorial/classes.html#class-objects
After defining the class attributes to a class, the class object can be created by assigning the
object to a variable. The created object would have instance attributes associated with it.
"""


def test_class_objects():
    """Class Objects.
    Class objects support two kinds of operations:
    - attribute references
    - instantiation.
    """

    # ATTRIBUTE REFERENCES use the standard syntax used for all attribute references in
    # Python: obj.name. Valid attribute names are all the names that were in the class’s namespace
    # when the class object was created. For class MyCounter the following references are valid
    # attribute references:

    class ComplexNumber:
        """Example of the complex numbers class"""

        real = 0
        imaginary = 0

        def get_real(self):
            """Return real part of complex number."""
            return self.real

        def get_imaginary(self):
            """Return imaginary part of complex number."""
            return self.imaginary

    assert ComplexNumber.real == 0

    # __doc__ is also a valid attribute, returning the docstring belonging to the class
    assert ComplexNumber.__doc__ == 'Example of the complex numbers class'

    # Class attributes can also be assigned to, so you can change the value of
    # ComplexNumber.counter by assignment.
    ComplexNumber.real = 10
    assert ComplexNumber.real == 10

    # CLASS INSTANTIATION uses function notation. Just pretend that the class object is a
    # parameterless function that returns a new instance of the class. For example
    # (assuming the above class):
    complex_number = ComplexNumber()

    assert complex_number.real == 10
    assert complex_number.get_real() == 10

    # Let's change counter default value back.
    ComplexNumber.real = 10
    assert ComplexNumber.real == 10

    # The instantiation operation (“calling” a class object) creates an empty object. Many classes
    # like to create objects with instances customized to a specific initial state. Therefore a
    # class may define a special method named __init__(), like this:

    class ComplexNumberWithConstructor:
        """Example of the class with constructor"""
        def __init__(self, real_part, imaginary_part):
            self.real = real_part
            self.imaginary = imaginary_part

        def get_real(self):
            """Return real part of complex number."""
            return self.real

        def get_imaginary(self):
            """Return imaginary part of complex number."""
            return self.imaginary

    complex_number = ComplexNumberWithConstructor(3.0, -4.5)
    assert complex_number.real, complex_number.imaginary == (3.0, -4.5)
```
## 实例对象(instance objects)
```python
"""Class Definition Syntax.
@see: https://docs.python.org/3/tutorial/classes.html#instance-objects
"""


def test_instance_objects():
    """Instance Objects.
    Now what can we do with instance objects? The only operations understood by instance objects
    are attribute references. There are two kinds of valid attribute names:
    - data attributes
    - methods.
    """

    # DATA ATTRIBUTES need not be declared; like local variables, they spring into existence when
    # they are first assigned to. For example, if x is the instance of MyCounter created above,
    # the following piece of code will print the value 16, without leaving a trace.

    # pylint: disable=too-few-public-methods
    class DummyClass:
        """Dummy class"""
        pass

    dummy_instance = DummyClass()

    # pylint: disable=attribute-defined-outside-init
    dummy_instance.temporary_attribute = 1
    assert dummy_instance.temporary_attribute == 1
    del dummy_instance.temporary_attribute
```
## 方法对象(method objects)
```python
"""Class Definition Syntax.
@see: https://docs.python.org/3/tutorial/classes.html#method-objects
Classes can have two types of attribute references: data or methods. Class methods are called
by [variable_name].[method_name]([parameters]) as opposed to class data which lacks the ().
"""


class MyCounter:
    """A simple example of the counter class"""
    counter = 10

    def get_counter(self):
        """Return the counter"""
        return self.counter

    def increment_counter(self):
        """Increment the counter"""
        self.counter += 1
        return self.counter


def test_method_objects():
    """Method Objects."""

    # The other kind of instance attribute reference is a method. A method is a function that
    # “belongs to” an object. (In Python, the term method is not unique to class instances: other
    # object types can have methods as well. For example, list objects have methods called append,
    # insert, remove, sort, and so on. However, in the following discussion, we’ll use the term
    # method exclusively to mean methods of class instance objects, unless explicitly stated
    # otherwise.)

    # But be aware that counter.get_counter() is not the same thing as MyCounter.get_counter() —
    # it is a method object, not a function object.

    # Usually, a method is called right after it is bound
    counter = MyCounter()
    assert counter.get_counter() == 10

    # However, it is not necessary to call a method right away: counter.get_counter() is a method
    # object, and can be stored away and called at a later time. For example:
    get_counter = counter.get_counter
    assert get_counter() == 10

    # What exactly happens when a method is called? You may have noticed that counter.get_counter()
    # was called without an argument above, even though the function definition for get_counter()
    # specified an argument (self). What happened to the argument? Surely Python raises an
    # exception when a function that requires an argument is called without any — even if the
    # argument isn’t actually used…

    # Actually, you may have guessed the answer: the special thing about methods is that the
    # instance object is passed as the first argument of the function. In our example, the call
    # counter.get_counter() is exactly equivalent to MyCounter.get_counter(counter). In general,
    # calling a method with a list of n arguments is equivalent to calling the corresponding
    # function with an argument list that is created by inserting the method’s instance object
    # before the first argument.

    assert counter.get_counter() == 10
    assert MyCounter.get_counter(counter) == 10
```
## 类和实例变量(class and instance variables)
```python
"""Class and Instance Variables.
@see: https://docs.python.org/3/tutorial/classes.html#class-and-instance-variables
Generally speaking, instance variables are for data unique to each instance and class variables are
for attributes and methods shared by all instances of the class.
"""


def test_class_and_instance_variables():
    """Class and Instance Variables."""

    # pylint: disable=too-few-public-methods
    class Dog:
        """Dog class example"""
        kind = 'canine'  # Class variable shared by all instances.

        def __init__(self, name):
            self.name = name  # Instance variable unique to each instance.

    fido = Dog('Fido')
    buddy = Dog('Buddy')

    # Shared by all dogs.
    assert fido.kind == 'canine'
    assert buddy.kind == 'canine'

    # Unique to fido.
    assert fido.name == 'Fido'

    # Unique to buddy.
    assert buddy.name == 'Buddy'

    # Shared data can have possibly surprising effects with involving mutable objects such as lists
    # and dictionaries. For example, the tricks list in the following code should not be used as a
    # class variable because just a single list would be shared by all Dog instances.

    # pylint: disable=too-few-public-methods
    class DogWithSharedTricks:
        """Dog class example with wrong shared variable usage"""
        tricks = []  # Mistaken use of a class variable (see below) for mutable objects.

        def __init__(self, name):
            self.name = name  # Instance variable unique to each instance.

        def add_trick(self, trick):
            """Add trick to the dog
            This function illustrate mistaken use of mutable class variable tricks (see below).
            """
            self.tricks.append(trick)

    fido = DogWithSharedTricks('Fido')
    buddy = DogWithSharedTricks('Buddy')

    fido.add_trick('roll over')
    buddy.add_trick('play dead')

    assert fido.tricks == ['roll over', 'play dead']  # unexpectedly shared by all dogs
    assert buddy.tricks == ['roll over', 'play dead']  # unexpectedly shared by all dogs

    # Correct design of the class should use an instance variable instead:

    # pylint: disable=too-few-public-methods
    class DogWithTricks:
        """Dog class example"""

        def __init__(self, name):
            self.name = name  # Instance variable unique to each instance.
            self.tricks = []  # creates a new empty list for each dog

        def add_trick(self, trick):
            """Add trick to the dog
            This function illustrate mistaken use of mutable class variable tricks (see below).
            """
            self.tricks.append(trick)

    fido = DogWithTricks('Fido')
    buddy = DogWithTricks('Buddy')

    fido.add_trick('roll over')
    buddy.add_trick('play dead')

    assert fido.tricks == ['roll over']
    assert buddy.tricks == ['play dead']
```
## 继承(Inheritance)
```python
"""Inheritance
@see: https://docs.python.org/3/tutorial/classes.html#inheritance
Inheritance is one of the principles of object-oriented programming. Since classes may share a lot
of the same code, inheritance allows a derived class to reuse the same code and modify accordingly
"""


# pylint: disable=too-few-public-methods
class Person:
    """Example of the base class"""
    def __init__(self, name):
        self.name = name

    def get_name(self):
        """Get person name"""
        return self.name


# The syntax for a derived class definition looks like this.
# pylint: disable=too-few-public-methods
class Employee(Person):
    """Example of the derived class
    The Base Class (in our case Person) must be defined in a scope containing the derived class
    definition. In place of a base class name, other arbitrary expressions are also allowed.
    Derived classes may override methods of their base classes. Because methods have no special
    privileges when calling other methods of the same object, a method of a base class that calls
    another method defined in the same base class may end up calling a method of a derived class
    that overrides it.
    An overriding method in a derived class may in fact want to extend rather than simply replace
    the base class method of the same name. There is a simple way to call the base class method
    directly: just call BaseClassName.methodname(self, arguments). This is occasionally useful to
    clients as well. (Note that this only works if the base class is accessible as BaseClassName
    in the global scope.)
    """
    def __init__(self, name, staff_id):
        Person.__init__(self, name)
        # You may also use super() here in order to avoid explicit using of parent class name:
        # >>> super().__init__(name)
        self.staff_id = staff_id

    def get_full_id(self):
        """Get full employee id"""
        return self.get_name() + ', ' + self.staff_id


def test_inheritance():
    """Inheritance."""

    # There’s nothing special about instantiation of derived classes: DerivedClassName() creates a
    # new instance of the class. Method references are resolved as follows: the corresponding class
    # attribute is searched, descending down the chain of base classes if necessary, and the method
    # reference is valid if this yields a function object.
    person = Person('Bill')
    employee = Employee('John', 'A23')

    assert person.get_name() == 'Bill'
    assert employee.get_name() == 'John'
    assert employee.get_full_id() == 'John, A23'

    # Python has two built-in functions that work with inheritance:
    #
    # - Use isinstance() to check an instance’s type: isinstance(obj, int) will be True only if
    # obj.__class__ is int or some class derived from int.
    #
    # - Use issubclass() to check class inheritance: issubclass(bool, int) is True since bool is
    # a subclass of int. However, issubclass(float, int) is False since float is not a subclass
    # of int.

    assert isinstance(employee, Employee)
    assert not isinstance(person, Employee)

    assert isinstance(person, Person)
    assert isinstance(employee, Person)

    assert issubclass(Employee, Person)
    assert not issubclass(Person, Employee)
```

## 多重继承(multiple inheritance)
```python
"""Multiple Inheritance
@see: https://docs.python.org/3/tutorial/classes.html#multiple-inheritance
Some classes may derive from multiple classes. This means that the derived class would have
its attributes, along with the attributes of all the classes that it was derived from.
"""


def test_multiple_inheritance():
    """Multiple Inheritance"""

    # pylint: disable=too-few-public-methods
    class Clock:
        """Clock class"""

        time = '11:23 PM'

        def get_time(self):
            """Get current time
            Method is hardcoded just for multiple inheritance illustration.
            """
            return self.time

    # pylint: disable=too-few-public-methods
    class Calendar:
        """Calendar class"""

        date = '12/08/2018'

        def get_date(self):
            """Get current date
            Method is hardcoded just for multiple inheritance illustration.
            """
            return self.date

    # Python supports a form of multiple inheritance as well. A class definition with multiple
    # base classes looks like this.
    class CalendarClock(Clock, Calendar):
        """Class that uses multiple inheritance.
        For most purposes, in the simplest cases, you can think of the search for attributes i
        nherited from a parent class as depth-first, left-to-right, not searching twice in the same
        class where there is an overlap in the hierarchy. Thus, if an attribute is not found in
        CalendarClock, it is searched for in Clock, then (recursively) in the base classes of
        Clock, and if it was not found there, it was searched for in Calendar, and so on.
        In fact, it is slightly more complex than that; the method resolution order changes
        dynamically to support cooperative calls to super(). This approach is known in some other
        multiple-inheritance languages as call-next-method and is more powerful than the super call
        found in single-inheritance languages.
        Dynamic ordering is necessary because all cases of multiple inheritance exhibit one or more
        diamond relationships (where at least one of the parent classes can be accessed through
        multiple paths from the bottommost class). For example, all classes inherit from object,
        so any case of multiple inheritance provides more than one path to reach object. To keep
        the base classes from being accessed more than once, the dynamic algorithm linearizes the
        search order in a way that preserves the left-to-right ordering specified in each class,
        that calls each parent only once, and that is monotonic (meaning that a class can be
        subclassed without affecting the precedence order of its parents).
        """

    calendar_clock = CalendarClock()

    assert calendar_clock.get_date() == '12/08/2018'
    assert calendar_clock.get_time() == '11:23 PM'
```
# 模块(modules)
## 模块
```python
"""Modules.
@see: https://docs.python.org/3/tutorial/modules.html
As your program gets longer, you may want to split it into several files for easier maintenance.
You may also want to use a handy function that you’ve written in several programs without copying
its definition into each program.
To support this, Python has a way to put definitions in a file and use them in a script or in an
interactive instance of the interpreter. Such a file is called a module; definitions from a module
can be imported into other modules or into the main module (the collection of variables that you
have access to in a script executed at the top level and in calculator mode).
A module is a file containing Python definitions and statements. The file name is the module name
with the suffix .py appended. Within a module, the module’s name (as a string) is available as the
value of the global variable __name__.
When the interpreter executes the import statement, it searches for module in a list of
directories assembled from the following sources:
- The directory from which the input script was run or the current directory if the interpreter is
being run interactively
- The list of directories contained in the PYTHONPATH environment variable, if it is set. (The
format for PYTHONPATH is OS-dependent but should mimic the PATH environment variable.)
- An installation-dependent list of directories configured at the time Python is installed
The resulting search path is accessible in the Python variable sys.path, which is obtained from a
module named sys:
>>> import sys
>>> sys.path
@see: https://realpython.com/python-modules-packages/
"""

# This does not enter the names of the functions defined in fibonacci_module directly in the
# current symbol table; it only enters the module name fibonacci_module there.
import fibonacci_module

# There is a variant of the import statement that imports names from a module directly into the
# importing module’s symbol table. For example:

# pylint: disable=reimported
from fibonacci_module import fibonacci_at_position, fibonacci_smaller_than

# There is even a variant to import all names that a module defines. This imports all names except
# those beginning with an underscore (_). In most cases Python programmers do not use this facility
# since it introduces an unknown set of names into the interpreter, possibly hiding some things you
# have already defined.
# >>> from fibonacci_module import *

# If the module name is followed by as, then the name following as is bound directly to the
# imported module:
import fibonacci_module as fibonacci_module_renamed

# It can also be used when utilising from with similar effects:
from fibonacci_module import fibonacci_at_position as fibonacci_at_position_renamed

# When a module named spam is imported, the interpreter first searches for a built-in module with
# that name. If not found, it then searches for a file named spam.py in a list of directories
# given by the variable sys.path. sys.path is initialized from these locations:
#
# - The directory containing the input script (or the current directory when no file is specified).
# - PYTHONPATH (a list of directory names, with the same syntax as the shell variable PATH).
# - The installation-dependent default.


def test_modules():
    """Modules"""

    assert fibonacci_module.fibonacci_at_position(7) == 13
    assert fibonacci_at_position(7) == 13
    assert fibonacci_module_renamed.fibonacci_at_position(7) == 13
    assert fibonacci_at_position_renamed(7) == 13

    assert fibonacci_module.fibonacci_smaller_than(100) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
    assert fibonacci_smaller_than(100) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
    assert fibonacci_module_renamed.fibonacci_smaller_than(10) == [0, 1, 1, 2, 3, 5, 8]

    # If you intend to use a function often you can assign it to a local name.
    fibonacci = fibonacci_module.fibonacci_smaller_than
    assert fibonacci(100) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]

    # The built-in function dir() is used to find out which names a module defines. It returns a
    # sorted list of strings.
    assert dir(fibonacci_module) == [
        '__builtins__',
        '__cached__',
        '__doc__',
        '__file__',
        '__loader__',
        '__name__',
        '__package__',
        '__spec__',
        'fibonacci_at_position',
        'fibonacci_smaller_than',
    ]
```

```python
"""Fibonacci numbers module.
@see: https://docs.python.org/3/tutorial/modules.html
A module is a file containing Python definitions and statements. The file name is the module name
with the suffix .py appended. Within a module, the module’s name (as a string) is available as the
value of the global variable __name__.
"""


def fibonacci_at_position(position):
    """Return Fibonacci number at specified position"""
    current_position = 0
    previous_number, current_number = 0, 1
    while current_position < position:
        current_position += 1
        previous_number, current_number = current_number, previous_number + current_number
    return previous_number


def fibonacci_smaller_than(limit):
    """Return Fibonacci series up to limit"""
    result = []
    previous_number, current_number = 0, 1
    while previous_number < limit:
        result.append(previous_number)
        previous_number, current_number = current_number, previous_number + current_number
    return result


# When you run a Python module with:
#
# >>> python fibonacci.py <arguments>
#
# the code in the module will be executed, just as if you imported it, but with
# the __name__ set to "__main__". That means that by adding this code at the end of your module
# you can make the file usable as a script as well as an importable module, because the code that
# parses the command line only runs if the module is executed as the “main” file:
#
# >>> python fibonacci.py 50
if __name__ == '__main__':
    import sys
    print(fibonacci_smaller_than(int(sys.argv[1])))
```
## 包(packages)
```python
"""Packages.
@see: https://docs.python.org/3/tutorial/modules.html#packages
Packages are a way of structuring Python’s module namespace by using “dotted module names”. For
example, the module name A.B designates a submodule named B in a package named A. Just like the
use of modules saves the authors of different modules from having to worry about each other’s
global variable names, the use of dotted module names saves the authors of multi-module packages
like NumPy or Pillow from having to worry about each other’s module names.
The __init__.py files are required to make Python treat the directories as containing packages;
this is done to prevent directories with a common name, such as string, from unintentionally hiding
valid modules that occur later on the module search path. In the simplest case, __init__.py can
just be an empty file, but it can also execute initialization code for the package or set the
__all__ variable, described later.
When the interpreter executes the import statement, it searches for module in a list of
directories assembled from the following sources:
- The directory from which the input script was run or the current directory if the interpreter is
being run interactively
- The list of directories contained in the PYTHONPATH environment variable, if it is set. (The
format for PYTHONPATH is OS-dependent but should mimic the PATH environment variable.)
- An installation-dependent list of directories configured at the time Python is installed
The resulting search path is accessible in the Python variable sys.path, which is obtained from a
module named sys:
>>> import sys
>>> sys.path
@see: https://realpython.com/python-modules-packages/
"""

# Users of the package can import individual modules from the package, for example.
import sound_package.effects.echo

# An alternative way of importing the submodule is:

# pylint: disable=reimported
from sound_package.effects import echo

# Yet another variation is to import the desired function or variable directly:
from sound_package.effects.echo import echo_function

# Note that when using from package import item, the item can be either a submodule (or subpackage)
# of the package, or some other name defined in the package, like a function, class or variable.
# The import statement first tests whether the item is defined in the package; if not, it assumes
# it is a module and attempts to load it. If it fails to find it, an ImportError exception is
# raised.

# Contrarily, when using syntax like import item.subitem.subsubitem, each item except for the last
# must be a package; the last item can be a module or a package but can’t be a class or function or
# variable defined in the previous item.


def test_packages():
    """Packages."""
    assert sound_package.effects.echo.echo_function() == 'Do echo effect'
    assert echo.echo_function() == 'Do echo effect'
    assert echo_function() == 'Do echo effect'
```
# 错误和异常(errors andd exceptions)
## 处理异常(handle exceptions)
```python
"""Errors and Exceptions.
@see: https://docs.python.org/3/tutorial/errors.html#errors-and-exceptions
Even if a statement or expression is syntactically correct, it may cause an error when an attempt
is made to execute it. Errors detected during execution are called exceptions and are not
unconditionally fatal.
It is possible to write programs that handle selected exceptions.
"""


def test_handle_exceptions():
    """Handling of exceptions
    The try statement works as follows.
    - First, the try clause (the statement(s) between the try and except keywords) is executed.
    - If no exception occurs, the except clause is skipped and execution of the try statement
    is finished.
    - If an exception occurs during execution of the try clause, the rest of the clause is skipped.
    Then if its type matches the exception named after the except keyword, the except clause is
    executed, and then execution continues after the try statement.
    - If an exception occurs which does not match the exception named in the except clause, it is
    passed on to outer try statements; if no handler is found, it is an unhandled exception and
    execution stops with a message.
    """

    # Let's simulate division by zero exception.
    exception_has_been_handled = False
    try:
        result = 10 * (1 / 0)  # division by zero
        # We should not get here at all.
        assert result
    except ZeroDivisionError:
        # We should get here because of division by zero.
        exception_has_been_handled = True

    assert exception_has_been_handled

    # Let's simulate undefined variable access exception.
    exception_has_been_handled = False
    try:
        # pylint: disable=undefined-variable
        result = 4 + spam * 3  # name 'spam' is not defined
        # We should not get here at all.
        assert result
    except NameError:
        # We should get here because of division by zero.
        exception_has_been_handled = True

    assert exception_has_been_handled

    # A try statement may have more than one except clause, to specify handlers for different
    # exceptions. At most one handler will be executed. Handlers only handle exceptions that occur
    # in the corresponding try clause, not in other handlers of the same try statement. An except
    # clause may name multiple exceptions as a parenthesized tuple, for example:

    exception_has_been_handled = False
    try:
        result = 10 * (1 / 0)  # division by zero
        # We should not get here at all.
        assert result
    except (ZeroDivisionError, NameError):
        # We should get here because of division by zero.
        exception_has_been_handled = True

    assert exception_has_been_handled

    # Exception handlers may be chained.
    exception_has_been_handled = False
    try:
        result = 10 * (1 / 0)  # division by zero
        # We should not get here at all.
        assert result
    except NameError:
        # We should get here because of division by zero.
        exception_has_been_handled = True
    except ZeroDivisionError:
        # We should get here because of division by zero.
        exception_has_been_handled = True

    assert exception_has_been_handled

    # The try … except statement has an optional else clause, which, when present, must follow all
    # except clauses. It is useful for code that must be executed if the try clause does not raise
    # an exception. For example:

    exception_has_been_handled = False
    no_exceptions_has_been_fired = False

    try:
        result = 10
        # We should not get here at all.
        assert result
    except NameError:
        # We should get here because of division by zero.
        exception_has_been_handled = True
    else:
        no_exceptions_has_been_fired = True

    assert not exception_has_been_handled
    assert no_exceptions_has_been_fired
```

## 触发异常(raise exceptions)
```python
"""Raising Exceptions.
@see: https://docs.python.org/3/tutorial/errors.html#raising-exceptions
The raise statement allows the programmer to force a specified exception to occur.
"""


def test_raise_exception():
    """Raising Exceptions.
    The raise statement allows the programmer to force a specified exception to occur.
    """
    exception_is_caught = False

    try:
        # The sole argument to raise indicates the exception to be raised. This must be either an
        # exception instance or an exception class (a class that derives from Exception). If an
        # exception class is passed, it will be implicitly instantiated by calling its constructor
        # with no arguments
        raise NameError('HiThere')  # shorthand for 'raise ValueError()'
    except NameError:
        exception_is_caught = True

    assert exception_is_caught


def test_user_defined_exception():
    """User-defined Exceptions"""

    # Programs may name their own exceptions by creating a new exception class. Exceptions should
    # typically be derived from the Exception class, either directly or indirectly.
    # Most exceptions are defined with names that end in “Error,” similar to the naming of the
    # standard exceptions. Many standard modules define their own exceptions to report errors
    # that may occur in functions they define.
    class MyCustomError(Exception):
        """Example of MyCustomError exception."""
        def __init__(self, message):
            super().__init__(message)
            self.message = message

    custom_exception_is_caught = False

    try:
        raise MyCustomError('My custom message')
    except MyCustomError:
        custom_exception_is_caught = True

    assert custom_exception_is_caught
```
# 文件(files)
## 读和写(reading and writing)
```python
"""Reading and Writing Files
@see: https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files
The process of reading and writing to a file is like finding a book and opening a book.
First, the file is located, opened to the first page, then reading/writing begins until it reaches
the end of the file.
"""


def test_files_open():
    """Open files
    open() returns a file object, and is most commonly used with two arguments:
    open(filename, mode).
    The first argument is a string containing the filename. The second argument is another string
    containing a few characters describing the way in which the file will be used. mode can be:
    - 'r' when the file will only be read,
    - 'w' for only writing (an existing file with the same name will be erased),
    - 'a' opens the file for appending; any data written to the file is automatically added to end.
    - 'r+' opens the file for both reading and writing.
    The mode argument is optional; 'r' will be assumed if it’s omitted.
    Normally, files are opened in text mode, that means, you read and write strings from and to the
    file, which are encoded in a specific encoding. If encoding is not specified, the default is
    platform dependent (see open()). 'b' appended to the mode opens the file in binary mode: now
    the data is read and written in the form of bytes objects. This mode should be used for all
    files that don’t contain text.
    In text mode, the default when reading is to convert platform-specific line endings (\n on
    Unix, \r\n on Windows) to just \n. When writing in text mode, the default is to convert
    occurrences of \n back to platform-specific line endings. This behind-the-scenes modification
    to file data is fine for text files, but will corrupt binary data like that in JPEG or EXE
    files. Be very careful to use binary mode when reading and writing such files.
    It is good practice to use the with keyword when dealing with file objects. The advantage is
    that the file is properly closed after its suite finishes, even if an exception is raised at
    some point. Using with is also much shorter than writing equivalent try-finally blocks:
    """

    # Open files without using 'with' statement.
    file = open('src/files/multi_line_file.txt', 'r')

    assert not file.closed

    read_data = file.read()

    assert read_data == (
        'first line\n'
        'second line\n'
        'third line'
    )

    file.close()

    assert file.closed

    # Open file using with.
    with open('src/files/multi_line_file.txt', 'r') as file:
        read_data = file.read()

        assert read_data == (
            'first line\n'
            'second line\n'
            'third line'
        )

    assert file.closed

    # If you’re not using the with keyword, then you should call f.close() to close the file and
    # immediately free up any system resources used by it. If you don’t explicitly close a file,
    # Python’s garbage collector will eventually destroy the object and close the open file for you,
    # but the file may stay open for a while. Another risk is that different Python implementations
    # will do this clean-up at different times.
```
## 文件对象的方法(file methods)
```python
"""Methods of File Objects
@see: https://docs.python.org/3/tutorial/inputoutput.html#methods-of-file-objects
Reading from a file does not always have to be sequential. There are methods to look for
specific locations in the file, much like flipping to a page in a book.
"""


def test_file_methods():
    """Methods of File Objects"""

    multi_line_file = open('src/files/multi_line_file.txt', 'r')
    binary_file = open('src/files/binary_file', 'r')

    # To read a file’s contents, call f.read(size), which reads some quantity of data and returns
    # it as a string (in text mode) or bytes object (in binary mode). size is an optional numeric
    # argument. When size is omitted or negative, the entire contents of the file will be read and
    # returned; it’s your problem if the file is twice as large as your machine’s memory. Otherwise,
    # at most size bytes are read and returned. If the end of the file has been reached, f.read()
    # will return an empty string ('').
    read_data = multi_line_file.read()

    # pylint: disable=duplicate-code
    assert read_data == 'first line\nsecond line\nthird line'

    # To change the file object’s position, use f.seek(offset, from_what). The position is computed
    # from adding offset to a reference point; the reference point is selected by the from_what
    # argument. A from_what value of 0 measures from the beginning of the file, 1 uses the current
    # file position, and 2 uses the end of the file as the reference point. from_what can be omitted
    # and defaults to 0, using the beginning of the file as the reference point.
    assert binary_file.seek(0) == 0  # Go to the 0th byte in the file
    assert binary_file.seek(6) == 6  # Go to the 6th byte in the file

    assert binary_file.read(1) == '6'

    # f.readline() reads a single line from the file; a newline character (\n) is left at the end
    # of the string, and is only omitted on the last line of the file if the file doesn’t end in a
    # newline. This makes the return value unambiguous; if f.readline() returns an empty string,
    # the end of the file has been reached, while a blank line is represented by '\n', a string
    # containing only a single newline.
    multi_line_file.seek(0)

    assert multi_line_file.readline() == 'first line\n'
    assert multi_line_file.readline() == 'second line\n'
    assert multi_line_file.readline() == 'third line'
    assert multi_line_file.readline() == ''

    multi_line_file.close()
    binary_file.close()
```
# 拓展(additions)
## `pass`语句
```python
"""PASS statement
@see: https://docs.python.org/3/tutorial/controlflow.html
The pass statement does nothing. It can be used when a statement is required syntactically but
the program requires no action.
"""


def test_pass_in_function():
    """PASS statement in function
    "Pass" can be used as a place-holder for a function or conditional body when you are working on
    new code, allowing you to keep thinking at a more abstract level.
    The pass statement below is silently ignored but it makes current test_pass() function valid.
    """
    pass


def test_pass_in_loop():
    """PASS in loops.
    "Pass" can be used when a statement is required syntactically but the program requires no
    action. For example:
    """

    # pylint: disable=unused-variable
    for number in range(100):
        # It just don't do anything but for loop is still valid.
        pass

    # Example above is quite useless but it was given just for illustration of the idea.
    # The more useful example might be:
    #
    # while True:
    #   pass  # Busy-wait for keyboard interrupt (Ctrl+C)


# pylint: disable=too-few-public-methods
class MyEmptyClass:
    """PASS statement in class
    "Pass" is commonly used for creating minimal classes like current one.
    """
    pass
```
## 生成器(generattors)
```python
"""Generators.
@see: https://www.learnpython.org/en/Generators
Generators are used to create iterators, but with a different approach. Generators are simple
functions which return an iterable set of items, one at a time, in a special way.
When an iteration over a set of item starts using the for statement, the generator is run. Once the
generator's function code reaches a "yield" statement, the generator yields its execution back to
the for loop, returning a new value from the set. The generator function can generate as many
values (possibly infinite) as it wants, yielding each one in its turn.
"""

import random


def lottery():
    """Generator function example.
    Here is a simple example of a generator function which returns random integers.
    This function decides how to generate the random numbers on its own, and executes the yield
    statements one at a time, pausing in between to yield execution back to the main for loop.
    """
    # returns first 3 random numbers between 1 and 10
    # pylint: disable=unused-variable
    for i in range(3):
        yield random.randint(1, 10)

    # returns a 4th number between 10 and 20
    yield random.randint(10, 20)


def test_generators():
    """Yield statement"""
    for number_index, random_number in enumerate(lottery()):
        if number_index < 3:
            assert 0 <= random_number <= 10
        else:
            assert 10 <= random_number <= 20
```

# 标准库概要(standard libraries)
## `json`文件
```python
"""Serialization.
@see: https://www.learnpython.org/en/Serialization
Python provides built-in JSON libraries to encode and decode JSON.
"""

import json


def test_json():
    """JSON serialization."""

    # There are two basic formats for JSON data. Either in a string or the object data-structure.
    # The object data-structure, in Python, consists of lists and dictionaries nested inside each
    # other. The object data-structure allows one to use python methods (for lists and dictionaries)
    # to add, list, search and remove elements from the data-structure. The String format is mainly
    # used to pass the data into another program or load into a data-structure.

    person_dictionary = {'first_name': 'John', 'last_name': 'Smith', 'age': 42}
    assert person_dictionary['first_name'] == 'John'
    assert person_dictionary['age'] == 42

    json_string = '{"first_name": "John", "last_name": "Smith", "age": 42}'

    # To load JSON back to a data structure, use the "loads" method. This method takes a string
    # and turns it back into the json object data-structure:
    person_parsed_dictionary = json.loads(json_string)

    assert person_parsed_dictionary == person_dictionary
    assert person_parsed_dictionary['first_name'] == 'John'
    assert person_parsed_dictionary['age'] == 42

    # To encode a data structure to JSON, use the "dumps" method. This method takes an object and
    # returns a String:
    encoded_person_string = json.dumps(person_dictionary)

    assert encoded_person_string == json_string
```
## 文件通配符(glob)
```python
"""File Wildcards.
@see: https://docs.python.org/3/tutorial/stdlib.html#file-wildcards
The glob module provides a function for making file lists from directory wildcard searches:
"""

import glob


def test_glob():
    """File Wildcards."""

    # == operator for lists relies on the order of elements in the list.
    # In some cases (like on Linux Mint, python3.6) the glob() function returns list
    # in reverse order then  it might be expected. Thus lets sort both lists before comparison
    # using sorted() built-in function.
    assert sorted(glob.glob('src/standard_libraries/glob_files/*.txt')) == sorted([
        'src/standard_libraries/glob_files/first_file.txt',
        'src/standard_libraries/glob_files/second_file.txt'
    ])
```
## 正则匹配(`re`)
```python
"""String Pattern Matching.
@see: https://docs.python.org/3/tutorial/stdlib.html#string-pattern-matching
The re module provides regular expression tools for advanced string processing.
For complex matching and manipulation, regular expressions offer succinct, optimized solutions:
"""

import re


def test_re():
    """String Pattern Matching"""

    assert re.findall(r'\bf[a-z]*', 'which foot or hand fell fastest') == [
        'foot',
        'fell',
        'fastest'
    ]

    assert re.sub(r'(\b[a-z]+) \1', r'\1', 'cat in the the hat') == 'cat in the hat'

    # When only simple capabilities are needed, string methods are preferred because they are
    # easier to read and debug:
    assert 'tea for too'.replace('too', 'two') == 'tea for two'
```
## 命令行参数(argparse)
```python
import argparse

parser = argparse.ArgumentParser(prog = 'top',
    description = 'Show top lines from each file')
parser.add_argument('filenames', nargs='+')
parser.add_argument('-l', '--lines', type=int, default=10)
args = parser.parse_args()
print(args)
```
## 数学(math)
```python
"""Math.
@see: https://docs.python.org/3/tutorial/stdlib.html#mathematics
Math module is useful as many math functions are already implemented and optimized.
"""

import math
import random
import statistics


def test_math():
    """Math.
    The math module gives access to the underlying C library functions for floating point math.
    """
    assert math.cos(math.pi / 4) == 0.70710678118654757
    assert math.log(1024, 2) == 10.0


def test_random():
    """Random.
    The random module provides tools for making random selections.
    """

    # Choose from the list randomly.
    random_options = ['apple', 'pear', 'banana']
    random_choice = random.choice(random_options)  # i.e. 'apple'
    assert random_choice in random_options

    # Sampling without replacement.
    random_sample = random.sample(range(100), 10)  # i.e. [30, 83, 16, 4, 8, 81, 41, 50, 18, 33]
    for sample in random_sample:
        assert 0 <= sample <= 100

    # Choose random number.
    random_float = random.random()  # i.e. 0.17970987693706186
    assert 0 <= random_float <= 1

    # Random integer chosen from range(6)
    random_integer = random.randrange(6)  # i.e. 4
    assert 0 <= random_integer <= 6


def test_statistics():
    """Statistics.
    The statistics module calculates basic statistical properties (the mean, median,
    variance, etc.) of numeric data.
    """

    data = [2.75, 1.75, 1.25, 0.25, 0.5, 1.25, 3.5]

    assert statistics.mean(data) == 1.6071428571428572
    assert statistics.median(data) == 1.25
    assert statistics.variance(data) == 1.3720238095238095
```
## 日期和时间(date and times)
```python
"""Dates and Times.
@see: https://docs.python.org/3/tutorial/stdlib.html#dates-and-times
The datetime module supplies classes for manipulating dates and times in both simple and complex
ways. While date and time arithmetic is supported, the focus of the implementation is on efficient
member extraction for output formatting and manipulation. The module also supports objects that
are timezone aware.
"""

from datetime import date


def test_datetime():
    """Dates and Times"""

    real_now = date.today()
    assert real_now

    fake_now = date(2018, 8, 29)

    assert fake_now.day == 29
    assert fake_now.month == 8
    assert fake_now.year == 2018
    assert fake_now.ctime() == 'Wed Aug 29 00:00:00 2018'
    assert fake_now.strftime(
        '%m-%d-%y. %d %b %Y is a %A on the %d day of %B.'
    ) == '08-29-18. 29 Aug 2018 is a Wednesday on the 29 day of August.'

    # Dates support calendar arithmetic.
    birthday = date(1964, 7, 31)
    age = fake_now - birthday

    assert age.days == 19752
```
## 数据压缩(data compression)
```python
"""Data Compression.
@see: https://docs.python.org/3/tutorial/stdlib.html#data-compression
Common data archiving and compression formats are directly supported by modules including: zlib,
gzip, bz2, lzma, zipfile and tarfile.
"""

import zlib


def test_zlib():
    """zlib."""
    string = b'witch which has which witches wrist watch'
    assert len(string) == 41

    zlib_compressed_string = zlib.compress(string)
    assert len(zlib_compressed_string) == 37

    zlib_decompressed_string = zlib.decompress(zlib_compressed_string)
    assert zlib_decompressed_string == b'witch which has which witches wrist watch'

    assert zlib.crc32(string) == 226805979
```

# 项目框架(Project structure)

```python
An example structure for a python project:
my_project/
    README.md
    requirements.txt
    setup.py

    src/
        my_project/
            __init__.py
            my_module.py
            other_module.py

            my_pkg1/
                __init__.py
                my_third_module.py

    tests/
        conftest.py
        test_module.py
        test_other_module.py

        my_pkg1/
            test_my_third_module.py
```
```python

* requirements.txt lists the Python packages from which my_project depends on.
    * these can be installed by running pip install -r requirements
* setup.py is a file in which you include relevant information about your project and the file is also used for packaging your project. Here's a minimal example of a setup.py:

'''Minimal setup.py file'''

from setuptools import setup, find_packages

setup(
    name='my_project',
    version='0.1',
    packages=find_packages(where="src"),
    package_dir={"": "src"})

* Once you have the setup.py file in place, you can install your project in editable mode by running pip install -e . in the root directory of your project. In editable mode the installed version is updated when you make changes to the source code files.
```

# Reference
https://github.com/jerry-git/learn-python3

https://github.com/trekhleb/learn-python.git