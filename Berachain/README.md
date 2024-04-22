# Berachain 熊链测试网搭建


[toc]

[Berachain](https://twitter.com/berachain)


## 参与方式

挖矿

## 推特

[熊链Berachain](https://twitter.com/berachain)

## 背景

Berachain 是一个EVM L1区块链，使用Cosmos SDK构建并由流动性证明共识协议提供支持。Polaris虚拟机 (Polaris VM) 建立在Cosmos SDK之上，Polaris提供对以太坊虚拟机 (EVM) 的支持。这个区块链库是Berachain EVM网络的基础和底板。该链的经济通过三代币结构联系在一起：GAS费用$BERA 、稳定币$HONEY和治理代币$BGT。

这个社交媒体数据不算太高，但是粉丝胜在高质量，同时在推特上面搜索度很高，你可以看到很多推特用户名字后面带个的符合，几乎就是berachain的早期关注者。




## 搭建

服务器自行准备或者参照第一篇[服务器准备](https://github.com/0x000jack)



安装Go 1.20+以上版本，我用的1.21.6：

```bash
cd ~
wget https://go.dev/dl/go1.21.6.linux-amd64.tar.gz
sudo tar -xzf go1.21.6.linux-amd64.tar.gz -C /usr/local/
```

安装以下软件：

```bash
sudo apt-get install golang jq -y
echo 'export PATH=$PATH:/usr/local/go/bin' | tee -a ~/.bashrc
echo 'export PATH=$PATH:$(go env GOPATH)/bin' | tee -a ~/.bashrc
source ~/.bashrc
```


安装Foundry：

```bash
curl -L https://foundry.paradigm.xyz | bash
```

Clone源码并执行：

```bash
cd ~
git clone https://github.com/berachain/polaris
cd polaris
git checkout main
make test-unit
```

启动测试网：

```bash
screen -S polaris
cd ~/polaris
make start
```


参考鸣谢：@tujj99 


原文：<https://github.com/0x000jack/mining/blob/main/Berachain/README.md>

<https://medium.com/@0x000jack/berachain-%E7%86%8A%E9%93%BE%E6%B5%8B%E8%AF%95%E7%BD%91%E6%90%AD%E5%BB%BA-ab3b9827c5af>


