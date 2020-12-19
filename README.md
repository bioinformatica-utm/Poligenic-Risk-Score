# prs
# Polygenic Risk Score
# R
# pregătim datele statistice GWAS pentru bază
summary.statistics.gwas<-read.table(gzfile("CATH.bgz"), header = T, stringsAsFactors = F, sep="\t")
variant.info<-read.table(gzfile("variants.bgz"), header = T, stringsAsFactors = F, sep="\t")
cath<-merge(summary.statistics.gwas, variant.info, by="variant")
rm(summary.statistics.gwas)
rm(variant.info)

