- 启动速度优化
	- 【Templater】插件实现的建议管控加载插件速度，相信大家可能都要加载十几甚至几十个插件，那么启动速度自然成了问题。
	- 文件位置，Template/startup 文件夹下
		- 【FastStart-Plugins-ShortDelay】（优先加载的插件名单）
		- 【FastStart-Plugins-LongLongDelay】（次要加载的插件名单）
		- 【FastStart-Plugins-LongDelay】（最后加载的插件名单）
		- 【FastStart-GenerateListOfInstalledPlugins】
		- 【FastStart-StartupScript】（控制几个加载过程的延迟毫秒数）
			- 我这里分别设置了三段：4s，12s，40s
- 优点：
	- 加载名单里面只需要填写插件，对应电脑中的目录名称即可，很方便，无需去看代码或者找准代码位置；
	- 可以分组控制加载速度
- 缺点：
	- 此方法强依赖 【Templater】插件，所以这个插件默认需要加载的，不能设置任何延迟逻辑