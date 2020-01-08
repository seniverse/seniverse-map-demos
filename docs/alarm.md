## 预警图层

获取正在发生的 12379 国家预警中心发布的预警并展示在地图上，可以以图片和点两种形式进行展示。

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

// 添加预警图层
var layer = new SenseMap.Alarm({
    map: map // 高德地图map实例
    level: '蓝色', // 只展示蓝色等级的预警
    type: '大风' // 只展示大风预警
});
```

### 参数

| 参数名 |                类型                 |  默认值  |                            取值范围                            | 必须 |          备注           |
| :----: | :---------------------------------: | :------: | :------------------------------------------------------------: | :--: | :---------------------: |
|  map   |               Object                |    -     |                               -                                |  是  | 高德地图的 map 实例对象 |
| level  | [Level](./common.md#预警等级-level) | 全部等级 |                           见类型说明                           |  否  |  只展示需要的预警等级   |
|  type  |  [Type](./common.md#预警等级-type)  | 全部类型 |                           见类型说明                           |  否  |  只展示需要的预警类型   |
|  city  |               String                |    -     | [心知城市 V3](https://docs.seniverse.com/api/start/start.html) |  否  |    只展示需要的城市     |
|  mode  |               String                |  point   |                         point 或 image                         |  否  |  图片形式展现或点形式   |

### 方法

#### show()

显示图层

#### hide()

隐藏图层

#### updateParams(config)

更新相关参数，只支持下面展示的参数:

```js
layer.updateParams({
  level: "蓝色",
  type: "大风",
  city: "WX4FBXXFKE4F"
});
```
