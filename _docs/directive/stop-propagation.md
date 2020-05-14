---
title: stop-propagation
category: Directive
order: 1
---

用于阻止元素冒泡事件，选择器如下：

```typescript
@Directive({
  selector: '[stop-propagation]'
})
```

<br>

范例：

```html
<div (click)="divClick()">
  <a href="javascript:void(0)" (click)="aClick()">Click Me</a>
</div>
```

正常情况下，点击 `a` 元素，会先触发 `aClick()`，  继而冒泡触发 `divClick()`，某些时候这可能不符合需求，阻止冒泡方法如下：

```html
<div (click)="divClick()">
  <a href="javascript:void(0)" (click)="aClick()" stop-propagation>Click Me</a>
</div>
```

这样点击 `a` 元素将不会触发 `divClick()`。
