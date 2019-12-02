# 使用说明

目前图层产品属于公测阶段，可以免费使用，开始使用之前，你需要至少有一个[免费版](https://www.seniverse.com/products?iid=new)产品，并在使用图层前全局性的设置产品的公钥和私钥，以确保可以正确的获取气象图层数据。

## 设置 accessToken

在使用任何一个图层前，你需要在全局设置 accessToken，将其挂在到浏览器的 window 对象中，在**本地**开发环境中，accessToken 的格式为`公钥_私钥`，**注意**，在**生产**环境中**不**需要提供私钥，accessToken 的格式为`公钥_`

```html
sensemap.accessToken = 公钥_私钥 或 公钥_
```

## js 文件的使用方式

```html
<html>
  <head>
    <!-- 确保你引入了某个地图框架，例如amap -->
    <script src="//cache.amap.com/lbs/static/es5.min.js"></script>
    <script src="//webapi.amap.com/maps?v=1.4.15&key=your_amap_key"></script>
    <!-- 引入相对应地图框架的sensemap地图文件 -->
    <script src="http://cdn.sencdn.com/sensemap/umd/amap.js"></script>
  </head>
  <body>
    <script>
      // 设置 accessToken
      sensemap.accessToken = "公钥_私钥 或 公钥_";
      // 创建想要的图层并加入到map中
      new SenseMap.Temp({ options }).addTo(map);
    </script>
  </body>
</html>
```

## 图层目录

1. 天气要素, [文档](./docs/weather.md), [demo](https://seniverse.github.io/seniverse-map-demos/example/amap/temp.html)
2. 空气质量要素, [文档](./docs/air.md), [demo](https://seniverse.github.io/seniverse-map-demos/example/amap/aqi.html)
3. 动态风场, [文档](./docs/windy.md), [demo](https://seniverse.github.io/seniverse-map-demos/example/amap/windy.html)

## 目前支持地图

- [高德地图](https://lbs.amap.com/api/javascript-api/summary)
- [Leaflet](https://leafletjs.com/index.html)

更多地图的支持我们会逐步增加
