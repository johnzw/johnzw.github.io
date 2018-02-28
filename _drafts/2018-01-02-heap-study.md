---
layout: post
title: "Heap Study"
description: ""
category: 
tags: [algorithm]
---
{% include JB/setup %}

Let's begin with **heapify**

​	adsf

```java
private void More ...heapify() {
	for (int i = (size >>> 1) - 1; i >= 0; i--){
		siftDown(i, (E) queue[i]);
	}
}
```

Time Complexity Analysis:

Assuming it is a complete tree, the depth of which is n

```latex
\begin{equation}
n + (n-1)*2^n
\end{equation}
```

