source activate ngs1
conda install -c bioconda sra-tools
conda install -c bioconda seqkit
#Create a new file directory for the assignment
mkdir assign && cd assign
#Download dataset SRA file
wget -c ftp://ftp-trace.ncbi.nih.gov/sra/sra-instant/reads/ByRun/sra/SRR/SRR879/SRR8797509/SRR8797509.sra
