============
Python Koans
============

Adapted from https://github.com/gregmalcolm/python_koans
------------------------

Python Koans is an interactive tutorial for learning the Python programming
language by making tests pass.

Most tests are *fixed* by filling the missing parts of assert functions. Eg:

    self.assertEqual(__, 1+2)

which can be fixed by replacing the __ part with the appropriate code:

    self.assertEqual(3, 1+2)

Occasionally you will encounter some failing tests that are already filled out.
In these cases you will need to finish implementing some code to progress. For
example, there is an exercise for writing some code that will tell you if a
triangle is equilateral, isosceles or scalene.

As well as being a great way to learn some Python, it is also a good way to get
a taste of Test Driven Development (TDD).

Downloading Python Koans
------------------------

Python Koans is available through git on Github:

    http://github.com/gregmalcolm/python_koans

Either site will allow you to download the source as a zip/gz/bz2.


Installing Python Koans
-----------------------

* Optimizing this repo for Ubuntu...You should have python and python3 available.

Getting Started
---------------

Jake Hebbert has created a couple of screencasts available here:

http://www.youtube.com/watch?v=e2WXgXEjbHY&list=PL5Up_u-XkWgNcunP_UrTJG_3EXgbK2BQJ&index=1

Or if you prefer to read:

From a \*nix terminal or windows command prompt run::

    python contemplate_koans.py

or::

    python3 contemplate_koans.py


Apparently a test failed::

    AssertionError: False is not True

It also tells me exactly where the problem is, it's an assert on line 12
of .\\koans\\about_asserts.py. This one is easy, just change False to True to
make the test pass.

Sooner or later you will likely encounter tests where you are not sure what the
expected value should be. For example::

    class Dog:
        pass

    def test_objects_are_objects(self):
        fido = self.Dog()
        self.assertEqual(__, isinstance(fido, object))

Sniffer Support
---------------

Sniffer allows you to run the tests continuously. If you modify any files files
in the koans directory, it will rerun the tests.

To set this up, you need to install sniffer::

    $ pip install sniffer

You should also run one of these libraries depending on your system. This will
automatically trigger sniffer when a file changes, otherwise sniffer will have
to poll to see if the files have changed.

On Linux::

    $ pip install pyinotify

Once it is set up, you just run::

    $ sniffer

Just modify one of the koans files and you'll see that the tests are triggered automatically. Sniffer is controlled by `scent.py`

Getting the Most From the Koans
-------------------------------

Quoting the Ruby Koans instructions::

	"In test-driven development the mantra has always been, red, green,
	refactor. Write a failing test and run it (red), make the test pass
	(green), then refactor it (that is look at the code and see if you
	can make it any better). In this case you will need to run the koan
	and see it fail (red), make the test pass (green), then take a
	moment and reflect upon the test to see what it is teaching you
	and improve the code to better communicate its intent (refactor)."

Content
-------

The Python Koans is a made up of about 2/3 Ruby Koans ported material and 1/3
Python specific tests. The content ported from Ruby Koans includes all the
assignment projects.

Content for Python 3 is a little different to the Python 2 flavor due to big
changes between the two different versions of the language.  For example, in
the Python 2 variant the differences between old and new style classes are
covered. This loses relevance in in the Python 3 version, but there are some
extra tests covering new functionality.

Finding More Koan Projects
--------------------------

There are number of other great Koan projects out there for various languages
and frameworks. Most of them can be found in github. Also there is a little
koans activity on bitbucket.

* Github koan projects:
    https://github.com/search?q=koans&ref=cmdform

* Bitbucket koan projects:
    https://bitbucket.org/repo/all?name=koans

Acknowledgments
---------------

Thanks go to Jim Weirich and Joe O'Brien for the original Ruby Koans that the
Python Koans is based on! Also the Ruby Koans in turn borrows from Metakoans
so thanks also go to Ara Howard for that!

Also thanks to everyone who has contributed to Python Koans! I got a great
headstart by taking over a code base initiated by the combined Mikes of
FPIP. So here's a little plug for their very cool Python podcast:

  http://frompythonimportpodcast.com/

A big thanks also to Mike Pirnat @pirnat and Kevin Chase @kjc have pitched in
as co-maintainers at various times

============
JJ SET UP
============
Recall bash install of venv
    661  python3 -m venv venv
    662  sudo apt-get install python3-venv
    664  python3 -m venv venv
    665  . venv/bin/activate
Tidy some dependencies
  666  python3 contemplate_koans.py
  667  pip install pyinotify
  671  pip install sniffer
  672  sniffer
Work your solutions branch