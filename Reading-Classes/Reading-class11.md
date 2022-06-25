
## Numpy
Standard Python distribution doesn't come bundled with NumPy module. 
A lightweight alternative is to install NumPy using popular Python package installer, pip.

    pip install numpy
The best way to enable NumPy is to use an installable binary package specific to your operating system. 
These binaries contain full SciPy stack 
(inclusive of NumPy, SciPy, matplotlib, IPython, SymPy and nose packages along with core Python).


The most important object defined in NumPy is an N-dimensional array type called ndarray. 
It describes the collection of items of the same type. Items in the collection can be accessed using a zero-based index.

Every item in an ndarray takes the same size of block in the memory. 
Each element in ndarray is an object of data-type object (called dtype).

Any item extracted from ndarray object (by slicing) is represented by a Python object of one of array scalar types. 
The following diagram shows a relationship between ndarray, data type object (dtype) and array scalar type −

    Ndarray
An instance of ndarray class can be constructed by different array creation routines described later in the tutorial. The basic ndarray is created using an array function in NumPy as follows −

    numpy.array
It creates an ndarray from any object exposing array interface, or from any method that returns an array.

    numpy.array(object, dtype = None, copy = True, order = None, subok = False, ndmin = 0)

### Example 1

    import numpy as np 
    a = np.array([1,2,3]) 
    print a
The output is as follows −
     
    [1, 2, 3]
### Example 2
 
more than one dimensions 
     
    import numpy as np 
    a = np.array([[1, 2], [3, 4]]) 
    print a
The output is as follows −

     [[1, 2],[3, 4]]
### Example 3
minimum dimensions 

    import numpy as np 
    a = np.array([1, 2, 3,4,5], ndmin = 2) 
    print a
The output is as follows −

    [[1, 2, 3, 4, 5]]
### Example 4
**dtype parameter** 

    import numpy as np 
    a = np.array([1, 2, 3], dtype = complex) 
    print a
The output is as follows −

    [ 1.+0.j, 2.+0.j, 3.+0.j]
The **ndarray** object consists of contiguous one-dimensional segment of computer memory, combined with an 
indexing scheme that maps each item to a location in the memory block. 
The memory block holds the elements in a row-major order (C style) or a column-major order (FORTRAN or MatLab style).

## NumPy - bitwise_and
The bitwise AND operation on the corresponding bits of binary representations of integers in input arrays is 
computed by np.bitwise_and() function.

### Example

    import numpy as np 
    print 'Binary equivalents of 13 and 17:' 
    a,b = 13,17 
    print bin(a), bin(b) 
    print '\n'  

    print 'Bitwise AND of 13 and 17:' 
    print np.bitwise_and(13, 17)
Its output is as follows −

    Binary equivalents of 13 and 17:
    0b1101 0b10001

    Bitwise AND of 13 and 17:
    1

## Jupyter

You can arrange multiple documents and activities side by side in the work area using tabs and splitters. 
Documents and activities integrate with each other, enabling new workflows for interactive computing, for example:

- Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.

- Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

- Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

- Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

JupyterLab also offers a unified model for viewing and handling data formats. 
JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) 
and can also display rich kernel output in these formats. See File and Output Formats for more information.

To navigate the user interface, JupyterLab offers customizable keyboard shortcuts and the ability to use key 
maps from vim, emacs, and Sublime Text in the text editor.

JupyterLab's extensions can customize or enhance any part of JupyterLab, including new themes, file editors, 
and custom components.

JupyterLab is served from the same server and uses the same notebook document format as the classic Jupyter Notebook.


