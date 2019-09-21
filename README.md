PLSM and ISM
================

This project tries to use ISM(the sequential mining technique) to improve the performance of EM algorithm in PLSM model(the probabilistic model).

### PLSM

The derivation of PLSM Model can be found [here](http://hero-plus-ultra.top/2019/04/18/PLSM-2019/).



### ISM

ISM is an implementation of the sequence miner from the paper:  
[*A Subsequence Interleaving Model for Sequential Pattern Mining*](http://arxiv.org/abs/1602.05012)  
J. Fowkes and C. Sutton. KDD 2016.   

#### Installation of ISM

The installation steps can be found [here](https://github.com/mast-group/sequence-mining).

##### Information for Maven Version:

Maven version: 3.5.3(The latest maven 3.6.1 may lead to some problems)
Java version: 1.8.0_191



### The combination of ISM and PLSM

The detailed combination method can be checked [here]([https://github.com/joseph-mutu/PLSM_Intern/blob/master/PLSM%20and%20ISM.pdf]).

- Using ISM to find important positions of the temporal data.
- Using the nature of the conjugation of Dirichlet-Multinomial to update the non-informative distribution of motifs.
- Feed the initialized motifs into the inference algorithm of PLSM.



### Experiment Strategy

For the experiment, we want to demonstrate that the combined method can converge faster than using Non-informative prior distribution.

**Note:**

During the experiments, we call the gradient descent to do the optimization with a fixed step. By tuning this step, we may get better results instead of integrating ISM into PLSM.



### Drawback

- The combination set is too large to enumerate. (exponential increase)
- ISM can not handle too large sequences.