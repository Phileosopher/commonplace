
# Awk summarized

Awk treats each line of text as a record and splits it into fields, with whitespace being the default delimiter.

- In practice, it can visualize as what you observe in a [spreadsheet](database.md).
- This is different than standard [regular expression](cs-langs-specific-regex.md) or grep because it asks what matches inside an abstracted column instead of whether a line matches conditions.

Like [bash](cs-cli-specific-bash.md), options and arguments are separated by spaces.

"print" outputs, but "printf" makes a clean tabular output.

## Syntax

```awk
BEGIN{actions} #will run time before reading the input data

/pattern or condition/ {actions} #will run for each line of input

END{actions} #will run after processing the input
```
