**Welcome! Here you find the pygrametl source code. Let us know if you have any comments and/or suggestions!**

_pygrametl_ (pronounced py-gram-e-t-l) is a Python framework which offers commonly used functionality for development of Extract-Transform-Load (ETL) processes for dimensional data warehouses. It is currently being used in different production systems and with many different DBMSs.

When using pygrametl, the developer _codes_ the ETL process in [Python](http://python.org) code. This turns out to be very efficient, also when compared to _drawing_ the process in a graphical user interface (GUI).

Concretely, the developer creates an object for each dimension and fact table. (S)he can then easily add new members by `dimension.insert(row)` where `row` is a `dict` holding the values to insert. This is a very simple example, but pygrametl also supports much more complicated scenarios. For example, it is possible to create a single object for a _snowflaked dimension_. It is then still possible to add a new dimension member with a single method call as in `snowflake.insert(row)`. This will automatically do the necessary lookups and insertions in the tables participating in the snowflake.

pygrametl also supports _slowly changing dimensions_. Again, the programmer only has to invoke a single method: `scdim.scdensure(row)`. This will perform the needed updates of both type 1 (i.e., overwrites) and type 2 (i.e., addition of new versions).

There is a small example [here](http://code.google.com/p/pygrametl/wiki/SimpleExampleProgram).

The 2nd major release of pygrametl was made publicly available ultimo 2011. Among other things, version 0.2 added support for parallel processing. Further, we have changed the license to a BSD licence and added much more support for [Jython](http://jython.org) such that you also can use Java code and JDBC drivers in your ETL program (but pygrametl of course continues to work with CPython as well). Since then, we have made small and big improvements here and there (versions 0.2.1 and 0.2.2). Version 0.2.2 was renamed to version 2.2 since the code had been stable for long time.

The 3rd major release of pygrametl was made publicly available in Sep. 2014. In version 2.3, we added support for Python 3 (while still supporting Python 2).

If you choose to use pygrametl, we would be very happy if you would let us know. You can do so by sending a private email to **chr** _AT_ **cs** _DOT_ **aau** _DOT_ dk.

If you use pygrametl in academia, we would also appreciate if you cite the relevant paper(s) from [DOLAP'09](http://dl.acm.org/citation.cfm?doid=1651291.1651301) and [DOLAP'11](http://dl.acm.org/citation.cfm?doid=2064676.2064684).