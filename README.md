# HexBuilder
Command line tool that converts a text file to its representing hex code.

HexBuilder is a command line tool that was put together in 15 minutes to make byte code writing easier for the eye. It converts a commented text file:

```java
// header
ABCD DCBA 0000 0000
0000 0000 0000 0000

/*
    This is a multi-line comment.
*/
1239 9129

// oh and caps don't matter
AbCd cAfe
```

and converts it to a binary file whose hex dump is:

```java
ABCD DCBA 0000 0000
0000 0000 0000 0000
1239 9129 ABCD CAFE
```

So it basically strips all comments and whitespaces and does some random converting like ignore caps.

## Installation

Install with pip:

```sh
pip install hexbuilder
```

## Usage

Enter in command line:

```sh
hexbuilder my_text_file
```

This will create a `.hex` file (same name as input) as output in the same directory.

Alternatively, the output file can be specified with `-o`:

```sh
hexbuilder my_text_file -o output.hex
```