---
title: $http
category: Service
order: 3
---

注入方式，注入名称使用 `$http`，禁止使用其它名称；

{% highlight javascript %}
//从 @global 引入
import { HttpService } from '@global/service/http.service'

//初始化时注入
constructor(private $http: HttpService) { }
{% endhighlight %}

<br />
<br />

###### 1 $http.search()

获取当前 url 的 GET 参数，返回一个对象；

<br />
<br />

###### 2 $http.post()

默认的 POST 请求，已加入错误处理，返回一个可观察对象；

入参如下：

{% highlight javascript %}
post(url: string, data: any = {}, header: object = {})
{% endhighlight %}

* 参数 `url`: 必填；
* 参数 `data`: 可为空，默认为一个空对象 {}；
* 参数 `header`: 选填，要添加的 header 字段；

如果header 中有字段 `force` 为 `true`，则该请求不进行错误处理，并全文返回；

{% highlight javascript %}
this.$http.post('/dim-api/user', {name: 'dfrrdi'}).subscribe(data => {
  console.log(data)
)
{% endhighlight %}


