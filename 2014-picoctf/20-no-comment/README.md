# No Comment

## 題目

種類： Web Exploitation

分數： 20 分

敘述：
> The CD you find has a copy of your father's website: homepage.html. Maybe something is hidden in the site...

提示：
> You may want to use your browser to view the source of the web page.

## 解題

使用瀏覽器直接打開該網頁的原始碼，很快就可以看到有一段很顯眼的註解：

```html
<html>
	<head>
		<title>Dr. Claudio Drake's Personal Website</title>
	</head>

	<body>
		<center>
			<div style="width: 500px">
				<h1>Dr. Claudio Drake</h1>

				<img src="/problem-static/web/no-comment/me.png">

				<p>
					I am a roboticist with a Doctorate Degree in Robotics. My primary interests are in developing new medical robotics to help doctors
better perform surgery on high risk patients.
				</p>

				<!-- In case you forget, the password for this site is: flag_affa5271dfd8d0de07b823c8c78ebd9c2441008a -->

			</div>
		</center>
	</body>
</html>
```

註解上直接寫著密碼是 `flag_affa5271dfd8d0de07b823c8c78ebd9c2441008a`，這就是這題的 flag。
