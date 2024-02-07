---
tags:
  - perl/variable/array
links: 
reference: "[[Perl]]"
path: Notes
created: 2023-09-11 17:21
modified: 2023-09-11 17:21
---
## Array 
*<mark style="background: #FFB8EBA6;">my</mark> <mark style="background: #FF5582A6;">@</mark> <mark style="background: #FFB86CA6;">array_name</mark> = <mark style="background: #FFF3A3A6;">("valuer1", "valuer2", "valuer3", 3.14, 69, undef) </mark>*

```perl
use strict;
use warnings;

# ARRAYS
my @arr0 = ("string1", "string2", "string3", "string2");
my @arr1 = (3.14, "string2", undef, "string2");
my $thing = "I'm just a thing";
my @arr2 = ("Hello", $thing, undef, "string2", 69);

# QW ARRAYS
my @quoteWord = qw(each of these words is an array);

# Elements
my $element1 = $arr0[0]; 
my $element2 = $arr1[0]; 
my $element3 = $quoteWord[3]; 

print $element1; # "string1"
print $element2; # 3.14
print $element3; # words

my @anotherArray = ('Uwe', 'Karl');
# PUSH

push(@anotherArray, 'Rolf');
printf(@anotherArray); # 'UweKarlRolf'
# POP 

my $lastValuer = pop(@anotherArray); # Remove last valuer of array and return into $lastValuer 

# UNSHIFT
unshift(@anotherArray, 'Anna'); # Same as PUSH but set Anna in the first index

# SHIFT
my $firstValuer = shift(@anotherArray); # Same as POP but the first valuer

# push    -> hinten dran
# pop     -> hinten weg
# shift   -> vorne weg
# unshift -> vorne dran


**REFERENCE**
my $nestedArrayRef = [ [ 0, 'A' ], [ 1, 'B'], 2, 'C' ];
printf "My nested array: %s\n", $nestedArrayRef; # My nested array: ARRAY(0x563b820475d8)

print Dumper $nestedArrayRef, { label => 'Nested Array Ref' };
# ╔═════════ Nested Array Ref ══[ $nestedArrayRef ]══[ main | ./test.pl +8 ]══
#║[
#║    [0] [
#║            [0] 0,
#║            [1] "A"
#║        ],
#║    [1] [
#║            [0] 1,
#║            [1] "B"
#║        ],
#║    [2] 2,
#║    [3] "C"
#║]
#╚═════════ Nested Array Ref


# From a reference $nestedArrayRef:
my $thirdValue = $nestedArrayRef->[2];

my $nestedArrayRef = [ [ 0, 'A' ], [ 1, 'B'], 2, 'C' ];
my @mixedArray = (3, 'A', 'Harald', 32323.54);

# From a reference $nestedArrayRef:
my $thirdValue = $nestedArrayRef->[2];
my $fourthValue = $mixedArray[3];

#print Dumper [ $fourthValue, $thirdValue ];
#╔═════════[ main | ./test.pl +15 ]══
#║[
#║    [0] 32323.54,
#║    [1] 2
#║]
#╚═════════ 

# Push a value to $nestedArrayRef
push($nestedArrayRef->@*, 'SomeValue');
# Shift
shift($nestedArrayRef->@*);

print Dumper $nestedArrayRef, { label => 'After push' };


# LENGTH
print scalar @quoteWord; # 8

#ODER

my $length = @arr2;
print $length; # 5

# Reference / Pointer
my $nestedArrayRef = [[0, 'A'], [1, 'B'], 2 'C'];
printf

```

>[!warning] switching between Array and ArrayReference
>**Always** use `->@*`  