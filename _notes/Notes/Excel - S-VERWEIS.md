---
tags:
  - sae
links: 
reference: 
path: Notes
created: 2023-10-13 16:06
modified: 2023-10-13 16:06
---
## Excel - S-VERWEIS 
>Tabellen vergleichen in Excel.

```Excel
=SVERWEIS(valuerToBeAssociated,matrix,indexMatrix,valuersSorted)
```
- valuerToBeAssociated = Valuer that will be compared with the other valuers in the matrix.

- matrix = matrix used to get the valuers from.
- indexMatrix = specific which column of the matrix you want to extract the valuer.
- specific with a `1` or `0` if the valuers are sorted or not.

**OR**

```
Fx -> nach "SVERWEIS" suchen
```

![[Pasted image 20231013161544.png]]

|         |      |      |         |          |             |
| ------- | ---- | ---- | ------- | -------- | ----------- |
|         | KA 1 | KA 2 | Endnote | Gerundet | In Worten   |
| Deutsch | 4    | 4    | 4       | 4        | =SVERWEIS(E3;$K$9:$L$14;2;1) |
| Mathe   | 4    | 5    | 4,5     | 5        | =SVERWEIS(E4;$K$9:$L$14;2;1)  |
| English | 4    | 4    | 4       | 4        | =SVERWEIS(E5;$K$9:$L$14;2;1) |
| SAE     | 5    | 6    | 5,5     | 6        | =SVERWEIS(E6;$K$9:$L$14;2;1)    |
| ITS     | 4    | 4    | 4       | 4        | =SVERWEIS(E7;$K$9:$L$14;2;1) |
| WK      | 4    | 4    | 4       | 4        | =SVERWEIS(E8;$K$9:$L$14;2;1) |

|  -   |      -        |
| --- | ------------ |
| 1   | Sehr Gut     |
| 2   | Gut          |
| 3   | Befriedigend |
| 4   | Ausreichend  |
| 5   | Mangelhaft   |
| 6   | Schlecht     |

___

![[Pasted image 20231013164100.png]]

>[!important] 
>Do not forget to use [[Excel - $]]  to fix the columns and rows. 

