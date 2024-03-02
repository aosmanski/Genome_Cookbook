We’ll give them a combined fasta with their assemblies

mafft --auto --thread 1 mulberry_chloroplast_combined.fa > mulberry_chloroplast_combined.temp.aln
awk '/^>/{print (NR==1)?$0:"\n"$0;next}{printf "%s", $0}END{print ""}' mulberry_chloroplast_combined.temp.aln > mulberry_chloroplast_combined.aln
rm mulberry_chloroplast_combined.temp.aln
