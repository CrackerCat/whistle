# cssAppend

往 content-type 为 html 或 css 的响应内容后面追加数据，如果是 html，则会自动加上 style 标签在追加到响应内容，如果是 css，则会自动追加到文本后面，这个与 [resAppend](#rules_resAppend) 的区别是 [resAppend](#rules_resAppend) 不区分类型，对所有匹配的响应都会追加指定的数据，配置模式：

	pattern cssAppend://filepath

filepath 为 [Values](http://local.whistlejs.com/#values) 里面的 {key} 或者本地文件(如：`e:\test\xxx`、`e:/test/xxx`、`/User/username/test/xxx` 等)，pattern 参见[匹配方式](#pattern)，更多模式请参考[配置模式](#mode)。

例子：

	www.ifeng.com cssAppend://{test.css}

test.css:

	html, body {background: red!important;}
