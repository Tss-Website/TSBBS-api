## 用户详细信息
> http://api.tsfk.top/x/user/

*请求方式：GET*

认证方式：Cookie（SESSDATA）

**url参数：**

| 参数名 | 类型 | 内容        | 必要性 | 备注 |
| ------ | ---- | ----------- | ------ | ---- |
|  id    | num  | 目标用户UID | 必要   |      |

**json回复：**

根对象：

| 字段    | 类型 | 内容     | 备注                        |
| ------- | ---- | -------- | --------------------------- |
| code    | num  | 返回值   | 0：成功<br />-400：请求错误 |
| message | str  | 错误信息 | 默认为空                     |
| ttl     | num  | 1        |                             |
| data    | obj  | 信息本体 |                             |

`data`中的`user_info`对象：

| 字段        | 类型 | 内容             | 备注                                                         |
| ----------- | ---- | ---------------- | ------------------------------------------------------------ |
| id         | num  | UID              |                                                              |
| username        | str  | 昵称             |                                                              |
| avatar         | str  | 头像             | 0为默认头像，其他为有头像                                                   |
| face        | str  | 头像链接         |                                                              |
| sign        | str  | 签名             |                                                              |
| rank        | num  | 10000            | **作用尚不明确**                                             |
| level       | num  | 当前等级         | 0-6级                                                        |
| jointime    | num  | 0                | **作用尚不明确**                                             |
| moral       | num  | 0                | **作用尚不明确**                                             |
| silence     | num  | 封禁状态         | 0：正常<br />1：被封                                         |
| birthday    | str  | 生日             | MM-DD                                                        |
| coins       | num  | 硬币数           | 需要登录(Cookie) <br />只能查看自己的<br />默认为0           |
| fans_badge  | bool | 是否具有粉丝勋章 | false：无<br />true：有                                      |
| official    | obj  | 认证信息         |                                                              |
| vip         | obj  | 大会员信息       |                                                              |
| pendant     | obj  | 头像框信息       |                                                              |
| nameplate   | obj  | 勋章信息         |                                                              |
| is_followed | bool | 是否关注此用户   | true：已关注<br />false：未关注<br />需要登录(Cookie) <br />未登录恒为false |
| top_photo   | str  | 主页头图链接     |                                                              |
| theme       | obj  | 空               | **作用尚不明确**                                             |
| sys_notice  | obj  | 系统通知         | 无内容则为空                                                 |
