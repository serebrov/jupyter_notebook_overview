The example Jupyter Notebook with features overview (how to use markdown and formulas, how to plot graphs, etc).

Setup: run `./install.sh` then open the [jupyter_notebook_overview.ipynb](./jupyter_notebook_overview.ipynb).

Live preview in `nbviewer`: https://nbviewer.jupyter.org/github/serebrov/jupyter_notebook_overview/blob/master/jupyter_notebook_overview.ipynb.

The [sympy_examples.ipynb](./sympy_examples.ipynb) contains some of [SymPy](http://docs.sympy.org/latest/tutorial/intro.html) examples.
See also: https://github.com/jrjohansson/scientific-python-lectures/blob/master/Lecture-5-Sympy.ipynb

# Reference: Python Math / Science Libraries

## NumPy

[NumPy](https://docs.scipy.org/doc/numpy/user/whatisnumpy.html) is the fundamental package for scientific computing in Python. It is a Python library that provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and much more.

At the core of the NumPy package, is the **ndarray** object. This encapsulates n-dimensional arrays of homogeneous data types, with many operations being performed in compiled code for performance.

Links:

* Reference: https://docs.scipy.org/doc/numpy/reference/
* Manual: https://docs.scipy.org/doc/numpy/contents.html
* User guide: https://docs.scipy.org/doc/numpy-dev/user/

## SciPy

[SciPy](https://docs.scipy.org/doc/scipy/reference/) is a collection of mathematical algorithms and convenience functions built on the Numpy extension of Python. Provides high-level commands and classes for manipulating and visualizing data: **interpolation, integration, clusterization, FFT, linear algebra, statistics**, etc.

With SciPy an interactive Python session becomes a data-processing and system-prototyping environment rivaling systems such as MATLAB, IDL, Octave, R-Lab, and SciLab.

Docs: https://docs.scipy.org/doc/scipy/reference/

## NumPy vs. SciPy vs. other packages

From [FAQ](https://www.scipy.org/scipylib/faq.html):

> What is the difference between NumPy and SciPy?
> In an ideal world, NumPy would contain nothing but the array data type and the most basic operations: indexing, sorting, reshaping, basic elementwise functions, et cetera. All numerical code would reside in SciPy. However, one of NumPy’s important goals is compatibility, so NumPy tries to retain all features supported by either of its predecessors. Thus NumPy contains some linear algebra functions, even though these more properly belong in SciPy. In any case, SciPy contains more fully-featured versions of the linear algebra modules, as well as many other numerical algorithms. If you are doing scientific computing with python, you should probably install both NumPy and SciPy. Most new features belong in SciPy rather than NumPy.

> How do I make plots using NumPy/SciPy?
> Plotting functionality is beyond the scope of NumPy and SciPy, which focus on numerical objects and algorithms. Several packages exist that integrate closely with NumPy to produce high quality plots, such as the immensely popular [Matplotlib](http://matplotlib.org/) and the extensible, modular toolkit [Chaco](http://code.enthought.com/projects/chaco/).

> How do I make 3D plots/visualizations using NumPy/SciPy?
> Like 2D plotting, 3D graphics is beyond the scope of NumPy and SciPy, but just as in the 2D case, packages exist that integrate with NumPy. [Matplotlib](http://matplotlib.org/) provides basic 3D plotting in the mplot3d subpackage, whereas [Mayavi](http://code.enthought.com/projects/mayavi/) provides a wide range of high-quality 3D visualization features, utilizing the powerful [VTK](http://www.vtk.org/) engine.

> Why both numpy.linalg and scipy.linalg? What’s the difference?
> scipy.linalg is a more complete wrapping of Fortran [LAPACK](http://www.netlib.org/lapack/) using [f2py, fortran to python interface generator](https://docs.scipy.org/doc/numpy/f2py/index.html).
> One of the design goals of NumPy was to make it buildable without a Fortran compiler, and if you don’t have LAPACK available NumPy will use its own implementation. SciPy requires a Fortran compiler to be built, and heavily depends on wrapped Fortran code.

## SymPy

[SymPy](http://www.sympy.org/en/index.html) is a Python library for symbolic mathematics.

SymPy can simplify expressions, compute derivatives, integrals, and limits, solve equations, work with matrices, and much, much more, and do it all symbolically. It includes modules for plotting, printing (like 2D pretty printed output of math formulas, or LATEXLATEX), code generation, physics, statistics, combinatorics, number theory, geometry, logic, and more.

See examples: [sympy_examples.ipynb](./sympy_examples.ipynb) contains some [SymPy](http://docs.sympy.org/latest/tutorial/intro.html).

## pandas

[pandas](http://pandas.pydata.org/pandas-docs/stable/) is a Python package providing fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python.

The two primary data structures of pandas, [Series](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.html#pandas.Series) (1-dimensional) and [DataFrame](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.html#pandas.DataFrame) (2-dimensional), handle the vast majority of typical use cases in finance, statistics, social science, and many areas of engineering.

Here are just a few of the things that pandas does well:

* Easy handling of missing data (represented as NaN) in floating point as well as non-floating point data
* Size mutability: columns can be inserted and deleted from DataFrame and higher dimensional objects
* Automatic and explicit data alignment: objects can be explicitly aligned to a set of labels, or the user can simply ignore the labels and let Series, DataFrame, etc. automatically align the data for you in computations
* Powerful, flexible group by functionality to perform split-apply-combine operations on data sets, for both aggregating and transforming data
* Make it easy to convert ragged, differently-indexed data in other Python and NumPy data structures into DataFrame objects
* Intelligent label-based slicing, fancy indexing, and subsetting of large data sets
* Intuitive merging and joining data sets
* Flexible reshaping and pivoting of data sets
* Hierarchical labeling of axes (possible to have multiple labels per tick)
* Robust IO tools for loading data from flat files (CSV and delimited), Excel files, databases, and saving / loading data from the ultrafast HDF5 format
* Time series-specific functionality: date range generation and frequency conversion, moving window statistics, moving window linear regressions, date shifting and lagging, etc.

## theano

[Theano](http://deeplearning.net/software/theano/) is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently. Theano features:

* tight integration with NumPy – Use numpy.ndarray in Theano-compiled functions.
* transparent use of a GPU – Perform data-intensive computations much faster than on a CPU.
* efficient symbolic differentiation – Theano does your derivatives for functions with one or many inputs.
* speed and stability optimizations – Get the right answer for log(1+x) even when x is really tiny.
* dynamic C code generation – Evaluate expressions faster.
* extensive unit-testing and self-verification – Detect and diagnose many types of errors.

Theano has been powering large-scale computationally intensive scientific investigations since 2007. But it is also approachable enough to be used in the classroom (University of Montreal’s [deep learning/machine learning](https://mila.umontreal.ca/en/cours/) classes).

Theano is a Python library and optimizing compiler for manipulating and evaluating expressions, especially matrix-valued ones. Manipulation of matrices is typically done using the numpy package, so what does Theano do that Python and numpy do not?

* execution speed optimizations: Theano can use g++ or nvcc to compile parts your expression graph into CPU or GPU instructions, which run much faster than pure Python.
* symbolic differentiation: Theano can automatically build symbolic graphs for computing gradients.
* stability optimizations: Theano can recognize [some] numerically unstable expressions and compute them with more stable algorithms.

The closest Python package to Theano is sympy. Theano focuses more on tensor expressions than Sympy, and has more machinery for compilation. Sympy has more sophisticated algebra rules and can handle a wider variety of mathematical operations (such as series, limits, and integrals).

If numpy is to be compared to MATLAB and sympy to Mathematica, Theano is a sort of hybrid of the two which tries to combine the best of both worlds.

See: http://deeplearning.net/software/theano/introduction.html

## Blaze

The Blaze ecosystem is a set of libraries that help users store, describe, query and process data. It is composed of the following core projects:

* Blaze: An interface to query data on different storage systems
* Dask: Parallel computing through task scheduling and blocked algorithms
* Datashape: A data description language
* DyND: A C++ library for dynamic, multidimensional arrays
* Libndtypes: A C/C++ library for a low-level version of Datashape
* Ndtypes-python: Python bindings for libndtypes
* Odo: Data migration between different storage systems

## Sage

[Sage](http://www.sagemath.org/) - Sage is a full-featured and very powerful CAS enviroment that aims to provide an open source system that competes with Mathematica and Maple. Sage is not a regular Python module, but rather a CAS environment that uses Python as its programming language.

Sage is in some aspects more powerful than SymPy, but both offer very comprehensive CAS functionality. The advantage of SymPy is that it is a regular Python module and integrates well with the IPython notebook.

## Spyder

[Spyder](http://code.google.com/p/spyderlib/) is a MATLAB-like IDE for scientific computing with python. It has the many advantages of a traditional IDE environment, for example that everything from code editing, execution and debugging is carried out in a single environment, and work on different calculations can be organized as projects in the IDE environment.

## References

* [A gallery of interesting Jupyter Notebooks](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)
* [Scientific python lectures (numpy, scipy, matplotlib, sympy overview)](https://github.com/jrjohansson/scientific-python-lectures)
