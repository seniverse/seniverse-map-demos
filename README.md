# 使用说明

目前图层产品属于公测阶段，如果需要测试使用，请联系我们获得试用密钥，包含公钥和私钥。

## 设置 accessToken

在使用任何一个图层前，你需要在全局设置 accessToken，将其挂在到浏览器的 window 对象中，在**本地**开发环境中，accessToken 的格式为`公钥/私钥`，**注意**，在**生产**环境中**不**需要提供私钥，accessToken 的格式为`公钥/`

```html
sensemap.accessToken = 公钥/私钥 或 公钥/
```

## js 文件的使用方式

```html
<html>
  <head>
    <!-- 确保你引入了某个地图框架，例如amap -->
    <script src="//cache.amap.com/lbs/static/es5.min.js"></script>
    <script src="//webapi.amap.com/maps?v=1.4.15&key=your_amap_key"></script>
    <!-- 引入相对应地图框架的sensemap地图文件 -->
    <script src="http://static.sencdn.com/sensemap/umd/amap.js"></script>
  </head>
  <body>
    <script>
      // 设置 accessToken
      sensemap.accessToken = "公钥/私钥 或 公钥/";
      // 创建想要的图层并加入到map中
      new SenseMap.Temp({ options }).addTo(map);
    </script>
  </body>
</html>
```

## 高德地图目录

[所有图层 demo](http://map.seniverse.com/examples/map/temp/index.html)

1. 天气要素, [文档](./docs/weather.md)
2. 空气质量要素, [文档](./docs/air.md)
3. 动态风场, [文档](./docs/windy.md)
4. 等值线图层, [文档](./docs/contour.md)
5. 预警图层, [文档](./docs/alarm.md)
6. 雷达图层, [文档](./docs/radar.md)

## 目前支持地图

- [高德地图](https://lbs.amap.com/api/javascript-api/summary)

更多地图的支持我们会逐步增加，如果您急需某个地图，可以直接和我们联系或 提 issue
