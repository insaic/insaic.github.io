---
title: $utils
category: Service
order: 3
---

注入方式，注入名称使用 `$utils`，禁止使用其它名称

```typescript
//从 @global 引入
import { UtilsService } from '@global/service/utils.service'

//初始化时注入
constructor(private $utils: UtilsService) { }
```

<br />
<br />

###### 1 $utils.setDocTitle()

设置浏览器页面的标题

入参如下：

```typescript
setDocTitle(title: string)
```

* 参数 `title`: 必填；

<br />
<br />

###### 2 $utils.pureChart()

过滤字符串，只允许数字，字母，中文

入参如下：

```typescript
 pureChart(text: string, length: number = null)
 ```

 * 参数 `text`: 必填；
 * 参数 `length`: 选填，可对字符串进行长度限制；

 返回字符串。

<br />
<br />

###### 3 $utils.isMobile()

判断是否是大陆地区手机号码

```typescript
isMobile(phone: string | number)
 ```

  * 参数 `phone`: 必填；
   
返回布尔值。

<br />
<br />

###### 4 $utils.isPhone()

判断是否是大陆地区固定电话

```typescript
isPhone(phone: string | number)
 ```

  * 参数 `phone`: 必填；
   
返回布尔值。

<br />
<br />

###### 5 $utils.isOrgCode()

判断是否是组织机构

```typescript
isOrgCode(code: string)
 ```

  * 参数 `code`: 必填；
   
返回布尔值。

<br />
<br />

###### 6 $utils.isVin()

判断是否是 vin 码

```typescript
isVin(code: string)
 ```

  * 参数 `code`: 必填；
   
返回布尔值。