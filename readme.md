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

    ```
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

    ```
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

    ```
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

    ```
    {
      "code": "0000",
      "data": "success"
    }
    ```

  - 错误

    - `u002` 验证码错误

## 微信授权

##信息完成度检测

## 个人信息数据（包含芯灵卡）

### 个人报告(给页面)

### 好友报告(给页面)

## 星盘数据

## 九个问题

## 问题提交

## 好友列表

## 邀请卡

## 拍脸上传

## 面向结果返回

## 意见反馈