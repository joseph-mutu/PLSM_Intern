# Explanation of variables in code

In order to run the combined use, first ISM should be installed. 



## Variables

- flag_ISM

0 means do not use ISM. 1 means use ISM.

- overlap_flag

There are three databases(each has two documents) used in the experiment with three overlapping levels.

- PLSM parameters

nw: number of words;

ntr: length of the relative time;

nd: number of documents;

Td: length of time period;

nz: assumed number of latent motifs;



## Functions

- string_to_matrix

Use fonts to represent the patterns embedded in documents. This function means to convert font into matrixes.

- save_ism_data

Based on the process of generating sequences, this function saves the generated sequences into one certain file following the ISM data format. **Change the path of your file**. 

After running this, you should run ISM following the instructions of ISM to find "position sequences". 

- model and guide

Pyro function. Define the generative process of PLSM and the artificial distribution. 

- cal_median_KL

Calculate the KL divergence between the inferred motifs and real motifs. **One thing should be noticed:** Inferred motifs should be similar with the real motifs but with the random order. When doing the comparison of inferred motifs and real motifs, you should make sure you are comparing the right motifs.

- Draw-KL

The pics in the report are drawn using R. This function is a test.