# NTRU

The NTRU cryptosystem (NTRUEncrypt) is a post-quantum public key cryptosystem, developed by J.Hoffstein, J.Pipher and J.Silverman [1]. The system is naturally described using polynomial arihtmetic in the quotient rings  R = Z[x]/(x^N-1)  and Rq = Zq[x]/(x^N-1), for some modulus q. The private and the public key are polynomials in R and Rq, respectively. In practice, the private key has one of the following two forms.

(i) A pair (f,g), where f,g  are trinary polynomials (i.e. polynomials in R with coefficients in the set {-1,0,1}). 

(ii) A pair (1+pF,g), where F is product-form polynomial (i.e. F=F1F2+F3, with F1,F2,F3 trinary), g is trinary and p is a public parameter of the system. 

In addition, NTRUEncrypt is lattice-based cryptosystem, since the private key recovery problem can be formulated as a computational lattice problem on a special type of lattices, called NTRU lattices. Specifically, if the private key is of the form (i), then we have to solve a Shortest Vector Problem (SVP), to recover it. If it is of the form (ii), then we have to solve a Bounded Distence Decoding (BDD) problem.

The main attacks on the NTRUEncrypt private key are:

(1) Combinatorial attacks (Brute force, meet-in-the-middle, etc.)

(2) Lattice attacks (Lattice reduction and algorithms for the solution of SVP,CVP and BDD on the NTRU lattices)

(3) Hybrid attack (Combination of the above two types)


This repository contains a description of the NTRUEncrypt in SageMath. Also, it includes the code of the experiments about the running 
time of the hybrid attack and the GSA in NTRU lattices, which are mentioned in my Msc Thesis "The NTRU cryptosystem and attacks on the private key".
In particular, the repository contains the following folders.


1. NTRUEncrypt_in_SageMath

A description of the NTRU public key cryptosystem using SageMath for the operations in the rings R and Rq.



2. hybrid_attack_set_S

Includes the SageMath code of the experiment mentioned in the Remark 6.2.2 of my Msc Thesis. 



3. hybrid_attack_prob_p

Includes the SageMath code of the experiment mentioned in the Example 6.2.2 of my Msc Thesis for the calculation of the probability p of the hybrid attack. This probability is the probability p as it was presented in [2] and [3]. 



4. GSA_NTRU

Includes the fpylll code of the experiment mentioned in the Section 6.4 of my Msc Thesis, about the truth of GSA on NTRU lattices.



References

[1]  J. Hoffstein, J. Pipher and J.H. Silverman. NTRU: A ring-based public key cryptosystem. In Algorithmic Number Theory, volume 1453 of Lecture Notes in Computer Science, pages 267-288. Springer Berlin 1998.

[2] J. A. Buchmann, F. Gopfert, R. Player, and T. Wunderer. On the hardness of LWE with binary error: 
Revisiting the hybrid lattice-reduction and meet-in-the-middle attack. AFRICACRYPT 2016, volume 9646 of LectureNotes in Computer Science, pages 24 - 43. Springer, 2016.

[3]  T. Wunderer. Revisiting the hybrid attack: Improved analysis and refined security estimates. IACR Cryptology ePrint Archive, 2016:733, 2016.


