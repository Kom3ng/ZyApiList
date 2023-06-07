# HTTP Api

## 目录
- [天气](#天气)
  - [获取天气信息](#获取天气信息)
    - [请求地址](#请求地址)
    - [请求头](#请求头)
    - [请求参数](#请求参数)
    - [返回值](#返回值)
- [设置](#设置)
  - [获取学生设置](#获取学生设置)
    - [请求地址](#请求地址-1)
    - [请求头](#请求头-1)
    - [请求参数](#请求参数-1)
    - [返回值](#返回值-1)
  - [获取所有设置](#获取所有设置)
    - [请求地址](#请求地址-2)
    - [请求头](#请求头-2)
    - [请求参数](#请求参数-2)
    - [返回值](#返回值-2)
- [消息](#消息)
  - [获取消息列表](#获取消息列表)
    - [请求地址](#请求地址-3)
    - [请求头](#请求头-3)
    - [请求内容](#请求内容)
    - [返回值](#返回值-3)
  - [设置消息已读](#设置消息已读)
    - [请求地址](#请求地址-4)
    - [请求头](#请求头-4)
    - [请求内容](#请求内容-1)
    - [返回值](#返回值-4)
  - [获取通知](#获取通知)
    - [请求地址](#请求地址-5)
    - [请求头](#请求头-5)
    - [请求内容](#请求内容-2)
    - [返回值](#返回值-5)
  - [获取未读消息列表](#获取未读消息列表)
    - [请求地址](#请求地址-6)
    - [请求头](#请求头-6)
    - [请求内容](#请求内容-3)
    - [返回值](#返回值-6)
- [白名单](#白名单)
  - [获取共同的网址](#获取共同的网址)
    - [请求地址](#请求地址-7)
    - [请求头](#请求头-7)
    - [请求内容](#请求内容-4)
    - [返回值](#返回值-7)
  - [获取白名单](#获取白名单)
    - [请求地址](#请求地址-8)
    - [请求头](#请求头-8)
    - [请求内容](#请求内容-5)
    - [返回值](#返回值-8)
- [网阅联考](#网阅联考)
  - [获取懂你100URL](#获取懂你100url)
    - [请求地址](#请求地址-9)
    - [请求头](#请求头-9)
    - [请求内容](#请求内容-6)
    - [返回值](#返回值-9)


## 天气
### 获取天气信息
#### 请求地址
**GET** ` http://sxz.api.zykj.org/api/services/app/Weather/GetQWeatherAsync `
#### 请求头
无
#### 请求参数
| 字段名 | 类型 |
| ------------ | ------------ |
| location | Integer |
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | WeatherReport |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object

*WeatherReport*

| 字段名 | 类型 |
| ------------ | ------------ |
| code | String |
| updateTime | String |
| fxLink | String |
| daily | DailyReport[] |

*DailyReport*

| 字段名 | 类型 |
| ------------ | ------------ |
| fxDate | String |
| tempMax | String |
| tempMin | String |
| iconDay | String |
| textDay | String |
| iconNight | String |
| textNight | String |
| windDirDay | String |
| windScaleDay | String |
| windDirNight | String |
| windScaleNight | String |

## 设置
### 获取学生设置
#### 请求地址
**GET** ` http://sxz.api.zykj.org/api/services/app/Setting/GetSystemSettingsForStudentAsync `
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求参数
无
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | StudentSetting |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object


*StudentSetting*

|字段名|类型|
|-|-|
|studentSelectActivity|String|
|studentSatisfaction|String|

---

### 获取所有设置
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Setting/GetAllSettings`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求参数
无
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | AllSettings |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object


*AllSettings*

| 字段名 | 类型 |
| ------------ | ------------ |
| schoolName|String|
|schoolShortName|String|
|systemName|String|
|stuNumLength|String|
|backgroundImage|String|
|icon|String|
|stageIds|Integer[]|
|xkwOrder|String|
|dnOrder|String|
|newDeviceSmsAuthentication|String|
|studentSelectActivity|String|
|studentSatisfaction|String|
|qq|String|
|emailAddress|String|
|wechat|String|
|telephone|String|
|mobile|String|


## 消息
### 获取消息列表
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Message/GetMyMessageListAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
maxResultCount|Integer
skipCount|Integer
type|Integer
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | AllSettings |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object

*MessageList*

字段名|类型
-|-
totalCount|Integer
items|Message[]

*Message*

字段名|类型
-|-
title|String
type|Integer
isRead|Boolean
parameter|Parameter
senderInfo|SenderInfo
isDeleted|Boolean
deleterUserId|String
deletionTime|String
lastModificationTime|String
lastModifierUserId|String
creationTime|String
creatorUserId|Integer
id|Integer

*Parameter*

字段名|类型
-|-
id|Integer

*SenderInfo*

字段名|类型
-|-
fullName|String
gender|Integer
picture|String
roleType|Integer


---

### 设置消息已读
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Message/SetMessageReadAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Params**

字段名|类型
-|-
messageId|Integer

#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Object |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object


---

### 获取通知
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Notice/GetNoticeAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Params**

字段名|类型
-|-
id|Integer

#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Notice |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object

*Notice*

字段名|类型
-|-
title|String
content|String
type|Integer
targetCount|Integer
readCount|Integer


---

### 获取未读消息列表
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Message/GetMyUnreadMessageCountAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
无
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | UnreadMessageInfo[] |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object

*UnreadMessageInfo*

字段名|类型
-|-
type|Integer
count|Integer


---

## 白名单
### 获取共同的网址
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/WebWhiteList/GetAllCommonWebSiteAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
无
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Object[] |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object


---

### 获取白名单
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/WebWhiteList/GetAllWhiteUrlAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
无
#### 返回值
| 字段名 | 类型 |
| ------------ | ------------ |
| result | String |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object


## 网阅联考
### 获取懂你100URL
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/dn/GetDnUrl`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Params**

字段名|类型
-|-
clientType|Integer
#### 返回值
| 字段名 | 类型 |
| ------------ | ------------ |
| result | String |
| targetUrl | String |
| success | Boolean |
| error | Error |
| unAuthorizedRequest | Boolean |
| __abp | Boolean |

*Error*

字段名|类型
-|-
 code|Integer
message|String
details|Object
validationErrors|Object
