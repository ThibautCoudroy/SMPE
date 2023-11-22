# Laboratory Notebook for a user pointing experiment

This analysis is based on [this one](https://gricad-gitlab.univ-grenoble-alpes.fr/coutrixc/m2r_pointingxp) and aims to compare the experimental design and results obtained.

## Project overview

Fitts described 1954 the relationship between the distance to a target, its width, and the time needed to acquire it [[Fitts, 1954](http://www2.psychology.uiowa.edu/faculty/mordkoff/InfoProc/pdfs/Fitts%201954.pdf)]. 
To aquire a target, e.g., to move the mouse cursor and click on a file to select it, Fitts' law describes how the distance between the start point and the target (_A_: amplitude of the movement), and the size of the target (_W_: width of the target) impacts the index of difficulty of the task (_ID_) [[MacKenzie and Buxton, 1992](http://www.billbuxton.com/fitts92.html)]:

> _ID_ = log2(_A_/_W_ + 1)

The time (_MT_: movement time) needed for a user to acquire a target is linearly correlated to _ID_:

> _MT_ = a + b × _ID_

A large part of Human-Computer Interaction research since then builds on top of Fitts' law.

This project aims at finding the values of the _a_ and _b_ parameters. This document contains my attempts to experimentally find _a_ and _b_ parameters.

## General Organization

### data/

This folder contains both raw and processed experimental data that is returned from the experimental software. 
Each file name is named after the following format: `YYYYMMDD_HHMM_RawData_<testname>_<name>` where the arguments are the following:
- `RawData`, i.e. the raw data  as returned from the experimental software. (We choose not to use the mean time provided by the website in our analysis because we are able to reproduce it in R and can check the results and computation)
- `<testname>`:
  - `Small` means the experiment variables (explained later) were $W=1,2,4$ and $A=16,32,64$
  - `Big` means the experiment variables were $W=16,32,64$ and $A=128,256,512$
  - `12W` means the experiment variables were $W=12,12,12$ and $A=128,256,512$
  - `128A` means the experiment variables were $W=16,32,64$ and $A=128,128,128$
- `<name>`: Initial of the name of the user who has done the test.


### analysis/

This folder contains the R markdown script used to analyze the data collected from the experiment. 

## Experimental Reports

### 2023-11-16

#### Experimental task

We did the same experimental task as the original study and analysis, on the website [pointing experiment from Ergonomics Web at Cornell University](http://ergo.human.cornell.edu/FittsLaw/FittsLaw.html).
On this Webpage, one can gather data for controlled 1D user pointing experiments. 
1. In the first text field, the experimenter enters the _widths_ of the targets, seperated with ','. 
2. In the second text field, the experimenter enters the _distance_ between targets, also called "_amplitude_", seperated with ','. 
3. In the last text field, the experiment enters the number of trial s·he wants to collect for each combination of _widths_ and _distances_. 

#### Experimental variables

The original experiment only did one type of test and with six trials for each combination.
We decided to do multiple experiments, as seen before, by modifying the values of the width of the target and the distances between them. We also did 10 trials for each combination.

#### Data collected

The Webpage returns the following results:
- Number of pointing errors (they are not counted in the experiment and it only stops when we touch enough time the target)
- A Fitts modelling in the form of _MT_ = a + b × log(A/W + 1) with an R2 shown
- The table of mean data, which we decide to compute ourselves.
- The raw data which can be found in the `data` folder.

#### Data analysis

Ths analysis is done in the [pointingAnalysis.Rmd file](./analysis/pointingAnalysis.Rmd) (R markdown file) and shows the differences with the original analysis.
