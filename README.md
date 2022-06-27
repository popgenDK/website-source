# Welcome to the UCPH Popgen group's website


## Guide of editing the content

The files you need to edit are markdown files with ```.md``` suffix. Here is the [markdown syntax](https://wowchemy.com/docs/content/writing-markdown-latex/) for quick lookup.

### Edit the content online

The only fold you need to touch is the ```content``` fold if you just wanna create some contents instead of changing the website's UI.

## Guide of development locally

### IMPORTANT!!!

This repository is non centralized, which means there are no reviewers being responsible for what you committed. Anyone is invited as collaborator can have the right to wipe out the whole repository! We believe you won't be the evil guy :) 

For people developing the website using ```git``` locally, I'd like to suggest some rules to be followed so that you won't get other people in trouble: 

- never do ```git push --force```
- do not reset the commits no matter how meaningless they are.
- always ```git stage```your commits first then ```git pull```, ```git commit```, ```git push```. save your time fixing merging issues!
- do not touch ```.github/workflow``` unless the CI is broken
- do not enter the ```public``` folder and make commits. this is a submodule linked to the real pages for publishing which will be auto generated by github workflows.

### Requirements

- [go](https://go.dev/dl/)
- [hugo](https://gohugo.io/getting-started/installing/)
- git
- any editors you like

