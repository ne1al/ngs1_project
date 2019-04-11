# ngs1_project
Root project for the ngs1 course @ NU
#Install SRA toolkit
source activate ngs1
conda install -c bioconda sra-tools 
#Create a new file directory for the assignment
mkdir assign && cd assign
#Download dataset SRA file
wget -c ftp://ftp-trace.ncbi.nih.gov/sra/sra-instant/reads/ByRun/sra/SRR/SRR879/SRR8797509/SRR8797509.sra
# Create a new directory for FASTQC files
mkdir fastqc && cd fastqc
#Converting 5M from SRA to FASTQ format
fastq-dump -X 5000000 /home/nehal/assign/SRR8797509.sra
# Counting result reads
cat SRR8797509.fastq | wc -l
# Splitting unshuffled samples
cd..
mkdir unshuffled && cd unshuffled





