A simple perl script to generate the expected site frequency spectrum for a sample of size n for a population mutation rate of theta. 
I am no longer entirely sure why you would want to do this.  Requires Math::BigFloat

Run as "ewens.pl theta n", where n is the sample size, and theta the populaiton mutation rate (4Nμ ).  Generates a file "ewens.out".

Example: run "ewens.pl 5 10" and the output file should read:

3.55
1.39
0.66
0.30
0.10
0
0
0
0
0

Which says that one expects a sample of size 10 with a theta of 5 to have 6 allelesi (the sum of all bins). 
Further, it says that roughly 3-4 alleles are expected to be singletons, 1-2 doubletons, and less than 1 allele is expected to be at higher frequencies.

Note that this script outputs the expectation, not a distribution or confidence interval, and assumes a neutral population in demographic equilibrium following the infinite alleles model of mutation.

Note that this is also a very slow way of doing this. 
