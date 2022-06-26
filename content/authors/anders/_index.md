---
# Display name
title: "Anders Albrechtsen"

# Username (this should match the folder name and the name on publications)
authors:
- "Anders Albrechtsen"

# Is this the primary user of the site?
# if true then it will show up on each post
superuser: true

# Role/position (e.g., Professor of Artificial Intelligence)
role: Professor of Population Genetics

# Organizations/Affiliations
organizations:
- name: 
  url: ""

# Short bio (displayed in user profile at end of posts)
bio: 

# List each interest with a dash
interests:
- Population Genetics
- Bioinformatics
- Human and Animals

education:
  courses:
  - course: Title course 1
    institution: Name of Institution
    year: 2012
  - course: Title course 1
    institution: Name of Institution
    year: 2012

# Social/Academic Networking
# For available icons, see: https://wowchemy.com/docs/page-builder/#icons
#   For an email link, use "fas" icon pack, "envelope" icon, and a link in the
#   form "mailto:your-email@example.com" or "#contact" for contact widget.
social:
- icon: envelope
  icon_pack: fas
  link: '#contact'  # For a direct email link, use "mailto:test@example.org".
- icon: twitter
  icon_pack: fab
  link: https://twitter.com/A_Albrechtsen
- icon: google-scholar
  icon_pack: ai
  link: https://scholar.google.com/citations?user=20oVxFsAAAAJ
- icon: github
  icon_pack: fab
  link: https://github.com/USERNAME
# Link to a PDF of your resume/CV from the About widget.
# To enable, copy your resume/CV to `static/files/cv.pdf` and uncomment the lines below.
# - icon: cv
#   icon_pack: ai
#   link: files/cv.pdf

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ""

# Highlight the author in author lists? (true/false)
highlight_name: false

# Organizational groups that you belong to (for People widget)
#   Set this to `[]` or comment out if you are not using People widget.
user_groups:
  - Principal Investigators

---

Anders Albrechtsen is a professor of population genetics at University of Copenhagen. His research interests include applying Statistical and computational methods for analysis of genomic data including methods for quantifying and correcting for population structure, detecting selection across the genome, loci dependent methods for modeling identity by descent, associations in small historically isolated population and various topics for analysis of next generation sequencing including low pass sequencing and ancient DNA.



[![Build Status](https://travis-ci.org/aalbrechtsen/relateAdmix.svg?branch=master)](https://travis-ci.org/aalbrechtsen/relateAdmix)

# relateAdmix
Estimating relatedness coefficients from admixed populations

The method is implemented in an R package and as a commandline based C++ program embeded in the R package. 

# Install
### R package using devtools

If you have the devtools packages (https://github.com/hadley/devtools) installed in R then you can install the package i R directly from github

```
library(devtools)
install_github("aalbrechtsen/relateAdmix")
```

### To compile the C++ version
download the code

```
git clone https://github.com/aalbrechtsen/relateAdmix.git
```

go to the scr folder that contains the C++ files 
type 

```
cd relateAdmix/scr
mv CPP_Makefile Makefile
make
```
### R package without devtools

If you do not have the devtools package (and dont want to install it) then you will have to build the R package 

first download the code (you need to have a clean version without the compiled c++ code)
```
git clone https://github.com/aalbrechtsen/relateAdmix.git
```

```
R CMD build relateAdmix
```

or  build and install

```
R CMD build relate
R CMD INSTALL Relate_<add version number>.tar.gz
```


# getting started

 * The manual can be found on the wiki [http://www.popgen.dk/software/index.php/RelateAdmix]

### in R
```
library(relateAdmix)
example(relate))
```

### C++ from commandline
After installing the program you can try running it on the example data set in the data folder, which consists of 50 individuals that are admixed from 2 source populations.

If you are in the src folder where you installed relateAdmix and you have the software ADMIXTURE installed this can be done as follows: 
```
cd ../data

# First run Admixture using a plink ".bed" as input to produce population specific allele 
# frequencies (smallPlink.2.P)  and individual ancestry proportions (smallPlink.2.Q).
# (note other programs can be used instead of Admixture, e.g. Structure and FRAPPE)
admixture smallPlink.bed 2 

# Then run relateAdmix with plink bed, bim and fam files plus the Admixture output files as input
../src/relateAdmix -plink smallPlink -f smallPlink.2.P -q smallPlink.2.Q -P 20

```
 


