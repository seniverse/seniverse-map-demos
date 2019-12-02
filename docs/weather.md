## 天气图层

获取中国范围内的天气要素图层并渲染在地图上,支持降水、风速、温度、湿度四种要素，更多要素逐步增加中。

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

//添加温度图层
const tempLayer = new SenseMap.Temp({ map, time: "2019120216" });

// 或添加降水图层
const rainLayer = new SenseMap.Rain({ map });

// 其他可选
// const layer = new SenseMap.Wind({ map }); 风速
// const layer = new SenseMap.Humidity({ map }); 湿度
```

### 参数

| 参数名 |  类型  |         默认值          | 必须 |                          备注                           |
| :----: | :----: | :---------------------: | :--: | :-----------------------------------------------------: |
|  time  | Number | 当前时刻(如 2019120215) |  否  | 不支持使用小于当前时刻的数值，支持 3 天之内任意小时数据 |
