# vue的生命周期及钩子函数详解

```
1.vue的生命周期，就是从实例被创建开始到实例销毁的过程，
整个过程主要分为八个阶段(生命周期的钩子函数):
创建前(beforeCreate)、已创建(created)、
编译前(beforeMount)、编译后(mounted)、更新前(beforeUpdate)、
更新后(update)、销毁前(beforeDestory)、销毁后(destoryed)
```
```
beforeCreate:function(){
	alert("此时Vue实例被创建，但是却没有开始观测(并监视)数据和初始化事件，也就是说此时只是有一个Vue实例的空壳子")
},
在这期间开始监听data对象数据变化(observe data)及内部事件初始化(init events)
created:function(){//常用，可以用来进行数据的初始化
	alert("此时Vue实例已经被创建，而且完成了数据的观测和事件的初始化")
},
初始化el节点，并编译template，生成html节点，在el上挂载虚拟dom节点
beforeMount:function(){
	alert("模板编译之前，此时还没有将数据挂载到元素上")
},
把数据渲染到虚拟dom里
mounted:function(){//常用，
	alert("模板已经完成了编译和已经挂载，此时才开始渲染界面，并显示到页面上")
},
beforeUpdate:function(){
	alert("实例更新之前,在这里所谓的更新，实例上任意一部分更新均会触发此函数，在这里是更新了数据")
},
updated:function(){
	alert("实例更新之后")
},
beforeDestroy:function(){
	alert("实例销毁之前,所谓的销毁就是该实例所拥有的内存空间被释放和销毁,组件销毁前调用，
    此时将组件上的watchers、子组件和事件都移除掉")
    有关于销毁，暂时还不是很清楚。我们在console里执行下命令对 vue实例进行销毁。
    销毁完成后，我们再重新改变message的值，vue不再对此动作进行响应了。
    但是原先生成的dom元素还存在，可以这么理解，执行了destroy操作，后续就不再受vue控制了。
    this.$destroy();
},
destroyed:function(){
	alert("实例销毁之后")
}
```