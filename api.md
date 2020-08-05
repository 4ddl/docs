# 后端的API接口

## User模块
| url | method | params | data | description |
| --- | --- | --- | --- | --- |
| `/api/user/info` | get | - | - | 请求用户信息 |
| `/api/user/login` | post | - | {"username": "banana", "password":"banana-pass", "captcha":"CAPS"} | 登录验证 |
| `/api/user/register` | put | - | {"username": "banana", "password": "banana-pass", "captcha": "CAPS"} | 注册账号 |
| `/api/user/logout` | delete | - | - | 退出登陆 |
| `/api/user/activate` | put | - | {"id": 1, "code":"657673"} | 验证邮箱 |
