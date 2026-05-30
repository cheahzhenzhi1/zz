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

    <!-- 1. 引入 PyScript 核心资源 -->
    <link rel="stylesheet" href="https://pyscript.net" />
    <script type="module" src="https://pyscript.net"></script>
    
    <style>
        body { font-family: sans-serif; padding: 20px; }
        .interactive-box { 
            background: #f4f4f9; 
            padding: 15px; 
            border-left: 5px solid #306998; 
            margin-top: 20px; 
        }
        input, button { padding: 5px 10px; margin: 5px; font-size: 16px; }
        #output { font-weight: bold; color: #306998; margin-top: 10px; }
    </style>
</head>
<body>

    <h1>WELCOME!</h1>
    <p>I love you, because you are my son.</p >

    <!-- 2. 创建网页上的交互界面 (用于代替标准 Python 的 input) -->
    <div class="interactive-box">
        <h3>Python 网页互动区</h3>
        <label for="num-input">输入一个数字：</label>
        <input type="number" id="num-input" placeholder="例如: 5">
        <button id="run-btn">运行 Python</button>
        
        <!-- Python 打印结果会显示在这里 -->
        <div id="output"></div>
    </div>

    <!-- 3. 这里是真正运行的 Python 代码 -->
    <script type="py">
        from idom import component, html
        from pyscript import document
        from pyodide.ffi import create_proxy

        # 定义点击按钮时触发的 Python 函数
        def on_click(event):
            # 获取网页中输入框的值
            input_element = document.querySelector("#num-input")
            s = input_element.value
            
            # 如果用户输入了内容，在网页上打印输出
            if s:
                output_element = document.querySelector("#output")
                output_element.innerText = f"I am your dad in next {s} years"
            else:
                document.querySelector("#output").innerText = "请先输入一个数字！"

        # 将按钮绑定 Python 的点击事件
        button = document.querySelector("#run-btn")
        button.addEventListener("click", create_proxy(on_click))
    </script>

</body>
</html>
