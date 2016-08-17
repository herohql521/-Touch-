# -Touch事件
html5标准新增，跨移动端设备普遍支持的三种基本事件。

  <b>touchstart</b>　　　触摸屏幕时候触发</br>
  
  <b>touchmove</b>　　　滑动屏幕时连续触发</br>
  
  <b>touchend</b>　　　 离开屏幕时触发</br>
  
####每个事件都包3个触摸列表

    1.e.touches　　　　　　当前屏幕上所有手指列表数组
    
    2.e.targetTouches　　　当前DOM元素上手指列表数组
    
    3.e.changedTouches　　　发生改变的手指列表数组
    
  
  
