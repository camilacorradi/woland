Install
=======

WOLAND is a multiplatform tool based on Perl and R. Please observe prerequisites and modules and libraries need. 
They must be installed before WOLAND installation. 

Prerequisites
-------------

The following software must be present before installing Woland:

Perl (Minimal recommended Perl version: 5.17)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To check Perl version type::

	$ perl -v 

The following Perl modules should be present:

	* Bio::DB::Fasta
	* Cwd
	* List::Util
	* IPC::System::Simple
	* IPC::Run
	* Parallel::ForkManager
	* Regexp::Common
	* Text::Balanced(>=1.97)
	* Text::Wrap
	* Statistics::R

R (Minimal recommended R version: 3.1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To check R version type (in R)::

	$ R.Version()

The following R packages must be installed:

	* plyr	
	* reshape2
	* ggplot2
	* qqman
	* RColorBrewer
	
Installation
-------------

Installing Perl modules
~~~~~~~~~~~~~~~~~~~~~~~

You can use CPAN to get any missing module. First install cpanm::

	$ sudo cpan App::cpanminus

Them you can install each module::

	$ sudo cpanm Module::Name

Installing R packages
~~~~~~~~~~~~~~~~~~~~~

You can use this following command in R to install each missing library:

$R install.packages(``packagename``)

Installing source WOLAND files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Download last Woland source release in <link>. Woland is provided as a tar.gz file which could be extracted using, for example::

	$ tar -xvzf woland-<version>-install.tar.gz

Woland will be installed inside woland installation folder ``install_dir``.

Copying genome sequences and annotation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Woland needs genome reference sequence and its gene annotation for each organism in the ``$install_dir/genomes`` folder. User should download two files in order to perform its analysis:

.. note:: These files can be downloaded using UCSC database (http://hgdownload.cse.ucsc.edu/downloads.html). See below how to rename them::

	$install_dir/genomes/genome_<genome_version>.fa
	$install_dir/genomes/refseq_<genome_version>.txt

.. warning:: You must rename ``<genome_version>.fa`` and ``refGene.txt`` according to ``<genome_version>``. 

For example:

- hg19::

	$install_dir/genomes/genome_hg19.fa

	$install_dir/genomes/refseq_hg19.fa

- mm10::

	$install_dir/genomes/genome_mm10.fa

	$install_dir/genomes/refseq_mm10.fa
