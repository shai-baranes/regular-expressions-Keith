# Complete Regular Expressions Tutorial!
Code &amp; text examples for my video tutorials on regular expressions (regex).

The first part of the video tutorial can be found here: https://youtu.be/vsa9GGzMFXQ

Some additional practice exercises can be found here: https://youtu.be/Qv_RYpREz5k

## Exercises

[Exercise \#1](https://github.com/KeithGalli/regular-expressions/blob/master/examples/meme-example.txt): Write a regex to match meme text format <br/>
[Exercise \#2](https://github.com/KeithGalli/regular-expressions/blob/master/examples/date-matching.txt): Write a regex to match a specific date format <br/>
[Exercise \#3](https://github.com/KeithGalli/regular-expressions/blob/master/examples/advanced-sentence-examples.txt): Detect if the same word pops up in a sentence multiple times <br/>
[Exercise \#4](https://github.com/KeithGalli/regular-expressions/blob/master/examples/password_regex_match.txt): Password matching with rules

## Resources

Here are some resources I find useful when learning regular expressions:
- [Regex101.com](https://regex101.com)
- [Regex cheat sheet](https://cheatography.com/davechild/cheat-sheets/regular-expressions/)
- [Regex golf practice exercises](https://alf.nu/RegexGolf)
- [Interactive learning walkthrough](https://regexlearn.com/)
- [Lookaheads & Lookbehinds Info](https://javascript.info/regexp-lookahead-lookbehind)


## My Comments

- [regex-basics.txt] looking for all words without any vouls: pattern = "\b[^aeiou\s]+\b" (\b for words boundaries, '^'to negate such chars and \s to also exclude the spaces)
find-all provides these 3 strings: 0123456789, dry, crypt

- [regex-groups.txt] looking at a specific pattern of 3 chars to be repeated elswhere in the same string: "(\d{3}).*\1"
note that \1 is holding the first group in parenthsys and looks for it elswhere as well*

- [regex-advanced.txt] 'look behind' - looking for all numbers that are preceded by a Dollar sign $: "(?<=\$)\d+(,\d+)?"
the group is for the 'possitive look behind': '?<=' which is regex feature preceded by $, grouped, w/ optional ',' w/ additional numbers
and we get all applicable values: 9 - 12 - 1,000 - 10,000 - 3 - 60 (without the preceded $ sign)
there's also a look ahead option

- [regex-advanced.txt] 'look ahead' - looking for all time values followed by 'pm' or 'am': "(\d+:)?\d* ?(?=pm|am)"
and we get all applicable values: 9 - 12 - 1,000 - 10,000 - 3 - 60 (without the folowed am|pm values): 9:30, 10, 1, 7:45, 11:20 , 11:35