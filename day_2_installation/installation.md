# dataScience30
## [Day 2: Installation Guide & Getting Acquainted with Jupyter Notebooks](https://youtu.be/JUKD3Nw166U)
#### By [Glitched Failure](https://www.youtube.com/channel/UCErSNiDZV4rJCNB8NrDGREA)
---
## Objectives
- Participants will have a working environment for executing python code in a Jupyter Notebook
- Participants will be familiar with navigating and interacting with a Jupyter Notebook

---
## Code Along
### Installation Guide Links:
- https://www.google.com/chrome/
- https://git-scm.com/downloads
- https://www.anaconda.com/distribution/

### Use Anaconda Navigator or the Anaconda terminal to create a new Jupyter Notebook
- Create new cells
- Practice navigating
- Practice editing and running "Markdown" and "Code" cells

---
## Assignments
### Practice using the Jupyter Notebook GUI
Either use the notebook in this folder called "testing_ground.ipynb" or create your own notebook to complete this assignment.  


Jupyter notebooks will be the main tool we'll be using throughout this course. __Spending time learning how to use this tool now will save a lot of later!__ The following tasks are by far the most common, so you'll want to commit these keyboard shortcuts to muscle memory.

While in a Jupyter notebook, near the top navigate to "Help > Keyboard Shortcuts". Use these shortcuts to complete the following tasks WITHOUT touching your mouse:
- Create 2 new cell above the current cell
- Create 2 new cell below the current cell
- Delete one of the newly created cells
- Convert 1 cell to Markdown
    - Write a few lines of content in the Markdown cell
    - _NOTE: You should have at least 2 code cells and 1 Markdown cells after this point_
- Split the markdown cell from the previous cell roughly in half
- In one code cell write `x = 5`, and in __another__ code cell, write `y = 10`
    - Make sure these two cells are next to each other
- Merge the 2 code cells from the previous step

---
## BONUS
I've found moving cells on the fly to be invaluable, however, there is no default keyboard shortcut for this functionality.
- Create keyboard shortcuts to move cells up and down

There are a number of great widgets for Jupyter Notebooks called [nbextensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/). I highly recommend downloading the package in Anaconda and browsing to see which extensions you might want to use. I personally love the "Sketchpad"!
- You can install through Anaconda Navigator through "Environments > {select your environment - dataScience30} > Search Packages"
- Or using the Anaconda Terminal with `conda install -c conda-forge jupyter_contrib_nbextensions`
- _NOTE: Once nbextensions is installed, you'll have to restart your Jupyter Notebook instance (close the terminal serving Jupyter and open a new instance)_

Markdown can seem intimidating at first, but knowing even a little markdown syntax can drastically improve the readability of your code. Check out this [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet) and get familiar with at least 5-6 markdown elements.

---
## Vocabulary
### Environment - ([source](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html))
- An environment is a directory that contains a specific collection of packages/libraries that you have installed. For example, you may have one environment with NumPy 1.7 and its dependencies, and another environment with NumPy 1.6 for legacy testing. If you change one environment, your other environments are not affected. You can easily activate or deactivate environments, which is how you switch between them. You can also share your environment with someone by giving them a copy of your `environment.yaml` file.
### Package
- The terms has many synonyms, depending on the language. You may hear of packages, modules, libraries, gems (Ruby), etc., but these terms all refer to essentially the same thing.
- A package is a piece of software, code that has a specific functionality.
- Modules in Python are simply Python files. They have the `.py` extension, and the name of the file is the name of the module.
- What the code looks like can differ - a module can have a set of functions, classes or variables typically encapsulated in some way to abstract the nitty gritty work being done. This simplifies burdensome or difficult tasks for the user. 
- For example, the Numpy package has many convenient math operations that work seamlessly with Numpy Arrays (these are similar to normal Python lists). 
    - With regular Python lists, it's a burden to make item-wise calculations (`double_nums = [num * 2 for num in my_list]`).
    - Numpy allows for quick and intuitive item-wise calculations (`double_nums = 2 * my_numpy_array`).

### Markdown - ([source](https://www.ultraedit.com/company/blog/community/what-is-markdown-why-use-it.html))
- Markdown is a plain text formatting syntax aimed at making writing for the internet easier. 
- The idea is write in a way that allows plain text documents to be styled, but still readable. Think HTML, but without tags getting in the way of reading the content.
- Markdown is everywhere! Facebook chat, Skype, and Reddit all let you use different flavors of Markdown to format your messages.
- Unfortunately, there is __no standard or universal guide__ for how Markdown works. Every company, website, IDEs, etc. can use dictate which syntax works and how it works. GitHub, for example, will not allow for much customization (as a security concern), while VSCode allows you to do pretty much anything.

---
## References
- [Google Chrome Installation](https://www.google.com/chrome/)
- [Git Installation](https://git-scm.com/downloads)
- [Anaconda Installation](https://www.anaconda.com/distribution/)
- [nbextensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/)
- [Conda Concepts Documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html)
- [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet)

---
## Have Feedback?
[Submit feedback here](https://docs.google.com/forms/d/e/1FAIpQLScvsDT2Q2VH26FvvfQhjNmP4RwXqh9GWiKSIcTFAHdfCKZdlg/viewform?usp=sf_link)