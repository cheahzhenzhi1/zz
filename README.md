<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>HI</title>
</head>
<body>
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HI</title>

    <!-- 引入最新的 PyScript 核心资源 -->
    <link rel="stylesheet" href="https://pyscript.net" />
    <script type="module" src="https://pyscript.net"></script>
    
    <style>
        body { 
            font-family: 'Courier New', Courier, monospace; 
            padding: 30px; 
            background-color: #1e1e1e; 
            color: #ffffff;
        }
        h1 { color: #4fc3f7; }
        p { color: #e0e0e0; }
        /* 专门用来显示 Python 打印结果的容器 */
        #python-terminal {
            background-color: #000000;
            border: 1px solid #333;
            padding: 15px;
            margin-top: 20px;
            color: #00ff00; /* 经典的黑客绿 */
            font-size: 18px;
            white-space: pre-wrap;
        }
    </style>
</head>
<body>

    <h1>WELCOME!</h1>
    <p>I love you, because you are my son.</p >

    <!-- Python 的 print() 结果会自动注入到这个容器里 -->
    <div id="python-terminal"></div>

    <!-- 这里是真正运行的 Python 代码 -->
    <script type="py" target="python-terminal">
import js

# 1. 弹出浏览器输入框，等待用户输入数字（还原 input 效果）
s = js.prompt("输入一个数字：")

# 2. 如果用户输入了内容，则执行打印调侃的句子
if s:
    print(f"I am your dad in next {s} years.")
else:
    print("你没有输入任何数字！")
    </script>

</body>
</html>
</body>
</html>
