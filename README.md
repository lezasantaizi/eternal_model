# eternal_model
ASR-TTS-VC-DF

## 1. 从docker hub上拉取镜像：
docker pull xiaomingren/mycentos:v0.1
## 2. 启动镜像，进行修改：
docker run -it xiaomingren/mycentos:v0.1 /bin/bash

[root@64039bb3f2f1 /]# gcc -v

这个容器是centos8，包含：gcc 8.3.1; python 3.8.5; miniconda3;

## 3. 在拉取下来的镜像上修改之后，提交：
将现有容器生成新的镜像： docker commit -m ”提交信息” 容器ID 镜像名称：tag名称； 
譬如： docker commit -m "test v0.2" 64039bb3f2f1 xiaomingren/mycentos:v0.2
## 4. 上传镜像：(tag 镜像的时候，要加上自己docker hub 的用户名,要不然push会失败) 
docker push xiaomingren/mycentos:v0.2
