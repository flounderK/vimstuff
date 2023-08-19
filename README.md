# vimstuff
I will probably delete this later.


# Random stuff for Converting C headers to python
## Convert a Struct field from c to python's struct
```
V - to start highlight
: - to start match and replace
s/\(\s*\)\(\S\+\)\s*\([[:alnum:]_\[\]]\+\);/\1("\3", \2),/g
```

## add python enum auto for an enum in C
```
^Ea = auto()^[<80><fd>aj^
```

## Others
```
replace multiline comment headers with python comment
%s/\/\*/#/g

remove all multiline comment suffixes
%s/\*\///g

replace tabs with four spaces
%s/\t/    /g

remove commas
s/,//g

convert single line defines to global assignments
s/#define\s\+\(\S\+\)\s\+\(.\+\)/\1 = \2/g


# replace C int types with python ctypes equivalent
%s/uint\(\d\+\)_t/c_uint\1/g
%s/int\(\d\+\)_t/c_int\1/g

```

