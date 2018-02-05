# Geometrism

<p align="center">
  <img src="https://user-images.githubusercontent.com/29079048/34967785-d45e2846-fa2a-11e7-8d49-e831c8faf5f0.png"/>
</p>

Geometrism is a library of sequences for use with TidalCycles, a mini-language of Haskell. The sequences are generally appropriated from the Online Encyclopedia of Integer Sequences (oeis). They are currently focused around 3 main geometry themes:

- FIBONACCI numbers. Including various related sequences such as tribonacci numbers, Pisano sequences, etc.

- LATTICES. Often coordinate sequences of polyhedra or chemical structures (ie silicon)

- FRACTALS

Each module has 3 different expressions, followed by a corresponding A, B, or C like so:
fibonacciA
fibonacciB
fibonacciC

'A' expressions are sequences ranging from 20 - 20K
'B' expressions are comma separated sequences
'C' expressions are sequences ranging from 1-10, & inserted inside the spread function in TidalCycles (< >) 

An example pattern using the Geometrism library is expressed like so:
d1 $ density fibonacciC $ f tetranacci # s "S"

where 'f' is frequency, 'S' is a sine wave synth, & 'tetranacci' runs the pattern '20 20 23 21 58 35 61 22 29 211 34 35 30 229 58 24 622 67 861 211 565 34 1512 51 211 71 48 229 54 211 7575 29 211 3034 2202 67 187 4228 153 211 49 2748 20000 34 58 7485 12761 83'


