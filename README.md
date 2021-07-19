# sortopts
Allows you to combine getopt with getopts and also get rid of the need for --longopt=x

## Variabels
`OPTOUT=1` - Only display all received arguments, do not parse

`SHORTDASH=1` - Print one dash before short parsed arguments

`PARSED=1` - Separate the key and its value from each other with a straight line (`|`)

## Example:
```
./sortopts "a:b:c:d:-" "one:,two,three::" \
           -a1 -b 2 -c3 -d 4 \
	   --one --two --three 3
```

## Needed binaries:
`bash` \
`getopt` (from `util-linux`)

## if you want to use only bash built-in tools, no third party binaries
Use `legacyopts`. There, for parsing short arguments, `getopts` is used - a utility built into the bash.

Keep in mind that handling `x::` and `x:-` arguments will NOT work in this version of the script.
