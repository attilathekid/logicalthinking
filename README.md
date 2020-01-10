# logicalthinking
A simple bot to understand and evaluate arguments in symbolic logic

The Algorithm

The central idea behind general argument evaluation is that each premise can be thought of not only as a statement that
can be true or false but also as the set of worlds in which it holds. A claim refers to the set of conditions under which it is true.

Following this interpretation, an argument has three components: (1) a domain, the set of worlds in which it makes sense and is intended to apply, defined here by a set of sentential variables which can be either true or false, (2) a set of premises, each of which is a set of possible worlds (a space) in which a certain constraint holds, and (3) a conclusion space, or the set of possible worlds allowed by the conclusion. An argument is valid if and only if the intersection space---the intersection of all of the premise spaces---is a subset of the conclusion space.

Visually, this is easiest to represent as a Venn diagram, with the circles representing different sets of possible worlds. Here, two circles represent the spaces described by premises A and B while C represents the space which must be contained by the conclusion for the argument to be valid.

-------------------------------------------------------------

             ---------------------------
           /                             \
         / .     All possible worlds      \
        |                                  |
        | .   ---------      ---------     |
        | .  / .         \  /         \    |
        | . /             /\           \   |
        | . | .   A .   | C |     B     |  |
        | . \            \ /            /  |
        | .  \ .         / \ .         / . |
        | .   ---------      ---------     /
         \                                /
          \                              /
           -----------------------------
           
-------------------------------------------------------------

The Code

The code works by calculating the premise space for each premise and taking the intersection---creating the intersection space---and then checking that this space is contained by the conclusion space by making sure that the conclusion holds in every possible world contained by the intersection space.
