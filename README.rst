============
JJ SET UP
============
Recall bash install of venv \
    661  python3 -m venv venv \
    662  sudo apt-get install python3-venv \
    664  python3 -m venv venv \
    665  . venv/bin/activate
Tidy some dependencies \
  666  python3 contemplate_koans.py \
  667  pip install pyinotify \
  671  pip install sniffer \
  672  sniffer \
Work your solutions branch

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