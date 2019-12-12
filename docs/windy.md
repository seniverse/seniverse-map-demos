## 动态风场图层

获取中国范围内的动态风场并渲染在地图上。

### 使用示例（AMap）

```js
var layer = new SenseMap.Windy({
  map: map, // 高德地图map实例
  minVelocity: 0,
  maxVelocity: 10,
  velocityScale: 0.001,
  particleAge: 120,
  lineWidth: 1,
  particleMultiplier: 1 / 300
});
```

### 参数

|       参数名       |   类型   |     默认值     | 取值范围 | 必须 |              备注              |
| :----------------: | :------: | :------------: | :------: | :--: | :----------------------------: |
|        map         |  Object  |       -        |    -     |  否  |    高德地图的 map 实例对象     |
|    minVelocity     |  Number  |       0        |   0-20   |  否  |        最小的风速 (m/s)        |
|    maxVelocity     |  Number  |       10       |   0-20   |  否  |        最大的风速 (m/s)        |
|   velocityScale    |  Number  |     0.001      |  0-0.05  |  否  |           风速的比例           |
|    particleAge     |  Number  |      120       |  0-240   |  否  | 重绘之前生成的模拟点的最大帧数 |
| particleMultiplier |  Number  |    1 / 300     |  0-0.1   |  否  |         模拟点数量系数         |
|     lineWidth      |  Number  |       1        |   1-10   |  否  |           拖尾的线宽           |
|     colorScale     | [String] | 一组白色渐变色 |    -     |  否  | 字符串数组应为合法的颜色字符串 |

### 方法

#### updateParams(config)

更新风场动画相关参数:

```js
layer.updateParams({
  minVelocity: 1,
  maxVelocity: 4,
  velocityScale: 0.002,
  particleAge: 80,
  lineWidth: 2,
  particleMultiplier: 1 / 400,
  colorScale: ["blue"]
});
```

#### show()

显示风场图层

#### hide()

隐藏风场图层

#### start()

开启风场动画

#### stop()

停止风场动画
