.. VirAmp documentation master file, created by
   sphinx-quickstart on Mon Mar 17 10:38:15 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to VirAmp's documentation!
==================================

VirAmp is a galaxy-based system for fast virus genome assembly and variation discovery.

Quick Start Guide:

1) Launch the latest version of the "Szpara_Viramp" AMI from Amazon Web Services

2) SSH into the server and start the run.sh script using screen

``./run.sh``

Following is an overview of how the VirAmp platform works:

.. image:: viramp-doc/pipeline_overview.png

**For VirAmp platform installation and usage on the Cloud:**

.. toctree::
        :maxdepth: 2

        viramp_intro
        variation_assess
        ec2_import
        viramp_login


**To install VirAmp on your local machine**

* Download `Galaxy <http://galaxyproject.org/>`_ and follow the `installation instructions <https://wiki.galaxyproject.org/Admin/GetGalaxy>`_

* The Script/vamp directory contains all the scripts and galaxy tool config files. Place this folder under galaxy-dist/tools.

* Place the tool_config.xml in config under 'galaxy-dist'.

* Place the Proftpd configuration file (proftpd.conf) in 'config/proftpd.conf'.

* To get everything running, you will need the following software installed:

	* `seqtk <https://github.com/lh3/seqtk>`_
	* `diginorm <http://ged.msu.edu/angus/diginorm-2012/tutorial.html>`_
	* `velvet <http://www.ebi.ac.uk/~zerbino/velvet/>`_
	* `AMOS <http://sourceforge.net/apps/mediawiki/amos/index.php?title=AMOS>`_
	* `Quast <http://bioinf.spbau.ru/quast>`_
	* `MUMmer <http://mummer.sourceforge.net/>`_
	* `Circos <http://circos.ca/>`_


