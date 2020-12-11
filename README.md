# GRAPPA: Genome Rearrangements Analysis under Parsimony and other Phylogenetic Algorithms

GRAPPA is software for Genome Rearrangements Analysis under Parsimony
and other Phylogenetic Algorithms; the latest version can also be
found here.  Phylogenies derived from gene order data may prove
crucial in answering some fundamental open questions in biomolecular
evolution. Yet very few techniques are available for such phylogenetic
reconstructions. One method is breakpoint analysis, developed by
Blanchette and Sankoff for solving the ``breakpoint phylogeny.'' Our
earlier studies confirmed the usefulness of this approach, but also
found that BPAnalysis, the implementation developed by Sankoff and
Blanchette, was too slow to use on all but very small datasets. We
have re-implemented BPAnalysis using the principles of algorithmic
engineering. Our faster (by 2 to 3 orders of magnitude) and flexible
implementation allowed us to conduct studies on the characteristics of
breakpoint analysis, in terms of running time, quality, and
robustness, as well as to analyze datasets that had so far been
considered out of reach.  GRAPPA also provides the first linear-time
implementation of inversion distance. Hannenhalli and Pevzner gave the
first polynomial-time algorithm for computing the inversion distance
between two signed permutations, as part of the larger task of
determining the shortest sequence of inversions needed to transform
one permutation into the other. Their algorithm (restricted to
distance calculation) proceeds in two stages: in the first stage, the
overlap graph induced by the permutation is decomposed into connected
components, then in the second stage certain graph structures (hurdles
and others) are identified. Berman and Hannenhalli avoided the
explicit computation of the overlap graph and gave an O(nα (n))
algorithm, based on a Union-Find structure, to find its connected
components, where α is the inverse Ackerman function. Since for all
practical purposes α(n) is a constant no larger than four, this
algorithm has been the fastest practical algorithm to date. In this
code, we implement a new linear-time algorithm for computing the
connected components, which is more efficient than that of Berman and
Hannenhalli in both theory and practice. Our algorithm uses only a
stack and is very easy to implement.

References:

- B.M.E. Moret, S. Wyman, D.A. Bader, T. Warnow, M. Yan, "A New Implementation and Detailed Study of Breakpoint Analysis," presented at the Sixth Pacific Symposium on Biocomputing 2001 (PSB2001), pp. 583-594, Big Island, Hawaii, January 3-7, 2001.
- D.A. Bader, B. M.E. Moret, and M. Yan, "A Linear-Time Algorithm for Computing Inversion Distance Between Two Signed Permutations with an Experimental Study," Journal of Computational Biology, 8(5):483-491, October 2001.
- D.A. Bader, B. M.E. Moret, and L. Vawter, "Industrial Applications of High-Performance Computing for Phylogeny Reconstruction," SPIE ITCom: Commercial Applications for High-Performance Computing (SPIE ITCom2001), Denver, CO, SPIE Vol. 4528, pp. 159-168, August 21-22, 2001.

# Version 2.0

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation -- using version 2 (June 1991) of the
License or (at your option) any later version.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
General Public License for more details.

You should have received a copy of or a link to the GNU General Public
License along with this program; you can also write to the Free
Software Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA
02111-1307, USA.

GRAPPA is available as a gzipped tar file containing all source files
needed to compile an executable version. Documentation for this early
release is minimal (there is a README file and some online
help). GRAPPA changes quickly, so be sure to grab the latest release.

GRAPPA was featured in Access, the magazine of the NCSA/Alliance in
Vol. 14 (1) (Spring 2001). It is discussed at some length in

- Moret, B.M.E., Wyman, S., Bader, D.A., Warnow, T., and Yan, M., "A
new implementation and detailed study of breakpoint analysis,"
Proc. 6th Pacific Symp. on Biocomputing (PSB 2001), Hawaii, World
Scientific Pub. (2001), 583-594.

Its linear-time computation of inversion distance is presented in

- Bader, D.A., Moret, B.M.E., and Yan, M., "A linear-time algorithm
  for computing inversion distances between signed permutations with
  an experimental study," Proc. 7th Workshop on Algorithms and Data
  Structures (WADS 01), Providence (2001), Lecture Notes in Computer
  Science 2125, 365-376, Springer Verlag. Journal version appears in
  J. Comput. Biol. 8, 5 (2001), 483-491.

The improvements due to better bounding and new search ordering (the
layered method) are discussed in

- Moret, B.M.E., Tang, J., Wang, L.S., and Warnow, T., "Steps toward
  accurate reconstruction of phylogenies from gene-order data," to
  appear in J. Comput. Syst. Sci. (invited, special issue on
  computational biology), 2002.

while the improvements achieved through the use of true inversion
medians are documented in

- Moret, B.M.E., Siepel, A.C., Tang, J., and Liu, T., "Inversion
  medians outperform breakpoint medians in phylogeny reconstruction
  from gene-order data," Proc. 2nd Int'l Workshop on Algorithms in
  Bioinformatics (WABI'02), Rome (2002), to appear in Lecture Notes in
  Computer Science 2452, 2002.

which also contains references to the works of A. Caprara and of
A. Siepel, whose codes for the computation of true inversion medians
are included in this release.

The latest release is

<pre>
GRAPPA-2.0
from October 1, 2004.
Previous releases (1.6 and 1.03) are obsolete.

Authors (original):

    David A. Bader
    Bernard M.E. Moret
    Tandy Warnow
    Stacia K Wyman
    Mi Yan

Main contributors to version 1.6:

    Jijun Tang
    Adam C. Siepel
    Alberto Caprara

Main contributor to version 2.0:

    Jijun Tang

</pre>
