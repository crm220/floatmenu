# 微信小程序可折叠菜单

![作品显示](show.gif)


1. 把components/menu文件拉入项目中

2. 在.json文件中，添加
 
	```
	{
  		"usingComponents": {
    		"menu": "/components/menu/menu"
  		}
	}
	```

3. 在.wxml 文件,添加以下代码

	>bindmenuItemClick为按钮点击的时候的回调方法  mainmodel是显示的按钮，menulist为折叠的菜单的数组数据
 
	```
	<menu bindmenuItemClick="menuItemClick" mainmodel="{{mainmodel}}" menulist ="{{menulist}}" ></menu>

	```
4. 在.js里面实现方法
 
	```
	 ,menuItemClick:function(res){
	    console.log(res);
	    //获取点击事件的信息
	    let clickInfo = res.detail.iteminfo 
	    console.log(clickInfo);
	    // 根据不同类型进行判别处理
	    //事件的处理 代码

	  }
	```
>data中根据自己的情况添加数据

```
    menulist:[
      {
        "id":"1",
        "url":"../../images/top.png",
        "title":"顶部",
      },
      {
        "id": "2",
        "url": "../../images/add.png",
        "title": "添加",
      },
      {
        "id": "3",
        "url": "../../images/buy.png",
        "title": "购物车",
      },
    ],
    mainmodel:{
      "url": "../../images/home.png",
      "title": "菜单",
    }
```

完毕！O(∩_∩)O~~
