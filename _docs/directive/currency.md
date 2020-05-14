---
title: currency
category: Directive
order: 4
---

输入框只能输入数字，可包含小数，选择器如下：

```typescript
@Directive({
  selector: '[currency][ngModel]',
  providers: [NgModel]
})
```

<br>

范例：

```html
<mat-form-field>
  <input matInput currency type="number" [max]="100" [min]="10" [point]="3" [(ngModel)]="Req.money" />
</mat-form-field>
```

支持三个属性：

* \[max]: 限制最大值，非必须；
* \[min]: 限制最小值，非必须；
* \[point]: 支持几个小数点，非必须，默认为 2，如果为 0 则表示只能输入整数；