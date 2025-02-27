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
snpEff -Xmx32g ann GRCh38.p14 sv.vcf > sv.ann.vcf
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
