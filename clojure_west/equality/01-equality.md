!SLIDE

# Clojure Puzzler
## Sloppy Cleaning

!SLIDE small

    @@@ clojure
    (def base-map (hash-map)) ;; {}
    (def same-map
         (as-> base-map m
          (reduce #(assoc %1 %2 0) m (range 1000000))
          (reduce #(dissoc %1 %2) m (range 1000000)))) ;; {}
    (= base-map same-map) ;; true
    (time (into {} base-map)) ;; 140 microseconds
    (time (into {} same-map)) ;; ??? microseconds

!SLIDE

- A) 140 microseconds
- B) 280 microseconds
- C) 1400 microseconds
- D) 14000 microseconds
- E) 31000 microseconds

!SLIDE

## E) 31000 microseconds

!SLIDE

# Current Delete Algorithm

!SLIDE

![Node internals](../../images/naive-delete.svg)

!SLIDE

# This leads to

!SLIDE

![Node internals](../../images/example-base-delete.svg)

!SLIDE

![Node internals](../../images/example-sloppy-delete.svg)


!SLIDE

# CHAMP Delete Algorithm

!SLIDE

![Node internals](../../images/champ-delete-one.svg)

!SLIDE

![Node internals](../../images/champ-delete-two.svg)

!SLIDE

## Lowers memory overhead that occurs from `dissoc`

!SLIDE bullets incremental transition=fade

- So what? This only really matters in pathological cases
- Equal CHAMP maps have the exact same layout in memory
- We don't have to compare all Key Values we can compare nodes

!SLIDE

## Equality check is now O(log n) vs O(n) leading to 100x performance improvement
### This is when maps share structure

!SLIDE

## We still get 10x performance boost for maps don't share any structure

- Only Comparing two arrays
- Current comparison has overhead due to Clojure abstractions (sequences and lookup)
