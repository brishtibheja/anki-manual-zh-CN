# 缺少库

> 原
> 文：[Missing Libraries - Anki Manual (ankiweb.net)](https://docs.ankiweb.net/platform/linux/missing-libraries.html)

如果 Anki 无法启动，请在终端中使用 `anki` 运行它。如果它提示缺少库，请安装该库并重试。

如果它提示没有可用的平台，请使用以下命令行启动 Anki，这应该会显示缺少的库：

```shell
QT_DEBUG_PLUGINS=1 anki
```

用 apt-get 或类似工具安装库后，重复该过程。在安装所有所需的库之前，你可能需要这样做几次。
