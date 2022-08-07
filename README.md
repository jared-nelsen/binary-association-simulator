# Binary Association Simulator
# TODO

- Binary Associator as abstracted to contain Transformations which hold vectors
 of transforms.

## Order of development

        1. Data
        2. Evaluation
        3. Mutation
        4. Crossover
        5. GA algorithm

NEXT: TOPO Sort algorithm 

# Data

  Data is recorded in this form:

       -Vector of Frames
         - Vector of Pixels
           - Vector of Int 8s

# Selection

Selection will be tournament based. Tournaments will need to be allocated. Then they can
be sorted and the winners taken as the rightmost. Selected populations should be double
the size of the output population that will be fed into crossover. This is a good
opportunity for paralellization.

# Mutation

  - Change transform operation
  - Change transform bit operation index
  - Add a transform
    - Random amount of connections
    - Randomly link up new connections
  - Remove a transform
    - Randomly remove a transform and its outgoing connections
    - Remove dangling connections and transforms
    - Skip removing IO transforms
  - Add a random cross section of transformszs
    - Link up randomly
  - Remove a random cross section of transforms
    - Remove N randomly selected transforms and their connection
    - Remove dangling connections and transforms
  - Add a connection
    - Random start
    - Random end
  - Remove a connection
    - Random removal of a connection
    - Remove dangling connections and transforms

# Crossover

  - Weaker parent gets consolidate into stronger parent
  - Select N transforms and their destinations transforms
    - Omit IO transforms
  - Add these N transforms and their destination transforms to the stronger parent
  - Randomly link up

# Evaluation

  - Feed Forward
  - Evaluation against data

# Data

  - Generate
  - Read from file
  - Formatted for simulation
  - Loaded at simulation start time