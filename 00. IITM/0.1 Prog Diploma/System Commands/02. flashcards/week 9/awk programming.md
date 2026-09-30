![[Pasted image 20260929222535.png]] What does this print?

bash

```bash
awk '{ print $3, $1 }' marks.txt
``` 
?
Department and Name

![[Pasted image 20260929222730.png]]  Write a one-liner that prints only the names of students whose marks are strictly between 60 and 90. ;; `awk 'BEGIN`