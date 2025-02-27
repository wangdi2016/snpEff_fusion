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
snpEff -Xmx32g ann GRCh38.p14 SD250738.genotyped.sv.ann.vcf > SD250738.genotyped.sv.ann.vcf

## Extract fusion SVTYPE=BND  EWSR1-ERG fusion gene
grep BND SD250738.genotyped.sv.ann.vcf | grep EWSR1 | grep ERG > SD250738.EWSR1-ERG

```
![Screenshot 2025-02-26 at 8 47 52 PM](https://github.com/user-attachments/assets/d05602ac-8d43-42fc-95e4-4f21fd5a02a3)


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

## Note:
```
## Java version
java --version
openjdk 17.0.10 2024-01-16
OpenJDK Runtime Environment (build 17.0.10+7-Ubuntu-120.04.1)
OpenJDK 64-Bit Server VM (build 17.0.10+7-Ubuntu-120.04.1, mixed mode, sharing)

Error: LinkageError occurred while loading main class org.snpeff.SnpEff
	java.lang.UnsupportedClassVersionError: org/snpeff/SnpEff has been compiled by a more recent version of the Java Runtime (class file version 65.0), this version of the Java Runtime only recognizes class file versions up to 61.0
``` 
