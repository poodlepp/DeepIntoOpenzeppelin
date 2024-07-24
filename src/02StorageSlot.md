
### getAddressSlot

使用方式
```solidity
using StorageSlot for bytes32;
implementation.getAddressSlot().value
implementation.getBooleanSlot().value
implementation.getBytes32Slot().value
implementation.getUint256Slot().value

implementation(bytes32) 默认作为library  function的第一个参数
结果会格式化为不同的格式
```

支持格式： 使用bytes作为slot号来查询
- address
- boolean
- bytes32
- uint
- string  还支持传入storage指针
- bytes  还支持传入storage指针



