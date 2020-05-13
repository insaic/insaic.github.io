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

场景范例：

{% highlight html %}
<div (mouseWheelUp)="up($event)" (mouseWheel)="scroll($event)" (mouseWheelDown)="down($event)" mouse-wheel>
</div>
{% endhighlight %}

可以触发三个事件，均非必须，事件类型为 `WheelEvent`。
