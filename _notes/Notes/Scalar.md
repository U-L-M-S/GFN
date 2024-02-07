---
tags:
  - perl/variable/scalar
links: 
reference: "[[Perl]]"
path: Notes
created: 2023-09-11 16:26
modified: 2023-09-11 16:26
---
## Scalar 

^ea6205

*<mark style="background: #FFB8EBA6;">my</mark> <mark style="background: #FF5582A6;">$</mark> <mark style="background: #FFB86CA6;">variable_name</mark> = <mark style="background: #FFF3A3A6;">single valuer</mark>*
```perl
my $name = "Levi";
my $letter = 'U';
my $pi=3.14;
my $age = 69;
my $undefined = undef;
my $statement0 = False
my $reference = \$name; # it's a pointer 
```
>[!tip]  **statements**
>True or False.
>In Perl a function or a `if` will always return `False` by: *undef, 0, 0000000000, '0'*, ' '(empty).
>Everything else will `True` 

>[!warning] 
> Strings and numbers can not be determined
```perl
my $str1 = "4G";
my $str2 = "4H";

print $str1 . $str2;  # "4G4H"
print $str1 + $str2;  # "8" and 2 warnings
print $str1 eq $str2; # "" (empty string) == FALSE
print $str1 == $str2; # "1" (TRUE) and 2 warnings
```

In another words you **have** to use the correct operators.

numerical | < | > |<= | >= | == | != | <=> | + | * | 
-- | -- | -- | -- | -- | -- | -- | -- | -- | --| 
**String** | lt | gt | le | ge | eq | ne | cmp | . | x |