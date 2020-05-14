---
title: $app
category: Service
order: 1
---

注入方式，注入名称使用 `$app`，禁止使用其它名称

```typescript
//从 @global 引入
import { AppService } from '@global/service/app.service'

//初始化时注入
constructor(private $app: AppService) { }
```

<br />
<br />

###### 1 $app.name

获取当前项目的名称；

```typescript
$app.name
```

返回一个字符串类型，如 base, policy, renew, dim ....


<br />
<br />

###### 2 $app.getUser()

获取当前登陆用户的信息，通过订阅方式获得；

```typescript
this.$app.getUser().subscribe(user => console.log(user))
```

返回一个 `Observable<UserModel>` ，如下：

```typescript
{
  userCode: "sit-test",
  userName: "集成测试",
  password: null,
  userType: "dealer",
  redirect: null,
  newPassword: null,
  confirmPassword: null,
  manufactory: "SVW",
  captcha: null,
  brandCode: "VW"
}
```

<br />
<br />