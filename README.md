# BaiDuDiskAPI

### 项目概述
本项目旨在开发一个高效、灵活的百度网盘扫码登录系统，支持远程扫码。

### 关键词

- 百度网盘扫码登录系统
- 远程登录系统
- 共享账号系统

### 功能概述

- [x] 扫码登录API - 已完成
- [x] 踢人下线API - 已完成
- [x] 账号信息查询 - 已完成

### 接口地址
> 测试接口 / 随时关闭
> 基础URL: http://123.60.146.248:8010
### 接口地址
> 测试接口 / 随时关闭
 - **基础URL**: `http://123.60.146.248:8010`
 
#### 扫码登录
- **Endpoint**: `/apis/qrlogin`
- **方法**: POST
- **请求头**: 
  - `Cookie`: 用户登录的Cookie信息
  - `Content-Type`: `application/json`
- **请求体**: 
  - `sign` (string): 签名
  - `local` (string): 位置
- **示例**:
  ```json
  {
      "sign": "d2bb6e817f98ea3a7e3d89302ece41c6",
      "local": "上海"
  }
  ```

#### 获取在线设备数
- **Endpoint**: `/apis/devices`
- **方法**: GET
- **请求头**: 
  - `Cookie`: 用户登录的Cookie信息
- **查询参数**: 
  - `hasmore` (int): 是否有更多设备，0表示没有更多设备

#### 退出登录
- **Endpoint**: `/apis/logout`
- **方法**: POST
- **请求头**: 
  - `Cookie`: 用户登录的Cookie信息
- **请求体**: 
  - `devices` (array of strings): 设备ID列表
- **示例**:
  ```json
  {
      "devices": ["118604512741753426"]
  }
  ```

### TODO
- 后台设计
- 小程序设计

### 更新日志

- **更新时间**：2024-07-10

### 联系我
- 微信：viper_python
- 备注：网盘共享系统 / 接口源码（1k）

### 小伙伴召集
- 本人后端开发，项目计划使用Go Gin单体服务开发
- 找个一起玩的前端开发
