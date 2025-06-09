# AlignmentToVariants
This script converts multiple sequence alignments (in FASTA format) to a list of variants relative to one of the sequences

## Usage `AlignmentToVariants.py` Script

This script identifies amino acid differences and insertions/deletions between sequences in a nucleotide multiple sequence alignment with respect to a specified reference. This was used on core genes in the study to identiify variants associated with resistant phenotypes.

This was tested using Python 3.12+ so please ensure you are running with this version installed

```bash
python3 AlignmentToVariants.py [-h] fasta_file ref_header output_file

positional arguments:
  fasta_file   Input multiple sequence alignment nucleotide FASTA file. Please note that it is expected
               that the header will contain the strain name appended with an equals sign
               e.g. >AnythingYouWant=MyStrainName. The multiple alignment is expected to be in the
               same orientation for each strain starting at the N-terminus (i.e. with the first nucleotide in the positive orientation as the leftmost amino acid in the alignment)
  ref_header   Name of the reference strain appended to respective header e.g. MyStrainName
  output_file  Output TSV file to store the results

options:
  -h, --help   show this help message and exit
```
