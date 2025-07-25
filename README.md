# UCE_Aphidae_Phylogeny

## Outline 
* NCBI and BIPAA genome assembly downloads
* Pyluce UCE locating with hymenoptera-v2 bait set
* Pyluce UCE seequence extraction with lastz phyluce results
* MSA alignment and clustering with MAFFT via the Orthofinder pipeline
* RAXML tree generation with the MSA alignments as inputs


### NCBI and BIPAA genome assembly downloads

BIPAA genomes were obtained by runnin the script Get_BIPAA_links which would use the base layer of each species on the download portion on the website and search up to three layers deep for fasta genome assemblies

The list of returned links were then manually filtered to ensure only the newest version of each genotype was used.

The file or filtered links was then downloaded with the command below:
```
wget -i  filt-link.curated.list.filt 
```
NCBI refrence aphid genomes were downloaded in a similar way with a seperate script "NCBI_dowload_aphids"

### Pyluce UCE locating with hymenoptera-v2 bait set

Phyluce command ```phyluce_probe_run_multiple_lastzs_sqlite``` was used with the bait set ```/lustre/isaac24/scratch/jtorre28/peluche/hymenoptera-v2-PRINCIPAL-bait-set.fasta.txt```
