ntCard 
=
ntCard is a streaming algorithm for cardinality estimation in genomics datasets. As iput it takes file(s) is fastq, fastq, sam , or bam formats and computes the k-mer coverage frequency histogram.  

# Build the binary for ntcard
Run:
```
$ make
```
# Run ntcard
```
ntcard [OPTIONS] ... [FILE]
```
Parameters:
  * `-k`,  `--kmer=SIZE`: the length of k-mer used for runtime test hashing `[64]`
  * `-t`,  `--threads=N`: use N parallel threads `[1]`
  * `-c`,  `--cov=N`: the maximum coverage of kmer in output `[64]`
  * `FILE`: is the input file or set of files sepreted by space in fasta, fastq, sam, bam formats. The files can also be in compressed (.gz, .bz2, .xz) formats . A list of files containing file names in each rows can be passe with @ prefix.
  
For example to run ntcard on a test file `reads.fastq` with `k=50`:
```
$ ntcard -k50 reads.fastq 
```
