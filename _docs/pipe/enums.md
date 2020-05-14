---
title: enums / privateEnum
category: Pipe
order: 1
---

枚举转换，如果使用 `enums` 则枚举文件为 `@global/enums.ts`，如下：

<div class="language-html highlighter-rouge">
  <div class="highlight">
    <pre class="highlight">
      <code>
      {{val | enums: 'company'}}
      </code>
    </pre>
  </div>
</div>

<br>

如果使用 `privateEnum` 则可自定义枚举，如下：

<div class="language-html highlighter-rouge">
  <div class="highlight">
    <pre class="highlight">
      <code>
      {{emnuText | privateEnum: enums}}
      </code>
    </pre>
  </div>
</div>

```typescript
emnuText: string = 'a'

enums: object = {
  a: '1',
  b: 2
}
```

