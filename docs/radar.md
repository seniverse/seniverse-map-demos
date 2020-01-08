## 雷达图层

获取中国范围内的雷达数据并展示在地图上。

### 使用示例（AMap）

```js
// 创建高德地图对象
var map = new AMap.Map("map", {
  viewMode: "3D",
  resizeEnable: true,
  zoom: 5,
  center: [113.53450137499999, 34.44104525],
  mapStyle: "amap://styles/dark"
});

// 添加雷达图层
var layer = new SenseMap.Radar({
    map: map // 高德地图map实例
    time: 2020010613 // 时刻
});
```

### 参数

| 参数名  |  类型  |          默认值           | 取值范围 | 必须 |             备注             |
| :-----: | :----: | :-----------------------: | :------: | :--: | :--------------------------: |
|   map   | Object |             -             |    -     |  是  |   高德地图的 map 实例对象    |
|  time   | Number | 当前时刻(如 201912021500) |  0-3 天  |  否  | 不支持使用小于当前时刻的数值 |
| opacity | Number |            0.9            |   0-1    |  否  |          图层透明度          |

### 方法

#### show()

显示雷达图层

#### hide()

隐藏雷达图层

#### updateParams(config)

更新相关参数,仅支持时间:

```js
layer.updateParams({
  time: 201912021505
});
```
