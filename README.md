# snpEff_fusion
```
1. ## download snpEff

wget https://snpeff.blob.core.windows.net/versions/snpEff_latest_core.zip

2. ## unzip
unzip snpEff_latest_core.zip

3. download database

java -jar snpEff.jar download GRCh38.p14

4. ## run annotation

java -Xmx32g -jar snpeff-5.2-0/snpEff.jar ann GRCh38.p14 SD250738.genotyped.sv.vcf > SD250738.genotyped.sv.ann.vcf
```
