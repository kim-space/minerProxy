 高性能以太坊矿池代理中转, SSL/TCP转发加密,支持中转算力拦截,自定义抽水地址和比例
 
 
 # 参数 - 可以自定义矿池和本地端口
-pool      需要代理的矿池地址:端口 默认为ssl://eth-hk.flexpool.io:5555
-port      本地端口 默认为15555
-devPool   抽水目的矿池地址:端口 默认为ssl://eth-hk.flexpool.io:5555
-ethAddr   抽水以太坊地址
-devFee    抽水百分比,最高5 默认为0
-ssl       是否开启ssl,默认为1:开启(强烈建议开启,如果不开启,建议再包一层加密)
 
 # 安装
 
 ## Windows-CMD下矿池代理
 ```
 minermaster.exe -pool ssl://eth-hk.flexpool.io:5555 -port 15555
 ```
 
 ## Liunx下
 
 ### git 安装（若有则跳过）
 
 ######  ubuntu
 ```
apt update
apt install git

```

###### Cenos
```
yum update
yum install git
```

 ### 下载程序
```
git clone https://github.com/kim-space/minerMaster.git

cd minerMaster 

```

### 矿池代理(后台运行)
```
nohup ./minermaster -pool ssl://eth-hk.flexpool.io:5555 -port 15555 &

```

### 后台运行时关闭
```
killall minermaster
```

### 要运行多个代理矿池,设置不同的本地端口即可,例如
```
nohup ./minermaster -pool ssl://asia2.ethermine.io:5555 -port 18888 &

```

## 示例
#### 往0x8533551845362F845B6C5FECEF68923A9ef0Fa52钱包地址抽水0.5%
```
./minermaster -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5

```

## 连接tcp矿池
```
./minermaster -pool tcp://eth-hk.flexpool.io:4444

```