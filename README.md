# YAML Tutorial
YAML is a data serialization language. It's intended as a replacement for JSON. It's a format for config files.

A single yaml file can have multiple documents. Each document starts with 3 dashes (---) and ends with three ellipsis (...)

YAML files consist of key: value pairs.

String values can be stored in single/double/no quotes.

Indentation means nesting. Only space character is used for indentation not tabs.

Comments use hashtag #

To escape a character, double quotes must be used:
```
strval: "text line with a new line character escaped \n"
```

If no quotes were used, the \n will be treated as 2 characters.

### Multi-Line String Value
If > is used, yaml processor will process it as a single line "text line starts here and ends here":
```
strval: >
  text line starts
  here and ends here
```

If | is used, yaml processor will process it as a multi-line string value:
```
strval: |
  text line starts
  here and ends here
```

### Null Value:
Use the word null or ~ to represent a null value:
```
name: null
email: ~
```

### Numeric Values:
```
scale: .inf
scale: -.inf
scale: .NAN
scale: 10
scale: 10.829
```

### Booleans
Booleans accept True | False | On | Off

### Arrays
```
items: [1, 2, 3, 4]

# or

items:
  - 1
  - 2
  - 3
  - 4

# example: {'items': [{'things': {'thing1': 'x', 'thing2': 'y'}}, {'other things': {'other thing1': 'z'}}]}
items:
  - things:
      thing1: x
      thing2: y
  - other things:
      other thing1: z

# example: {'items': [{'things': [{'thing1': 'x'}, {'thing2': 'y'}]}, {'other things': [{'other thing1': 'z'}]}]}
items:
  - things:
      - thing1: x
      - thing2: y
  - other things:
      - other thing1: z
```

### Dictinaries
```
things: {key1: value1, key2: value2}

# or

things:
  key1: value1
  key2: value2
```

