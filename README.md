# lua-toys

A small collection of GPL3-licensed toy programs created to help me
learn Lua.  All of the toys are presented as shell scripts that can be
run from the command line, so no need to explicitly invoke Lua.

## `gol`

An implementation of Conway's Game of Life.  Accepts pattern files
depicting a starting state with `_` representing a dead cell and `#`
representing a live cell (see the example files in `gol_patterns/`)
and generates a given number of generations.

`gol` accepts two switches: `-p` tells `gol` to print the results to
the terminal, whereas `-i` tells it to generate an animated GIF,
`<INPUT_FILE>.gif`.  Note that `-i` is dependent upon ImageMagick and
gifsicle being installed.

**Example usage **(print the first 30 generations of `tumbler.gol` to
the terminal)**:**

`gol -p gol_patterns/tumbler.gol 30`

## `quine`

A Quine.  Prints its own source code.

**Example usage:**

`quine`

## `rekt`

A rektangle generator, in respose to [this
post](https://www.reddit.com/r/dailyprogrammer/comments/4tetif/20160718_challenge_276_easy_recktangles/)
on
[r/dailyprogrammer](https://www.reddit.com/r/dailyprogrammer).
Accepts a string, a width and a height, and generates a rektangle of
those dimensions.

**Example usage:**

`rekt REKT 4 3`

Output:

    R E K T K E R E K T K E R 
    
    E     K     E     K     E 
    
    K     E     K     E     K 
    
    T K E R E K T K E R E K T 
    
    K     E     K     E     K 
    
    E     K     E     K     E 
    
    R E K T K E R E K T K E R 
    
    E     K     E     K     E 
    
    K     E     K     E     K 
    
    T K E R E K T K E R E K T 
