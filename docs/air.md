## 空气质量图层

获取中国范围内的 AQI 要素图层并渲染在地图上,更多要素逐步增加中。

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

//添加Aqi图层
const aqiLayer = SenseMap.Aqi({ map });
```

### 参数

| 参数名  |                  类型                   |         默认值          |                 取值范围                  | 必须 |                         备注                         |
| :-----: | :-------------------------------------: | :---------------------: | :---------------------------------------: | :--: | :--------------------------------------------------: |
|  time   |                 Number                  | 当前时刻(如 2019120215) |                  0-3 天                   |  否  |             不支持使用小于当前时刻的数值             |
| opacity |                 Number                  |           0.9           |                    0-1                    |  否  |                      图层透明度                      |
|  range  |                [number]                 |         [0,500]         |               不超过默认值                |  否  | 传入需要筛选的数据区间，可以只绘制需要展示的数据范围 |
| legend  | [Legend](./common.md#自定义图例-legend) | 参考 seniverse 官网展示 | [参阅说明](./common.md#自定义图例-legend) |  否  |                    自定义图例数据                    |

### 方法

#### updateParams(config)

更新相关参数:

```js
layer.updateParams({
  opacity: 0.6,
  range: [0, 200]
});
```

#### show()

显示图层

#### hide()

隐藏图层
