# logicalthinking
A simple interpreter to understand and evaluate arguments in symbolic logic

The basic insight is to think of each statement in the argument in terms of the possible worlds in which it is true. An argument is valid if the set of possible worlds in which the conclusion holds is a superset of the set of possible worlds in which the premises hold. The algorithm works by finding a list of all possible worlds and then cutting this down with each additional premise. At the end, if the remaining premises are a subset of the conclusion space, then the argument is valid.

Unfortunately, this is an NP-hard problem, and so computation time and memory consumption are both O(2^n) in the number of sentential variables. If I cared, I could probably cut down the memory consumption to something more workable, but that is kind of low on my todo list.
