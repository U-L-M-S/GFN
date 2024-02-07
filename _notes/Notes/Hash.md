---
tags:
  - perl/variable/hash
links: 
reference: "[[Perl]]"
path: Notes
created: 2023-09-11 18:37
modified: 2023-09-11 18:37
---
## Hash 
*<mark style="background: #FFB8EBA6;">my</mark> <mark style="background: #FF5582A6;">%</mark> <mark style="background: #FFB86CA6;">hash_name</mark> = <mark style="background: #FFF3A3A6;">(key1 =>"valuer2", key2 => "3.14",  key3 => "69") </mark>*

```perl
use strict;
use warnings;

use Data::Dumper;

my %countries = (
	england => "small",
	austria => "large",
	germany => "medium",
);

my $country = $countries{"england"};
print $country; # small

#add 
$countries{"Brazil"} = "super large";

#remove
delete $countries{"austria"};

print Dumper(\%countries);

```

```perl
#!/usr/bin/perl -w

use strict;
use warnings;

use AKLib::Utils::Dumper;

# A simple Hash
my %languageMapping = (
	'de' => 'Germanisch',
	'en' => 'Englisch',
);

my ($lang, $book) = @ARGV;

$languageMapping{fr} = 'French';
#delete $languageMapping{de};

if(!$languageMapping{$lang}) {
	die("Ne, gibts nicht digger.\n");
}

printf "%s is: %s\n", $lang, $languageMapping{$lang};

my @allKeysInLanguageMapping = sort keys(%languageMapping);
print Dumper \@allKeysInLanguageMapping;

print Dumper [ sort values(%languageMapping) ];

# Hash Reference
my $bookMappings = {
	'Game of Thrones' => 'George R.R. Martin',
	'Project Hail Mary' => 'Ernest Cline',
	'Foundation' => 'Isaac Asimov',
};

$bookMappings->{'The Cleaner, the Cat and the Space Station'} = 'I don\'t know';

delete $bookMappings->{'Project Hail Mary'};

printf "Author of %s is %s\n", $book, $bookMappings->{$book};
print Dumper $bookMappings;

```