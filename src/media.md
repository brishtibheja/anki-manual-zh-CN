# 媒体

> 原文：[Media - Anki Manual (ankiweb.net)](https://docs.ankiweb.net/media.html)

Anki 将你笔记中使用的声音和图像存储在靠近集合的一个文件夹中。有关文件夹位置的更多信息，请参阅
[文件位置](files.md#文件位置)部分。当你在 Anki 中添加媒体时，无论是使用[编辑器](editing.md)中的回形
针图标，还是将其粘贴到字段中，Anki 都会将其从原位置复制到媒体文件夹中。这使得备份集合的媒体或将其移
动到其他计算机上变得简单。

如果你的媒体文件名包含空格或其他特殊字符（如百分号），则文件名在 HTML 编辑器中的显示方式将与在磁盘上
的显示方式不同。例如，一个名为 `hello 100%.jpg` 的文件将在 HTML 编辑器中显示为
`hello%20100%25.jpg`。在内部，Anki 仍使用原始文件名，因此如果你希望[搜索](searching.md)文件或使用
[查找并替换](browsing.md#查找并替换)修改文件名，则需要使用磁盘上的名称，而非 HTML 编辑器中的名称。导
出到文本文件是查看底层表示的另一种方法。

## 检查媒体

你可以使用工具菜单中的「检查媒体」选项来扫描你的笔记和媒体文件夹。它将生成一个报告，列出媒体文件夹中
未被任何笔记使用的文件，以及笔记中引用但在你的媒体文件夹中缺失的媒体。它还允许你：

- 删除未使用的媒体文件。
- 标记引用缺失媒体文件的笔记。
- 清空你的回收站文件夹。
- 将已删除的文件恢复到你的媒体文件夹。

此工具不会扫描问题或答案模板，这就是为什么你不能在模板中引用字段中的媒体。如果你需要在每张卡片上放置
静态图像或声音，请在文件名前加上下划线（例如，`_dog.jpg`），以告知 Anki 在检查媒体时忽略它。当你使用
未使用的媒体检查删除媒体时，Anki 会将其移动到你的操作系统的回收站中，因此如果你误删了不该删除的媒
体，可以恢复它。

## 手动添加媒体

当你通过 Anki 的界面添加媒体时，Anki 会确保文件名经过编码，可以在不同的设备上正常工作，删除不适用于
某些操作系统的字符，并截断非常长的文件名。

如果你手动将文件添加到 [媒体文件夹](files.md#文件位置)，你应该在之后使用工具菜单中的「检查媒体」，以
确保文件名编码正确。如果跳过此步骤，任何不兼容的文件名在同步时将被跳过。

## 支持的格式

Anki 使用一个名为 mpv 的程序（在必要时使用 mplayer 作为备选），以支持声音和视频。支持多种文件格式，
但并非所有格式都能在 AnkiWeb 和移动客户端上工作。MP3 音频和 MP4 视频似乎是最通用的支持格式。
