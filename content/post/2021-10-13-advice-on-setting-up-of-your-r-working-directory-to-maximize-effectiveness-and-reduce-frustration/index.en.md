---
title: 
author: Oluwafemi Oyedele
date: '2021-10-13'
slug: advice-on-setting-up-of-your-r-working-directory-to-maximize-effectiveness-and-reduce-frustration
categories:
  - R path
tags:
  - here
subtitle: ''
summary: ''
authors: []
lastmod: '2021-10-13T02:39:23-11:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
title: Advice on setting up your R working directory to maximize effectiveness and reduce frustration
---

The goal of the here package is to enable easy file referencing in a project-oriented workflow. In contrast to using setwd(), which is fragile and dependent on the way you organize your files, here uses the top-level directory of a project to easily build paths to files. 
When I got started with R, I learned to put setwd() and rm(list=ls()) at the beginning of my scripts. It made sense to me but it seems like it got rid of any leftovers in the environment and set up the working directory, so I could use relative paths. That seems to be a good practice, right? The idea definitely is, but setwd() and rm(list=ls()) are problematic. rm() doesn't give you a clean R session; it won't for instance, detach packages. setwd(), meanwhile, is completely dependent on the way you organize your files because the absolute file path in your computer is different from the file path in my computer; so if you have to share that R script with anyone the file path needs to be modified before that script will run in another system.
In 2018, Jenny Bryan gave a talk at the R studio conference on setting up your R session for better workflow. A couple of slides, in particular, set off a bit of controversy:
If the first line of your R script is:

setwd('C:/Users/Jenny/Path/that/only/I/have')


I will come into your office and **SET YOUR COMPUTER ON FIRE**

If the first line of your R script is:

rm(list=ls())


I will come into your office and **SET YOUR COMPUTER ON FIRE**


I agree with this opinion from Jenny Bryan! Here I explain why these habits can be harmful and may be indicative of an awkward workflow.
-	I strongly recommend that we should use the R studio projects. These set up a local working directory in a fresh R session, which makes it much easier for someone else to open and run your code.


-	Use *here()* from here package to write file paths.


In conclusion projects can not only help solve the problems of *setwd()* but also *rm(list=ls())*. The need for *setwd()* is automatically eliminated by using projects because the default directory will be wherever the project is located. You can learn more by reading the vignette of the here package.

<style>
body{
text-align: justify}
</style>

