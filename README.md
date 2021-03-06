# Go library for easy usage of PhenixChain
[![Build Status](https://travis-ci.org/PhenixChain/phenix-go.svg?branch=dev)](https://travis-ci.org/PhenixChain/phenix-go)

# API
* [创建账户](#创建账户)  
* [查询](#查询)  
    * [账户](#账户)  
    * [交易](#交易)  
* [广播](#广播)  
    * [交易](#交易)  

## 创建账户
```
公钥前缀: pub
地址前缀: adr
```
参考: [bip39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)
[bip44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki)
[bech32](https://github.com/bitcoin/bips/blob/master/bip-0173.mediawiki#Bech32)

## 查询
### 账户
```
http://127.0.0.1:26657/abci_query?path="/store/acc/key"&data=<Address HexString>
Address HexString 如: 0x01524c0ddd8582f3f6ac04b5a5b56760f9f204b1da
```
### 交易
```
http://127.0.0.1:26657/tx?hash=<TX HASH>
TX HASH 如: 0xBB83B9A3A0D41CF0FAB1933F08CD6FD7000F28CB04AAEAD30FDF70BE466D3714

http://127.0.0.1:26657/abci_query?path="/store/address/key"&data=<Address HexString>
Address HexString 如: 0x01524c0ddd8582f3f6ac04b5a5b56760f9f204b1da
```

## 广播
### 交易
```
http://127.0.0.1:26657/broadcast_tx_sync?tx=<Hex SignData>
```