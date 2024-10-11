问题：无法在html文件中成功链接css和js文件
原因：浏览器不允许直接加载本地文件，而是需要通过一个服务器来访问。这通常发生在使用文件路径（file:///）时。
方案：
1、确保使用 Live Server：
确保通过 VSCode 的 Live Server 插件打开 index.html 文件。
右键点击 index.html，选择“Open with Live Server”。这将启动一个本地服务器并提供一个 URL，例如 http://127.0.0.1:5500。
检查路径设置：

2、在 index.html 中，确保链接的 JS 文件路径是相对的。例如，如果结构是这样的：
E:/
└── web-learning/
    └── web-frontprojects/
        └── table-edit/
            ├── index.html
            ├── js/
            │   └── table.js
那么在 index.html 中，链接应为：
<script src="js/table.js"></script>
3、访问 Live Server 地址：
打开浏览器，确保访问的是 Live Server 提供的地址，而不是本地文件地址。比如 http://127.0.0.1:5500/web-learning/web-frontprojects/table-edit/index.html。
