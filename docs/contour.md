## 天气图层

获取中国范围内的天气要素图层并用等值线图的方式展示在地图上, 支持降水、风速、温度、湿度四种要素。

### 使用示例

```js
// 创建高德地图对象
var map = new AMap.Map("map", {
  viewMode: "3D",
  resizeEnable: true,
  zoom: 5,
  center: [113.53450137499999, 34.44104525],
  mapStyle: "amap://styles/dark"
});

// 添加温度图层
const tempLayer = new SenseMap.Contour({
  map,
  element: "temp", // 选择展示的要素
  time: "2019120216"
});
```

### 参数

| 参数名  |                  类型                   |         默认值          | 取值范围 | 必须 |             备注             |
| :-----: | :-------------------------------------: | :---------------------: | :------: | :--: | :--------------------------: |
|   map   |                 Object                  |            -            |    -     |  是  |   高德地图的 map 实例对象    |
| element | [Element](./common.md#天气要素-element) |           无            |    -     |  是  |      需要展示的天气要素      |
|  time   |                 Number                  | 当前时刻(如 2019120215) |  0-3 天  |  否  | 不支持使用小于当前时刻的数值 |
| opacity |                 Number                  |           0.9           |   0-1    |  否  |          图层透明度          |

### 方法

#### updateParams(config)

更新相关参数，只支持下面展示的参数:

```js
layer.updateParams({
  element: "wind",
  opacity: 0.6,
  time: "2019120217"
});
```

#### show()

显示图层

#### hide()

隐藏图层
