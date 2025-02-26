# snpEff_fusion

## download database
```
java -jar snpEff.jar download GRCh38.p14
```
## run annotation
```
java -Xmx32g -jar snpeff-5.2-0/snpEff.jar ann GRCh38.p14 SD250738.genotyped.sv.vcf > SD250738.genotyped.sv.ann.vcf
```
