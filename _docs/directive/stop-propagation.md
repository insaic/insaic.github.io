---
title: stop-propagation
category: Directive
order: 1
---

用于阻止元素冒泡事件，选择器如下：

{% highlight typescript %}
@Directive({
  selector: "[stop-propagation]"
})
{% endhighlight %}

 范例如下：

{% highlight html %}
 <div (click)="divClick()">
  <a href="javascript:void(0)" (click)="aClick()">Click Me</a>
</div>
{% endhighlight %}

正常情况下，点击 `a` 元素，会先触发 `aClick()`， 也会冒泡触发 `divClick()`，某些时候这可能不符合需求，阻止冒泡如下：

{% highlight html %}
 <div (click)="divClick()">
  <a href="javascript:void(0)" (click)="aClick()" stop-propagation>Click Me</a>
</div>
{% endhighlight %}

这样点击 `a` 元素将不会触发 `divClick()`。
