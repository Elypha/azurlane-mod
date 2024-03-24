下面是我当时打包时备忘用的笔记，里面包含了简单的工作流程。你可以参考下面的方法来自己创建 mod

---

-   从游戏目录中获得 l2d 文件，命名为 `{name} raw`
-   使用 `UnityLive2DExtractor.v1.0.2` 提取贴图，方法为
    -   拖动 `daofeng_5` 到 `UnityLive2DExtractor.exe`上
    -   在 `textures` 中查看/修改贴图
-   使用 `Live2D Cubism Viewer 4.2` 预览效果
    -   安装
        -   Live2D Cubism Editor
        -   https://www.live2d.com/en/download/cubism/
    -   使用
        -   打开 `Live2D Cubism Viewer`
        -   把 `daofeng_5.moc3` 拖进去
-   使用 `Unity Assets Bundle Extractor` 打包
    -   运行 `AssetBundleExtractor.exe`
    -   打包
        -   File - Open - `daofeng_5 raw`
        -   do you with to unpack it?
            -   Yes - `daofeng_5 unpack`
        -   Info
            -   Sort by `Type`, 找到 `texture_00` (Type = `Texture2D`)
            -   选中 - Plugins - Edit - OK - (Texture) Load
                -   选择修改过的贴图 - OK
            -   选择 `Fast` - OK (等待) - OK
            -   would you like to save the changes?
                -   Yes
        -   File - Save - `daofeng_5 unpack save`
    -   压缩
        -   File - Compress - `daofeng_5 unpack save`
        -   All files: 选择 `LZMA`
        -   File table 也可以选 `LZMA`
        -   OK - `daofeng_5`

