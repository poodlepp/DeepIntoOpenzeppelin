## Arrays.sol

uint256[]   address[]   bytes32[]

定长数组 从第一个slot顺序存放数据
动态数组 第一个slot存放length  第一个item存储在kecaak256(slot first)

- unsafeAccess 返回数组中指定索引的元素值,自行保证pos不会超出
- 支持不同的类型 address uint256 bytes32
- 支持storage  支持 memory
> function unsafeAccess(address[] storage arr, uint256 pos) internal pure returns (StorageSlot.AddressSlot storage)

- findUpperBound
- 第一个大于或等于element的元素的索引值   logn
- 只适用于storage，storage一般用于存储完整数据，memory可以考虑使用其他的库
> findUpperBound(uint256[] storage array, uint256 element)