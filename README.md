# CryptoZombies.io 

### Lessons learned
- contracts are immutable. Change requires address change.
- smart contracts can interact with other contracts e.g. crypto kitties via Interfaces contructed with address param
- `gas` is computing credit bought for Ether
- invoking functions costs `gas`. Some operations are more costful, e.g. IO operations to `storage`
- `view` functions are read-only and are free of charge if they are `external`
- `now` returns UNIX timestamp
- functions can return multiple arguments, e.g.: `(a,,c,d) = getABCD()`
- Variables declared as `memory` persist only for the time of function invocation and unlike `storage` do not persist
- modifiers works like `decorators`, they can also have arguments, symbol `_;` works similar to `express.js` `next()`
- variables size in `struct` matters, just like in C
- security is essential, inspect your `external` and `public` functions to analyze logic. Keep in mind Ownable `onlyOwner` modifier
- Mappings: `mapping (uint => address) public zombieToOwner;`, usage: `address owner = zombieToOwner[zombieId]`


### Concerns
- Why `ZombieHelper` derives from `ZombieFeeding`?