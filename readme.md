# 接口文档

## 登录注册

### 发送短信

- 请求方式：GET

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appregister?phone=15102724518`

  - 参数说明

    ```
    phone 电话号码

    ```

- 返回结果：

  - 正常

    ```json
    {
      "code": "0000",
      "data": "success"
    }
    ```

  - 错误

    ```
    u003 //验证码发送失败
    u004 //用户已经存在
    ```

### 注册

- 请求方式：POST

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appregister`

  - 参数说明

    ```
    phone //手机号
    password //密码
    code //验证码
    nickname //昵称
    ```

- 返回结果：

  - 正常

    ```json
    {
        "code": "0000",
        "data": {
            "uid": "284" //用户id
        }
    }
    ```

  - 错误

    - `u002` 验证码错误
    - `u004` 用户已经存在

### 登录

- 请求方式：POST

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appuser`

  - 参数说明

    ```
    phone //手机号
    password //密码
    ```

- 返回结果：

  - 正常

    ```json
    {
        "code": "0000",
        "data": {
            "id": "290",
            "openid": null,
            "nickname": "辛丙亮",
            "phone": "15102724518",
            "gender": null,
            "avator": null,
            "sun_constellation": null, //当该参数为null,说明没有完成先天报告
            "moon_constellation": null,
            "element": null,
            "birth": null,
            "gua": null,
            "gua_ping": null,
            "gua_jie": null,
            "token": "C4IAqGV3cQ",
            "xing": null,
            "ming": null,
            "wuxing1": null,
            "wuxing2": null,
            "constellation_info": null,
            "rengge_id": null, //当该参数为null，说明没有完成后天报告
            "time": "1517881076",
            "unionid": null,
            "ka_time": "1517381511",
            "password": "e10adc3949ba59abbe56e057f20f883e"
        }
    }
    ```

  - 错误

    - `u005` 该用户不存在，或用户名密码错误

##找回密码

### 发送找回验证码

- 请求方式：GET

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appuserback?phone=15102724528`

  - 参数说明

    ```
    phone //手机号
    ```

- 返回结果：

  - 正常

    ```json
    {
      "code": "0000",
      "data": "success"
    }
    ```

  - 错误

    - `u002` 发送验证码失败

###提交找回表单

- 请求方式：POST

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appregister`

  - 参数说明

    ```
    phone //手机号
    password //密码
    code //验证码
    ```

- 返回结果：

  - 正常

    ```json
    {
      "code": "0000",
      "data": "success"
    }
    ```

  - 错误

    - `u002` 验证码错误

## 先天报告数据提交

- 请求方式：POST

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appcongenital`

  - 参数说明

    ```
    xing //姓
    ming //名
    time //时间,使用时间戳
    sex //性别
    uid //用户id
    ```

- 返回结果：

  - 正常

    ```json
    {
      "code": "0000",
      "data": "success"
    }
    ```

  - 错误

    - `u006` 先天报告生成失败

## 九个问题

- 请求方式：POST

- 链接：`https://suan.co-links.com/app.php/v0.0.1/appquestion`

- 返回结果：

  - 正常

    ```json
    {
        "code": "0000",
        "data": [
            "我是一个不断朝向目标生活的外向人。",
            "我觉得许多人依赖我的帮忙和慷慨。",
            "我是一个彻头彻尾、站在路中心的人，我最大的敌人是自己的恐惧。",
            "我常为事情未能按意想中的路向发展而烦躁不乐。",
            "我对过去的事有着一份近乎执着的怀恋。",
            "我善于计划却不善于实行。",
            "我很容易察觉别人的弱点，假如我遇到不公平的待遇，我会攻击这弱点。",
            "我不害怕面对别人，事实上，我经常面对不同类型的人。",
            "我是很容易说话的人，凡事都有商量余地。"
        ]
    }
    ```

## 问题提交





##星盘数据



## 微信授权

## 个人信息数据（包含芯灵卡）

### 个人报告(给页面)

### 好友报告(给页面)

## 好友列表

## 邀请卡

## 拍脸上传

## 面向结果返回

## 意见反馈