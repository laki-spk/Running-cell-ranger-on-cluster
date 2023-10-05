# Running-cell-ranger-on-cluster
# log in to cluster
# type PW for the cardiology dptment / or your account 3kO82JVb@apps
# to get in to the cardiology account type; you can change number of cores and mem according to the reqyuremnets.
srun -A pcbg -p pcbg-compute --qos=pcbg -c 16 --mem=32G --pty bash 
# set_Path
export PATH=/home/ch250798/yard/apps/cellranger-7.1.0:$PATH
# check it by 
which cellranger
# move each fastaq.gz file to its specific folder and for sample type excicsting sample name which is the first name of the fastaq file (Folder name = CD1_S57 AND INSIDE THERE WE CAN FINE r001 AND r002 FILES)
# cellranger count --id <folder_name> --transcriptome <Path to referencedata> --fastqs <Path to fastq files> --sample=<PREFIX> (optional)
cellranger count --id sample1 --transcriptome /home/ch250798/yard/refdata-gex-mm10-2020-A/ --fastqs /home/ch250798/yard/CD1_S57/ --sample=CD1 --expect-cells 10000 --localcores 8 --localmem 16
# this might take more than one hour to complete per sample
# open the html file: it will give the t-SNE files and also about the quality of the samples
# Final data will be in the sample_directory/outs/filtered_feature_bc_matrix
# create a csv file by using sample id and molecule.info.h5 file path as shown in https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/using/aggregate#creating_categories
# cd to the working directory 
cellranger aggr --id <AGG123> --csv <AGG123_libraries.csv>
