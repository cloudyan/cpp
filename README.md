# cpp

学习 C++

- http://www.runoob.com/cplusplus/cpp-tutorial.html

## VSCode 编译 c++

- https://code.visualstudio.com/docs/languages/cpp
- https://www.zhihu.com/question/30315894
- https://www.cnblogs.com/lianshuiwuyi/p/8094388.html
- https://blog.csdn.net/yangzuo_chester/article/details/80644226

## 编译配置

`launch.json`

```js
{
  // 使用 IntelliSense 了解相关属性。
  // 悬停以查看现有属性的描述。
  // 欲了解更多信息，请访问: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "name": "(lldb) Launch",
      "type": "cppdbg",
      "request": "launch",
      // "program": "${file}.out",
      "program": "${workspaceFolder}/a.out",
      "args": [],
      "stopAtEntry": false,
      "cwd": "${workspaceFolder}",
      "environment": [],
      "externalConsole": true,
      "MIMode": "lldb"
    }
  ]
}
```

`tasks.json`

```js
{
  // See https://go.microsoft.com/fwlink/?LinkId=733558
  // for the documentation about the tasks.json format
  "version": "2.0.0",
  "tasks": [
    {
      "label": "echo",
      "type": "shell",
      "command": "g++",
      // Add any required args (for example -g to build for debugging).
      "args": [
        "-g",
        "main.cpp"
      ],
      "group": {
        "kind": "build",
        "isDefault": true
      }
    }
  ]
}
```

## 编译调试

`command + shift + b` 即可调试了
