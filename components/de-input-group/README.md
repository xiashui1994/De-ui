### de-input属性
属性 | 类型 | 说明 | 默认值
:- | :-: | :-: | -: 
type | String | 类型 input、textarea | input
labelText | String  | 说明文字（传入该参数则显示label） | ''
buttonText | String | button文字（传入该参数则显示button） | ''
required | Boolean | 是否是必填项 | false
placeholder | String | 占位文字 | ''
maxLength | Number | input最大长度 | 11
cursorSpacing | Number | 键盘弹起后距离光标的距离 | 0
value | any | input 默认文本 | ''

### 事件
事件 | 说明
:- | -:
bind:input | 输入框输入事件
bind:btnclick | 按钮点击事件

### 成组使用，父组件de-input-group调用子组件de-input的方法，去除第一个input的上边框与最后一个input的下边框

json文件
```
{
  "usingComponents": {
    "de-input": "/components/de-input/de-input",
    "de-input-group": "/components/de-input-group/de-input-group"
  }
}
```

wxml文件
```
<de-input-group>
  <de-input labelText='验证码' placeholder='请输入验证码' maxLength="6" required bind:input="input"></de-input>
  <de-input labelText='验证码' placeholder='请输入验证码' maxLength="6" required bind:input="input"></de-input>
  <de-input labelText='验证码' placeholder='请输入验证码' maxLength="6" required bind:input="input"></de-input>
</de-input-group>
```