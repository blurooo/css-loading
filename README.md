# H5Loading
一个基于css3的加载Loading，用于ajax等耗时操作的阻塞。纯js编写，不依赖Jquery，兼容所有支持H5的浏览器，css和js文件总大小仅5.7KB，支持定制Loading颜色，遮罩颜色，以及Loading淡入淡出动画时长。适用性强，使用简单方便。

[查看演示](http://chenmuxin.cn/Loading)

# 使用教程：


1. 引入css：`<link rel="stylesheet" type="text/css" href="css/loading.css"/>`
2. 引入js： `<script src="js/loading.js" type="text/javascript" charset="utf-8"></script>`
3. loading向window注册了一个全局对象名：H5_loading。
4. H5_loading对象拥有两个方法：show()和hide()。
5. show()接受一个option对象参数，option允许三个子参数：colorloading圆圈的颜色、background遮罩层的颜色、timeout淡入动画时长(s)。
6. hide()接受一个timeout参数
7. 使用示例：

```
    H5_loading.show();    //默认配置显示loding

    H5_loading.show({color:"#666",background:"rgba(0,0,0.5)",timeout:0.5});    //配置参数显示，允许只配置需要修改的参数

    H5_loading.hide();     //默认配置隐藏loading

    H5_loading.hide(0.5);  //隐藏loading的淡出动画时长修正为0.5s
```

8. 配合ajax使用：

    ```
    $(document).ajaxSend(function(){
        H5_loading.show();
    });
    ```

    ```
    $(document).ajaxComplete(function(){
        H5_loading.hide();
    });
    ```
