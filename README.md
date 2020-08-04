[![Build Status](https://travis-ci.org/tseemann/polisha.svg?branch=master)](https://travis-ci.org/tseemann/polisha)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Don't judge me](https://img.shields.io/badge/Language-Perl_5-steelblue.svg)

:warning: This software is still in early development

# polisha

Correct long read or hybrid genome 
assemblies using Illumina reads

## Introduction

Microbial genome assemblies involving
long reads from Nanopore or Pacbio 
often contain some mistakes due to the
error profile of those technologies.
It is common to use Illumina data to
identify and correct these mistakes
due to the different error profile of
Illumina reads.

## Method

Align reads to the genome and repair
and mistakes identified. ROtate the
genome and repeat, to ensure mistakes
near the ends are not missed. Keep 
repeating this process until no more 
mistakes are found.

## Quick Start

```
% polisha -V
polisha 0.0.1

% polisha -j 4 -f R1.fq -r R2.fq good.fa > better.fa
Correctetions made:
2 substitutions
8 insertions
1 deletions
```

## Installation

### Conda
Install [Conda](https://conda.io/docs/) or [Miniconda](https://conda.io/miniconda.html):
```
conda install -c conda-forge -c bioconda -c defaults polisha # COMING SOON
```

### Homebrew
Install [HomeBrew](http://brew.sh/) (Mac OS X) or [LinuxBrew](http://linuxbrew.sh/) (Linux).
```
brew install brewsci/bio/polisha # COMING SOON
```

### Source

This will install the latest version direct from Github.  You'll need to add
the polisha `bin` directory to your `$PATH`, and also ensure all the
[dependencies](#Dependencies) are installed.

```
cd $HOME
git clone https://github.com/tseemann/polisha.git
$HOME/polisha/bin/polisha -h
```

## Dependencies

* `perl` >= 5.26
* `pilon` >= 0.9.9.18
* `bcftools` >= 1.10
* `minimap2` >= 2.17

## Etymology

The name `polisha` comes from
the verb "polish" which means
to remove imperfections on a 
surface, or to make something
shiny and new looking.

## License

polisha is free software, released under the
[GPL 3.0](https://raw.githubusercontent.com/tseemann/polisha/master/LICENSE).

## Issues

Please submit suggestions and bug reports to the
[Issue Tracker](https://github.com/tseemann/polisha/issues)

## Author

* [Torsten Seemann](https://tseemann.github.io/)
