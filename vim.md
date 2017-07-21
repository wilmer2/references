# VIM References

## Normal Mode
```
q{letter} Record a macro
@{letter} Play a macro
@@        Repeat last macro
q{LETTER} Append to register
```

## Visual Mode
```
~   Swap case
u   Lowercase
U   Uppercase
```

## Commands
```
:read [file]  Insert from another file
:{range}
  ranges:
    {number}    The number of the line
    .           Current line
    $           Last line
    %           All lines
    ?{pattern}? Use pattern range
    +{n}        n lines below
    -{n}        n lines above
    '{letter}   use a mark
```
