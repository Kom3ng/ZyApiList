# Http Api
## 目录

## 天气
### 获取天气信息
#### 请求地址
**GET** ` http://sxz.api.zykj.org/api/services/app/Weather/GetQWeatherAsync `
#### 请求头
无
#### 请求参数
| 字段名 | 类型 |
| ------------ | ------------ |
| location | int |
#### 返回值
**JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | WeatherReport |
| targetUrl | String |
| success | bool |
| error | String |
| unAuthorizedRequest | bool |
| __abp | bool |

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
**JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | StudentSetting |
| targetUrl | String |
| success | bool |
| error | String |
| unAuthorizedRequest | bool |
| __abp | bool |

*StudentSetting*

|字段名|类型|
|-|-|
|studentSelectActivity|String|
|studentSatisfaction|String|
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
**JSON**

| 字段名 | 类型 |
| ------------ | ------------ |
| result | AllSettings |
| targetUrl | String |
| success | bool |
| error | String |
| unAuthorizedRequest | bool |
| __abp | bool |

*AllSettings*

| 字段名 | 类型 |
| ------------ | ------------ |
| schoolName|String|
|schoolShortName|String|
|systemName|String|
|stuNumLength|String|
|backgroundImage|String|
|icon|String|
|stageIds|int[]|
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


