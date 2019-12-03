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

//添加温度图层
const tempLayer = SenseMap.Aqi({ map });
```
