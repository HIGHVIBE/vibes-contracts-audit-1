# vibes-contracts-audit-1

# VIBES upgradable Token contract, its TransparentUpgradeableProxy and a vesting contract

## Introduction

In this audit request our purpose is to audit our VIBES Token contract and its supplementary contracts.

Our Token contract:
`VIBESToken.sol`

our proxy contracts to make our token upgradable:
`VIBESProxy.sol`
`VIBESProxyAdmin.sol`

and our vesting contract to create new vesting logics for developers, shareholders etc.
`VIBESVesting.sol`

## Tech stack

[**OpenZeppelin**](https://openzeppelin.com/) - verified market standards

[**Remix IDE**](https://remix.ethereum.org/) - for deployment tests

## Deployment steps

Deployment order is as follows:

1. Deploy and initialize VIBESToken.sol with "name: VIBES, symbol: VIBES and 21 Billion * 10^18 totalSupply"
2. Deploy VIBESProxyAdmin.sol
3. Deploy VIBESProxy.sol
4. Change the proxy address on the Admin contract
5. Deploy VIBESVesting.sol with the VIBES Token address and transfer VIBES Tokens to the Vesting address.
6. Now you can create new vesting logics on the vesting contract


