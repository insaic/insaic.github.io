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

###### $utils.setDocTitle()

设置浏览器页面的标题

入参如下：

```typescript
setDocTitle(title: string)
```

* 参数 `title`: 必填；

<br />
<br />

###### $utils.pureChart()

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

###### $utils.isMobile()

判断是否是大陆地区手机号码

```typescript
isMobile(phone: string | number)
 ```

  * 参数 `phone`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isPhone()

判断是否是大陆地区固定电话

```typescript
isPhone(phone: string | number)
 ```

  * 参数 `phone`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isOrgCode()

判断是否是组织机构

```typescript
isOrgCode(code: string)
 ```

  * 参数 `code`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isVin()

判断是否是 vin 码

```typescript
isVin(code: string)
 ```

  * 参数 `code`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isEngineNo()

判断是否是发动机编号

```typescript
isEngineNo(code: string)
 ```

  * 参数 `code`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isIdNo()

判断是否是大陆地区身份证号码

```typescript
isIdNo(ID: string)
 ```

  * 参数 `ID`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isPassport()

判断是否符合护照号码格式

```typescript
isPassport(num: string)
 ```

  * 参数 `num`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isBussinessLicense()

判断是否是营业执照

```typescript
isBussinessLicense(num: string)
 ```

  * 参数 `num`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isTaxRegNumber()

判断是否是税务登记号

```typescript
isTaxRegNumber(num: string | number)
 ```

  * 参数 `num`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isCarLicense()

判断是否是车牌

```typescript
isCarLicense(num: string)
 ```

  * 参数 `num`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isEmail()

判断是否是电子邮箱

```typescript
isEmail(mail: string)
 ```

  * 参数 `mail`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.isName()

判断是否是电子邮箱

```typescript
isName(name: string)
 ```

  * 参数 `name`: 必填；
   
返回布尔值。

<br />
<br />

###### $utils.arbitrationText()

判断是否是电子邮箱

```typescript
arbitrationText(texr: string)
 ```

  * 参数 `text`: 必填；
   
返回字符串。

<br />
<br />

###### $utils.fullTwo()

补全两位

```typescript
fullTwo(num: number)
 ```

  * 参数 `num`: 必填；
   
返回字符串，比如 `fullTwo(2)` 返回 '02'。

<br />
<br />

###### $utils.getDate()

格式化日期 

```typescript
getDate(timestamp: string | number | Date, full: boolean)
 ```

  * 参数 `timestamp`: 必填，可以字符串，数组，或者日期；
  * 参数 `full`: 选填，布尔值；
   
返回字符串，默认 yyyy-mm-dd  full为 `true` 则 yyyy-mm-dd hh:mm'。

<br />
<br />

###### $utils.mutilSpaceToOne()

多个空格转成一个空格

```typescript
mutilSpaceToOne(str: string)
 ```

  * 参数 `str`: 必填；
   
返回字符串。

<br />
<br />

###### $utils.replaceNewLines()

多个空格转成一个空格

```typescript
replaceNewLines(str: string)
 ```

  * 参数 `str`: 必填；
   
返回字符串。