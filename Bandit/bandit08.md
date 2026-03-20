## Level 8
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Requirements
- sort
- uniq

## Solution
```bash
# uniq command is used to filter out adjacent identical lines, and we use sort with it so sort the data so uniq command can filter out the duplicate lines

$ sort data.txt | uniq -u
