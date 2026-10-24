# 总结

## 案例代码
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 导入ehcarts -->
    <script src="./echarts.js">

    </script>
</head>
<!-- 创建div容器  1 唯一属性 2 宽 高 -->
<div id="main" style="width: 500px ;height: 500px;">
</div>
<script>
    //创建ecahrts实例 要和id对应上
    var mycharts = echarts.init(document.getElementById("main"));

    //创建配置项
    var option = {
        title: {
            text: "用户浏览量变化折线图",
        },
        //坐标轴组件
        xAxis: {
            name: "星期",
            type: "category",
            data: ['周一', '周二', '周三', '周四', '周五', '周六', '周日'],
        },
        yAxis: {
            name: '浏览量（次）',
            type: 'value',
        },
        series: [
            {
                data: [20000, 22000, 25000, 20000, 28000, 24700, 20000],
                type: 'line',
            }
        ]


    };
    option && mycharts.setOption(option);
</script>

<body>

</body>

</html>


## 案例效果图
![alt text](image/line.png)

## 标题组件 text；“ ”
## 坐标轴组件 xAxis name type data   yxAis name type
## 系列组件 seris type‘line’折线图 data一一对应
