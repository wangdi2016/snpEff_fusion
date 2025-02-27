# snpEff_fusion

https://pcingola.github.io/SnpEff/snpeff/introduction/

## Use mamba
```

## create mamba env
mamba create -n snpeff

## use snpeff env
mamba activate snpeff

## install snpeff via bioconda
mamba install snpeff -c bioconda

## check Human Genome
snpEff databases | grep Human | cut -f1

## use GRCh38.p14 Human genome GRCh38 using RefSeq transcripts
snpEff download GRCh38.p14

## run snpEff
snpEff ann GRCh38.p14 sv.vcf > sv.ann.vcf
```

## Directly download snpEff

```
1. ## download snpEff

wget https://snpeff.blob.core.windows.net/versions/snpEff_latest_core.zip

2. ## unzip
unzip snpEff_latest_core.zip
cd snpEff

3. download database Note: java version should be more than xxx

java -jar snpEff.jar download GRCh38.p14

4. ## run annotation

java -Xmx32g -jar snpeff-5.2-0/snpEff.jar ann GRCh38.p14 sv.vcf > sv.ann.vcf
```
