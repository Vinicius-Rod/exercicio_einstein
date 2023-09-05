# exercicio_einstein
Exercicio comandos-linux
Vinicius Garcia Rodolfo
seq 1 22 | awk '{print("wget -c https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr"$1".fa.gz")}' > pegar-fa.txt
sh pegar-fa.txt
for chr in {1..22}; do zcat "chr${chr}.fa.gz"; done > hg38.fa
grep ">" hg38.fa
