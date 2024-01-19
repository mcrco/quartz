Kinda similar to C++.

# Data Types

- int: +, -, $*$, div
- real: +, -, $*$, /
- string
- bool
- char ```#"t"```

When declaring variable, must use val keyword. To set type, use :type.

# Conversion

SML doesn't allow mixing of different types. Instead,
- real -> int: ```trunc, round ``` 
- int -> real: ```real```

# Function

```sml
fun inc (x:int) :int = x + 1;
```
