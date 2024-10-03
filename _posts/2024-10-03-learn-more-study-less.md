---
layout: post
title: ifLab新生训练营笔记
categories: Blog
description: 展示ifLab新生训练营的学习成果
keywords: GitHub, Markdown, Vscode
---
通过这一周多的的学习，我在各位导师的指导下，学习到了不少有用的知识，收获颇多，以下是我在这段时间的的学习成果。


## 任务①：博客搭建与GitHub的初接触
经过各位导师的细心指导，我初步了解了Github的使用，并成功通过Github搭建了自己的博客。在这一过程中，我还学会了如何使用Markdown来编写博客文章并将该文章上传到Github上。这篇博客即为我在这一阶段的学习成果。
## 任务②：vscode安装配置与代码自测
在这一阶段，虽然我之前已经使用过vscode并且配好了相应的C++环境，但对Vscode的使用并不熟练。经过这一阶段的学习，加深了我使用vscode的熟练程度，以下即为我在Vscode中的代码自测结果。

### C++测试代码：
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
#### 测试结果：
![](/images/blog/1.0.png)

### 井字棋测试代码结果：

<video width="320" height="240" controls>
    <source src="井字棋.mp4" type="video/mp4">
</video>

### pyhon测试代码：
```Python
import numpy as np
import matplotlib.pyplot as plt
from pylab import mpl 
# 设置字体属性，确保在生成的图像中能够正常显示中文
mpl.rcParams['font.sans-serif'] = ['SimHei']        # 指定默认字体为黑体
# rcParams['font.sans-serif'] = ['SimSun']            #【若电脑上没有黑体，可指定默认字体为宋体】
mpl.rcParams['axes.unicode_minus'] = False      # 解决将负号'-'显示为方块的问题
years = np.arange(2011, 2024)
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
#### 测试结果：

![](/images/blog/1.1.png)
## 任务③：从零入门CPU部署大模型&应用开发
### 智谱清言智能体链接：
https://chatglm.cn/main/gdetail/66f7ef5c81047b45dcf07ea2?lang=zh

#### 智能体相关配置如下：
![](/images/blog/2.1.png)
![](/images/blog/2.2.png)
![](/images/blog/2.3.png)
![](/images/blog/2.4.png)
### CPU大模型搭建结果：
#### 流式输出:
![](/images/blog/2.5.png)
#### 构建简单 Gradio 前后端应用:
![](/images/blog/2.6.png)
#### 构建Streamlit 应用:
![](/images/blog/2.7.png)
