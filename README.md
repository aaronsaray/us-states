# US State Utilities

This library adds in the US states in various formats. Why re-invent the
wheel?

## Installation

Install with composer

`composer require aaronsaray/us-states`

## Requirements

* PHP 7.1+

## Usage

This is just about providing the US states. You will end up using them
in your own application in custom ways. For example, you might pass the
results of abbreviations to the `Rule::in` in Laravel- like this:

```php
return [
    'state' => [
        'required',
        Rule::in(USStates::abbreviations())
    ]
];
```

All abbreviations are capitalized and all state names are proper noun
capitalized.

### Functions

All of these examples are assuming you're using the library in your
scope doing something like this:

`use AaronSaray\USStates\USStates;`

`USStates::abbreviations()` returns an array of capitalized
abbreviations only.

`USStates::namesKeyedByAbbreviations()` returns a key of abbreviation
and a value of the state name.

`USStates::abbreviationsKeyedByNames()` returns a key of state name and
a value of the abbreviation.

## Todo

- [ ] figure out if there is some sort of unit test that makes sense for
    this package

## Credits

This package is created and maintained by [Aaron Saray](https://github.com/aaronsaray) 
