VirAmp assembly pipeline manual
================================

This is a general description of the function of each tool found in `VirAmp website <http://viramp.com/>`_ or in your own version of the platform. A detailed description is posted under the webpage of each tool.

One-click pipeline
-------------------
Two general pipelines are provided with a one-click option, one for paired-end data and the other for single-end data.  Users only need to submit the raw data of read files and a reference file.  Besides running with the default settings, advanced users may custom configure the pipeline with their desired parameters.

.. image:: manual-pic/paired_end_pipeline.png

Step-by-Step Process
---------------------

Next we provide an introduction of each step in the pipeline individually.

Quality Control
^^^^^^^^^^^^^^^
First, trim out the low quality bases of the input fastq files, either by removing low quality bases or mandatorily trimming a certain length from each end.

.. image:: manual-pic/trim_qual.png

Diginorm
^^^^^^^^^
Next, reduce coverage and bias using `Digital normalization <http://ged.msu.edu/papers/2012-diginorm/>`_. This step reduce the sample variation as well as sample bias.

.. image:: manual-pic/diginorm.png

`de novo` Contig assembly
^^^^^^^^^^^^^^^^^^^^^^^^^

Next, the pipeline assembles the short reads into longer contigs, by default the **One-click pipeline** uses `velvet <https://www.ebi.ac.uk/~zerbino/velvet/>`_. Two alternatives `SPAdes <http://bioinf.spbau.ru/spades>`_ and `VICUNA <http://www.broadinstitute.org/scientific-community/science/projects/viral-genomics/vicuna>`_ are provided and can be selected either as individual tools or through the advanced options in the one-click pipeline.

.. image:: manual-pic/de-novo.png

Reference-based scaffolding
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Next, the contigs are assembled into even longer `super-contigs`. This step is a modification from `AMOScmp <http://sourceforge.net/apps/mediawiki/amos/index.php?title=AMOScmp>`_ 

.. image:: manual-pic/amoscmp.png

Reference-independent scaffolding
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This step performs super-contig extension and connection using `SSPACE <http://www.baseclear.com/landingpages/basetools-a-wide-range-of-bioinformatics-solutions/sspacev12/>`_.  At the end of this step, the pipeline will produce a draft genome, which is a multi-fasta usually contains 5~15 contigs, listed in the same order as the reference.

.. image:: manual-pic/sspace.png

Gap closing
^^^^^^^^^^^
This step connects all the contigs in the multi-fasta from the previous step into one linear genome. This is for the convenience of downstream functional analysis.  However, this is **optional** and highly recommended to be done after all the assessment of the draft genome, as the gaps between the contigs could from misassembly, sequencing, genome feature etc. 

.. image:: manual-pic/linear.png 


