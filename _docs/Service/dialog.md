---
title: $dialog
category: Service
order: 2
---

注入方式，注入名称使用 `$dialog`，禁止使用其它名称

{% highlight javascript %}
//从 @global 引入
import { DialogService } from '@global/service/dialog.service'

//初始化时注入
constructor(private $dialog: DialogService) { }
{% endhighlight %}

<br />
<br />

###### 1 $dialog.alert()

弹出一个对话框，相当于浏览器内置的 `alert()`

入参如下：

{% highlight javascript %}
alert(text: string, okText?: string)
{% endhighlight %}

* 参数 `text`: 必填，为弹出内容；
* 参数 `okText`: 选填，为确定按钮的显示文本，默认为”确定“；

如果需要回调，则使用订阅方式，范例如下：

{% highlight javascript %}
this.$dialog.alert('You Are OK!', 'OK').subscribe(() => {
  console.log('you clicked ok')
})
{% endhighlight %}

<br />
<br />

###### 2 $dialog.confirm()

弹出一个确认框，相当于浏览器内置的 `confirm()`

入参如下：

{% highlight javascript %}
confirm(text: string, okText?: string, cancelText?: string)
{% endhighlight %}

同上 `$dialog.alert()`，新增一个 `cancelText` 参数为取消按钮的显示文本，选填，默认为”取消“，范例如下：

{% highlight javascript %}
this.$dialog.confirm('Are You OK ?').subscribe(() => {
    console.log('yes, i am ok!')
  }, () => {
    console.log('no, i am bad!')
  }
)
{% endhighlight %}


