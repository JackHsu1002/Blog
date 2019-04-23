---
layout: post
title: Java8 LocalDate
tags: [Java]
description: Java8 LocalDate.
fullview: true
comments: true
---

#### 常用LocalDate與LocalDateTime方法。

Java8 的 LocalDate 與 LocalDateTime實在太好用了，整理一下常用的方法，免得東找西找像個無頭蒼蠅，一方面手打下來也有助於記憶。

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