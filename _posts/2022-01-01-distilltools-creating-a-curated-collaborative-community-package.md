---
title: "Distilltools: Creating a Curated, Collaborative Community Package"
date: 2022-01-01 00:00:00
description: Ella Kaye, Distilltools hex sticker by Freddie Yauner (https://freddieyauner.co.uk).
featured_image: /assets/img/theme/kaye_header_image.jpg
---

Whether you’re working in data science, design, or at the intersection of the two, whether you’re just starting out in these areas or are an established pro, having a website and blog makes sense. It allows you to present yourself and your work to the world. Blogging gives you a chance to practice your skills, share what you know, and receive feedback from your readers. And, as David Robinson puts it: Things that are still on your computer are approximately useless in comparison to anything out in the world<sup>1</sup>.

There is a wide range of different tools available for building personal websites. For those with some familiarity with R, markdown, and GitHub (or a willingness to learn), to my mind the best option, in terms of balancing flexibility with ease of use, is the R package **distill**<sup>2</sup>.

In April 2021, I rebuilt my personal website [https://ellakaye.rbind.io](https://ellakaye.rbind.io){:target="_blank"}{:rel="noopener noreferrer"} using **distill**. I was so impressed by how quick and easy it was to create a basic site and moreover how enjoyable the process was. Version 1.0 of **distill** was still relatively new (there was an RStudio blogpost<sup>3</sup> introducing it in December 2020) but already a community was forming around users. In particular, John Paul Helveston had started the distillery<sup>4</sup>, a showcase for websites created with **distill** sharing both the sites and the source behind them as well as a collection of blogposts with various tips and tricks for customisation. Some of these tricks were functions that the authors had written for themselves to make it easier to create or style content on their website.

As I adapted some of these functions for my own site, it occurred to me that if the original author and I both found them useful, then other **distill** users might, too, and therefore it’d be a good thing to wrap these functions in an R package, in collaboration with the original authors, to make them more widely available. And so I created the **distilltools** package<sup>5</sup>.

**distilltools** is a collection of tools to support the creation and styling of content on websites that are built using the **distill** package in R. Although it is possible to get a basic distill website up and running in under an hour, the possibilities for customisation are endless, particularly with some knowledge of CSS and HTML. The idea of the **distilltools** package is to make these customisations easy by using just R (possibly with guidance from within the package for a little bit of CSS).

The package is in its early stages of development. My vision for it is something rather different from any other R package that I am aware of. It is a **curated**, **collaborative** **community** project.

It is a **community** project in the sense that I actively encourage people to contribute to the package, and its direction will be driven in large part by these contributions. There are a wide range of ways to get involved, including sharing the package, asking questions, proposing ideas, reporting bugs, improving the documentation, and contributing code. There are further details in the contributing guide<sup>6</sup>.

I strive to make the distilltools community a welcoming, friendly, accessible place. I value all contributions, however big or small, whatever your previous experience of package development happens to be. Anyone who contributes a function will be credited as an author of the package.

It is **collaborative** because I work with people who contribute ideas and code to bring them to fruition as functions in the package. Are you a newbie to R or to contributing to packages? No worries! We will work through the process together, and it will be a learning opportunity for both of us. It’s a great experience to exchange ideas, streamline code, and turn a vision into a reality.

It is **curated** because, despite drawing ideas and code from many contributors, it is still important for ease of use that the functions in the package have a consistent user interface and a consistent approach to creating and styling content, especially where CSS is involved. There is still much to be worked out on that front. The package is very much a work in progress, and I am excited to continue to make that progress alongside a diverse community of contributors.

*Ella Kaye is a graduate research student in statistics at the University of Warwick and an R enthusiast. Her eclectic path has taken her from a BA in mathematics and philosophy (University of Oxford) through an MA in history and philosophy of science and technology (University of Toronto), an MPhil in mathematics education (University of Cambridge), and an MSc in applied statistics (University of Oxford). She has also been a secondary school maths teacher and worked in market research. She loves R and the R community and was the previous co-organiser of the Oxford R User Group. She takes great pleasure in sharing what she knows/is learning about R with others, particularly by speaking at R-Ladies and R User Group meetups and on her blog, [ellakaye.rbind.io](https://ellakaye.rbind.io/){:target="_blank"}{:rel="noopener noreferrer"}.*

<sup>1</sup> Advice to aspiring data scientists: start a blog. Variance Explained [http://varianceexplained.org/r/start-blog/](http://varianceexplained.org/r/start-blog/){:target="_blank"}{:rel="noopener noreferrer"}.

<sup>2</sup> Allaire, J. J., Iannone, R., Hill, A. P. & Xie, Y. Distill for R markdown. (2018).

<sup>3</sup> (re-)introducing distill for R markdown. [https://blog.rstudio.com/2020/12/07/distill/](https://blog.rstudio.com/2020/12/07/distill/){:target="_blank"}{:rel="noopener noreferrer"} (2020).

<sup>4</sup> Helveston, J. The distillery. [https://distillery.rbind.io](https://distillery.rbind.io){:target="_blank"}{:rel="noopener noreferrer"}.

<sup>5</sup> Distilltools. [https://ellakaye.github.io/distilltools/](https://ellakaye.github.io/distilltools/){:target="_blank"}{:rel="noopener noreferrer"}.

<sup>6</sup> Contributing to distilltools. [https://ellakaye.github.io/distilltools/CONTRIBUTING.html](https://ellakaye.github.io/distilltools/CONTRIBUTING.html){:target="_blank"}{:rel="noopener noreferrer"}.