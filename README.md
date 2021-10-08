# project-template
@eeshanbot's project template for organized exploratory computational research

## welcome
Welcome to my project template! I see automation and transparency as key components for following [FAIR](https://www.nature.com/articles/sdata201618) data principles:
- Findability
- Accessibility
- Interoperability
- Reusability

As this is a GitHub "template", the best way to use it is to download to your own computer or click "use this template". 

## structure

#### data
This folder holds local data. This is a *read-only* folder. I will put project specific data here and more general or multiple-project data products somewhere else.

#### src
This folder holds *functions*. I like to use the following syntax. I put anything into a function that I might use more than once.

###### function calls
All functions start with `eb_` for autocompletion (eager beaver). They are then followed by one of:
* `view_` = makes a figure (does not save it automatically)
* `get_` = runs a small computation
* `compute_` = runs a large computation
* `read_` = reads some kind of input file, generally customized by data stream
* `write_` = writes some kind of output file
* `h_` = helper for miscellaneous, useful tasks

###### variable style guide
* constants = `A_CONSTANT_VARIABLE`
* number of = `nVal, nSamples, num_samples`
* important / dynamic = `importantVariablesHere`
* scratch = `k, m, n, x, y, z, a, b, c, d` (never i or j) 
* iterator = `iVal, iSamples` or `kk,mm,nn...`

#### pipeline
This folder holds *scripts*. These scripts access data from `data` and functions from `src`. Each script or collection of scripts lives in an aptly named sub-folder based on the desired task.

#### results
This folder holds figures, tables, etc, that you may want to decouple from the processing pipeline. You can always automate this with a symbolic link.

#### doc
This folder holds LaTeX code, makefiles, bib files, etc for eventual journal submission. Sometimes I like to add a `journal` folder and write entries in Markdown; this is a nice [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/). 
