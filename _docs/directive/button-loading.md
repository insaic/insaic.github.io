---
title: button-loading
category: Directive
order: 3
---

为 `button` 元素增加 loading 效果，选择器如下：

```typescript
@Directive({
  selector: 'button[loading]'
})
```

效果：

<img src="{{ site.baseurl }}/images/button-loading.gif" width="200" height="76" />

<br>

HTML 代码：

```html
<button mat-flat-button [loading]="isSearching" (click)="getUser()" color="primary">搜 索</button>
```

脚本：

```typescript
isSearching: boolean = false

getUser() {
  this.isSearching = true
  setTimeout(() => this.isSearching = false, 3000)
}
```