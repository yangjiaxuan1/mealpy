# A collection of the state-of-the-art MEta-heuristics ALgorithms in PYthon (mealpy)
[![GitHub release](https://img.shields.io/badge/release-0.8.2-yellow.svg)]()
[![Wheel](https://img.shields.io/pypi/wheel/gensim.svg)](https://pypi.python.org/pypi/mealpy) 
[![PyPI version](https://badge.fury.io/py/mealpy.svg)](https://badge.fury.io/py/mealpy)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3711949.svg)](https://doi.org/10.5281/zenodo.3711948)
[![License](https://img.shields.io/packagist/l/doctrine/orm.svg)]()


---
> "Knowledge is power, sharing it is the premise of progress in life. It seems like a burden to someone, but it is the only way to achieve immortality."
>  --- [Thieu Nguyen](https://www.researchgate.net/profile/Thieu_Nguyen6)
---

## Introduction
* MEALPY is a python module for the most of cutting-edge population meta-heuristic algorithms and is distributed
under MIT license.

* The goals of this framework are:
    * Sharing knowledge of meta-heuristic fields to everyone without a fee
    * Helping other researchers in all field access to optimization algorithms as quickly as possible
    * Implement the classical as well as the state-of-the-art meta-heuristics (The whole history of meta-heuristics)
    

## Installation

### Dependencies
* Python (>= 3.6)
* Numpy (>= 1.15.1)
* Scikit-learn (>= 0.22.1)
* Matplotlib (>=3.1.3)
* Opfunu (>= 0.4.3)

### User installation
Install the [current PyPI release](https://pypi.python.org/pypi/mealpy):
```code 
    pip install mealpy
    pip install --upgrade mealpy 
```
Or install the development version from GitHub:
```bash
    pip install git+https://github.com/thieunguyen5991/mealpy
```

### Example
```code 
* Simple example:

    from opfunu.type_based.uni_modal import Functions
    from mealpy.evolutionary_based.GA import BaseGA
    t1 = Functions()
    
    ## Setting parameters
    objective_func = t1._sum_squres__
    problem_size = 30
    domain_range = [-15, 15]
    log = True
    epoch = 100
    pop_size = 50
    pc = 0.95
    pm = 0.025
    
    md = BaseGA(objective_func, problem_size, domain_range, log, epoch, pop_size, pc, pm)
    best_position, best_fit, list_loss = md._train__()
    print(best_fit)

* Or run the simple:
    python examples/simple_run.py

* The more complicated tests in the folder: examples
```
The documentation includes more detailed installation instructions.

### Changelog
* See the "ChangeLog.md" for a history of notable changes to mealpy.


### Important links

* Official source code repo: https://github.com/thieunguyen5991/mealpy
* Download releases: https://pypi.org/project/mealpy/
* Issue tracker: https://github.com/thieunguyen5991/mealpy/issues

* This project also related to my another projects which are "meta-heuristics" and "neural-network", check it here
    * https://github.com/thieunguyen5991/opfunu
    * https://github.com/thieunguyen5991/metaheuristics
    * https://github.com/chasebk
    

## Contributions 

### Citation
If you use mealpy in your project, I would appreciate citations: 

```code 
@software{thieu_nguyen_2020_3711949,
  author       = {Thieu Nguyen},
  title        = {A collection of the state-of-the-art MEta-heuristics ALgorithms in PYthon: Mealpy},
  month        = march,
  year         = 2020,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.3711948},
  url          = {https://doi.org/10.5281/zenodo.3711948}
}
```

### Documents
* Group: 
    + Evolu: Evolutionary-based
    + Swarm: Swarm-based
    + Physic: Physics-based
    + Human: Human-based
    + Bio: Biology-based
    + System: System-based (eco-system, immune-system, network-system, ...)
    + Math: Math-based
    + Music: Music-based
    + Proba: Probabilistic based algorithm
    
* Levy: Using levy-flight technique or not
* Version: 
    + original: Taken exactly from the paper
    + changed: I changed the flow or equation to make algorithm works
* Type:
    + weak: working fine with uni-modal and some multi-modal functions
    + strong: working good with uni-modal, multi-modal, some hybrid and some composite functions
    + best: working well with almost all kind of functions
    + BEST: the best among all algorithms

* Some algorithm with original version and no levy techniques still belong to the best type such as:
    + Whale Optimization Algorithm
    + Bird Swarm Algorithm
    + Swarm Robotics Search And Rescue
    + Manta Ray Foraging Optimization
    + Henry Gas Solubility Optimization	
    + Atom Search Optimization
    + Equilibrium Optimizer
    + Artificial Ecosystem-based Optimization

* Paras: The number of parameters in the algorithm (Not counting the fixed parameters in the original paper)
    + Almost algorithms have 2 paras (epoch, population_size) and plus some paras depend on each algorithm.
    + Some algorithms belong to "best" type and have only 2 paras meaning that algorithm is outstanding
    
* Diffic - Difficulty Level: Objective observation from author.
    + Depend on the number of parameters, number of equations, the original ideas, time spend for coding, source lines of code (SLOC)
    + Easy: A few paras, few equations, SLOC very short
    + Medium: more equations than Easy level, SLOC longer than Easy level
    + Hard: Lots of equations, SLOC longer than Medium level, the paper hard to read.
    + Hard* - Very hard: Lots of equations, SLOC too long, the paper is very hard to read.

** For newbie, I recommend to read the paper of algorithms belong to "best or strong" type, "easy or medium" difficulty level.


| Group  | STT | Name                                       | Short | Year | Version   | Levy | Type   | Paras | Diffic |
|--------|-----|--------------------------------------------|-------|------|-----------|------|--------|-------|--------|
| Evolu  | 1   | Evolutionary Programming                   | EP    | 1964 | original  | no   | strong | 3     | easy   |
|        | 2   | Evolution Strategies                       | ES    | 1971 | original  | no   | strong | 3     | easy   |
|        | 3   | Memetic Algorithm                          | MA    | 1989 | original  | no   | weak   | 7     | easy   |
|        | 3   | Genetic Algorithm                          | GA    | 1992 | original  | no   | strong | 4     | easy   |
|        | 4   | Differential Evolution                     | DE    | 1997 | original  | no   | weak   | 4     | easy   |
|        | 5   | Flower Pollination Algorithm               | FPA   | 2014 | orginal   | yes  | strong | 3     | easy   |
|        | 6   | Coral Reefs Optimization                   | CRO   | 2014 | original  | no   | weak   | 7     | medium |
|        | 7   |                                            |       |      |           |      |        |       |        |
| Swarm  | 1   | Particle Swarm Optimization                | PSO   | 1995 | original  | no   | strong | 6     | easy   |
|        | 2   | Bacterial Foraging Optimization            | BFO   | 2002 | orginal   | no   | weak   | 11    | hard   |
|        | 3   | Cat Swarm Optimization                     | CSO   | 2006 | original  | no   | weak   | 9     | hard   |
|        | 4   | Artificial Bee Colony                      | ABC   | 2007 | changed   | no   | strong | 6     | easy   |
|        | 5   | Fireworks Algorithm                        | FA    | 2010 | original  | no   | strong | 7     | medium |
|        | 6   | Bat Algorithm                              | BA    | 2010 | original  | no   | weak   | 5     | easy   |
|        | 7   | Social Spider Optimization                 | SSO   | 2013 | changed   | no   | weak   | 3     | hard\* |
|        | 8   | Pigeon\-Inspired Optimization              | PIO   | 2014 | changed   | no   | strong | 2     | medium |
|        | 9   | Grey Wolf Optimizer                        | GWO   | 2014 | original  | no   | strong | 2     | easy   |
|        | 10  | Social Spider Algorithm                    | SSA   | 2015 | original  | no   | strong | 5     | easy   |
|        | 11  | Ant Lion Optimizer                         | ALO   | 2015 | original  | no   | weak   | 2     | medium |
|        | 12  | Moth Flame Optimization                    | MFO   | 2015 | changed   | no   | strong | 2     | easy   |
|        | 13  |  Elephant Herding Optimization             | EHO   | 2015 | original  | no   | strong | 5     | easy   |
|        | 14  | Whale Optimization Algorithm               | WOA   | 2016 | original  | no   | best   | 2     | easy   |
|        | 15  | Bird Swarm Algorithm                       | BSA   | 2016 | original  | no   | best   | 9     | medium |
|        | 16  | Swarm Robotics Search And Rescue           | SRSR  | 2017 | original  | no   | best   | 2     | hard\* |
|        | 17  | Grasshopper Optimisation Algorithm         | GOA   | 2017 | original  | no   | weak   | 3     | easy   |
|        | 18  | Earthworm Optimisation Algorithm           | EOA   | 2018 | original  | no   | weak   | 8     | medium |
|        | 19  | Moth Search Algorithm                      | MSA   | 2018 | changed   | no   | weak   | 5     | easy   |
|        | 20  | Rhino Herd Optimization                    | RHO   | 2018 | original  | no   | weak   | 6     | easy   |
|        | 21  | Emperor Penguin Optimizer                  | EPO   | 2018 | changed   | no   | strong | 2     | easy   |
|        | 22  | Nake Mole\-rat Algorithm                   | NMRA  | 2019 | original  | no   | strong | 3     | easy   |
|        | 23  | Bald Eagle Search                          | BES   | 2019 | changed   | no   | best   | 7     | medium |
|        | 24  | Pathfinder Algorithm                       | PFA   | 2019 | original  | no   | strong | 2     | easy   |
|        | 25  | Sailfish Optimizer                         | SFO   | 2019 | original  | no   | strong | 5     | medium |
|        | 26  | Harris Hawks Optimization                  | HHO   | 2019 | original  | yes  | best   | 2     | medium |
|        | 27  | Sea Lion Optimization                      | SLO   | 2019 | orginal   | no   | strong | 2     | easy   |
|        | 28  | Manta Ray Foraging Optimization            | MRFO  | 2020 | original  | no   | best   | 3     | easy   |
|        | 29  |                                            |       |      |           |      |        |       |        |
| Physic | 1   | Wind Driven Optimization                   | WDO   | 2013 | original  | no   | strong | 7     | easy   |
|        | 2   | Multi\-Verse Optimizer                     | MVO   | 2016 | changed   | no   | strong | 3     | easy   |
|        | 3   | Tug of War Optimization                    | TWO   | 2016 | original  | no   | strong | 2     | easy   |
|        | 4   | Electromagnetic Field Optimization         | EFO   | 2016 | original  | no   | strong | 6     | easy   |
|        | 5   | Nuclear Reaction Optimization              | NRO   | 2019 | original  | yes  | best   | 2     | hard\* |
|        | 6   | Henry Gas Solubility Optimization          | HGSO  | 2019 | original  | no   | best   | 3     | medium |
|        | 7   | Atom Search Optimization                   | ASO   | 2019 | original  | no   | best   | 4     | medium |
|        | 8   | Equilibrium Optimizer                      | EO    | 2019 | original  | no   | BEST   | 2     | easy   |
|        | 9   |                                            |       |      |           |      |        |       |        |
| Human  | 1   | Teaching Learning Optimization             | TLO   | 2011 | original  | no   | strong | 2     | easy   |
|        | 2   | Brain Storm Optimization                   | BSO   | 2011 | original  | no   | strong | 10    | easy   |
|        | 3   | Queuing Search Algorithm                   | QSA   | 2019 | original  | no   | strong | 2     | hard   |
|        | 4   | Search And Rescue Optimization             | SARO  | 2019 | original  | no   | strong | 4     | medium |
|        | 5   | Life Choice\-Based Optimization            | LCBO  | 2019 | original  | no   | strong | 2     | easy   |
|        | 6   | Social Ski\-Driver Optimization            | SSDO  | 2019 | changed   | no   | weak   | 2     | easy   |
|        | 7   | Gaining Sharing Knowledge\-based Algorithm | GSKA  | 2019 | original  | no   | strong | 6     | easy   |
|        | 8   |                                            |       |      |           |      |        |       |        |
| Bio    | 1   | Invasive Weed Optimization                 | IWO   | 2006 | original  | no   | strong | 5     | easy   |
|        | 2   | Biogeography\-Based Optimization           | BBO   | 2008 | original  | no   | strong | 4     | easy   |
|        | 3   | Virus Colony Search                        | VCS   | 2016 | changed   | no   | best   | 4     | hard\* |
|        | 4   | Satin Bowerbird Optimizer                  | SBO   | 2017 | original  | no   | strong | 5     | easy   |
|        | 5   | Wildebeest Herd Optimization               | WHO   | 2019 | changed   | no   | weak   | 12    | medium |
|        | 6   | Black Widow Optimization                   | BWO   | 2020 | changed   | no   | weak   | 5     | medium |
|        | 7   |                                            |       |      |           |      |        |       |        |
| System | 1   | Germinal Center Optimization               | GCO   | 2018 | changed   | no   | weak   | 4     | medium |
|        | 2   | Artificial Ecosystem\-based Optimization   | AEO   | 2019 | original  | no   | best   | 2     | easy   |
|        | 3   |                                            |       |      |           |      |        |       |        |
| Math   | 1   | Sine Cosine Algorithm                      | SCA   | 2016 | changed   | no   | strong | 2     | easy   |
|        | 2   |                                            |       |      |           |      |        |       |        |
| Music  | 1   | Harmony Search                             | HS    | 2001 | changed   | no   | weak   | 5     | easy   |
|        | 2   |                                            |       |      |           |      |        |       |        |
| Proba  | 1   | Cross Entropy Method                       | CEM   | 1997 | original  | no   | strong | 4     | medium |
|        | 2   |                                            |       |      |           |      |        |       |        |



### A

* **ABC - Artificial Bee Colony** . Karaboga, D. (2005). An idea based on honey bee swarm for numerical optimization (Vol. 200, pp. 1-10). Technical report-tr06, Erciyes university, engineering faculty, computer engineering department.

* **ALO - Ant Lion Optimizer** . Mirjalili S (2015). “The Ant Lion Optimizer.” Advances in Engineering Software, 83, 80-98. doi: [10.1016/j.advengsoft.2015.01.010](https://doi.org/10.1016/j.advengsoft.2015.01.010)

* **AEO - Artificial Ecosystem-based Optimization** . Zhao, W., Wang, L., & Zhang, Z. (2019). Artificial ecosystem-based optimization: a novel nature-inspired meta-heuristic algorithm. Neural Computing and Applications, 1-43.

* **ASO - Atom Search Optimization** . Zhao, W., Wang, L., & Zhang, Z. (2019). Atom search optimization and its application to solve a hydrogeologic parameter estimation problem. Knowledge-Based Systems, 163, 283-304.

### B

* **BFO - Bacterial Foraging Optimization** . Passino, K. M. (2002). Biomimicry of bacterial foraging for distributed optimization and control. IEEE control systems magazine, 22(3), 52-67.

* **BBO - Biogeography-Based Optimization** . Simon, D. (2008). Biogeography-based optimization. IEEE transactions on evolutionary computation, 12(6), 702-713.

* **BA - Bat Algorithm** . Yang, X. S. (2010). A new metaheuristic bat-inspired algorithm. In Nature inspired cooperative strategies for optimization (NICSO 2010) (pp. 65-74). Springer, Berlin, Heidelberg.

* **BSO - Brain Storm Optimization** . Shi, Y. (2011, June). Brain storm optimization algorithm. In International conference in swarm intelligence (pp. 303-309). Springer, Berlin, Heidelberg.

* **BSA - Bird Swarm Algorithm** . Meng, X. B., Gao, X. Z., Lu, L., Liu, Y., & Zhang, H. (2016). A new bio-inspired optimisation algorithm: Bird Swarm Algorithm. Journal of Experimental & Theoretical Artificial Intelligence, 28(4), 673-687.

* **BES - Bald Eagle Search** . Alsattar, H. A., Zaidan, A. A., & Zaidan, B. B. (2019). Novel meta-heuristic bald eagle search optimisation algorithm. Artificial Intelligence Review, 1-28.

* **BWO - Black Widow Optimization** . Hayyolalam, V., & Kazem, A. A. P. (2020). Black Widow Optimization Algorithm: A novel meta-heuristic approach for solving engineering optimization problems. Engineering Applications of Artificial Intelligence, 87, 103249.


### C

* **CEM - Cross Entropy Method** . Rubinstein, R. (1999). The cross-entropy method for combinatorial and continuous optimization. Methodology and computing in applied probability, 1(2), 127-190.

* **CSO - Cat Swarm Optimization** . Chu, S. C., Tsai, P. W., & Pan, J. S. (2006, August). Cat swarm optimization. In Pacific Rim international conference on artificial intelligence (pp. 854-858). Springer, Berlin, Heidelberg.

* **CRO - Coral Reefs Optimization** . Salcedo-Sanz, S., Del Ser, J., Landa-Torres, I., Gil-López, S., & Portilla-Figueras, J. A. (2014). The coral reefs optimization algorithm: a novel metaheuristic for efficiently solving optimization problems. The Scientific World Journal, 2014.


### D

* **DE - Differential Evolution** . Storn, R., & Price, K. (1997). Differential evolution–a simple and efficient heuristic for global optimization over continuous spaces. Journal of global optimization, 11(4), 341-359.

* **DSA - Differential Search Algorithm** . Civicioglu, P. (2012). Transforming geocentric cartesian coordinates to geodetic coordinates by using differential search algorithm. Computers & Geosciences, 46, 229-247.



### E

* **ES - Evolution Strategies** . Schwefel, H. P. (1984). Evolution strategies: A family of non-linear optimization techniques based on imitating some principles of organic evolution. Annals of Operations Research, 1(2), 165-167.

* **EP - Evolutionary programming** . Fogel, L. J. (1994). Evolutionary programming in perspective: The top-down view
. Computational intelligence: Imitating life.

* **EHO - Elephant Herding Optimization** . Wang, G. G., Deb, S., & Coelho, L. D. S. (2015, December). Elephant herding optimization. In 2015 3rd International Symposium on Computational and Business Intelligence (ISCBI) (pp. 1-5). IEEE.

* **EFO - Electromagnetic Field Optimization** . Abedinpourshotorban, H., Shamsuddin, S. M., Beheshti, Z., & Jawawi, D. N. (2016). Electromagnetic field optimization: A physics-inspired metaheuristic optimization algorithm. Swarm and Evolutionary Computation, 26, 8-22.

* **EOA - Earthworm Optimisation Algorithm** . Wang, G. G., Deb, S., & dos Santos Coelho, L. (2018). Earthworm optimisation algorithm: a bio-inspired metaheuristic algorithm for global optimisation problems. IJBIC, 12(1), 1-22.

* **EPO - Emperor Penguin Optimizer** . Dhiman, G., & Kumar, V. (2018). Emperor penguin optimizer: A bio-inspired algorithm for engineering problems. Knowledge-Based Systems, 159, 20-50.

* **EO - Equilibrium Optimizer** . Faramarzi, A., Heidarinejad, M., Stephens, B., & Mirjalili, S. (2019). Equilibrium optimizer: A novel optimization algorithm. Knowledge-Based Systems.


### F
* **FA - Fireworks algorithm** . Tan, Y., & Zhu, Y. (2010, June). Fireworks algorithm for optimization. In
 International conference in swarm intelligence (pp. 355-364). Springer, Berlin, Heidelberg.

* **FPA - Flower Pollination Algorithm** . Yang, X. S. (2012, September). Flower pollination algorithm for global optimization. In International conference on unconventional computing and natural computation (pp. 240-249). Springer, Berlin, Heidelberg.


### G

* **GA - Genetic Algorithm** . Holland, J. H. (1992). Genetic algorithms. Scientific american, 267(1), 66-73.

* **GWO - Grey Wolf Optimizer** . Mirjalili, S., Mirjalili, S. M., & Lewis, A. (2014). Grey wolf optimizer. Advances in engineering software, 69, 46-61.

* **GOA - Grasshopper Optimisation Algorithm** . Saremi, S., Mirjalili, S., & Lewis, A. (2017). Grasshopper optimisation algorithm: theory and application. Advances in Engineering Software, 105, 30-47.

* **GCO - Germinal Center Optimization** . Villaseñor, C., Arana-Daniel, N., Alanis, A. Y., López-Franco, C., & Hernandez-Vargas, E. A. (2018). Germinal center optimization algorithm. International Journal of Computational Intelligence Systems, 12(1), 13-27.

* **GSKA - Gaining Sharing Knowledge-based Algorithm** . Mohamed, A. W., Hadi, A. A., & Mohamed, A. K. (2019). Gaining-sharing knowledge based algorithm for solving optimization problems: a novel nature-inspired algorithm. International Journal of Machine Learning and Cybernetics, 1-29.


### H

* **HS - Harmony Search** . Geem, Z. W., Kim, J. H., & Loganathan, G. V. (2001). A new heuristic optimization algorithm: harmony search. simulation, 76(2), 60-68.

* **HHO - Harris Hawks Optimization** . Heidari, A. A., Mirjalili, S., Faris, H., Aljarah, I., Mafarja, M., & Chen, H. (2019). Harris hawks optimization: Algorithm and applications. Future Generation Computer Systems, 97, 849-872.

* **HGSO - Henry Gas Solubility Optimization** . Hashim, F. A., Houssein, E. H., Mabrouk, M. S., Al-Atabany, W., & Mirjalili, S. (2019). Henry gas solubility optimization: A novel physics-based algorithm. Future Generation Computer Systems, 101, 646-667.

### I


* **IWO - Invasive Weed Optimization** . Mehrabian, A. R., & Lucas, C. (2006). A novel numerical optimization algorithm inspired from weed colonization. Ecological informatics, 1(4), 355-366.

### J

### K

### L

* **LCBO - Life Choice-Based Optimization** . Khatri, A., Gaba, A., Rana, K. P. S., & Kumar, V. (2019). A novel life choice-based optimizer. Soft Computing, 1-21.

### M

* **MA - Memetic Algorithm** . Moscato, P. (1989). On evolution, search, optimization, genetic algorithms and martial
 arts
: Towards memetic algorithms. Caltech concurrent computation program, C3P Report, 826, 1989.

* **MFO - Moth Flame Optimization** . Mirjalili, S. (2015). Moth-flame optimization algorithm: A novel nature-inspired heuristic paradigm. Knowledge-based systems, 89, 228-249.

* **MVO - Multi-Verse Optimizer** . Mirjalili, S., Mirjalili, S. M., & Hatamlou, A. (2016). Multi-verse optimizer: a nature-inspired algorithm for global optimization. Neural Computing and Applications, 27(2), 495-513.

* **MSA - Moth Search Algorithm** . Wang, G. G. (2018). Moth search algorithm: a bio-inspired metaheuristic algorithm for global optimization problems. Memetic Computing, 10(2), 151-164.

* **NMRA - Nake Mole-rat Algorithm** . Salgotra, R., & Singh, U. (2019). The naked mole-rat algorithm. Neural Computing and Applications, 31(12), 8837-8857.

* **MRFO - Manta Ray Foraging Optimization** . Zhao, W., Zhang, Z., & Wang, L. (2020). Manta ray foraging optimization: An effective bio-inspired optimizer for engineering applications. Engineering Applications of Artificial Intelligence, 87, 103300.



### N


* **NRO - Nuclear Reaction Optimization** . Wei, Z., Huang, C., Wang, X., Han, T., & Li, Y. (2019). Nuclear Reaction Optimization: A novel and powerful physics-based algorithm for global optimization. IEEE Access. 


### O

### P

* **PSO - Particle Swarm Optimization** . Eberhart, R., & Kennedy, J. (1995, October). A new optimizer using particle swarm theory. In MHS'95. Proceedings of the Sixth International Symposium on Micro Machine and Human Science (pp. 39-43). Ieee.

* **PIO - Pigeon-Inspired Optimization** . Duan, H., & Qiao, P. (2014). Pigeon-inspired optimization: a new swarm intelligence optimizer for air robot path planning. International journal of intelligent computing and cybernetics.

* **PFA - Pathfinder Algorithm** . Yapici, H., & Cetinkaya, N. (2019). A new meta-heuristic optimizer: Pathfinder algorithm. Applied Soft Computing, 78, 545-568.


### Q

* **QSA - Queuing Search Algorithm** . Zhang, J., Xiao, M., Gao, L., & Pan, Q. (2018). Queuing search algorithm: A novel metaheuristic algorithm for solving engineering optimization problems. Applied Mathematical Modelling, 63, 464-490.


### R


* **RHO - Rhino Herd Optimization** . Wang, G. G., Gao, X. Z., Zenger, K., & Coelho, L. D. S. (2018, December). A novel metaheuristic algorithm inspired by rhino herd behavior. In Proceedings of The 9th EUROSIM Congress on Modelling and Simulation, EUROSIM 2016, The 57th SIMS Conference on Simulation and Modelling SIMS 2016 (No. 142, pp. 1026-1033). Linköping University Electronic Press.


### S

* **SSO - Social Spider Optimization** . Cuevas, E., Cienfuegos, M., ZaldíVar, D., & Pérez-Cisneros, M. (2013). A swarm optimization algorithm inspired in the behavior of the social-spider. Expert Systems with Applications, 40(16), 6374-6384.

* **SSA - Social Spider Algorithm** . James, J. Q., & Li, V. O. (2015). A social spider algorithm for global optimization. Applied Soft Computing, 30, 614-627.

* **SCA - Sine Cosine Algorithm** . Mirjalili, S. (2016). SCA: a sine cosine algorithm for solving optimization problems. Knowledge-Based Systems, 96, 120-133.

* **SRSR - Swarm Robotics Search And Rescue** . Bakhshipour, M., Ghadi, M. J., & Namdari, F. (2017). Swarm robotics search & rescue: A novel artificial intelligence-inspired optimization approach. Applied Soft Computing, 57, 708-726.

* **SBO - Satin Bowerbird Optimizer** . Moosavi, S. H. S., & Bardsiri, V. K. (2017). Satin bowerbird optimizer: a new optimization algorithm to optimize ANFIS for software development effort estimation. Engineering Applications of Artificial Intelligence, 60, 1-15.

* **SFO - Sailfish Optimizer** . Shadravan, S., Naji, H. R., & Bardsiri, V. K. (2019). The Sailfish Optimizer: A novel nature-inspired metaheuristic algorithm for solving constrained engineering optimization problems. Engineering Applications of Artificial Intelligence, 80, 20-34.

* **SARO - Search And Rescue Optimization** . Shabani, A., Asgarian, B., Gharebaghi, S. A., Salido, M. A., & Giret, A. (2019). A New Optimization Algorithm Based on Search and Rescue Operations. Mathematical Problems in Engineering, 2019.

* **SSDO - Social Ski-Driver Optimization** . Tharwat, A., & Gabel, T. (2019). Parameters optimization of support vector machines for imbalanced data using social ski driver algorithm. Neural Computing and Applications, 1-14.

* **SLO - Sea Lion Optimization** . Masadeh, R., Mahafzah, B. A., & Sharieh, A. (2019). Sea Lion Optimization Algorithm. Sea, 10(5).

### T

* **TLO - Teaching Learning Optimization** . Rao, R. V., Savsani, V. J., & Vakharia, D. P. (2011). Teaching–learning-based optimization: a novel method for constrained mechanical design optimization problems. Computer-Aided Design, 43(3), 303-315.

* **TWO - Tug of War Optimization** . Kaveh, A., & Zolghadr, A. (2016). A novel meta-heuristic algorithm: tug of war optimization. Iran University of Science & Technology, 6(4), 469-492.


### U

### V

* **VCS - Virus Colony Search** . Li, M. D., Zhao, H., Weng, X. W., & Han, T. (2016). A novel nature-inspired
 algorithm for optimization: Virus colony search. Advances in Engineering Software, 92, 65-88.

### W

* **WOA - Whale Optimization Algorithm** . Mirjalili, S., & Lewis, A. (2016). The whale optimization algorithm. Advances in engineering software, 95, 51-67.

* **WHO - Wildebeest Herd Optimization** . Amali, D., & Dinakaran, M. (2019). Wildebeest herd optimization: A new global optimization algorithm inspired by wildebeest herding behaviour. Journal of Intelligent & Fuzzy Systems, (Preprint), 1-14.

* **WDO - Wind Driven Optimization** . Bayraktar, Z., Komurcu, M., & Werner, D. H. (2010, July). Wind Driven Optimization (WDO): A novel nature-inspired optimization algorithm and its application to electromagnetics. In 2010 IEEE antennas and propagation society international symposium (pp. 1-4). IEEE.

### X

### Y

### Z



# Not done - Not working yet

* **Artificial Algae Algorithm** . Uymaz, S. A., Tezel, G., & Yel, E. (2015). Artificial algae algorithm (AAA) for
 nonlinear global optimization. Applied Soft Computing, 31, 153-171.
