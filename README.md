# Bcftools
Work with VCF files/convert them to BED files

First you need to upload the entire folder with files to the directory /home/YOUR_NAME/bcftools-1.9/
Then run this command if you need to convert many files

example:
```
for t in /home/YOUR_NAME/bcftools-1.9/NAME_FOLDER/*
do 
         bcftools query -f'%CHROM\t%POS0\t%END\t%ID\n'  $t > $t.bed
done
```
This command converts your file and gives the output columns: CHROM, POS0, END, ID.
You can change the name of the columns
