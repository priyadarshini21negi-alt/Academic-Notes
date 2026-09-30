![[Pasted image 20260929221954.png]]

`$0` is the whole line, `$1` the first field, `$2` the second, and so on. `NF` is the _number_ of fields, so `$NF` is the last field.



`NR` is the running count of records read so far (it's the line number, and in `END` it holds the total).


### example codes, 
![[Pasted image 20260929222359.png]]`print $1, $2` puts the output separator (a space) between them, while `print $1 $2` _concatenates_ with nothing in between. The comma matters. 

