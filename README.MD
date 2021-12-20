# 全新桌面版
![Desktop](https://user-images.githubusercontent.com/17792707/146715950-a0c99bcc-fad6-4f43-be32-09dcc40823bc.png)


# 终端配置版
## 代理ethermine的Asia2地区矿池+抽水到(默认抽算力flexpool矿池)
```
minerProxy.exe -pool ssl://asia2.ethermine.org:5555 -port 9001 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 1 -devWorkerName devFee111 -ssl 1
```
> 开启后，接入矿池的地址为:`stratum+ssl://ip:端口`

###### 脚本解释
`-pool ssl://asia2.ethermine.org:5555` 指定需要中转的矿池,此处表示中转的矿池是使用ssl协议，端口为555的ethermine.org的矿池

`-port 9001` 矿出转出端口为9001,即通过本机的该端口可接入上述中转的矿池

`-ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52` 指定抽水算力获得的ETH钱包地址为0x8533551845362F845B6C5FECEF68923A9ef0Fa52

`-devFee 1` 指定抽水算力的比例为1%，支持小数点，最大5

`-ssl 1` 指定是支持ssl安全加密,0为不使用ssl，默认为TCP方式

> 若开启了ssl,即在脚本内写入了`-ssl 1`, 则接入矿池的格式为`stratum+ssl://ip:端口`；若不使用ssl的都则修改成`-ssl 0`，接入矿池的格式为`ip:端口`


-------


## 代理ethermine的Asia2地区矿池+抽水到(抽算力ethermine矿池)
```
minerProxy.exe -pool ssl://asia2.ethermine.org:5555 -port 9002 -devPool ssl://asia2.ethermine.org:5555 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 1  -devWorkerName devFee111 -ssl 
```
> 开启后，接入矿池的地址为:`stratum+ssl://ip:端口`
> 
###### 脚本解释
`-pool ssl://asia2.ethermine.org:5555` 指定需要中转的矿池,此处表示中转的矿池是使用ssl协议，端口为555的ethermine.org的矿池

`-port 9001` 矿出转出端口为9001,即通过本机的该端口可接入上述中转的矿池

`-devPool ssl://asia2.ethermine.org:5555` 指定将算了抽到ethermine矿池,若不带该参数默认为ssl://eth-hk.flexpool.io:5555


`-ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52` 指定抽水算力获得的ETH钱包地址为0x8533551845362F845B6C5FECEF68923A9ef0Fa52

`-devFee 1` 指定抽水算力的比例为1%，支持小数点，最大5

`-ssl 1` 指定是支持ssl安全加密,0为不使用ssl，默认为TCP方式

> 若开启了ssl,即在脚本内写入了`-ssl 1`, 则接入矿池的格式为`stratum+ssl://ip:端口`；若不使用ssl的都则修改成`-ssl 0`，接入矿池的格式为`ip:端口`

-------

## 其他矿池示例

#### hiveon
```
minerProxy.exe -pool ssl://hk-eth.hiveon.net:24443 -port 9010 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### okex欧意
```
minerProxy.exe -pool tcp://stratum.okpool.me:3556 -port 9040 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### 币印
```
minerProxy.exe -pool tcp://eth.ss.poolin.me:1883 -port 9060 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### 鱼池
```
minerProxy.exe -pool tcp://eth.f2pool.com:6688 -port 9030 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### flexpool
```
minerProxy.exe -pool ssl://eth-hk.flexpool.io:5555 -port 9020 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa52 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
