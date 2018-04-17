# bootstrap_modal

### 说明
 * 1、基于bootstrap的模态框增加一些扩展
 * 2、弃用bootstrap的遮罩，可以自定义遮罩，但是，原遮罩对应的事件的并未实现，请谨慎使用
 * 3、该插件可以应用给局部元素，因此会默认给模态框的父级元素加上相对定位，使用前请确认不会影响页面结构
 * 4、弹窗或动画会默认出现在父级元素的水平垂直剧中的位置，请确保父级元素都拥有高度和宽度。
### 使用
##### 1、提前引用jquery后再引用该插件js
```
$dom.myModal({
      type:'loading',
      duration:2000
  })
```
##### 2、参数配置
字段  | 说明 | 默认值
-----|  ----- |-----
msg  |弹窗内容,支持html插入| ""
width| 宽度 | "600"
height | 高度 | "300"
type |弹窗类型，有两种类型（modal、modal-sm） | 'modal'
backdrop | 是否开启遮罩 | false
backdrop_style | 自定义遮罩样式,必须backdrop为true时才有效,只支持JSON格式 | ''
keyboard | 是否开启esc建退出| true
remote| 远程加载url,在没有配置msg时有效| ""
openEvent | 弹窗打开后的会回调函数 | null
closeEvent | 弹窗关闭后的回调函数 |null
okEvent | 点击确定按钮的回调函数 |null
##### 3、扩展模板
```
$.fn['myModal'].extendTemplate({
      type:"",//你需要定义一个type,然后在上面使用时传入定义的type
      template:""//自定义弹框内容（貌似没有多大作用）
})
```
