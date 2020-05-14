---
title: mouse-wheel
category: Directive
order: 2
---

监听在元素上的鼠标滚动事件，选择器如下：

{% highlight typescript %}
@Directive({
  selector: '[mouse-wheel]'
})
{% endhighlight %}

<br>

范例：

{% highlight html %}
<div (mouseWheelUp)="up($event)" (mouseWheel)="scroll($event)" (mouseWheelDown)="down($event)" mouse-wheel>
</div>
{% endhighlight %}

支持三个属性：

* (mouseWheel): 鼠标滚动时触发，非必须；
* (mouseWheelUp): 鼠标向上滚动时触发，非必须；
* (mouseWheelDown): 鼠标向下滚动时触发，非必须；

事件类型均为 `WheelEvent`。
