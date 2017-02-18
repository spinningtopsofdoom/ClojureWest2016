!SLIDE

## Caveats
- Javascript version: addition: 8% slower; deletion: 10 - 20% slower
    - Compared to current ClojureScript version
- JVM version: comparable speed to HAMT
  - Used in [Rascal](http://www.rascal-mpl.org/) (Steindorfer & Vinju)
  - Christopher Grand has [ported CHAMP to Java using Clojure's hashing functions](https://gist.github.com/cgrand/ecab0e13d1e7ff64a2d2)

!SLIDE

## CHAMP improvements paves the way for future improvements
### CHAMP internals are much easier to work with and reason about

!SLIDE

## Two Future possibilities

- Merge and Diff operations could have greatly increased performance
- Similar to RRB Vectors for Vectors

!SLIDE

## Interesting work on merging

- Christopher Grand is investigating using CHAMP as a basis for confluent hash maps
    - Uses node metadata to mark transient / persistent nodes
    - Removes marker objects needed for addition and deletion
    - Makes CHAMP "confluent"


!SLIDE

# CHAMP is not as cool as working nanobots

!SLIDE

![LISP Alien](../../images/lisp_alien_fancy.png)

!SLIDE

## CHAMP shows Hash Maps have plenty of room at the bottom compared to original ClojureScript HAMT implementation

- 2x speed up for iteration
- 10 - 100x speed up for equality checking
- Lower memory overhead

!SLIDE

## For Peter the biggest win is making Hash Maps much easier to understand and implement

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
