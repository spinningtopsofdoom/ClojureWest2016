!SLIDE

# Clojure Hash Maps:
## plenty of room at the bottom

&nbsp;
## @spinningtopsofdoom
## @2kliph

## @bendyworks

!SLIDE

## Building an alien space ship

- Avoiding the gray goo scenario when making nano machines
- What cup of tea is best to power your Infinite Improbability Drive (earl gray hot)
- How to make the spaceship bigger on the inside than on the outside

!SLIDE

## Talk about real alien technology

!SLIDE

![LISP Alien](../../images/lisp_alien_fancy.png)

!SLIDE

## Immutability: a cornerstone of functional programming

!SLIDE

## See it's used in

- Scala
- Elixir
- Haskell
- Clojure

!SLIDE

## Why immutable?

- Deeply nested heterogeneous data
- Send data off to another part of the code: fire and forget :)
- Fast delta diffing
  - E.g. React shouldComponentUpdate

!SLIDE

## There's always a catch
- Orders of magnitude slower
- Efficient implementations have constraints, like sortable keys,
  storing deltas in the data structure itself
  - Increasing cognitive overhead for developers

!SLIDE

## Hash Array Mapped Tries provide performance improvements

- 2 to 3 times slower for common operations
  - That's a lot better than an order of magnitude slower
- No constraints
    - Only need a hashable key
- Reduced cognitive overhead

!SLIDE

## Optimizing Hash-Array Mapped Tries for Fast and Lean Immutable JVM Collections
### by Michael J. Steindorfer and Jurgen J. Vinju

!SLIDE

## Compressed Hash-Array Mapped Prefix-tree

&nbsp;
## CHAMP

!SLIDE

# ClojureScript implementation

## https://github.com/bendyworks/lean-map

!SLIDE

## CHAMP gives you guaranteed Hash Map performance gains

- Iteration by 2x
- Equality checking by 10x to 100x

!SLIDE

## CHAMP trims your Hash Maps

!SLIDE center

![Wizard School](../../images/John_William_Waterhouse_-_The_Crystal_Ball.JPG)

!SLIDE

CHAMP makes Hash Maps more wieldy, making them both simpler and easier

Code size is two thirds the size of the original implementation
