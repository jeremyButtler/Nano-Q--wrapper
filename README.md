# Nano-Q--wrapper

Wrapper to run Nano-Q (https://github.com/PresetonLeung/Nano-Q)

Input:

    -fastq:
        - fastq file with reads to detect varaints in
    -ref:
         - fasta file with references to align reads to
    -p:
         - prefix to name everything
    -h:
         - Print help message with all possible commands (there are more options)
Output:

    - file: prefix.bam used with Nano-Q
    - Diretory: prefix, holding output from Nano-Q
    
Run: bash runNanoQ.sh -fastq reads.fastq -ref refs.fasta
    
Required programs:

    - Nano-Q, Some possible locations to install
        - In home directory (~)
        - Or puth this script in Nano-Q directory
    - samtools
    - minimap2
