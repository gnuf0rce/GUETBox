*  [API NAME] 

    > 登陆账号提交接口

---
* [API DESCRIPTION]

    > url: /Login/SubmitLogin
    > 
    > method: POST
    > 
    > note: 
    > 根据输入的账号密码和验证码进行登陆，不用指定用户类型。
    > 用户识别优先级为管理员 > 教师 > 学生
    > 提交成功后会将当前cookie设置为对应账号权限。

---
* [API ARGUMENTS]

    > Name | type | info | example
    > :---:|:---:|:---:|:---:
    > us | string | 用户名 | 19003001
    > pwd | string | 密码 | 003001
    > ck | char(4) | 验证码 | 7846

--- 
* [RETURN DATA]
  
    > type: json
    > example: {"success": true, "msg": "操作成功", "data": "2" }
    > format:
    > > Name | Type | Info | example
    > > :---:|:---:|:---:|:---:
    > > sucess | bool | 操作是否成功 | true <br> false
    > > msg | string | 提示信息 | "操作成功" <br> "验证码不正确" <br> "用户或密码错误!"
    > > data | int | 用户类型 | 0: 管理员 <br> 1: 教师 <br> 2: 学生




