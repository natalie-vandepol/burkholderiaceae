# FriPan

**MOVED TO [https://github.com/drpowell/FriPan]**

## Introduction
FriPan is a web-based tool for exploring the pan-genome of multiple bacterial genomes. FriPan does not perform the ortholog clustering itself, but it can import data from ProteinOrtho5 output files. Each isolate/strain is a row, and there is a columnar position for each gene cluster. You can zoom/scroll through the pan-proteome, and hover over sections to see a description of the gene. 

## Installation

Ensure you have CoffeeScript >= 1.4 installed:

    npm install -g coffee-script

Install the code and run the demo code:

    git clone https://github.com/Victorian-Bioinformatics-Consortium/FriPan
    cd FriPan
    make demo
    ./server.sh
    firefox http://localhost:8030/pan.html

Instead of using the provided Python-based server in `server.sh` 
you can put it all in your `public_html` folder if you are running Apache already.

    make install  # will put in $HOME/public_html/fripan
    firefox http://localhost/~user/fripan/pan.html
    
## Input file
An example ProteinOrtho5 result is provided: `pan.proteinortho.example` and `pan.descriptions.example` .



To view results just rename them `pan.proteinortho` and `pan.descriptions`. You can view other files by naming them with a consistent stem, for example `my-pan1.proteinortho` and `my-pan1.descriptions`.  Then you view them by using the url `pan.html?my-pan1`.  Note the suffix of the filenames are important.

It is also possible to give arbitrary information on strains for sorting or colouring.  See the `pan.strains.example` file for an example.  This is expected to be a tab separated file with the first column named "ID" with the strain names matching those in pan.`proteinortho`.  Create such a tab separated file and put name it `pan.strains`.

### Authors
* David Powell
* Torsten Seemann

### Source
* Github: https://github.com/Victorian-Bioinformatics-Consortium/FriPan
* Website: http://www.vicbioinformatics.com/software.fripan.shtml
