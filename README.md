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
  -racon:
     - Bulid a consensus using racon
     - This is here because I found that Nano-Q sometimes outputs a consensus
       with just N's. This is likely just be for reads simulated with
       badread. Real data may be better.
  -h:
     - Print help message with all possible commands (there are more options)
Output:

  - Diretory: prefix, holding output from Nano-Q
    
Run: bash runNanoQ.sh -fastq reads.fastq -ref refs.fasta
    
Required programs:

  - Nano-Q
    - Some possible locations to install
      - In home directory (~)
      - Put this script in the Nano-Q directory
    - https://github.com/PresetonLeung/Nano-Q (only need to download)
  - racon
    - Only if using -racon
    - https://github.com/isovic/racon
  - samtools
    - Samtools can likely be installed by your OS's package manager.
    - https://github.com/samtools/htslib (install first)
    - https://github.com/samtools/samtools (install second)
  - minimap2
    - https://github.com/lh3/minimap2

Note:

  - This asssumes nothing is installed on a virtual enviroment.
