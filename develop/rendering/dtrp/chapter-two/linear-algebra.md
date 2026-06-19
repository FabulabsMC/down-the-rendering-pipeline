---
title: Vectors and Matrices
description: A very concise explanation of mathematical concepts necessary in rendering.
authors:
  - sylv256
  - Kilip1000
---
## Matrices

A matrix is a grid of numbers with certain mathematical qualities that make them very useful for graphics programming.
Namely, a number of operations such as **addition**, **subtraction**, and **multiplication** may be performed on them.

A matrix can be used to store a number of numerical values in a variety of units, like spacial dimensions, when storing the position a minecraft block should be rendered.

All matrices have a width and a height.
TODO: Possibly mention application of matrix operations on PBR.
TODO: Possibly say a matrix may have any number of dimensions.

## Vectors

A vector is a geometric object with a direction and a length, it can be thought of as an arrow pointing from one location to another.
They may be added to another by aligning the toe of the first to the tip of the second, or vice versa.

A vector may be used to model the direction of a ray of light hitting a surface, and a vector operation may be used to model said ray bouncing of the surface.
Vectors may be expressed in a multitude of ways, some of which include:
  - An ordered list of numbers representing an arrow from the origin pointing to a multidimensional position
      - This means that a vector can be expressed as matrix with a width of 1 and a heigh corresponding to its number of dimensions
  - A length (often called magnitude) and a direction

TODO: Possibly mention more ways a matrix could be expressed
TODO: Maybe explain more vector operations or explain further that the result of vector addition is another vector from the toe of one to the tip of the other
TODO: rest of **introduction** and article
