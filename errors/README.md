# Highcharts 内部定义的错误

Highcharts 内部定义了一下常见的错误，并通过控制打印 '#Error xx' 字样，这里是这些错误的收集整理。

## Error 10

### 对数轴的值不能为 0 或负数

下述情况下会发生这个错误：

* 在对数坐标轴中出现值为 0 或负数的情况
* 对数轴的最小值为0 或 小于 0
* 阀值（threshold）设置为 0 或小于 0

## Error 12

## Error 13

### 图表渲染容器（div）不存在

没有指定图表渲染容器或指定的渲染容器不存在。

指定图表容器的方式有两种：

1. $('#container') 的形式
2. chart.renderTo 的形式指定

```
var chart = new Highcharts({
    chart: {
      renderTo: 'container'
    }
})
```

针对 Error 13，请检查页面是否存在 ```<div id="container"></dvi>``` 及 js 代码中是否拼写错误。


## Error 14

### Highcharts 需要的是数值，而不是字符串

这个错误发送的主要原因是你直接将字符串赋值给数据点，例如下面的代码

```
series: [{
  data: ["3", "5", "1", "6"]
}]
```

针对这个问题，可以对字符串进行 ```parseFlot``` 或 ```parseInt``` 处理。

## Error 15

### X 轴数据未排序

在线图及时间轴图表中，X轴数据需要的数据是排好序的（正序和倒序都可以）。

## Error 16

### Highcharts 重复定义


## Error 17

### 执行的图表类型不存在

## Error 18

### 指定的数据轴不存在

## Error 19

### 坐标轴刻度过多

## Error 20

## Error 21

## Error 22

## Error 23
