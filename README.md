# TPX token smart contract

Topex.io is a crypto-currency exchange with a daily profit distribution between TPX token holders and compensation for trade losses.
It is a complex method that allows to simplify work on exchange and minimize losses in case of unsuccessful trades.

# TPX Token

TPX Token is the utility token that will be used on Topex.io platform and will have right to claim daily profit generated by Exchange.

All transactions outside Topex.io platform are done via Ethereum Smart Contract.

# Compiling and Running
## Preparations

Install the needed components:
- Truffle
- Test RPC

```
$ npm install -g ethereumjs-testrpc
$ npm install -g truffle
```

## Add Node modules
initialize all node components by doing node install
```
$ make init
```

## Compile

Compiling can be done as:
```
$ make
```

## Migrate the Contracts

To migrate the contract, run test RPC on a separate console, and do `make rpc`. Then run `make migrate` to migrate the contracts to the development network.
```
$ make rpc
$ make migrate
```

You should see something similar to below:
```
$ make migrate
truffle migrate --network development
Using network 'development'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  ... 0x77e33af2d950541c869e42d92dd631e1274cba37d4acce77b7c97afb8a98ce2d
  Migrations: 0xbf22b082b6ad2863e4d6bd980c87ebc584c81901
Saving successful migration to network...
  ... 0xf4d031eceba6433d8b4334b7d9719a573b0f4bf67c5b9c0c614a4bccc6e2e8ab
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying TPXToken...
  ... 0x94d275fb32d8ab2a2e1a74f0edbb353673bae83a8933204cb5056feb7f68729b
  TPXToken: 0xbc2edd737da84bfe92efc63da5aa7cfb5b6725b2
  Deploying TPXrowdsale...
  ... 0x541bb7d3c989d5831917d4a3e778d45a0ff52df83eda344a1b4b0f45e229600d
  TPXrowdsale: 0x33f4c9368033b9eba43bdeb1ca1f1928cc9fce1
Saving successful migration to network...
  ... 0x79b713cbea4c255bc46cc64f75c1544ee067c1d58cc191e72447a64062883b9d
Saving artifacts...
$
```