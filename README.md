# Ltanmu-gui
sudo mkdir -p build && cd build
sudo cmake -D DEV_MODE=OFF -DMANUAL_SUBMODULES=ON -D BUILD_64=ON -D CMAKE_BUILD_TYPE=Release ..
sudo make -j4


特性：区块奖励0区块后可用，区块生成时间达到240s（双倍门罗币，难度爆低），区块的生成时间变长，难度减小

013c01ff0001ffffffffffff039b2e4c0281c0b02e7c53291a94d1d0cbff8883f8024f5142ee494ffbbd08807121017767aafcde9be00dcfd098715ebcf7f410daebc582fda69d24a28e9d0bc890d1
version
01
unlock time (varint, height, 60 here)
3c
vin length (value in)
01
vin #1 (of 1) type (gen, 0xff)
ff
height for gen input
00
vout length (value out)
01
output #1 (of 1) amount (17592186044415 as varint)
ffffffffffff03
output #1 type (to key, 0x02)
02
output #1 key (32 bytes)
9b2e4c0281c0b02e7c53291a94d1d0cbff8883f8024f5142ee494ffbbd088071    - a1e5b7ce5ce0ada68e2ce3bbb4649d19dbce39f36d3a70e072b35655e92241c4
extra length in bytes (varint, here 33)
21
extra pubkey tag (0x01)
01
transaction pubkey (32 bytes)
7767aafcde9be00dcfd098715ebcf7f410daebc582fda69d24a28e9d0bc890d1     -   eff8c4af28cc92c15c5f477c6afec5c9a4496e7d31a893ba746937acd6c21045



打开钱包的钱包恢复模式：sudo ./ltanmu-wallet-cli --restore-deterministic-wallet
使monerod可以在Windows连接，但只是本地连接：./ltanmud --rpc-bind-ip=0.0.0.0 --rpc-bind-port=48081 --confirm-external-bind