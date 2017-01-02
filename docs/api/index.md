**注意**: DM Hub API只支持TLSv1.2及以上协议，在尝试连接DM Hub API发生连接问题之后，请确认使用的协议为TLSv1.2。

## 创建集成应用
登录DM Hub系统，点击菜单**设置>开发与集成**， 点击**新建**，创建一个应用。
<img src="../resources/create1.png" width="600" height="305"/>
<img src="../resources/create2.png" width="600" height="258"/>
保存之后，选择所需权限，点击更新。记住**appId**和**secret**留备后用。
<img src="../resources/create3.png" width="600" height="265"/>

## 获取身份权限
通过appid和appsecret获取access token, 并用于其它功能性API的请求。

**调用请求**
```
HTTP请求方式: GET
https://api.convertlab.com/security/accesstoken?grant_type=client_credentials&appid={appid}&secret={secret}
```  
**参数说明**

|参数|类型|必须|说明|
|:---|:---|:---|:---|  
|appid|string|是|集成应用保存的appId|  
|secret|string|是|集成应用保存的secret|  
**返回说明**
```{
  "error_code": 0,
  "access_token": "47c010ea********d30db952ac",
  "expires_in": 7200
}
```
**注意**: 记住access_token留备后用。
- - -

## 查询客户信息

服务器根据 WEBAPI 请求时的格式, 来确定响应数据的格式. 如果请求时没有指定返回格式, API 会报错. 

WEBAPI 返回的信息, 示例如下: 
```
    # 请求成功
    {
        "message": "success",
        ...
    }

    # 请求失败
    {
        "message": "error",
        "errors": {},
    }
```
- - -

## 客户