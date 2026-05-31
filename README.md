<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HI</title>
    <style>
        body { 
            font-family: 'Courier New', Courier, monospace; 
            padding: 30px; 
            background-color: #1e1e1e; 
            color: #ffffff;
        }
        h1 { color: #009925; }
        p { color: #F4B400; }
        /* 模拟 Python 终端的样式 */
        #python-terminal {
            background-color: pink;
            border: 1px solid #333;
            padding: 15px;
            margin-top: 20px;
            color: #00ff00; /* 经典的黑客绿 */
            font-size: 18px;
            white-space: pre-wrap;
            min-height: 50px;
        }
    </style>
</head>
<body>

    <h1>WELCOME!</h1>
    <p>I love you, because you are my son.</p >

    <!-- 结果输出终端 -->
    <div id="python-terminal">等待输入...</div>

    <!-- 用原生 JavaScript 零延迟模拟 Python 的 input 和 print -->
    <script>
        // 页面加载完成后延迟 0.5 秒弹出，防止页面还没刷出来就弹窗
        window.onload = function() {
            setTimeout(function() {
                // 1. 弹出输入框 (模拟 Python 的 s = input("输入一个数字："))
                let s = prompt("输入一个数字：");
                
                let terminal = document.getElementById("python-terminal");

                // 2. 模拟 Python 的条件判断和 print 输出
                if (s !== null && s.trim() !== "") {
                    terminal.innerText = "I am your dad in next " + s + " years.";
                } else {
                    terminal.innerText = "你没有输入任何数字！";
                }
            }, 500);
        };
    </script>

</body>
</html>
