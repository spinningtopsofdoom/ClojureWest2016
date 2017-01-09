!SLIDE

## Caveats
- Currently slower compared to HAMT adding 8% and deletion 10 - 20% slower
- This is JavaScript version (not JVM)
- JVM version has comparable speeds to HAMT

!SLIDE

## CHAMP improvements paves the way for future improvements
### CHAMP internals are much easier to work with and reason about

!SLIDE

## Two Future possibilities

- Merge and Diff operations could have greatly increased performance
- Similar to RRB Vectors for Vectors

!SLIDE

# CHAMP is not as cool as working nanobots

!SLIDE

![LISP Alien](../../images/lisp_alien_fancy.png)

!SLIDE

## CHAMP shows Hash Maps have plenty of room at the bottom

- 2x perf for iteration
- 10 - 100x perf for equality checking
- Lower memory overhead

!SLIDE

## For Peter biggest win is making Hash Maps much easier to understand and implement

!SLIDE

## Clojure Hash Maps is one of Clojure's best exports

- Scala (base hash map)
- Elixir (base hash map)
- Haskell (unordered-containers)
- Ruby (hamster)
- JavaScript (immutable.js)

!SLIDE smbullets

## Thanks

* Bendyworks for supporting our work on this
* Michael J. Steindorfer and Jurgen J. Vinju for the CHAMP Paper
* Zach Tellman for writing Collection Check
* Martin Klepsch for porting Collection Check to ClojureScript
* Nicolás Berger for helping Peter setup test harness
* David Nolen for perf and profiling suggestions

!SLIDE

# Fin

!SLIDE

# Questions?
