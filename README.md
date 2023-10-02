# Running-cell-ranger-on-cluster
# log in to cluster
# type PW
# set_Path
export PATH=/home/ch250798/yard/apps/cellranger-7.1.0:$PATH
# check it by 
which cellranger
# move each fastaq.gz file to its specific folder and for sample type excicsting sample name which is the first name of the fastaq file
cellranger count --id sample1 --transcriptome refdata-gex-mm10-2020-A --fastqs CD1_S57/ --sample=sample1 --expect-cells 10000 --localcores 8 --localmem 16
# this might take more than one hour to complete per sample
