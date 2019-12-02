## 动态风场图层

获取中国范围内的动态风场并渲染在地图上。

### 使用示例（AMap）

```js
var layer = new SenseMap.Windy({
  map: map, // 高德地图map对象
  minVelocity: 0,
  maxVelocity: 10,
  velocityScale: 0.001,
  particleAge: 120,
  lineWidth: 1,
  particleMultiplier: 1 / 300
});
```

### 参数

|       参数名       |  类型  | 默认值  | 必须 |              备注              |
| :----------------: | :----: | :-----: | :--: | :----------------------------: |
|    minVelocity     | Number |    0    |  否  |        最小的风速 (m/s)        |
|    maxVelocity     | Number |   10    |  否  |        最大的风速 (m/s)        |
|   velocityScale    | Number |  0.001  |  否  |           风速的比例           |
|    particleAge     | Number |   120   |  否  | 重绘之前生成的模拟点的最大帧数 |
| particleMultiplier | Number | 1 / 300 |  否  |           模拟点数量           |
|     lineWidth      | Number |    1    |  否  |           拖尾的线宽           |
