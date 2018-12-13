# SED-for-Big-Data

Using old tools on current BIG DATA problems

# SED - a __Stream Editor__

## Description:
One of the first editors on unix.

Different versions behave differently.  Many do not work as advertised

Allowed editing on files larger than available memory (ram).
* Most (all) editors loaded contents in memory.
* Memory was expensive per MEG... $$$ GIG's $$$.
* Editors and tools developed to deal with files larger than available memory.
- cat, split, join, grep, tr, tee, comm, uniq, awk, perl, col, fmt, etc.
- troff, nroff
- regular expressions

SED will process text files with unlimited size.
* Does not load the file in memory.
* Reads sequentially through file and writes output as it processes through the file.
* Uses record addressing scheme based on lines,
   ```(<cr> - carrage return and/or <lf> - line feed)```

```
** Most used operation: s/<old>/<new>/ **
     substitute first occurence on a line containing <old> with <new> through entire file.
```

## Usage:
```
sed '<address><command><modifier>' <filename>
  address = start,finish
  command = s/<old>/<new>/   
  modifier = 1st occurence    g - all occurences on a line 
  filename = perform operation on filename
```

## References:
* SED and AWK 2nd Edition, by Dale Dougherty, Arnold Robbins
* http://www.grymoire.com/Unix/Sed.html  -Good Read 
* http://sed.sourceforge.net/sedfaq.html
* http://sed.sourceforge.net/grabbag/tutorials/
* http://www.columbia.edu/~rh120/ch106.x09 -history of SED
