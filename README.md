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
    
    
    
    
    
  
  
