---
tags:
  - perl/variable/list
links: 
reference: "[[Perl]]"
path: Notes
created: 2023-09-11 19:14
modified: 2023-09-11 19:14
---
## List 
 *<mark style="background: #FFF3A3A6;">("key1", "valuer2", "key2", "3.14",  "key3", "69") </mark>*
 *<mark style="background: #FFF3A3A6;">("key1" =>"valuer2", "key2" => "3.14",  "key3" => "69") </mark>*

Even if the Lists look like a mix of [[Array]]  and [[Hash]]. They are **NOT** a variable and in this way they don't have a [[sigil]].

```perl
use strict;
use warnings;

# Array + List
my @array = (
	"apples",
	"bananas",
	(
	    "inner",
	    "list",
		"several",
		"entries",
	),
	"cherries",
);

print $array[0]; # "apples"
print $array[1]; # "bananas"
print $array[2]; # "inner"
print $array[3]; # "list"
print $array[4]; # "several"
print $array[5]; # "entries"
print $array[6]; # "cherries"

# Hash + List 
my %hash = (
	"beer" => "good",
	"bananas" => (
		"green"  => "wait",
		"yellow" => "eat",
	),
);

# The above raises a warning because the hash was declared using a 7-element list

print $hash{"beer"};    # "good"
print $hash{"bananas"}; # "green"
print $hash{"wait"};    # "yellow";
print $hash{"eat"};     # undef, so prints "" and raises a warning

```

>[!important] 
>In another words lists become a part of the [[Array]] and [[Hash]].