---
title: args[0] as self
layout: post
date: 2018-12-26 02:39 +0800
---

In declaring the python constructor as __init__(*args), the reference to the object (by convention named self) will be assigned to the first argument, which is args[0].

```
class Foo:
	def __init__(*args):
		args[0].line = "This refers to the object"
		print args[1]
	t = Foo("bar")
	print t.line
```

This prints out the following:
```
bar
This refers to the object
```