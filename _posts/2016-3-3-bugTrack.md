---
title:        "BugTrack"
# jekyll-seo-tag
description:  "iOS程序如何追踪bug"
image:        "http://placehold.it/400x200"
author:       "jiapeijun"
---

<p class="lead">
一般在app项目的开发过程中，都有专业的测试人员进行测试bug，而最严重的bug就是crash。而又因为一些其它原来，这些crash并不是能百分百的复现，所以看懂苹果的crash文件，也成为了app开发人员的重要能力之一。
</p>

## Crash文件
首先我们编写一段有Crash的代码

```
- (void)viewDidLoad {
    [super viewDidLoad]; 
    NSArray *array = [NSArray new];
    NSLog(@"%@", array[1]);
    // Do any additional setup after loading the view.
}
```
将程序运行在手机上，并拔线再运行一次，让手机生成crash文件。
再回到xcode

![](image/201603051518.jpg)
