# download_sra
sra-tools 2.11.1 [docker](https://hub.docker.com/r/ncbi/sra-tools)


input: SRR000001

output: fastq file


## 需要先pull docker images
docker pull ncbi/sra-tools:2.11.1


### 一次會開啟一個container，注意記憶體容量！


chmod u+x processSRA.sh 

./processSRA.sh -h

./processSRA.sh -f SRR000001


#### 將accession存在file
```
for i in $(cat file)
do
        ./processSRA.sh ${i}    
done
```
