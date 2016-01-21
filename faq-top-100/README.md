# 关于 Highcharts 的 100 个常见问题

为了方便大家阅读，这里简单用一张图来说明图表中各个部分的组成及名词解释。

![Highcharts-components](http://static.hcharts.cn/images/hc-anatomy.png)

### 名词解释

 | 名词  | 解释  |
 | ------------- | -------------         |
 | title, subtile| 标题，副标题            |
 | print, download| 打印，下载，这里统称导出 |
 | xAxis, yAxis  | 坐标轴，包含 x 轴和 y 轴 |
 | credits       | 版权信息，水印          |
 | series        | 数据列                 |
 | tooltip       | 数据提示框              |
 | legend        | 图例                  |


## Q：如何去掉水印（即图表中 highcharts.com 字样）

A：通过设置  credits.enabled = false 即可

```
$('#container').highcharts({
    // ...
    credits: {
      enabled: false
    },
    // ...
})
```

## Q：如何增加导出功能（或显示导出按钮）？

A：只需要引入 exporting.js 即可给图表加上导出功能

```
<script src="http://cdn.hcharts.cn/highcharts/modules/exporting.js"></script>
```

同样的，如果你不需要导出功能，不引入这个文件即可；另外，还可以在引入这个文件的情况下，通过配置  exporting.enabled = false 来禁用导出功能。

```
$('#container').highcharts({
  // ...
  exporting: {
    enabled: false
  },
  // ...
});
```

## Q：如果去掉（或不显示）图例（Legend）？

A：通过设置 legend.enabled = false 即可不显示图例，即

```
$('#container').highcharts({
  // ...
  legend: {
    enabled: false
  },
  // ...
})
```

### 相关扩展

在饼图中默认是不显示图例的，可以通过 plotOptions.pie.showInLegend = true 来显示

## Q：
