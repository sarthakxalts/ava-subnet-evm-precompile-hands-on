# Subnet EVM - Precompiles Hands On

```shell
Refer here : https://docs.avax.network/subnets/hello-world-precompile-tutorial
```

```shell
Notes:
  -> Must run yarn in contracts dir for the hardhat to work,
     or else build fails in 'Running E2E Tests' section.

  -> Many a times, if pending txns due to whatever reason, 
     nonce has to be set correctly manually in a transfer txn in metamask,
     so as to clear the pending txns associated with the wallet addr in subnet.

  -> Finally, if you try to simply deploy ExampleHelloWorld.sol contract, the get will work, but set won't.
     The reason is: the set txn is made by the contract and not the admin of hello_world precompile.
     So, either load the IAllowList.sol at hello_world precompile addr(0x030...) & setAdmin for ExampleHelloWorld contract.
     Or somehow in the contract, make the call from the admin of hello_world precompile. [todo]
```


