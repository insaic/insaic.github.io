---
title: enums / privateEnum
category: Pipe
order: 1
---

枚举转换，如果使用 `enums` 则枚举文件为 `@global/enums.ts`，如下：

```html
val | enums: 'company'
```

<br>

如果使用 `privateEnum` 则可自定义枚举，如下：

{% highlight html linenos %}
{{emnuText | privateEnum: enums}}
{% endhighlight %}


```typescript
emnuText: string = 'a'

enums: object = {
  a: '1',
  b: 2
}
```

