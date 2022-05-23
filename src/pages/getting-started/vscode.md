---
title: VSCode插件和设置
---

## VSCode插件和设置
个人推荐这些插件

### C语法高亮
必备，高亮能让你的代码可读性更高。
![vscode-c](../../assets/vscode-c.png)

### 调试
可选，如果你改动或者新增了一个函数，这插件可以更有效的帮你处理调试。
![vscode-nativedebug](../../assets/vscode-nativedebug.png)

### 流程管理
可选，可视化指令，
![vscode-task](../../assets/vscode-task.png)

在根目录新建`.vscode`文件夹，然后在该文件夹里新建`task.json`，内容范本如下：
```json
{
 "version": "2.0.0",
 "tasks": [
  {
   "label": "Build Debug",
   "type": "shell",
   "command": "make",
   "args": [
    "DINFO=1",
    "-j$(nproc)"
   ],
   "problemMatcher": [
    "$gcc"
   ]
  },
  {
   "label": "Build Release",
   "type": "shell",
   "command": "make",
   "args": [
    "-j$(nproc)"
   ],
   "problemMatcher": [
    "$gcc"
   ]
  }
 ]
}
```
然后就可以在vscode的左下角任务栏里的看到这个指令，以后直接运行就不需要打这么长的指令里。
![task-new](../../assets/task-new.png)

<Tip>调试的时候选择Build Debug, 发布的时候可以选择Build Release编译。</Tip>