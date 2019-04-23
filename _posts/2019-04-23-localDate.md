---
layout: post
title: Java8 LocalDate
tags: [Java]
description: Java8 LocalDate.
fullview: true
comments: true
---

#### 常用LocalDate與LocalDateTime方法。

Java8 的 LocalDate 與 LocalDateTime實在太好用了，他簡化了非常多轉換的問題，
這邊整理一下常用的方法，不然相同問題老是Google真令人汗顏，另一方面手打下來也可以幫助記憶。

### LocalDate ###  

1. 取得幾個月前的日期:

		LocalDate now = LocalDate.now();
		LocalDate lastMonth = now.minusMonths(1);
		※例如2019-01-01的上個月，會是2018-12-01。 參數代表幾個月前。	    

2. 取得當月最後一天的日期:  

		import java.time.temporal.TemporalAdjusters;		

		LocalDate now = LocalDate.now();
		LocalDate lastDayOfMonth = now.with(TemporalAdjusters.lastDayOfMonth());
		※例如2019-02-01的當月最後一天，會是2019-02-28。 閏月的日期也有考量進去。	