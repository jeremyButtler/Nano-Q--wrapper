# Nano-Q--wrapper

Wrapper to run Nano-Q (https://github.com/PresetonLeung/Nano-Q)

Input:

    -fastq:
        - fastq file with reads to detect varaints in
    -ref:
         - fasta file with references to align reads to
    -p:
         - prefix to name everything
    -l:
         - Trim length for Nano-Q.
         - Nano-Q discards and reads shorter then -l, so make sure is a good value.
         - If not provided is shortest reference - 50
    -h:
         - Print help message with all possible commands (there are more options)
Output:

    - Diretory: prefix, holding output from Nano-Q
    
Run: bash runNanoQ.sh -fastq reads.fastq -ref refs.fasta
    
Required programs:

    - Nano-Q, Some possible locations to install
        - In home directory (~)
        - Put this script in the Nano-Q directory
    - samtools
    - minimap2

Note:

    - This asssumes nothing is installed on a virtual enviroment.
