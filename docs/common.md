# 天气要素-element

天气要素 element 参数包含以下取值：

|  参数值  | 说明 |
| :------: | :--: |
|   rain   | 降水 |
|   wind   | 风速 |
|   temp   | 温度 |
| humidity | 湿度 |

# 空气质量要素-element

空气质量要素 element 参数包含以下取值：

| 参数值 |   说明   |
| :----: | :------: |
|  aqi   | 空气质量 |

# 自定义图例-legend

如果需要自定义图例，您需要提供一个 legend 数组，形式如下：

```js
const colors = [
  "rgba(30, 35, 137, 1)",
  "rgba(66, 184, 65, 1)",
  "rgba(255, 95, 89, 1)",
  "rgba(133, 61, 255, 1)",
  "rgba(117, 21, 45, 1)",
  "rgba(100, 111, 42, 1)"
];

// 每个阈值对应的颜色
const values = [0, 100, 200, 300, 400, 500];

// 复制给legend属性
legend = [colors, values];
```

具体使用可以参阅[案例](https://seniverse.github.io/seniverse-map-demos/example/amap/custom.html)
