# graph-pangenome
## PLAN 
### 7/20
1. 冠達：已建好 hisat 環境，初步了解 KIR allele typing pipeline。本週會 review Graph-KIR 碩論，了解的操作細節。
2. 亭堅：調整參數(--cn-individual + --cn-no-diploid)，重跑 twbb 1492 samples，確認跟原本沒下參數結果的差異。
3. 顯鈞：hisat2_extract_snps_haplotypes_UCSC.py debugging.
4. 冠穎：協助顯均建出 hisat graph。


### 07/27
這周主要是顯鈞和冠穎跟大家分享如何安裝、使用 Hisat2，以及介紹加 variant 進 hisat graph 的整個流程。再來是與冠達定下了Project的輪廓，目標是讓他嘗試使用不同的工具，並精進寫程式處理 data 的能力。
1. 顯鈞：<上周>有成功troubleshooting出hisat2_extract_snps_haplotypes_UCSC.py的問題，為官方文檔上的標示錯誤(解壓縮完即可使用的格式多了一步將'chr'去掉反而會產出空檔案)，用解壓縮完的txt即可產出有紀錄點位以及snp的snp files跟haplotypes file了。
<這周>開頭有稍微講解hisat2的整個pipeline以及小觀念，正在幫冠達下載hg19.fasta，檢視hisat2_extract_snps_haplotypes_VCF.py的code，因為其產出與先前一樣為空白的output，因此正在解決，根據目前看到以及之前弘曄學長遇到的問題，推判可能是吃input vcf files時格式出現問題。
2. 冠達：於screen中下載HISAT2所需的檔案、建置graph-KIR的環境；目前跑過並了解一下HISAT2的流程，而project預計使用50個sample去跑graph-KIR，並寫python進行資料統計。
3. 冠穎：繼上次裝好環境載好需要的檔案後，原定要實作hisat-genotype，實作後發現還有些indexes沒有裝好，所以目前就先下載，等載好之後再繼續實作
4. 亭堅：已經重新跑完 TWBB 1492 sample，目前正在對結果，看參數調整後是否仍對結果有影響(預期是沒有)。另外，希望能抓出造成 CN 變 2,4 的原因，並與紅葉討論可能的解決方案。

### 08/03
1. 冠達：經由學長指導解決hisatgenotype的index和samtools的error，預計要跑6組samples的A,B,C,DRB1,DQA目前graph_KIR仍有一些error無法順利跑，有與學長另外約時間解決；理想上希望下周能分享allele typing的結果、graph KIR的method比較結果。
3. 亭堅：(1) 和冠達分享 Graph-KIR 程式，讓他跑看看，目前測試時有遇到問題，會再確認是不是Graph-KIR本身的問題。 (2) 預期針對 TBB 50 samples 做 exon-firtst 的 typing，這部分會請冠達協助。
4. 顯鈞：整理好 hisat2 的流程， command 以及一些說明，若是在跑完 GRAPH-KIR 以及 hisat-genotype 之後希望能用準備好的 fasta 以及 fastq 檔順利產出最終的 output sam 檔
5. 冠穎：解決hisatgenotype的index和samtools的error，最後成功跑出一組HLA-A alleles的結果，後續會跑6組samples的A,B,C,DRB1,DQA，最後會將typing出的結果整理成表格，在下禮拜呈現。











