# matchmask
 Matches words from stdin to Hashcat masks from a file argument.

 ```
$ cat masks.txt
?u?l?l?l?u?u?l?u?d?u?u?d?d?d?s

$ echo 'ThisISaT3ST123!' | matchmask masks.txt
ThisISaT3ST123!
 ```

 ```
$ cat masks.txt
?u?l?l?l?u?u?l?u?d?u?u?d?d?d?s
?l?l?l?l

$ cat words.txt
ThisISaT3ST123!
test
bark
tree
Tree
Bark
NoMatch123

$ cat words.txt | matchmask masks.txt
ThisISaT3ST123!
test
bark
tree

```
Install
```
go install -v github.com/jakewnuk/matchmask@latest
```
Use with [maskcat](https://github.com/jakewnuk/maskcat) for a workflow.
