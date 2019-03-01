# weighted-rng
Generates random values with a specific hamming weight.

A random 64-bit value (r) is drawn from /dev/urandom. If r does not have the specified weight, another value between 0-63 inclusive is drawn, which selects a bit position of r. If the weight of r is less than specified, the selected bit is or'ed with 1. If the weight of r is greater than specified, it is and'ed with 0. This process repeats until r has the specified weight.
