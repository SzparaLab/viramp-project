.. VirAmp documentation master file, created by
   sphinx-quickstart on Mon Mar 17 10:38:15 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to VirAmp's documentation!
==================================

VirAmp is a galaxy-based system for fast virus genome assembly and variation discovery.

Quick start guide:
	From the AWS (Amazon Web Services) dashboard navigate to "EC2", then "AMIs". Change the dropdown box to indicate public instances, then search for "Szpara_Viramp" and click the blue "Launch" button. Due to storage and computational requirements this AMI is not free tier eligible, and the m3.xlarge instance size is recommended. After selecting an instance size follow the prompts until the configure security group page is reached. Three custom TCP rules are required and should be added using the "add rule" button. All three are custom TCP rules and should have the source column as "anywhere" (0.0.0.0) with port ranges 1) 8080, 2) 20-21, and 3) 40000 - 50000. With these added, follow the prompts to create a custom key pair, then click the "review and launch" button. The instance is now launched and can be accessed under the "instances" tab on the left of the dashboard. Selecting the instance and clicking the "Connect" button will display directions on how to connect to your instance using ssh. Once connected, run the run.sh script found in the home directory using screen (screen -> space -> space -> ./run.sh -> Ctrl-a-d). Until the system is stopped internally VirAmp will be accessible by typing the public IP address into the address bar of any internet browser.

Following is an overview of how VirAmp platform works:

.. image:: viramp-doc/pipeline_overview.png

**For VirAmp platform installation and usage on the Cloud:**

.. toctree::
        :maxdepth: 2

        ec2_import
        viramp_login
        viramp_intro
        variation_assess

**For install VirAmp on your local machine**

* Download an `Galaxy <http://galaxyproject.org/>`_ and follow the `installation instruction <https://wiki.galaxyproject.org/Admin/GetGalaxy>`_

* The Script/vamp directory contains all the scripts and galaxy tool config files, place the folder under galaxy-dist/tools.

* Place the tool_config.xml in config under 'galaxy-dist'.

* Proftpd configuration as in 'config/proftpd.conf'.

* To get everything running, your will need the following softwares installed:

	* `seqtk <https://github.com/lh3/seqtk>`_
	* `diginorm <http://ged.msu.edu/angus/diginorm-2012/tutorial.html>`_
	* `velvet <http://www.ebi.ac.uk/~zerbino/velvet/>`_
	* `AMOS <http://sourceforge.net/apps/mediawiki/amos/index.php?title=AMOS>`_
	* `Quast <http://bioinf.spbau.ru/quast>`_
	* `MUMmer <http://mummer.sourceforge.net/>`_
	* `Circos <http://circos.ca/>`_


