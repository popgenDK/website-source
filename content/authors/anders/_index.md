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


Framework for joint determination of individual sex and sex-linked scaffolds for non-model organism based on depth of coverage (DoC). Our method assign individual sex by projecting sequencing depth of the samples to a two dimensional Principal Component Analysis plot followed by Gaussian mixture clustering. Jointly sex-linked scaffolds are identified based on differences in male and female read depth by a two-sample t-test.

SATC works following these steps:

1. Normalizing the depth of each scaffold within each sample
2. Reducing the dimensionality of the normalized depths using PCA
3. Clustering the samples using Gaussian mixtures clustering on the top PCs, 
4. Identifying the sample sex and sex-linked scaffolds from the clustering and the DoC. 


<p align="center" width="100%">
    <img width="100%" src="https://github.com/popgenDK/SATC/blob/9c6724e6ca4f0357d0891166d4b1008ea6720819/examples/plots/leo_PCA_and_boxplot.png?raw=true">
</p>
  
# Using SATC
SATC is just a set of R functions. You can use SATC in R, in an interactive shiny app or run it from the command line. The depth of coverage information can quickly be calculated from index bam files e.g. 


```
 


