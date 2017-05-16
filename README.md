# Spatial Transcriptomics Transcription Termination Site Package

Different tools processing and analsysis of TAG based TTS data generated from Spatial Transcriptomics datasets.

The package is compatible with the output format of the data generated with the ST Pipeline (https://github.com/SpatialTranscriptomicsResearch/st_pipeline).

### License
MIT License, see LICENSE file.

### Authors
See AUTHORS file.

### Contact
For bugs, feedback or help you can contact Jose Fernandez Navarro <jose.fernandez.navarro@scilifelab.se>

### Installation

To install the ST TS packate just clone or download the repository, cd into the cloned folder and type:

    python setup.py install
    
A bunch of scripts will then be available in your system.
Note that you can always type script_name.py --help to get more information
about how the script works.

### Dependencies

The ST TS package depends on paraclu (link) which you can find
in ext/paraclu (link) with instructions on how to install it but basically you need to:

    cd ext/paraclu
    make
    sudo cp paraclu /usr/local/bin
    sudo cp paraclu-cut.sh /usr/local/bin
    
## Tools

###To generate ST TS peaks from a ST dataset (BED file):

    compute_st_ts.py --min-data-value 20 --max-cluster-size 200 --output peaks.txt st_data.bed
    
###To generate a matrix of ST TS counts from the ST TS peaks:

    tag_clusters_to_matrix.py peaks.txt st_data.bed
    

