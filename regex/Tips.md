# Sentence with time-duration
* ^(?!.*\\b(meet|meeting|hold|held)\\b)(?=.*\\bfrom\\b)(?=.*\d\d:\d\d).*$
* \bABC\b word boundary
* Match expression1 expression2 and expression3
* (?=expression1)(?=expression2)(?=expression3)

* ^ --> start of sentence(?=.*\\b(meet|meeting|hold|held)\\b) --> find occurence of any of the words (?=.*\\bfrom\\b\s*\d{1,4}:?\d{0,2}) * --> find occurence of "from" FOLLOWED BY  --> one or more spaces FOLLOWED BY  --> a number (1 to 4 digits) FOLLOWED BY --> an optional : FOLLOWED BY --> a number (1 to 2 digits) FOLLOWED BY
* (?=.*\\b(AM|PM)?\\b) --> find the occurence of AM or PM (optional).*$  --> end of line
# Removing Duplicate Lines
1. Open file in notepad++
2. Select all, Edit, Line Operations, Sort Lexicographically
3. Find regex ^(.*\r?\n)\1+ and replace with ''
