# flex布局和衔接动画

衔接动画，通过transitionend事件在某个动画结束后添加新动画。

## flex主轴与交叉轴的区别

- 主轴
  - 通过justify-content或justify-self分配主轴剩余尺寸到各个位置。无剩余尺寸无作用。
  - 无法控制每一项占据的大小
- 交叉轴
  - 通过align-content指定剩余尺寸分配。交叉轴方向有多行项目时才有效。无剩余尺寸无效。
  - 通过align-items或align-self指定对齐方式和交叉轴方向每项尺寸。stretch | auto(主轴方向包裹)

## flex-basic与width|height的区别

- flex-basic指定主轴方向尺寸，可以是固定或相对尺寸。
- 当有剩余空间时按照flex-grow比例分配增大
- 当容器尺寸不足时按照flex-shink比例缩小
- 当flex-grow flex-shink为0时，超出容器尺寸结合overflow在火狐与chrome下表现不一致，尽可能设置缩放避免溢出容器。