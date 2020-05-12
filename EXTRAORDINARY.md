<h1 align="center">Extra bash bible</h1> <p
align="center">An extension of pure bash bible.</p>

## Copy a dir include all subdirectories

```sh
cp -r /root/.android /opt/.android
```

## Match whole word

```sh
grep -w target
```

## Print a count of the lines that match a pattern

```sh
grep -c pattern
```

## Print out all the lines that do not match one pattern

**Example Usage:**
```sh
# filter pattern 
grep -v pattern
```

## Execute a command with a time limit

**Example Usage:**
```sh
# timeout sends TERM signal after the 10 seconds. If cmd didn't respond to TERM 
# (e.g. it could block the TERM signal) then timeout sends KILL signal after 5 more seconds.
timeout -k 5 10 cmd
```

## Sort file or context
| Expression       | Value  | What does it do? |
| ----------       | ------ | ---------------- |
| `sort -n`        | `file` | Sort a file numerically.
| `sort -t SEP`    | `file` | Use the provided separator to identify the fields.
| `sort -k POS`    | `file` | Sort on a certain column(sorting key).

Without the “-k” option, the sorting is performed using the entire line. The default separator for fields is the space character. The -t option can be used to change the separator.

You can also specify a more complex -k option. The complete positional argument looks like this:

`-k POS1,POS2`  
...where POS1 is the starting field position, and POS2 is the ending field position. Each field position, in turn, is defined as:

`F.C`  
...where F is the field number and C is the character within that field to begin the sort comparison.

**Example Usage:**  
So, let's say our input file data.txt contains the following data:  
developer_7  
developer_2  
developer_3  

We want to sort this file based on only the number after underline, like this:
```sh
sort -k 1.11
# set new seperater _, and specify the second field as the sort key 
sort -t_ -k 2
```
