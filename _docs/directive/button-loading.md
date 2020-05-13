---
title: button-loading
category: Directive
order: 3
---

为 `button` 元素增加 loading 效果，选择器如下：

{% highlight typescript %}
@Directive({
  selector: 'button[loading]'
})
{% endhighlight %}

效果：

<img src="{{ site.baseurl }}/images/button-loading.gif" width="200" height="76" />

<br>

HTML 代码：

{% highlight html %}
<button mat-flat-button [loading]="isSearching" (click)="getUser()" color="primary">搜 索</button>
{% endhighlight %}

脚本：

{% highlight typescript %}
isSearching: boolean = false

getUser() {
  this.isSearching = true
  setTimeout(() => this.isSearching = false, 3000)
}
{% endhighlight %}