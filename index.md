<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
</head>
<body>
<div id="app">
<!--<h2 :style="{key(属性名): value(属性值)}">{{message}}</h2>-->
<!--  50px必须加上单引号，否则当成一个变量去解析-->
<!--  <h2 :style="{fontsiza: '50px'}">{{message}}</h2>-->
<!--  <h2 :style="{fontsiza: finalsize + 'px'}">{{message}}</h2>-->
  <h2 :style="getStyles()">{{message}}</h2>
</div>
<script src="../js/vue.js"></script>
<script>
    const app = new Vue({
        el:'#app',
        data:{
            message:'你好啊',
            finalSize:100,
            finalColor:red
        },
        methods:{
            getStyles: function (){
                return {fontSize: this.finalSize + 'px',backgroundColor: this.finalColor}
            }
        }
    })
</script>
</body>
</html>
