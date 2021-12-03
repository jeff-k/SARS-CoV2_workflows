# SARS-CoV2_workflows


## Illumina Viridian workflow
These are the commands used for running the workflow on a GPAS stack in OCI. Data should be stored in an object store and described in the csv file. This is passed to `--objstore`.
```bash
nextflow run /data/pipelines/SARS-CoV2_workflows/main.nf \
	--seq_tech illumina \
	-profile singularity \
	-process.executor slurm \
	--objstore /tmp/illumina_data.csv \
	--TESToutputMODE true \
	--outdir /work/output/illumina_viridian_test
```

## Nanopore Viridian workflow
These are the commands used for running the workflow on a GPAS stack in OCI. Data should be stored in an object store and described in the csv file. This is passed to `--objstore`.
```bash
nextflow run /data/pipelines/SARS-CoV2_workflows/main.nf \
	--seq_tech nanopore \
	-profile singularity \
	-process.executor slurm \
	--objstore /tmp/illumina_data.csv \
	--TESToutputMODE true \
	--outdir /work/output/illumina_viridian_test
```
