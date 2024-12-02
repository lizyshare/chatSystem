# chatSystem

> 网页在线聊天系统

## Backend Stack

> `Spring Boot`、`Spring Security`、`Socket.io`、`Redis`、`MongoDB`、`Nginx`、`FastDFS`等。

## Description

- 该系统是基于前后端分离，采用`Spring Boot + Vue + React`开发的网页版聊天系统。

  - 前端使用`Vue.js`和`React`开发，`WebSocket`增强界面实时交互效果，`Element-UI`组件库提高用户体验，`WebRTC`技术实现`1v1`白板协作和语音视频通话功能。
  - 后端使用`Spring Boot` + `Spring Security`框架开发，结合`JWT`实现用户登录和权限认证，`MongoDB`用来存储该系统的所有数据，`Redis`不仅用来存储临时的验证码等待校验请求，还维护了所有在线的客户端及对应的用户信息；`netty-socketio`监听前端`WebSocket`发来的消息并处理后主动推送该消息给在线的目标客户端。
  - 搭建`FastDFS`服务器用来存储上传的图片和文件，搭建`coturn`中继服务器来收集端点信息，使得公网中任意2台不同主机能够进行`P2P`通话或白板协作。通过配置`Nginx`反向代理请求转发到内部端口，隐藏了真实的访问地址，提高了访问安全性。
- 已实现的功能：私聊、群聊、上传图片、文件、`1v1`白板协作和语音视频通话、敏感词过滤、历史消息、表情发送、消息已读提醒、好友分组、好友备注、在线用户头像高亮、添加好友、添加群聊、日程设置等。
