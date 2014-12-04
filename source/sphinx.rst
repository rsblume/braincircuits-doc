Sphinx
========

Sphinx is a lightweight program for creating documentation in Python. 
	* Sphinx uses restructured text
	* It can integrate with your python modules to automatically generate documentation based on your *docstrings*
	
Go `here <http://sphinx-doc.org/index.html>`_ for all things Sphinx


.. Important::
    *Would you like to go through some git and sphinx basics? If so, go to the * :ref:`Sphinx and Git Tutorial <sphinx_and_git_tutor>` 



**When you are in your root documentation directory this command will build your html files**::
	
	sphinx-build -b html source build

	where:
	
*source* 
		is your source directory
*build*
		is your build directory
	

**If you  want to make a flat html page use this command**::
	
	sphinx-build -b singlehtml source build

The advantage of this is that it makes fewer files in your directory, but the disadvantage is that the html page itself is messy


**To start from scratch type**::
	
	 sphinx-quickstart
	
follow the prompts and you are on your way	
	


Restructured Text (ReST):
--------------------------

Sphinx depends on a very simple mark-up syntax called restructured text or **"reST"**

One of the neat things about Sphinx and ReST is that you can always investigate the ReST code that was used to create the sphinx page by clicking on the View Source link on the html page


Here are some good links to follow to learn about **rEST**:

1. Go `here <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_ for a little tutorial

2. This `link <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_ is the quickref, it will be really helpful

3. go  `here <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html>`_ for the full reference guide
	
4. Here is a  Sphinx and ReST cheatsheet: `here <http://openalea.gforge.inria.fr/doc/openalea/doc/_build/html/source/sphinx/rest_syntax.html>`_	