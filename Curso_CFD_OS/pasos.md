
# coding: utf-8
Text provided under a Creative Commons Attribution license, CC-BY.  All code is made available under the FSF-approved MIT license.  (c) Lorena A. Barba, Gilbert F. Forsyth 2015. Thanks to NSF for support via CAREER award #1149784.
# [@LorenaABarba](https://twitter.com/LorenaABarba)

# ##### Version 0.12 (August 2015)

# 12 steps to Navier-Stokes
# ======
# ***

# Hello! Welcome to the **12 steps to Navier-Stokes**. This is a practical module that is used in the beginning of an interactive Computational Fluid Dynamics (CFD) course taught by [Prof. Lorena Barba](http://lorenabarba.com) since Spring 2009 at Boston University. The course assumes only basic programming knowledge (in any language) and of course some foundation in partial differential equations and fluid mechanics. The practical module was inspired by the ideas of Dr. Rio Yokota, who was a post-doc in Barba's lab, and has been refined by Prof. Barba and her students over several semesters teaching the course. The course is taught entirely using Python and students who don't know Python just learn as we work through the module.
# 
# This [IPython notebook](http://ipython.org/ipython-doc/stable/interactive/htmlnotebook.html) will lead you through the first step of programming your own Navier-Stokes solver in Python from the ground up.  We're going to dive right in.  Don't worry if you don't understand everything that's happening at first, we'll cover it in detail as we move forward and you can support your learning with the videos of [Prof. Barba's lectures on YouTube](http://www.youtube.com/playlist?list=PL30F4C5ABCE62CB61).
# 
# For best results, after you follow this notebook, prepare your own code for Step 1, either as a Python script or in a clean IPython notebook.
# 
# To execute this Notebook, we assume you have invoked the notebook server using: `ipython notebook`.

# Step 1: 1-D Linear Convection
# -----
# ***

# The 1-D Linear Convection equation is the simplest, most basic model that can be used to learn something about CFD. It is surprising that this little equation can teach us so much! Here it is:
# 
# $$\frac{\partial u}{\partial t} + c \frac{\partial u}{\partial x} = 0$