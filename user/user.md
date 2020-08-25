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
| code    | num  | 返回值   | 0：成功<br />-404：请求错误 |
| message | str  | 错误信息 | 默认为空                     |
| ttl     | num  | 1        |                             |
| data    | obj  | 信息本体 |                             |

`data`中的`user_info`对象：

| 字段        | 类型 | 内容             | 备注                                                         |
| ----------- | ---- | ---------------- | ------------------------------------------------------------ |
| id         | num  | UID              |                                                              |
| username        | str  | 昵称             |                                                              |
| avatar         | num  | 头像             | 0为默认头像，其他为有头像                                                   |
| regtime        | num  | 注册时间         |                                                              |
| message        | num  | 已发布的帖子数             |                                                              |
| status        | num  | 用户状态            | vaild-正常 <br />email-confirm 等待验证邮箱                                           |
| jyz       | num  | 当前经验值         |                                                         |
| ban    | num  | 是否被封禁                | 0：未被封禁 <br />1：已被封禁                                             |
| admin       | num  | 是否为管理                | 0：不是 <br />1：是                                            |
| staff     | num  | 是否为官方人员         | 0：不是<br />1：是                                         |
| warn    | num  | 警告点数            |                                                         |
| reasc       | num  | 反馈分数           |            |
| res  | num | 资源数 |                                  |
| award   | num  | 奖章数         |                                                              |
| coin  | num  | 硬币数         |                                                              |
