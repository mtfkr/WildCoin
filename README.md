WildCoin - Linux Build Guidance
===============================

Linux e.g. Ubuntu (docker image is fine as well)

Build Dependencies
------------------
```
apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
apt-get install libboost-all-dev

apt-get install software-properties-common
add-apt-repository ppa:bitcoin/bitcoin
apt-get update
apt-get install libdb4.8-dev libdb4.8++-dev
apt-get install libzmq3-dev
```
UI Dependencies
---------------
```
apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler
apt-get install libqrencode-dev
```
Clone WildCoin Repository
----------------
```
apt-get install git
git clone https://github.com/WildCoinNetwork/WildCoin.git
```
Build WildCoin
--------------
```
./autogen.sh
./configure
make
make install
```
Start WildCoin Wallet (incl. Node)
----------------------------------
```
dash-qt -addnode=<IP>
```
