Ports
=====

These are custom Portfiles I've written for MacPorts. The following ports are
currently included:

* mfold_util
* ncbi-blast+
* UNAFold
* ViennaRNA
* xstow

Local Portfiles
===============

You need to create a local MacPorts source.

    $ mkdir ~/Projects/ports
    # vim /opt/local/etc/macports/sources.conf

Add the following line above the `rsync://` bit:

    file:///Users/<username>/Projects/ports

Index your ports:

    $ cd ~/Projects/ports && sudo portindex -f -d

You'll need to run `portindex` for every modification you make or new port you add.

Creating a Portfile
===================

See these Portfiles and the [documentation][docs] for more details.

[docs]: http://guide.macports.org/#development

