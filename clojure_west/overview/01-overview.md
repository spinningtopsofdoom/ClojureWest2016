!SLIDE

#Overview of Clojure Hash Maps

!SLIDE

#Clojure Hash Maps tree of nodes
##32 way branching factor

!SLIDE

#Each node comtains
## Array of Key Value pairs and references to lower level node (sub node references)
##Metadata tells the location of a key in the array

:foo is in slot 0 of array
3 is in slot 2 of array

[:foo :bar, 3 5, nil <sub node refence>]

!SLIDE

#Location of key in map is determined by hash
## Hash is chunked into groups of 5 bits

|00110|01100|11100|

## first five bits determine location in level 1
## next five bits determine location in level 2

## for collisions at one level go down check the next five bits at a lower level
