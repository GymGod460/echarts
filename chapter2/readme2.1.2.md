# 总结
## 案例代码
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>折叠折线图</title>
    <script src="./echarts.js"></script>

</head>

<body>
    <div id="main" style="width: 900px;height: 
    500px;"></div>
    <script>
        var mychart = echarts.init(document.getElementById("main"));
        var option = {
title:{
   text: '初三某班部分学科学习成绩'
},
legend:{},
xAxis:{
    name:'考试时间',
    type :'category',
    data:['第一次月考','第二次月考','第三次月考','第四次月考']
},
yAxis:{
    name:'成绩',
    type:"value"

},
series:[{
    type:"line",
    name:'语文',
    stack:'a',
    data:[90,80,85,87],
    label:{
        show:true
    }
},
{ type:"line",
    name:'数学',
    stack:'a',
    data:[80,82,85,90],
    label:{
        show:true
    }
},

    { type:"line",
    name:'数学',
    stack:'a',
    data:[80,82,85,90],
    label:{
        show:true
    }},
{ type:"line",
    name:'道德与法治',
    stack:'a',
    data:[85,88,85,90],
    label:{
        show:true
    }
},
{ type:"line",
    name:'物理',
    stack:'a',
    data:[70,80,85,90],
    label:{
        show:true
    }
},

]

};
option&&mychart.setOption(option);
        
    </script>
</body>
```

## 图片展示

![art text](../image/mul%20line.png)

### 图例组件
legend:{
    data:['语文','数学','道德与法治','物理']
}

在 option 根节点配置`legend`对象，`data`数组内容需要和 series 中每个对象的`name`保持一致。
```javascript
legend:{
    data:['语文','数学','道德与法治','物理'],
    top: 0,
    left:'center',
    textStyle:{
        fontSize:20
    }

![art text](![alt text](../yulan/image1.png))
```
### 数据堆叠 
series:[
    {
        type:"line",
        name:'语文',
        stack:'a', //所有系列stack都为a，实现堆叠
        data:[90,80,85,87]
    },
    { 
        type:"line",
        name:'数学',
        stack:'a',
        data:[80,82,85,90]
    }
]
在 series 每个系列里面设置相同的`stack`属性值，相同 stack 值就开启堆叠效果。

### 文本标签label
label:{
    show:true
}
series 内配置`label`对象，设置`show:true`开启在折线上显示数值文本标签。
}