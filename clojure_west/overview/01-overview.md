!SLIDE

# Overview of Clojure Hash Maps

!SLIDE

# Clojure Hash Maps tree of nodes
## 32 way branching factor

!SLIDE

# Inside a node

`[:foo :bar, 3 5, nil <sub node refence>]`

## Metadata tells the location of a key in the array

!SLIDE

## Location of key in map is determined by hash
### Hash is chunked into groups of 5 bits

`:foo |6|23|15|7|30|2|`

`[6]`

`[X] [23]`

`[X] [15] [X] [X]`
