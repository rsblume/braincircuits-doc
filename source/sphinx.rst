Sphinx
========

Sphinx is a lightweight program for creating documentation in Python. 
	* Sphinx uses restructured text
	* It can integrate with your python modules to automatically generate documentation based on your *docstrings*
	
Go `here <http://sphinx-doc.org/index.html>`_ for all things Sphinx








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
	

Sphinx depends on a very simple mark-up syntax called restructured text or **"reST"**:

1. Go `here <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_ for a little tutorial

2. This `link <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_ is the quickref, it will be really helpful

3. Finally, go  `here <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html>`_ for the full reference guide
	
	
	