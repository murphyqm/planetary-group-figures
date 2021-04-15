---
title:
- Designing figures
theme:
- Berkeley
colortheme:
- dove
date:
- April 14th 2021

---

# Ten Simple Rules for Better Figures

## Pulled from...
Rougier NP, Droettboom M, Bourne PE (2014)
Ten Simple Rules for Better Figures.

Rolandi, M., Cheng, K. and Pérez‐Kriz, S. (2011),
A Brief Guide to Designing Effective Figures for the Scientific Paper.

**Two key ideas:** making plots aesthetically pleasing and easy to read, but also making sure you don't
unintentionally mislead readers and misrepresent your data (I mean also don't intentionally do it either...)

## 1. Know your audience

Design figures for the audience (not for you).

- A figure for a specialised journal/conference might need a different
design to one aimed at a broader audience.
  
- Of course *you* understand what the figure is showing, because you have
background knowledge and have spent hours staring at it, but would someone
with fresh eyes actually understand?
  
- Disciplinary conventions/journal specifications... what do figures in
papers on similar topics look like?
  
## 2. Know your message

Focus on the most important information you need to convey...

- Figures usually don't exist in isolation: identify the storyline in the
talk/poster/paper and decide how your figures contribute
  
- Based on this, what is the key message each figure needs to communicate?

- Without sacrificing clarity, can you remove some unnecessary detail?

## 3. Adapt figure to support the medium

How would design a figure specifically for:

- a paper
- a poster
- a talk (projected)
- a talk (online, shared screen)

Need to think about:

- different size
- time
- are you present to explain or is the audience reading it on their own?


**We'll discuss this more in a bit when we talk about tools for making figures**

## 4. Caption carefully

What would you say if you were presenting this figure during a poster
presentation? What questions might people have? Anticipate these and answer them in your caption.

## 5. Don't trust the defaults

When it comes to font, font size, colour palette, colour maps, axis labels,
legend position - don't assume the default settings are good enough; they 
might not suit the purpose of your plot.

Having an easily reproducible workflow (ie making custom plotting functions)
lets you roll out custom tweaks and changes easily and consistently
across all your figures.

## 6. Use colour effectively, not just for the sake of it

- Does it need to be in colour?
- Is colour the *only* way to tell apart different datasets or points? (It shouldn't be!)
- Is it colourblind and photocopier friendly?
- Are your colourmaps perceptually uniform?
- Might your colour choices accidentally incorrectly highlight certain features?

## 7. Don't mislead the reader

- Does the software you're using rescale values? Does this make the figure misleading? What 
implicit choices made by the software or library might result in a misleading figure?
  
- Have you sacrificed objectivity for aesthetics? 3D plots and pie charts are known to induce incorrect
perceptions of quantities. Use the simplest plot possible.
  
- Is your colourmap choice for any heatmap/surface plots perceptually uniform, or does it have
a luminance peak that can incorrectly highlight and draw attention to certain regions of the plot?
  
**[Never use a rainbow colourmap](https://blogs.egu.eu/divisions/gd/2017/08/23/the-rainbow-colour-map/)**

## 8. Banish chartjunk

**Make it as simple as possible** - chartjunk can add confusion.

- Chartjunk - too many colours, too many labels, coloured backgrounds, unnecessary gridlines,
  too many axes tick marks, verbose legends
  
- Avoid background colour in charts
- Think "save ink" when designing (even if your figure will only ever be viewed on a computer screen)
- If part of your figure doesn't make sense, try removing something for clarity as opposed to adding another label

[Chart Junk blog](https://junkcharts.typepad.com/)

## 9. Function over form

Or message over beauty... it is still a scientific figure, and conveying accurate information
objectively is the most important feature, more than aesthetics.

- Are you using extra colours for no good reason?
  
- Might your colour scheme, choice of scaling, fancy 3D effects etc., be unintentionally misleading
and highlighting or suggesting a trend in the data that doesn't actually exist?
  
Sometimes, the most clear and straightforward way of presenting data might not be the prettiest (RIP
my spiderweb diagram that showed both all the possible input parameters of my model and corresponding
outputs... information which now lives in a datatable.)
  
## 10. Use the right tool

There are loads of tools available - both very wide-ranging, general tools and then lots aimed at
specific applications (mapping, stats, etc)

What tools do you use?

- GMT (maps)
- matplotlib (general)
- R (stats)
- Inkscape (vector graphics)

**We'll return to this in a bit...**

# What rules do you have for making figures?

## Design principles

- Design a clear visual structure - use a grid system (applies to posters too)
- Use visual contrast, but keep figures simple (one type of contrast at a time)
- Keep it simple
- Check typography legibility

From [this paper](https://personal.egr.uri.edu/chelidz/Figures%20for%20papers.pdf)

## File types

Save your image as vector graphics if possible, or at least a high enough DPI.

# Tools you can use

## Python

- matplotlib
- cmocean
- seaborn

# References

## Other links and resources

[Useful slideshow on "Graphical Excellence"](https://www3.nd.edu/~pkamat/pdf/graphs.pdf)

[Designing more effective scientific figures](https://bioinformatics-core-shared-training.github.io/effective-figure-design/DesigningEffectiveScientificFigures_Zabala_afternoon_v00.pdf)

[Matplotlib tutorial for scientific figures](https://github.com/rougier/matplotlib-tutorial)

## Papers

D. Borland and R. Taylor II, "Rainbow Color Map (Still) Considered Harmful"
in IEEE Computer Graphics and Applications, vol. 27, no. 02, pp. 14-17, 2007.
https://doi.ieeecomputersociety.org/10.1109/MCG.2007.46

Rolandi, M., Cheng, K. and Pérez‐Kriz, S. (2011),
A Brief Guide to Designing Effective Figures for the Scientific Paper.
Adv. Mater., 23: 4343-4346. https://doi.org/10.1002/adma.201102518

Rougier NP, Droettboom M, Bourne PE (2014)
Ten Simple Rules for Better Figures.
PLoS Comput Biol 10(9): e1003833.
https://doi.org/10.1371/journal.pcbi.1003833

## Some more info

regenerate these slides

'pandoc -t beamer slides.md -o slides.pdf'