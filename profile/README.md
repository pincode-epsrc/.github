# PINCODE

Pooling INference and COmbining Distributions Exactly (PINCODE) is a £1 million EPSRC responsive mode grant, run by

- [Gareth Roberts](https://warwick.ac.uk/fac/sci/statistics/staff/academic-research/roberts/), University of Warwick ([EP/X028119/1](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/X028119/1))
- [Louis Aslett](https://www.louisaslett.com/), Durham University ([EP/X028100/1](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/X028100/1))
- [Murray Pollock](https://www.ncl.ac.uk/maths-physics/people/profile/murraypollock.html), Newcastle University ([EP/X028712/1](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/X028712/1))
- [Hongsheng Dai](https://www.ncl.ac.uk/maths-physics/people/profile/hongshengdai.html), Newcastle University ([EP/X027872/1](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/X027872/1))

The postdoctoral research associates on the project are

- [Shenggang Hu](https://warwick.ac.uk/fac/sci/statistics/staff/academic-research/hu/), University of Warwick
- A second PDRA is being recruited to be based at Newcastle University

### Grant Summary

While likelihood-based statistics and in particular the Bayesian paradigm represent the gold standards for theoretical underpinnings and uncertainty qualification in many contexts, implementing Bayesian methods can often be challenging, particularly in contexts where data is stored on a collection of disjoint servers and cannot be combined.
This situation is becoming increasing common, for instance in the big data context where storing all data on a single server is not technical feasible, or where privacy constraints preclude the sharing of individual shards of data.
One application which particularly motivates our work involves inference for rare diseases present in different European countries which cannot share data for confidentiality reasons, but where there is a desire to carry out inference based on the entire data set across all countries.

It is reasonable to assume that we can obtain the posterior distribution based just on the data from any one individual server, and that samples from this distribution (which we term a sub-posterior distribution) can be readily obtained, for example through some kind of MCMC approach.
Thus the problem reduces to that of generating samples from the product of densities from which we can individually sample.
This project will develop a novel approach to this problem.
Unlike existing techniques, it is not based on approximation or asymptotic justification.
In two proof of concept papers, Dai, Pollock and Roberts (2019, 2021) we have developed two closely related approaches: Monte Carlo Fusion (MCF) and Bayesian Fusion (BF).
These methods have many promising properties in terms of accuracy and robustness to inconsistency between sub posteriors.
However these methods are not scalable to very large problems and are restricted to the setting where all sub-posteriors describe distributions on the same data parameter sets.
In addition, neither MCF nor BF can be applied directly to data subject to privacy constraints.
The aims of this project will be to develop a robust scalable and accessible fusion methodology suitable for distributed inference in the variety of contexts described above.

Within the privacy context, we shall incorporate the use of homomorphic secret sharing (HSS), a simple multi-party information theoretically secure encryption technique which can be used to securely carry out arithmetic combinations of summaries from multiple parties which each individually do not wish to reveal their summary to the other parties.
Whilst we cannot use HSS directly to solve the fusion problem under confidentiality constraints (the so called ConFusion problem), we intend to use the technique in novel ways within the MCF and BF algorithms to solve the problem.

PINCODE will first develop a general framework for fusion methods based on the stochastic simulation of coalescing Markov processes with the property that their common coalesced value comes from the combined posterior distribution.
Considerable effort will go into the computational efficiency of these constructions with an eye to optimising scalability in data size, the number of distributed servers, dimensionality of the parameter set as well as robustness to sub-posterior heterogeneity.
We shall also consider principled approximations of these algorithms and provide provable accuracy guarantees for these methods. The methodology we consider will be widely applicable.
One targeted application will involve close collaboration with the FAIRVASC initiative (a Horizon 2020 project to borrow strength between distributed data sets for rare diseases in different European countries).
A further direction will involve the incorporation of fusion methodology to provide exact ABC methods.
There will be a strong emphasis within our project on software development for wide-ranging and effective dissemination.
