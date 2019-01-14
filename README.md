# ToDoMVC-Experience

http://todomvc.com 功能清单 by Jianlinker

- 添加todo项

  - 说明：直接输入到输入框并回车即可生成清单列表项

- 查询todo列表

  - 说明：根据All、Active、Completed三个功能选项标签查询不同选择下的todo列表
    - All：显示所有状态下的todo列表项（包括已完成和未完成的todo项），按创建时间的正序排列进行展示，最新创建的显示在最下面
    - Active：显示所有还没完成的列表项
    - Completed：显示所有已完成的列表项

- 修改todo项

  - 说明：修改todo项的状态及内容
    - 在todo项最前面的圆圈处单击可以进行打钩，会变化todo项的字体颜色和划线，在Active功能下还会直接消失
    - `Double-click to edit a todo`关于双击可进行todo项的内容修改，作者在输入框的下面已经有所提示了
    - 在输入框最左侧，可点击字体图标，使得所有的todo项变成已完成状态，也可用于快速删除todo列表

- 删除todo项

  - 说明：
    - 单个删除
      - 可点击单个列表项最后的小×进行单个列表项的删除
    - 多个删除 `Clear completed`字段
      - 当有任务已经处于完成状态时，右下角会出现`Clear completed`的功能选项，可以对所有已完成的todo项清除掉

- 数据的持久化

  - 用了本地存储技术：把每一个todo项都弄成了一个字段进行存储

  - 如：

    ```json
    [{id: 1, title: "了解vue的概念", completed: true}, {id: 2, title: "了解vue的家族", completed: false}...]
    ```

- 其他：

  - 应该是做了全转义处理
  - 不限输入长度
  - 左下角对todo列表项的数量进行的统计，不论完成还是未完成的

- 用户体验建议：

  - 提供优先级功能：可上下拖拽todo项表示任务的轻重缓急，虽然可以通过双击修改、删除重加等操作，但无疑增加了用户的操作成本
  - 每一个功能选项下灵活统计todo项的数量（All、Active、Completed）

- 整体功能

  作为一个任务清单的页面，结合了vue.js（example）这个，并提供一些其他的链接跳转，可以在学习知识的同时，从整体出发，把知识点写成任务清单，然后一步一步制定计划进行完成