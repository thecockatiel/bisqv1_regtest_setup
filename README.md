# Quick Regtest

a small repo for quickly setting up a bitcoin regtest network with an electrumx server locally.

contains initial regtest data for bisq dao setup.

## Getting Started

extract `Bitcoin-regtest/regtest` from `dao-setup.zip` to `./data_dirs/bitcoind/regtest`

run `docker compose up -d` to start containers

start your seed nodes. for example using:

```
--genesisBlockHeight=111
--genesisTxId=30af0050040befd8af25068cc697e418e09c2d8ebd8d411d2240591b9ec203cf
--baseCurrencyNetwork=BTC_REGTEST
--useLocalhostForP2P=true
--useDevPrivilegeKeys=true
--nodePort=2002
--appName=bisq-BTC_REGTEST_Seed_2002
--fullDaoNode=true
--isBmFullNode=true
--rpcUser=bitcoin
--rpcPassword=bisq
--rpcPort=18443
--rpcBlockNotificationPort=5120
```

run arbitrator node. for example using:

```
--baseCurrencyNetwork=BTC_REGTEST
--useLocalhostForP2P=true
--useDevPrivilegeKeys=true
--nodePort=4444
--appName=bisq-BTC_REGTEST_arbitrator
```

Open `Account` tab on your arbitrator node and register using `CMD + d` and `CMD + n`
