```
grep version package.json
```

```
grep gulp package.json
```

```
grep -r react .
```

```
find . -name "*.js"
```

#### Find all files in /docs folder that match the pattern of ending in .html
```
find docs/ -name "*.html"
```

#### Recursively search for all matching open and close parentheses with any number of characters in between.
```
grep -r --color "(.*)" .
```

#### search for either http or https
```
grep --color "http." readme.md
```

#### better search  \? match 0 or 1 time
```
grep --color "https\?" readme.md
grep --color -E "https?" readme.md
```

#### better search  \+ match 1 or more
```
grep --color "https\+" readme.md
grep --color -E "https+" readme.md
```

#### | either or
```
echo "is it grey or gray?" | grep --color "grey\|gray"
echo "is it grey or gray?" | grep --color -E "grey|gray"
grep --color -rE "grey|gray" /examples
```

#### using anchor characters - beginning
```
grep "^#" app-spec.md
```

#### using anchor characters - end
```
grep --color ",$" app-spec.md

grep --color -r "^import .* from" examples/
```

#### match 
```
echo abc123 | grep --color "[ab]"
echo abc123 | grep --color "[a-z]"
echo abc123 | grep --color "[1-9]"
```
#### blob character ...developer designer
```
grep --color "de[a-z]*er" readme.md
grep --color "de[[:alpha:]]*er" readme.md

find . -name "*.js" | grep --color -E "[sS]pec"

grep -rE --color "(grey|gray)(\'|\")" .
grep -rE --color "(grey|gray)(\'|\"): (\'|\")#?[[:xdigit:]]+"
```
#### 'grey': #445588
#### 'grey': 445588
```
find examples/angularjs -name "*js" | grep -v "node_modules"
```