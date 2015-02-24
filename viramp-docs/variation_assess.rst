Post-Assembly Process: Assessment and Variation Analysis
=====================

VIRAmp not only provides all the processes related with assembly, the platform also integrates multiple tools for post-assembly processing, including quality assessment and variation analysis.

QUAST REPORT
------------

It is important to evaluate how robust the new assembly is, before feeded it into the downstream functional analysis.  VIRAmp first provides a report of common assembly evaluation metrics based on comparisons with reference. A detailed `QUAST report <http://bioinf.spbau.ru/quast>`_ can be downloaded.

The input is the reference genome and newly created assembly.

.. image:: assess-pic/quast-input.png

Primary output is a summary of common assembly evaluation metrics.

.. image:: assess-pic/quast-basic.png

Alternatively, a full QUAST report can be downloaded for more details.

.. image:: assess-pic/quast-download.png

Unzip and open the report.

.. image:: assess-pic/quast-unzip.png

A demonstration of a QUAST plot:

.. image:: assess-pic/quast-demo.png

Assembly-Reference Alignment
----------------------------

VIRamp provides information about the difference between the reference and new assembly based on the MUMmer alignment.  Coordinates and percentage identities are provided for each aligned region between two sequences.  It helps the users to identify large INDELs as well as other complex structure and variations. Table 1 demonstrates an example of the comparison report.

.. image:: assess-pic/ref-assembly.png

Circos graph visualization
--------------------------

To help the users further understand the information provided above (Assembly-Reference Alignment), visualization is provided. Circos projects the assembled draft genome to the aligned part of reference, creating a straightforward visualization for large structural variation.

.. image:: assess-pic/comparison_circos.png

SNP analysis
-------------

With the alignment between assembly and reference, SNP information is also provided in VCF format.

.. image:: assess-pic/snp.png

Repeat and Tandem repeat analysis
---------------------------------

By aligning the assembly against itself, VIRAmp also provides repeat and tandem repeat information. The starting coordinates and length are dervied from this alignment.

.. image:: assess-pic/tandem-repeat.png

BWA aligner
-----------

Besides all the specific tools listed above, general tools like `bwa <http://bio-bwa.sourceforge.net/>`_ are also provided for use based on users' own needs. 
