# FOR and REPEAT UNTIL

Looping is bread and butter of software, but there's some parts of NextBASIC that catch me unawares, such as this:

```
10 FOR %i=0 TO 4
20   PRINT %i
30 NEXT %i
```

…will print 0…4 inclusive of 4.

However, this pattern looks similar, but the result is more aligned with what I expect with my day to day code:

```
10 %i=0
20 REPEAT
30   PRINT %i
40   %i=%i+1
50 REPEAT UNTIL %i=4
```

…will print 0…3 exclusive of 4 - because the `REPEAT` increments `%i` right before the check (by my own design).

Might be a good practise to stick to one loop type.
