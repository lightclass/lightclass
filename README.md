# lightclass
## 功能
构建学生和教师交流的在线平台。
1.学生请家教
2.家教招学生
3.在线交流
4.考试信息推送
## 技术路线
nodejs + express + mongodb + angularjs（nativescript）
## 时间规划
2015.03 完成简单的信息推送，信息展示；包括后台信息录入和前台模块展示。（最先针对移动平台）
2015.04-2015.05 完成老师评分规则的逻辑和基本的组课逻辑

## model设计
###user
```
var user = {
id：num
name：string
email:string
password:string
type:string
rank:number
info:string
tag:string[]
createAt:date
updateAt:date
}
```
###message
```
var message = {
id:num
title:string
content:string
author:ref(user)
tag:string[]
replay:ref(message)
createAt:date
updateAt:date
}
```
###iclass
```
var iclass = {
id:num
title:string
content:string
place:string
teacher:ref(user)
students:ref(user)
deadline:date
star:num
repaly:ref(message)
createAt:date
updateAt:date
}
```
