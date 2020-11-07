# CryptoCompare

[![Build Status](https://travis-ci.org/aviaviavi/cryptocompare.svg?branch=master)](https://travis-ci.org/aviaviavi/cryptocompare)
[![Hackage](https://img.shields.io/hackage/v/cryptocompare.svg)](https://hackage.haskell.org/package/cryptocompare-0.1.0)

A Haskell wrapper to the public [CryptoCompare API](https://www.cryptocompare.com/api/), a 
source of information and pricing of different crypto currencies. See hackage for API documentation.

## State

This library is usable but not complete. It currently covers a subset of the API.

## To run the project 

1. Download the compiler if necessary in an isolated location
```Haskell
stack setup
```
2.  Build the minimal project
```Haskell
stack build 
```
3.   Run the test 
```Haskell
stack test
```

This should gives you
```
cryptocompare> test (suite: cryptocompare-test)

Testing the library against the live CryptoCompare API
  performs basic example fetches

Finished in 4.5792 seconds
1 example, 0 failures
```

4. Launch a REPL
```Haskell
stack ghci
>fetchCoinSnapshot "BTC" "USD"
```
And we get 
```
Ok, modules loaded: CryptoCompare.
Loaded GHCi configuration from /tmp/haskell-stack-ghci/02e45673/ghci-script
*CryptoCompare CryptoCompare> fetchCoinSnapshot "BTC" "USD"
Right (CoinSnapshot {snapshotAlgorithm = "SHA-256", snapshotProofType = "PoW", blockNumber = 655788, netHashesPerSecond = 1.20173445e11, totalCoinsMined = 1.8536176e7, blockReward = 6.25, aggregatedSnapshotData = AggregatedSnapshot {market = "CCCAGG", fromSymbol = "BTC", toSymbol = "USD", flags = "2049", price = 15528.27, lastUpdate = 1604730898, lastVolume = 2.241e-3, lastVolumeto = 34.795513, lastTradeId = "3138666", volume24Hour = 62943.68, volume24HourTo = 9.772886e8, open24Hour = 15696.56, high24Hour = 15942.35, low24Hour = 15075.18, lastMarket = "binanceusa"}})
```

## Contributing

Contributions in any form are always welcome.
