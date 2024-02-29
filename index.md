
## Brief Bio

In June 2022 I joined the [Department of Computer Science and Engineering (CSE) at THE Ohio State University](https://cse.osu.edu/) as an Assistant Professor.
Prior to this I was an Assistant Professor in the [School of Computer Science at the University of Oklahoma (OU)](https://www.ou.edu/coe/cs).


## Research Interests

All of my research falls within the broad area of systems, and most of it within the sub-areas of Programming Languages and High Performance Computing (HPC). You can find OSU in [CSRankings](https://csrankings.org/#/index?hpc&plan&us). My research leverages programming languages and compilers as vehicles to achieve high-performance on modern heterogeneous and complex architectures. To achieve this goal, I like to find synergies among these areas, the underlying architecture as well as domain and algorithmic knowledge.

- Polyhedral compilation
- High-performance computing
- Domain-specific computing
- Quantum computing
- Automatic parallelization for data-flow and task-parallel run-times


## Funding

I'm currently externally funded by a PPoSS Large collaborative grant (Award Number 2234376) (Thank you NSF!), and I'm looking for students. If you are interested in my research, please see below.


## Publications

This is a sub-selection of my research articles in reverse chronological order (most recent at the top). You can find the complete list in my [DBLP](https://dblp.org/pers/k/Kong:Martin.html) and in my [Google Scholar](https://scholar.google.com/citations?user=A08cGJAAAAAJ&hl=en) profile. Next to each article you will find an informal summary of the paper's main contribution.

[*Energy-Aware Tile Size Selection for Affine Programs on GPUs*](TBD) 
Malith Jayaweera, Martin Kong, Yanzhi Wang, David Kaeli.
In *International Code Generation and Optimization (CGO'24)*.
<details>
  Approach to selecting tile sizes for affine computations to be executed on GPUs. Tile sizes are selected to maximize inter-thread intra-SM data sharing instead of maximizing parallelism (i.e. number of threads) or maximizing intra-thread locality. Our approach restricts the liveness of data tiles in cache to achieve energy improvements of up to 6x. Our formulation, implemented and solved using the Z3 SMT solver, also takes into account the mapping of array references to different types of GPU memories (Shared-Memory, L1 and L2 cache) and several GPU hardware limits to maximmize resource usage while also aiming to minimize energy consumption and throughput. 
</details>

[*Automatic Generation of Distributed-Memory Mappings for Tensor Computations*](https://dl.acm.org/doi/10.1145/3581784.3607096)
Martin Kong, Raneem Abu Yosef, Atanas Rountev and P. Sadayappan.
In *The International Conference for High Performance Computing, Networking, Storage, and Analysis (SC’23)*.
<details>
  A novel non-linear formulation to partition and map data and computations of tensor programs. Solutions to the formulation, found with the Z3 SMT solver, are used to generate efficient MPI code capable of making external library calls for local computations.
</details>

[*QRANE: Lifting QASM Programs to an Affine IR.*](https://dl.acm.org/doi/10.1145/3497776.3517775)
Blake Gerard, Tobias Grossser, Martin Kong in ACM SIGPLAN 2022 International Conference on Compiler Construction (CC'22),
2022
<details>
  <summary> Summary </summary>
  Automatic delinearization techniques to reconstruct the affine/polyhedral IR from a quantum assembly program.
</details>


[*On the Impact of Affine Loop Transformations in Qubit Allocation.*](https://dl.acm.org/doi/10.1145/3465409)
Martin Kong in
ACM Transactions on Quantum Computing (TQC),
2021
<details>
  <summary> Summary </summary>
  A high-level language to express quantum programs meeting the requirements of the polyhedral model; Exploration of off-the-shelf loop transformations on affine quantum circuits.
</details>

[*OCC: An Automated End-to-End Machine Learning Optimizing Compiler for Computing-In-Memory*](https://ieeexplore.ieee.org/abstract/document/9502921/)
Adam Siemieniuk, Lorenzo Chelini, Asif Ali Khan, Jeronimo Castrillon, Andi Drebes, Henk Corporaal, Tobias Grosser, Martin Kong
in EEE Transactions on Computer-Aided Design of Integrated Circuits and Systems,
2021
<details>
  <summary> Summary </summary>
  We propose a novel ML optimization framework for CIM (memristor crossbar-based) accelerators. We leverage the new MLIR pipepline and propose crossbar specific transformations to improve application performance and crossbar lifetime.
</details>

[*Tile Size Selection of Affine Programs for GPGPUs using Polyhedral Cross-Compilation.*](https://dl.acm.org/doi/abs/10.1145/3447818.3460369)
Khaled Abdelaal and Martin Kong in
International Conference on Supercomputing (ICS), 
June, 2021. [*Artifact Available*](https://github.com/mkongiv/polycross-comp-ics21).
<details>
<summary> Summary</summary>
In (almost) one line: We model the tile memory footprint induced by the chosen tile size under 3 loop fusion structures. A notion of ``balance'' is introduced to favor two heuristics, vector mode and reuse mode.
</details>

[*Automatic Generation of Multi-Objective Polyhedral Compiler Transformations.*](https://dl.acm.org/doi/10.1145/3410463.3414635)
Lorenzo Chelini, Tobias Gysi, Tobias Grosser, Martin Kong, Henk Corporaal in
International Conference on Parallel Architectures and Compilation Techniques (PACT),
October, 2020.
<details>
<summary> Summary</summary>
In one line: a database approach to polyhedral compiler transformations. Will expand this later :-)
</details>

[*Deriving Parametric Multi-way Recursive Divide-&-Conquer Dynamic Programming Algorithms using Polyhedral Compilers.*](https://dl.acm.org/doi/10.1145/3368826.3377916)
Mohammad Mahdi Javanmard, Zafar Ahmad, Martin Kong, Louis-No&euml;l Pouchet, Rezaul Chowdhury, Robert Harrison in
Code Generation and Optimization (CGO),
February, 2020.
<details>
<summary> Summary</summary>
  
This paper proposes techniques for automatically partitioning, tiling and parallelizing dynamic programming algorithms using a divide-and-conquer approach. Think of it as a mix of cache-oblivious tiling combined with polyhedral compilation.
</details>

[*Model-driven Transformations for Multi-and Many-core CPUs.*](https://dl.acm.org/doi/10.1145/3314221.3314653)
Martin Kong, Louis-No&euml;l Pouchet in
Programming Languages Design and Implementation (PLDI),
June, 2019.
<details>
<summary> Summary</summary>
  
The core contribution of this paper (one of my favorites!) is the design and implementation of a *performance lexicon* as an extensible set of Integer Linear
Program (ILP) cost functions, each of which attempts to maximize and extract a specific property on the optimized code. We define several cost functions, some 
heavily inspired in previous works, and others quite new. The motivation for having such lexicon is to be able to combine and reorder the ILP objectives based on the underlying computational and structural patterns found in the code.
</details>

[*A Performance Vocabulary for Affine Loop Transformations.*](https://arxiv.org/pdf/1811.06043.pdf)
Martin Kong, Louis-No&euml;l Pouchet in
ArXiv,
November, 2018.
<details>
<summary> Summary</summary>
  
Extended version of my PLDI'19 paper. Includes a few cost functions that literally did not fit in the PLDI'19 version.
</details>

[*Efficient cache simulation for affine computations.*](https://link.springer.com/chapter/10.1007/978-3-030-35225-7_6)
Wenlei Bao, Prashant Singh Rawat, Martin Kong, Sriram Krishnamoorthy, Louis-No&euml;l Pouchet, P. Sadayappan in
International Workshop on Languages and Compilers for Parallel Computing (LCPC),
October, 2017.
<details>
<summary> Summary</summary>
  
Had a relatively minor role in this paper. I was at Rice at the time. It proposes techniques to simulate the cache behavior of affine programs. This work was later extended by Wenlei Bao in a [POPL'17 paper](https://dl.acm.org/doi/10.1145/3158120) and then further extended by Gysi et al. in their [PLDI'19 paper](https://dl.acm.org/doi/10.1145/3314221.3314606) for fully associative caches. The latter one produces approximated results, albeit much faster!
</details>

[*PIPES: a Language and Compiler for Task-based Programming on Distributed-memory Clusters.*](https://dl.acm.org/doi/10.5555/3014904.3014957)
Martin Kong, Louis-No&euml;l Pouchet, P. Sadayappan, Vivek Sarkar in
The International Conference for High Performance Computing, Networking, Storage and Analysis (SC),
November, 2016.
<details>
<summary> Summary</summary>
  
I started this work towards the end of my PhD, and finished it during my post-doc at Rice University. It proposes a polyhedral data-flow graph language and compiler that permits to define graph computations. The compiler applies loop transformations such as tiling and fusion to coarse and optimize the graph. In addition, it also extracts the necessary information from the input graph to automatically produce Intel CnC tuners, runtime calls that heavily influence the program's performance.
</details>

[*Compiler/runtime Framework for Dynamic Dataflow Parallelization of Tiled Programs.*](https://dl.acm.org/doi/10.1145/2687652)
Martin Kong, Antoniu Pop, Louis-No&euml;l Pouchet, R. Govindarajan, Albert Cohen, P. Sadayappan in
ACM Transactions on Architecture and Code Optimization (TACO),
January, 2015.
<details>
<summary> Summary</summary>
  
This work started while in my internship at ENS Paris with Albert Cohen. The main contribution is the extraction of the necessary information to parallelize a tiled program and mapping it to a streaming task runtime with point-to-point communication capabilities, OpenStream. We use off-the-shelf polyhedral tools to compute the program synchronization points and instantiate the streams between producer and consumer tasks.
</details>

[*A Framework for enhancing data reuse via Associative Reordering.*](https://dl.acm.org/doi/10.1145/2594291.2594342)
Kevin Stock, Martin Kong, Tobias Grosser, Louis-No&euml;l Pouchet, Fabrice Rastello, J. Ramanujam, P. Sadayappan in
Programming Languages Design and Implementation (PLDI),
June, 2014.
<details>
<summary> Summary</summary>
  
This paper had deep effects in the optimization of iterative stencil computations. I was not the first author, that was Kevin, but I did the implementation in PoCC/PolyOpt for the ROSE compiler framework. The main contribution was the observation that register pressure was a significant performance bottleneck in iterative stencil computations. The solution was pretty clever. We recasted the stencil by formulating it as a sum of products, leveraging associative reordering. Then, leveraging these properties allowed us to use fixed loop-shifting (a.k.a *retiming*) to aling the loads and stores. The value of this work resides in the trade-off between using high-dimensional stencils that will converge in fewer iterations than their lower-dimensional counterpart. This work was followed by a number of papers in Saday's and other research groups, including addressing the same issue in GPUs.
</details>

[*When Polyhedral Transformations meet SIMD Code Generation.*](https://dl.acm.org/doi/10.1145/2491956.2462187)
Martin Kong, Richard Veras, Louis-No&euml;l Pouchet, Franz Franchetti, P. Sadayappan in 
Programming Languages Design and Implementation (PLDI),
June, 2013.
<details>
<summary> Summary</summary>
  
This is my very first paper, and probably my second favorite one, but a close call. The main contribution is a contract that establishes the roles and responsibilities between two powerful optimizing compilers, with the goal of synthesizing highly optimized SIMD-vectorized codelets. The first compiler finds and applies complex loop transformations to maximize and expose specific properties (e.g. permutability of loops). Later, the back-end compiler (Spiral), leverages the extracted and guaranteed properties to perform aggressive optimizations in straight-line code. The end result is a nice framework that achieves several commonly opposing goals: coarse-grained outer parallelism, locality and fine-grained (inner) vector-SIMD parallelism.
</details>


## Service

I've recently been or am currently involved in the following activities:
- HIPS’24 Workshop (Co-located with IPDPS’24).
- [Code Generation and Optimization (CGO) 2024](https://conf.researchr.org/committee/cgo-2024/cgo-2024-organizing-committee): Workshop and Tutorials Chair.
- [Compiler Construction (CC) 2024](https://conf.researchr.org/committee/CC-2024/CC-2024-organizing-committee): Chair of the Artifact Evaluation Committee.
- ACM TOPLAS: reviewer (2023).
- [The International Conference for High Performance Computing, Networking, Storage, and Analysis (SC’23)](https://sc23.supercomputing.org/planning-committee/): PC member
- Tapia Conference 2023 – Academic Deputy Chair
- NSF Panelist: 2023
- [IPDPS'23](https://www.ipdps.org/ipdps2023/2023-organization.html): Technical Track PC member. 
- [Principles and Practice of Parallel Programming (PPoPP) 2023](https://ppopp23.sigplan.org/committee/PPoPP-2023-organizing-committee): Submissions Chair and PC member.
- [Compiler Construction (CC) 2023](https://conf.researchr.org/committee/CC-2023/CC-2023-organizing-committee): Chair of the Artifact Evaluation Committee.
- [International Workshop on Polyhedral Compilation Techniques – IMPACT’23](https://impact-workshop.org/#committee): PC member.
- [International Conference on Parallel Processing (ICPP'22)](https://icpp22.gitlabpages.inria.fr/): Program Committee (PC) member, Software track.
- [2022 Tapia Conference](https://tapiaconference.cmd-it.org/): Financial aid reviewer, technical programming committee member.
- [International Workshop on Polyhedral Compilation Techniques (IMPACT'22)](https://acohen.gitlabpages.inria.fr/impact/impact2022/): Program Committee (PC) member.
- [International Workshop on Languages and Compilers for Parallel Computing (LCPC'21)](https://lcpc2021.github.io/): Program Committee (PC) member, Career Networking Session Chair.
- [International Conference on Parallel Processing (ICPP'21)](https://oaciss.uoregon.edu/icpp21/committees.php): Program Committee (PC) member, Software track.
- [2021 ACM Richard Tapia Celebration of Diversity in Computing](http://tapiaconference.org).
- [HIPS'21](http://www.cs.wm.edu/~bren/HIPS_2021.htm#committees): PC member.
- ACM TOPLAS: reviewer (2021).
- [IPDPS'21](https://www.ipdps.org/ipdps2021/2021-organization.html): Technical Track PC member. 
- [Techsuyo'20 (Education and Research Track)](https://www.techsuyo.org/speakers): Panelist
- [International Workshop on Languages and Compilers for Parallel Computing (LCPC'20)](https://lcpc2020.cs.stonybrook.edu/committees): Program Committee (PC) member, Networking (Social Breaks) Sessions Chair.
- ACM TACO, ACM TOPC: reviewer (2016-2021).
- IEEE TPDS: reviewer (2016-2020).
- [2020 ACM Richard Tapia Celebration of Diversity in Computing](http://tapiaconference.org).
- [International Conference on Parallel Processing (ICPP'20)](https://jnamaral.github.io/icpp20/organization/): Program Committee (PC) member, session chair.
- [ACM SIGPLAN 2020 International Conference on Compiler Construction (CC'20)](https://conf.researchr.org/committee/CC-2020/CC-2020-research-artifacts-artifact-evaluation-committee): Artifact Evaluation Co-Chair.
- Proposal Review Panelist for the National Science Foundation, USA.
- [International Workshop on Languages and Compilers for Parallel Computing (LCPC'19)](https://lcpc19.cc.gatech.edu/committee/): PC member, session chair.
- International Conference on Parallel Architectures and Compilation Techniques (PACT'19): Artifact Evaluation Committee.
- [Workshop on Optimization, Modeling, Analysis and Space Exploration (OMASE)](https://cgo.org/cgo2019/acceptedWorkshopTutorial/) (co-located with the Code Generation and Optimization Conference, CGO'19): Workshop Co-Chair.
- Proposal Review Panelist for the Department of Energy, USA.
- [International Workshop on OpenMP (IWOMP'18)](https://iwomp2018.bsc.es/organization): Program Committee.
- [Programming Models and Algorithms Workshop (PMAW)](https://kongm.github.io), co-located with [IPDPS'18](http://www.ipdps.org/ipdps2018/2018_advance_program.html): Workshop Chair.
- [International Workshop on Polyhedral Compilation Techniques (IMPACT'18)](http://impact.gforge.inria.fr/impact2018/): Workshop Co-Chair.


## Working with me

I am looking for smart, motivated, independent and hard-working students to join my research group. If you are interested in working on challenging problems in Quantum Computing (QC), HPC / parallel programming / programming languages / compilers, send me an email with the following, or stop by my office at DL 699. If sending me an email please include:

- Name
- Background: undergrad major, favorite courses, experience in HPC, QC, programming languages, compilers, computer architecture.
- Past experience: research, academic, industry.
- More importantly, please describe **why** do you want to work with me? Reading some of my papers or briefly describing an area you are interested in will help.


## Contact Information
- Current Position: Assistant Professor
- Affiliation: THE Ohio State University, Department of Computer Science and Engineering (CSE)
- Office: DL 699
- Phone: TBD

NOTE: This site is likely a bit more up-to-date than [my official OSU homepage](TBD). 
