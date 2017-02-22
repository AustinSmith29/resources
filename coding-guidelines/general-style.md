# General Style Guidelines

## Simple Example

```c++
// Description of why your code does what it does
public void myFunction(int anArg)
{
	int testVariable = 1;

	if (anArg != 0)
	{
		MyClass sampleClass = new MyClass(anArg);
	}
}
```

## Style Outline

- Comments
    - Used to describe why your code does what it does. Use proper grammar.
    - Place above the relevant lines of code
	- Comment classes, functions, and methods
	- Comment related blocks of code
	- Keep comments updated
- Line Length
    - 100 character limit
- Indention
    - Always indent for new scope
    - Indents are tabs
    - When you exceeded the line limit, create a new line and indent twice to signify continuation.
	- When breaking up a line return after commas, and before (+, -, ==, &&, etc).

```c++
if (aBar == 5 || aBar == 12 || aBar == 98 ||
		aBar == 120 || aBar == 177 || aVar == 180)
{
	foo = 2;
}
```
- Number of lines per file
    - Try to have a maximum of around 200 lines
- Spacing
	- Separate different tasks/ideas with a blank line
	- Separate different functions/classes/methods with a blank line
	- Use spaces around math operators and Boolean expressions

```c++
// Addition
int x = 1 + 3;

// Multiplication
bool y = true || false;
```
- Naming  
	- Use descriptive names, with correctly spelled words
	- Constants in CAPS_WITH_UNDER
	- Classes in CapWords
	- Variables and methods in mixedCase
	- Class and struct members start with "the"
	- Parameters start with "a" or "an"
- Braces
	- Shall be placed on a new line

```c++
for (int i = 0; i < count; i++)
{
	std::cout << i;
}
```
- Other
	- Group related code
	- Avoid deep nesting


## Example

```c++
/**
 * "Foo bar" program, provides a useful example for the
 * UFOSC coding guidelines.
 */

#include <iostream>

// Example class
class FooBar
{
	public int theFooBar;

	FooBar(int aFoo, int aBar)
	{
		this.theFooBar = aFoo + aBar;
	}
}

// Creates a foo from bar to add back to bar
private bool makeFoo(int aBar)
{
	// Normally foobar is twice bar
	int foo = aBar;

	// Foobar can't be 0, because of arbitrary
	// reason for an example
	if (aBar == 0)
	{
		foo = 1;
	}

	return foo;
}

// Adds foo and bar together
int main()
{
	int bar = 1;

	// Foo is derived from bar
	int foo = makeFoo(bar);

	FooBar fooBar = new FooBar(foo, bar);

	std::cout << fooBar.theFooBar << std::endl;
	return 0;
}
```