# geometrism

<p align="center">
  <img src=""/>
</p>

Geometrism is a library of sequences for use with TidalCycles. The sequences are generally appropriated from the Online Encyclopedia of Integer Sequences (oeis). They are currently focused around 2 main geometry themes:

- FIBONACCI numbers, including various related sequences such as tribonacci numbers, Pisano sequences, etc.

- LATTICES, often coordinate sequences of polyhedra or chemical structures (ie silicon)

Many of these sequences are cut off near 20K; this is because the library was initially used for frequency mappings with the included SuperCollider synths (human hearing rarely exceeds 20K hertz).

An example pattern using the Geometrism library is expressed like so:
d1 $ f tetranacci # s "S"

where 'f' is frequency, 'S' is a sine wave synth, & 'tetranacci' runs the pattern '1 5 26 10 312 130 342 20 78 1560 120 130 84 1710 312 40 4912 390 6858 1560 4446 120 12166 260 1560 420 234 1710 280 1560 61568 80 1560 24560 17784 390 1368 34290 1092 1560 240 22230 162800 120 312 60830 103822 520'

Note that the above sequence exceeds 20K. Sequences such as these can be scaled by declaring a function

linlin x y a b = (+ a) . (* ((b-a)/(y-x))) . (subtract x)

Where x & y are the low & high ranges of the sequence, & a & b are the desirable scaled ranges. This allows the user to do something like this:

d1 $ linlin 1 162800 100 200 tetranacci # s "S"
