# `CrossDomainMessenger` Invariants

## A call to `relayMessage` should succeed if at least the minimum gas limit is supplied and the message does not revert.
**Test:** [`CrossDomainMessenger.t.sol#L138`](../contracts/test/invariants/CrossDomainMessenger.t.sol#L138)

There are two minimum gas limits here: 
- The outer min gas limit is for the call from the `OptimismPortal` to the `L1CrossDomainMessenger`,  and it can be retrieved by calling the xdm's `baseGas` function with the `message` and inner limit. 
- The inner min gas limit is for the call from the `L1CrossDomainMessenger` to the target contract. 


## A call to `relayMessage` should not revert, but should silently fail if the relay gas cannot be reserved.
**Test:** [`CrossDomainMessenger.t.sol#L169`](../contracts/test/invariants/CrossDomainMessenger.t.sol#L169)

There are two minimum gas limits here: 
- The outer min gas limit is for the call from the `OptimismPortal` to the `L1CrossDomainMessenger`,  and it can be retrieved by calling the xdm's `baseGas` function with the `message` and inner limit. 
- The inner min gas limit is for the call from the `L1CrossDomainMessenger` to the target contract. 
