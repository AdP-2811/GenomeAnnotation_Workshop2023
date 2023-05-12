# 2023 Workshop on Genomics, Cesky Krumlov: Genome Annotation

This repository contains course materials for a workshop on structural genome annotation with BRAKER, GALBA, and TSEBRA. The course is part of the 2023 Workshop on Genomics in Cesky Krumlov, Czech Republic (https://evomics.org/2023-workshop-on-genomics-cesky-krumlov/).

Authors: Katharina Hoff & Natalia Nenasheva

Contact: katharina.hoff@uni-greifswald.de

## Cloning this repository

Open a terminal window, create a new directory for yourself and download the GenomeAnnotation_Workship2023.git:

```
mkdir your_name_GA
cd your_name_GA
git clone https://github.com/KatharinaHoff/GenomeAnnotation_Workshop2023.git
```

This will create a folder called `GenomeAnnotation_Workshop2023` in your home directory. This folder contains the JupyterNotebook for this course (GenomeAnnotation.ipynb).

## Opening the JupyterNotebook on Genome Annotation 

You can run the image for JupyterNotebook display in any bash terminal from your home directory as follows:

```
# execute from your_name_GA directory
singularity exec --cleanenv --bind /home/genomics/workshop_materials/genome_annotation:/home/genomics/workshop_materials/genome_annotation --bind ${PWD}:${PWD} --bind $PWD:/home/jovyan /home/genomics/workshop_materials/genome_annotation/genome_annotation.sif jupyter notebook --no-browser --ip=127.0.0.1
```

This will display 3 links in your terminal. The links will look something like this:

```
http://127.0.0.1:8888/?token=4aff4819888e4afd61a63b3015f8a1f816deea84efe2cd3f
```
Open one of the links by right-clicking on it and say "open link". This will open a firefox web browser window. You should see the following:

![image](https://github.com/AdP-2811/GenomeAnnotation_Workshop2023/assets/133369539/439ea468-7b16-499e-aa8a-dcf6fe086a0e)

DO NOT CLOSE YOUR TERMINAL! It's essential that you keep it open. 
Click on the folder to access the content. Double click to open the GenomeAnnotation.ipynb. Welcome to the starting point of this lab.


## Course contents

   * theory: repeat library generation and repeat masking with RepeatModeler2/RepeatMasker
   * theory: short read RNA-Seq to genome alignment with Hisat2
   * theory: sorting an RNA-Seq alignment file with Samtools
   * practice: application of BRAKER3 (structural genome annotation with RNA-Seq alignments and a large protein data base)
   * practice: application of BRAKER1 (structural genome annotation with short read RNA-Seq alignments)
   * practice: application of BRAKER2 (structural genome annotation with protein database)
   * practice: application of GALBA (structural genome annotation with proteins of a closely related species, suitable for e.g. vertebrate genomes)
   * practice: merging BRAKER1 and BRAKER2 (or GALBA) gene sets with TSEBRA
   * practice: BUSCO assessment of predicted gene set
   * practice: preparing an assembly hub for the UCSC Genome Browser with MakeHub 
   * for advanced learners: annotate a chromsome of *Basesia duncati*

## Data sets

If you want to execute the JupyterNotebooks, you will need data. At the Cesky Krumlov Workshop, these datasets have already been prepared for you at /home/genomics/workshop_materials/genome_annotation.

## Acknowledgements

Stefan Kemnitz from The University Compute Center at University of Greifswald (https://rz.uni-greifswald.de/dienste/allgemein/sonstiges/high-performance-computing/) kindly assisted in building docker containers for genome annotation with methods developed at University of Greifswald.
