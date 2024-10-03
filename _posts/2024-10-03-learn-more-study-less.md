---
layout: post
title: ifLab新生训练营笔记
categories: Blog
description: 展示ifLab新生训练营的学习成果
keywords: GitHub, Markdown, Vscode
---


通过这一周多的的学习，我在各位导师的指导下，学习到了不少有用的知识，收获颇多，以下是我在这段时间的学习学习感悟和成果。

## 学习感悟
在这一段时间里，我初步了解了GitHub和Markdown的使用，了解了GitHub的基本操作和Markdown的基本语法，并在GitHub上搭建了自己的第一个博客并发表了第一篇文章来记录我的学习。在学习过程中，我发现GitHub和Markdown是非常强大的工具，可以帮助我更好地记录和分享我的学习成果。同时，我学会了配置Vscode的环境并熟练使用Vscode，掌握了基本的代码编写和调试技巧。此外，我还对大模型的应用有了了初步的了解，希望在未来的学习中能够进一步深入学习和应用大模型。

## 学习成果
### 任务①：博客搭建与GitHub的初接触
![]()
### 任务②：vscode安装配置与代码自测


#### 井字棋测试结果

![](/images/blog/1.2.png) ![](/images/blog/1.3.png)

#### C++环境测试
##### 冒泡排序测试代码：
```c++
#include <iostream>
#include <vector>
using namespace std;

void bubbleSort(vector<int>& arr) {
    int n = arr.size();
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
            }
        }
    }
}

int main() {
    vector<int> arr = {64, 34, 25, 12, 22, 11, 90};
    bubbleSort(arr);
    cout << "排序后的数组: ";
    for (int num : arr) {
        cout << num << " ";
    }
    cout << endl;
    return 0;
}

}
```
##### 测试结果：
![]()
#### 其他语言测试：
##### python绘制图表代码：
```Python
import numpy as np
import matplotlib.pyplot as plt
from pylab import mpl 
# 设置字体属性，确保在生成的图像中能够正常显示中文
mpl.rcParams['font.sans-serif'] = ['SimHei']        # 指定默认字体为黑体
mpl.rcParams['axes.unicode_minus'] = False      # 解决将负号'-'显示为方块的问题
years = np.arange(2011, 2024)  # 生成从2011到2023的年份数组
beijing_gdp = [17188.8, 19024.7, 21134.6, 22926, 24779.1, 27041.2, 
29883, 33106, 35445.1, 35943.3, 40269.6, 41610.9, 43760.7] 
beijing_population = [2023.8, 2077.5, 2125.4, 2171.1, 2188.3, 2195.4, 
2194.4, 2191.7, 2190.1, 2189, 2185.6, 2184.3, 2185.8] 
width=0.35
colors = plt.cm.viridis(np.linspace(0, 1, 13))
plt.subplot(2,1,1)
plt.bar(years,beijing_population, width,color=colors,)
plt.xticks(years,fontsize=7)
plt.ylim(1900,+2300)
plt.legend("人口数")
for i in range(len(years)):
    plt.text(years[i],beijing_population[i],str(beijing_population[i]),ha="center",fontsize=7)
plt.title("张三-北京市历年人口数")
plt.xlabel("年份")
plt.ylabel("人口数（单位：万人）")
plt.subplot(2,1,2)
plt.plot(years,beijing_gdp,'r.--')
plt.xticks(years,fontsize=7)
plt.ylim(10000,+50000)
for i in range(len(years)):
    plt.text(years[i],beijing_gdp[i]+500,str(beijing_gdp[i]),ha="center",fontsize=7)
plt.legend("GDP增长")
plt.title("张三-北京市历年GDP增长")
plt.xlabel("年份")
plt.ylabel("GDP（单位：亿元）")
plt.tight_layout()
plt.show()
```
##### 测试结果：

![](/images/blog/1.1.png)
### 任务③：从零入门CPU部署大模型&应用开发
#### 创建Agent
##### 智谱清言智能体链接：
https://chatglm.cn/main/gdetail/66f7ef5c81047b45dcf07ea2?lang=zh

##### 智能体相关配置如下：
![](/images/blog/2.1.png)
![](/images/blog/2.2.png)
![](/images/blog/2.3.png)
![](/images/blog/2.4.png)
#### CPU大模型搭建结果
##### 流式输出:
![](/images/blog/2.5.png)
##### 构建简单 Gradio 前后端应用:
![](/images/blog/2.6.png)
##### 构建Streamlit 应用:
![](/images/blog/2.7.png)
