# sortopts
Allows you to combine getopt with getopts and also get rid of the need for --longopt=x

## Variabels
`OPTOUT=1` - Only display all received arguments, do not parse

`SHORTDASH=1` - Print one dash before short parsed arguments

`PARSED=1` - Separate the key and its value from each other with a straight line (`|`)

## Example:
```
./sortopts "a:b:c:" "one:,two,three::" \
           -a1 -b 2 -c3 \
	   --one --two --three 3
```
