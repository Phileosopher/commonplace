
# What regular expression is

Obviously, it's a good idea to search inside text and numbers for things. A "regular expression" is the code to do that.

The syntax changes depending on the programming language, but we'll use JavaScript here. Here's some examples of what text you could look for:

- a - the letter "a"
- a|b - the letter "a" or "b"
- .a. - the letter "a" when there's anything before it and after it
- a/g - all instances of the letter "a" (outputted as an array)
- a+/g - all times that you see "a", "aa", "aaa", etc. (outputted as an array)
- a/i - the letter "a" or "A"
- [a-g] - any of the range from "a" through "g"
- [0-4] - any of the numbers 0 through 4
- ahem - the specific string "ahem" somewhere in the text
- ^ahem - the string "ahem" at the beginning of the text
- ahem$ - the string "ahem" at the end of the text
- aher*m - the string "ahem", but also "aherm" or "aherrm"
- aher?m - the string "ahem, but also "aherm"
- a{2,5} - the strings "aa", "aaa", "aaaa", or "aaaaa"
- \s - a space (" ") in the text
- \S - NOT a space in the text
- \w - any of a-z, A-Z, or 0-9
- \W - NOT a-z, A-Z, or 0-9
- \d - any of 0-9
- \D - anything that's NOT 0-9

Thus, you can slam them all together and create /^\w\s*.bla+h{,6}\W$/ that fulfills the following:

1. There's a letter or number at the beginning, followed by a possible space and at least another character.
2. The word "blah" is in there, but could be "blaaaahhhhhh", but not "blaahhhhhhh".
3. It has to end with a special character.

This is just the *beginning* of how elaborate a regular expression can get. It's terrifying to glance at, but not hard to understand if you take it letter-by-letter. Take notes if you have to.

## Lookaheads

One of the more fiddly and confusing components of regular expressions is a "lookahead". Think of the computer holding onto a specific letter:

- /abbazabba/

It will go through each letter, step by step, to find the match ("a","b","b","a","z"...)

Now, what if you want to search for that element, but with a somewhat unrelated thing elsewhere in that string? You'd normally have to have the computer zip ahead to find it. with lots of text in the middle.

Instead, you can have the computer literally "look ahead" while holding its place:

- /abbazabba(?=wammajamma)/

In the above situation, it'll first look for "abbazabba", then try to find "wammajamma" *anywhere* else in the string. This can be useful to satisfy certain conditions ([password](encryption.md) requirements, for example).

## Greedy/lazy

The type of data regex returns can be greedy (where it pulls from a wider range of data to get a return) or lazy (where it grabs the next available data).

- e.g., given the text `<em>hello world</em>`
- If you search <.+> (which is looking for "<", then 1 or more non-newline character, then "<"), your intuition would say that it's present twice.
- A greedy search (which is typically standard) will yield 1 match, from the first "<" to the last ">".
- A lazy search (i.e., <.+?>) will tell it to repeat as few times as possible, which will stop the matching and yield 2 results.
