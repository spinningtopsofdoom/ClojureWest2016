!SLIDE

# First major improvement
##  Removes warts from Hash Map nodes

!SLIDE

# Sub Node references use nil as a "key" marker value

`[nil, <sub node reference>]`

!SLIDE

Turns into windows asking "Is it a Key Value pair or sub node?" for every operation

!SLIDE

## Adds incidental complexity
- Needs a flag for `nil` key and field for `nil` values
- Calls for optimized node (Array Node) just containing sub node references

!SLIDE

## Sub node references scattered throughout array

`[:foo, :bar, nil <sub node 1>, 3, 3, 6, 6, nil, <sub node 2>]`

!SLIDE

# Makes iteration a wiki walk

!SLIDE

- The Roman Empire was the post-**Roman Republic** period
- The Roman Republic was the period of **ancient Roman civilization** beginning with the
- Lots more link clicking...
- Awareness is the ability to perceive, to feel, or to be conscious of events, objects, thoughts, emotions, or sensory patterns

!SLIDE

## CHAMP fixes both warts by having Key Value pairs in the front of a node's array and the sub node references be in back

`[:foo, :bar, 3, 3, 6, 6, <sub node 1>, <sub node 2>]`

!SLIDE

## Decomplects metadata by splitting it into

- Key Value metadata
- Sub node reference metadata

!SLIDE

- Removes extra space taken up by nil marker values
- No incidental complexity (`nil` flag, Array Node)
- Iteration goes from a wiki walk to a linear scan

!SLIDE smbullets

## Current Hash Map iteration algorithm

- If `nil` flag is true return `[nil, <nil value>]`
- For normal nodes
  - If key is not `nil` then return the Key Value pair
  - Otherwise go to sub node and repeat
- For Array node
  - If element is `nil` continue
  - Otherwise go to sub node and repeat

!SLIDE

## CHAMP iteration algorithm

- Iterate though Key Value pairs
- Iterate through sub node(s) repeating step one

!SLIDE

# Two lines vs seven lines and no conditionals vs three
