# HTTP Api
## 前言

整理了部分api

不确定的用Object代替了

如有错误请指正

仍在更新中

## 目录
- [HTTP Api](#http-api)
  - [前言](#前言)
  - [目录](#目录)
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
  - [用户](#用户)
    - [获取主题](#获取主题)
      - [请求地址](#请求地址-9)
      - [请求头](#请求头-9)
      - [请求内容](#请求内容-6)
      - [返回值](#返回值-9)
    - [获取订阅课程](#获取订阅课程)
      - [请求地址](#请求地址-10)
      - [请求头](#请求头-10)
      - [请求内容](#请求内容-7)
      - [返回值](#返回值-10)
  - [对象储存](#对象储存)
    - [生成令牌](#生成令牌)
      - [请求地址](#请求地址-11)
      - [请求头](#请求头-11)
      - [请求内容](#请求内容-8)
      - [返回值](#返回值-11)
  - [网阅联考](#网阅联考)
    - [获取懂你100URL](#获取懂你100url)
      - [请求地址](#请求地址-12)
      - [请求头](#请求头-12)
      - [请求内容](#请求内容-9)
      - [返回值](#返回值-12)
  - [应用管理](#应用管理)
    - [获取打开摄像头权限](#获取打开摄像头权限)
      - [请求地址](#请求地址-13)
      - [请求头](#请求头-13)
      - [请求内容](#请求内容-10)
      - [返回值](#返回值-13)
    - [记录图片](#记录图片)
      - [请求地址](#请求地址-14)
      - [请求头](#请求头-14)
      - [请求内容](#请求内容-11)
      - [返回值](#返回值-14)
  - [应用商店](#应用商店)
    - [检查更新](#检查更新)
      - [请求地址](#请求地址-15)
      - [请求头](#请求头-15)
      - [请求内容](#请求内容-12)
      - [返回值](#返回值-15)
  - [错题本](#错题本)
    - [获取标签](#获取标签)
      - [请求地址](#请求地址-16)
      - [请求头](#请求头-16)
      - [请求内容](#请求内容-13)
      - [返回值](#返回值-16)
    - [移除多个错题](#移除多个错题)
      - [请求地址](#请求地址-17)
      - [请求头](#请求头-17)
      - [请求内容](#请求内容-14)
      - [返回值](#返回值-17)
    - [获取错题问题信息](#获取错题问题信息)
      - [请求地址](#请求地址-18)
      - [请求头](#请求头-18)
      - [请求内容](#请求内容-15)
      - [返回值](#返回值-18)
    - [搜索错题问题](#搜索错题问题)
      - [请求地址](#请求地址-19)
      - [请求头](#请求头-19)
      - [请求内容](#请求内容-16)
      - [返回值](#返回值-19)
    - [获取错题本](#获取错题本)
      - [请求地址](#请求地址-20)
      - [请求头](#请求头-20)
      - [请求内容](#请求内容-17)
      - [返回值](#返回值-20)
  - [随身答](#随身答)
    - [获取目录](#获取目录)
      - [请求地址](#请求地址-21)
      - [请求头](#请求头-21)
      - [请求内容](#请求内容-18)
      - [返回值](#返回值-21)
    - [获取学生主题](#获取学生主题)
      - [请求地址](#请求地址-22)
      - [请求头](#请求头-22)
      - [请求内容](#请求内容-19)
      - [返回值](#返回值-22)
    - [获取随身答](#获取随身答)
      - [请求地址](#请求地址-23)
      - [请求头](#请求头-23)
      - [请求内容](#请求内容-20)
      - [返回值](#返回值-23)
    - [删除目录](#删除目录)
      - [请求地址](#请求地址-24)
      - [请求头](#请求头-24)
      - [请求内容](#请求内容-21)
      - [返回值](#返回值-24)
    - [新建目录](#新建目录)
      - [请求地址](#请求地址-25)
      - [请求头](#请求头-25)
      - [请求内容](#请求内容-22)
      - [返回值](#返回值-25)
    - [搜索问题](#搜索问题)
      - [请求地址](#请求地址-26)
      - [请求头](#请求头-26)
      - [请求内容](#请求内容-23)
      - [返回值](#返回值-26)
    - [创建随身答](#创建随身答)
      - [请求地址](#请求地址-27)
      - [请求头](#请求头-27)
      - [请求内容](#请求内容-24)
  - [云笔记](#云笔记)


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
|schoolName|String|
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
**Body JSON**

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

## 用户
### 获取主题
#### 请求地址
**Get** `http://sxz.api.zykj.org/api/services/app/User/GetMyTopics`
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
| result | Topic[] |
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

*Topic*

字段名|类型
-|-
id|Integer
name|String
content|String
sort|Integer
isActive|Boolean

---

### 获取订阅课程
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/StudentUser/CoursesSubscribed`
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
| result | Course[] |
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

*Course*

字段名|类型
-|-
id|Integer
teacherUsers|Teacher[]
topics|Topic[]
classRoomId|Integer
title|String
subscribers|Integer
state|Integer
createUserId|Integer
createTime|String
editUserId|Integer
editTime|String

*Teacher*

字段名|类型
-|-
id|Integer
fullName|String

*Topic*

字段名|类型
-|-
name|String
content|String
sort|Integer
isActive|Boolean
system|Boolean
platformId|Integer
lastModificationTime|String
lastModifierUserId|Integer
creationTime|String
creatorUserId|Integer
id|Integer

---

## 对象储存
### 生成令牌
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/ObjectStorage/GeneratorTokenAsync`
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
| result | TokenInfo |
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

*TokenInfo*

字段名|类型
-|-
strategy|String
appId|Object
bucket|String
endpoint|String
region|String
accessKeyId|String
accessKeySecret|String
securityToken|String
expiration|String

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
**Body JSON**

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

## 应用管理
### 获取打开摄像头权限
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/StoreAppControl/CanIOpenCameraAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Params**

字段名|类型
packageName|String
#### 返回值
| 字段名 | 类型 |
| ------------ | ------------ |
| result | Boolean |
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

### 记录图片
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/StoreAppControl/RecordPicturesAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
appName|String
packageName|String
pictures|String[]
#### 返回值
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


## 应用商店
### 检查更新
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/AppStore/CheckUpdateAsync`
#### 请求头
无
#### 请求内容
**Query Params**

字段名|类型
packageName|String
appType|Integer

#### 返回值

| 字段名 | 类型 |
| ------------ | ------------ |
| result | VersionInfo |
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

*VersionInfo*

id|Integer
appVersionId|Integer
packageName|String
score|Double
creationTime|String
creatorUserId|Integer
summary|String
description|String
downloads|Integer
fileUrl|String
forceUpdate|Boolean
icon|String
name|String
size|Integer
versionCode|Integer
versionName|String
appType|Integer
disabled|Boolean
lastModificationTime|String

## 错题本
### 获取标签
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/MistakeBook/GetMyTags`
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
| result | Tag[] |
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

*Tag*

字段名|类型
-|-
name|String
bindItemCount|Integer
id|Integer

---

### 移除多个错题
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/MistakeBook/MultiRemoveMistakeItemsAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
bookId|Integer
itemIds|Integer[]

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

### 获取错题问题信息
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/MistakeBook/GetMistakeQstItemDetailInfoAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Params**

字段名|类型
-|-
itemId|Integer
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | QstInfo |
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

*QstInfo*

字段名|类型
-|-
questionId|Integer
examId|Integer
number|Integer
name|String
qstFlows|QstFlow[]
qstPath|String
attachments|Object[]
answerInfos|AnswerInfo[]
revisingResult|Integer
microClassToQuestionList|Object[]
microClassToStudentList|Object[]
typicalErrorAnswers|Object[]
typicalRightAnswers|Object[]
itemType|Integer
isShowAnswer|Boolean
isShowMicroLesson|Boolean
itemId|Integer
bookId|Integer
extraStems|Object[]
diff|Object
attainedLevel|Object
errorReason|Object
mistakeTags|Object[]
note|String
pictureNote|Object

*QstFlow*

字段名|类型
-|-
type|Integer
score|Double
missScore|Double
number|Integer
uuid|String
qstType|Integer
options|Object
subQuestions|QstFlow[]
getScore|Double
originScore|Object

*AnswerInfo*

字段名|类型
-|-
uuid|String
number|Integer
result|Integer
examAnswers|String[]
examComments|String[]
examMicroLessonComment|String
revisingAnswers|Object[]
reviseMicroLessonComment|String
revisingComments|Object[]

---

### 搜索错题问题
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/MistakeBook/SearchMistakeQstItemsAsync`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
attainedLevel|Integer[]
bookId|Integer
diff|Integer[]
errorReason|Integer[]
haveNoTag|Boolean
maxResultCount|Boolean
skipCount|Integer
tagIdList|String[]

#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Qsts |
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

*Qsts*

字段名|类型
-|-
totalCount|Integer
items|QstItem[]

*QstItem*

字段名|类型
-|-
source|String
creationTime|String
stemShoot|String
hasStem|Boolean
diff|Integer
attainedLevel|Integer
errorReason|Integer
tagNames|String[]
isRelatedQstGroup|Boolean
number|Integer
name|String
id|Integer

### 获取错题本
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/MistakeBook/GetMyMistakeBooksAsync`
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
| result | MistakeBook[] |
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

*MistakeBook*

字段名|类型
-|-
topicId|Integer
topic|Topic
studentUserId|Integer
newQstCount|Integer
totalQstCount|Integer
id|Integer

*Topic*

字段名|类型
-|-
id|Integer
name|String
content|String
sort|Integer
isActive|Boolean


## 随身答
### 获取目录
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Quora/GetCatalogs`
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
| result | Catalog[] |
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

*Catalog*

字段名|类型
-|-
id|Integer
name|String
hasNewMsgs|Boolean
newMsgCount|Integer
hasNewParimaryMsgs|Boolean
newParimarMsgCount|Integer
sort|Integer

---

### 获取学生主题
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Quora/GetQuoraStudentTopicsAsync`
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
| result | StudentTopic[] |
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

*StudentTopic*

字段名|类型
-|-
topicId|Integer
topicName|String

---

### 获取随身答
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Quora/GetSessions`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
catalogId|Integer
joinTime|TimeFrame
justWatch|Integer[]
keyword|String
orderBy|Integer
skip|Integer
take|Integer
topicId|Integer
updateTime|TimeFrame

*TimeFrame*

字段名|类型
-|-
end|String
start|String

#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Session[] |
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

*Session*

字段名|类型
-|-
cleared|Integer
closed|Boolean
courseId|Integer
createTime|String
askUserId|Integer
members|Integer
messages|Integer
snapshot|String
summary|String
updateTime|String
updateUserId|Integer
sessionRole|Integer
unRead|Integer
primaryUnReadInteger
sentMessages|Integer
openCount|Integer
state|Integer,
userId|Integer
joinType|Integer
joinTime|String
askUserName|String
askUserPhoto|String
updateUserName|String
updateUserPhoto|String
disabled|Boolean
class|String
topicName|String
isCollect|Boolean
searched|Boolean
id|Integer

---

### 删除目录
#### 请求地址
**GET** `http://sxz.api.zykj.org/api/services/app/Quora/DeleteCatalog`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Authorization|String|Bearer *Token* |
#### 请求内容
**Query Param**

字段名|类型
-|-
id|Integer

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

### 新建目录
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Quora/AddCatalog`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
name|String
#### 返回值
**Body JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | Integer |
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

### 搜索问题
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Quora/SearchQuora`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
imageUrl|String

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

### 创建随身答
#### 请求地址
**POST** `http://sxz.api.zykj.org/api/services/app/Quora/CreateSession`
#### 请求头
|字段名|类型|值|
|-|-|-|
|Content-Type|String|application/json
|Authorization|String|Bearer *Token* |
#### 请求内容
**Body JSON**

字段名|类型
-|-
content|String
courseId|String
snapshot|String
summary|String

## 云笔记

这部分参见[此处](https://blog.djdjz7.ml/blogs/2023-01-24-zy-apis/)