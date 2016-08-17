# -Touch事件
html5标准新增，跨移动端设备普遍支持的三种基本事件。

  <b>touchstart</b>　　　触摸屏幕时候触发</br>
  
  <b>touchmove</b>　　　滑动屏幕时连续触发</br>
  
  <b>touchend</b>　　　 离开屏幕时触发</br>
  
####每个事件都包3个触摸列表数组

    1.e.touches　　　　　　当前屏幕上所有手指列表数组
    
    2.e.targetTouches　　　当前DOM元素上手指列表数组
    
    3.e.changedTouches　　　发生改变的手指列表数组
    
####这些数组由包含触摸信息的对象组成
    
    identifier：　　　　标识触摸的唯一ID
    
    target：　　　　　　触摸的dom目标节点
    
    clientX：　　　　　触摸目标在视口中的x坐标
    
    clientY：　　　　　触摸目标在视口中的y坐标
    
    pageX：　　　　　　触摸目标在页面中的x坐标
    
    pageY：　　　　　　触摸目标在页面中的y坐标
    
    screenX：　　　　　触摸目标在屏幕中的x坐标
    
    screenY：　　　　　触摸目标在屏幕中的y坐标
    
####下面展示一个用touchmove实现的单指拖拽块元素的效果 [demo](https://herohql521.github.io/HTML5-Touch-Events/drag.html)

```javascript
<script>
	var drag = document.getElementById("drag");
	drag.addEventListener('touchmove',function(event){
		event.preventDefault();
			if(event.targetTouches.length==1){
				var  touch = event.targetTouches[0];
				//钯元素放在手指所在的位置
				drag.style.left = touch.pageX + "px";
				drag.style.top = touch.pageY + "px";
			}
		},false)
</script>
```

####用touchend　touchstart　来判断滑动方向

  用到了Math.atan2(y,x)方法,返回从X轴正向到(x,y)之间的角度，值介于-PI和PI之间
  
  
  ![img](https://herohql521.github.io/HTML5-Touch-Events/atan2.jpg)
  
  如果　45°<滑动角度<135° 　则返回 　向上滑
  
  如果　-45°<=滑动角度<=45°　则返回　向右滑
  
  如果　-135°<=滑动角度<-45°　则返回　向下滑
  
  如果　-180°<=滑动角度<-135°　&&　135°<=滑动角度<=180°　向左滑


    
    
    
  
  
