# TRF部署指南

# 一、环境准备

### 系统配置

> - 服务器：鲲鹏服务器
> - 操作系统：Huawei Cloud EulerOS 2.0 64bit
> - CPU: 2vCPUs 或更高
> - RAM: 8GB 或更大
> - Disk: 至少 40GB

### 配置编译环境

```
sudo yum update -y
sudo yum install -y gcc make wget
```

# 二、源码下载与编译安装

### 1. 下载并解压TRF-4.09.1源码，下载目录以/home为例

```
cd /home
wget https://github.com/Benson-Genomics-Lab/TRF/archive/refs/tags/v4.09.1.tar.gz
tar -xzf TRF-4.09.1.tar.gz
```

若国内服务器连接github超时，则手动下载。

### 3. 配置与编译安装,指定CPPFLAGS以正确预处理。
默认安装至目录/usr/local/bin中

```
mkdir build
cd build
../configure
make
sudo make install
```

### 4. 删除压缩包和多余文件
```
cd ../../
rm -rf TRF-4.09.1 TRF-4.09.1.tar.gz
```