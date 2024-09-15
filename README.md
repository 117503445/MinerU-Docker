# MinerU-Docker

```sh
wget https://github.com/opendatalab/MinerU/raw/master/Dockerfile

# 修改 Dockerfile 镜像源

docker build -t mineru:latest . # 构建镜像
docker tag mineru:latest registry.cn-hangzhou.aliyuncs.com/117503445/mineru
docker push registry.cn-hangzhou.aliyuncs.com/117503445/mineru

docker run --rm -it -v $PWD:/workspace  --gpus=all registry.cn-hangzhou.aliyuncs.com/117503445/mineru /bin/bash
magic-pdf -p ./input -o ./output # 将 input 内的文件转为 output
```
