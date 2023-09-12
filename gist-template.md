# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors specify positions in the text:

^: Matches the start of a line.
$: Matches the end of a line.
\b: Matches a word boundary.
\B: Matches a non-word boundary.
Examples:

^start matches "start" at the beginning of a line.

end$ matches "end" at the end of a line.

\bword\b matches "word" as a whole word.

\Bword\B matches "word" within other text.

<a name="quantifiers"></a>

### Quantifiers
Quantifiers specify how many times a character or group should be matched:

*: Matches zero or more times.
+: Matches one or more times.
?: Matches zero or one time.
{n}: Matches exactly n times.
{n,}: Matches n or more times.
{n,m}: Matches between n and m times.

Examples:

\d+ matches one or more digits.

\w{2,4} matches 2 to 4 word characters.

### OR Operator
The | (pipe) acts as an OR operator between expressions:

Example:

(cat|dog) matches "cat" or "dog."

### Character Classes
Character classes match a single character from a set of characters:

[ ] (Square Brackets): Matches any character within the brackets.
[^ ] (Negated Square Brackets): Matches any character NOT within the brackets.
- (Hyphen): Specifies a range of characters.

Examples:

[aeiou] matches any vowel.

[^0-9] matches any non-digit.

[a-z] matches any lowercase letter.


### Flags
Flags modify the behavior of the regex pattern:

i: Case-insensitive matching.
g: Global matching (find all matches).
m: Multi-line matching.

Examples:

/abc/i matches "abc" case-insensitively.

/abc/g finds all occurrences of "abc."

/^abc/m matches "abc" at the start of each line.

### Grouping and Capturing
( ) (Round Brackets) create capturing groups:

Example:

(abc)+ matches "abc" one or more times.

### Bracket Expressions
Bracket expressions define character sets:

Example:

[a-zA-Z] matches any uppercase or lowercase letter.

### Greedy and Lazy Match
Quantifiers are greedy by default, but can be made lazy:

Greedy: Matches as much as possible.

Lazy: Matches as little as possible.

Examples:

.* is greedy and matches everything.

.*? is lazy and matches the minimum possible.

### Boundaries
Boundaries match positions, not characters:

Examples:

\bword\b matches "word" as a whole word.

\Bword\B matches "word" within other text.

### Back-references
Back-references match the same text as captured groups:

Example:

(abc)\1 matches "abcabc."

### Look-ahead and Look-behind
Look-ahead and look-behind assert conditions without consuming characters:

(?=...): Positive look-ahead.
(?!...): Negative look-ahead.
(?<=...): Positive look-behind.
(?<!...): Negative look-behind.
Examples:

foo(?=bar) matches "foo" only if followed by "bar."
foo(?!bar) matches "foo" only if not followed by "bar."
