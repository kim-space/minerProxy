## 服务器厂商选择

服务器务必选择不实名境外的,不要买腾讯，阿里，华为这类的,容易嗅探检测并且收到监管,目前国内受政策影响，这些服务器都会收到监控, 可从一下选择购买, 都买过实际测试过,线路延迟等方面都没问题.

[恒创](http://my.henghost.com/aff.php?aff=7708)

[快云](https://www.345idc.com/)

[衡天云](https://my.htstack.com/aff.php?aff=6019)

[LocVPS](https://my.locvps.net/page.aspx?c=referral&u=43845) 专业VPS商，CN2+BGP线路非常好,但需要个人实名认证, 介意勿买



# 全新桌面版
## 中转+抽水聚合版本
![Snipaste_2021-12-27_14-07-52](https://user-images.githubusercontent.com/17792707/147440090-7f40ef62-7a1c-4d14-8657-552975b37b31.png)


## 纯中转分离
![Snipaste_2021-12-27_12-24-14](https://user-images.githubusercontent.com/17792707/147434301-faae0497-11dd-4414-a7eb-5489fa4ae173.png)


# 终端配置版
## 代理ethermine的Asia2地区矿池+抽水到(默认抽算力flexpool矿池)
```
minerProxy.exe -pool ssl://asia2.ethermine.org:5555 -port 9001 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 1 -devWorkerName devFee111 -ssl 1
```
> 开启后，接入矿池的地址为:`stratum+ssl://ip:端口`

###### 脚本解释
`-pool ssl://asia2.ethermine.org:5555` 指定需要中转的矿池,此处表示中转的矿池是使用ssl协议，端口为555的ethermine.org的矿池

`-port 9001` 矿出转出端口为9001,即通过本机的该端口可接入上述中转的矿池

`-ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02` 指定抽水算力获得的ETH钱包地址为0x8533551845362F845B6C5FECEF68923A9ef0Fa02

`-devFee 1` 指定抽水算力的比例为1%，支持小数点，最大5

`-ssl 1` 指定是支持ssl安全加密,0为不使用ssl，默认为TCP方式

> 若开启了ssl,即在脚本内写入了`-ssl 1`, 则接入矿池的格式为`stratum+ssl://ip:端口`；若不使用ssl的都则修改成`-ssl 0`，接入矿池的格式为`ip:端口`


-------


## 代理ethermine的Asia2地区矿池+抽水到(抽算力ethermine矿池)
```
minerProxy.exe -pool ssl://asia2.ethermine.org:5555 -port 9002 -devPool ssl://asia2.ethermine.org:5555 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 1  -devWorkerName devFee111 -ssl 
```
> 开启后，接入矿池的地址为:`stratum+ssl://ip:端口`
> 
###### 脚本解释
`-pool ssl://asia2.ethermine.org:5555` 指定需要中转的矿池,此处表示中转的矿池是使用ssl协议，端口为555的ethermine.org的矿池

`-port 9001` 矿出转出端口为9001,即通过本机的该端口可接入上述中转的矿池

`-devPool ssl://asia2.ethermine.org:5555` 指定将算了抽到ethermine矿池,若不带该参数默认为ssl://eth-hk.flexpool.io:5555


`-ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02` 指定抽水算力获得的ETH钱包地址为0x8533551845362F845B6C5FECEF68923A9ef0Fa02

`-devFee 1` 指定抽水算力的比例为1%，支持小数点，最大5

`-ssl 1` 指定是支持ssl安全加密,0为不使用ssl，默认为TCP方式

> 若开启了ssl,即在脚本内写入了`-ssl 1`, 则接入矿池的格式为`stratum+ssl://ip:端口`；若不使用ssl的都则修改成`-ssl 0`，接入矿池的格式为`ip:端口`

-------

## 其他矿池示例

#### hiveon
```
minerProxy.exe -pool ssl://hk-eth.hiveon.net:24443 -port 9010 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### okex欧意
```
minerProxy.exe -pool tcp://stratum.okpool.me:3556 -port 9040 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### 币印
```
minerProxy.exe -pool tcp://eth.ss.poolin.me:1883 -port 9060 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### 鱼池
```
minerProxy.exe -pool tcp://eth.f2pool.com:6688 -port 9030 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
#### flexpool
```
minerProxy.exe -pool ssl://eth-hk.flexpool.io:5555 -port 9020 -ethAddr 0x8533551845362F845B6C5FECEF68923A9ef0Fa02 -devFee 0.5  -devWorkerName devFee111 -ssl 1
```
