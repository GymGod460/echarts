# 总结

## 源代码

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script src="./echarts.js"></script>
  </head>
  <body>
    <div id="main" style="width: 500px; height: 500px"></div>
    <script>
      var mycharts = echarts.init(document.getElementById("main"));

      var option = {
        // 标题组件
        title: {
          text: "小王运营账号这些年的粉丝数量",
        },
        // 标题组件
        grid: {
          show: true,
        },
        xAxis: {
          name: "年份",
          type: "category",
          data: ["2018", "2019", "2020", "2021", "2022"],
        },
        yAxis: {
          name: "粉丝数量(人)",
          type: "value",
        },
        series: [
          {
            data: ["12000", "30000", "30300", "40020", "55000"],
            type: "line",
            areaStyle: {},
            label: {},
          },
        ],
      };

      option && mycharts.setOption(option);
    </script>
  </body>
</html>
```

## 效果图

! [效果图](../image/2.1.3.png)

### 组件

#### 标题组件

源代码： title: {
text: "小王运营账号这些年的粉丝数量",
},

<h3 style='color:red;'>扩展属性</h3>
title:{
  text:"主标题",
  subtext:"副标题",       //拓展：副标题
  left:"center", top:10,   //定位 left/center/right，像素/百分比
  textStyle:{color:"#333",fontSize:18}, //主标题文字样式
  subtextStyle:{color:"#666"} //副标题样式
}

![](../yulan/image1.png)

#### 表格组件

源代码： grid: {
show: true,
},

#### 坐标轴组件

xAxis: {
name: "年份",
type: "category",
data: ["2018", "2019", "2020", "2021", "2022"],
},
yAxis: {
name: "粉丝数量(人)",
type: "value",
},

#### 系列组件、

series: [
{
data: ["12000", "30000", "30300", "40020", "55000"],
type: "line",
areaStyle: {},
label: {},
},
],
