# JavaScript Drum Kit

## 标准与兼容性

UI Event keypress **已废弃**(Firefox已不能正常使用)

KeyboardEvent.keyCode **已废弃**

## 实现与思考

- Document Event keydown<UI Event>
  - 持续触发（触发频率无标准）
  - 限制事件触发频率
- 通过keydown事件的事件对象获取按键
  - KeyboardEvent.key => '[a-z]'