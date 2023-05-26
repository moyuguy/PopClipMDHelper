# PopClip的Markdown格式插件

我现在高频使用Obsidian、Mweb等markdown的编辑器来做读书笔记，对摘录的文章或笔记做渐进式阅读时，经常需要对原文进行的，比如高亮、加粗、引用、行内代码（我用它来记录自己的想法）。

我本身对开发只懂一点点，借助chatgpt我提出我的需求，一点点把这个插件完成了。

功能如下：
1. 支持加粗、高亮、斜体、删除线、引用、注释（行内代码）6个动作，其中高亮语法不是markdown原生的，在obsidian中是支持的；
2. 6合1的插件，支持在插件设置中关掉不想用的；
3. 仅在部分markdown编辑器中生效（Drafts 5、Obsidian、MWeb Pro、Ulysses和iA Writer），在其他非markdown软件中不生效。如果想改的话，可以动手改一下Config.plist中的这一段



```
<key>Required Apps</key>
	<array>
		<string>com.agiletortoise.Drafts-OSX</string>
		<string>md.obsidian</string>
		<string>com.coderforart.MWeb3</string>
		<string>com.ulyssesapp.mac</string>
		<string>pro.writer.mac</string>
	</array>
```
添加支持的Markdown应用，添加一行将应用的CFBundleIdentifier加进array里
> bundle identifier 在 info.plist 文件的最上方，即文件头部。它是一个键值对，键为 CFBundleIdentifier。
