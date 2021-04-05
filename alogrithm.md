@[TOC](小文目录：)
算法笔记   ~码~ 码~不停蹄~

# 1、贪心算法（集合覆盖）
 <img src="https://img-blog.csdnimg.cn/20210401160331741.jpg#pic_center"   width="80%" >

# 2、普里姆算法（最小生成树-修路）

 - 应用场景——修路问题
 <img src="https://img-blog.csdnimg.cn/20210401155444828.png#pic_center"   width="70%" >
 - 思路分析

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210401155424653.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDg1NjQ5Mg==,size_16,color_FFFFFF,t_70)
# 3、克鲁斯卡尔算法（最小生成树-公交站）

 - 应用场景——公交站问题

 <img src="https://img-blog.csdnimg.cn/20210401170539579.png#pic_center"   width="85%" >
 - 思路分析
 - 
 <img src="https://img-blog.csdnimg.cn/20210401173358724.jpg#pic_center"   width="80%" >
 
#  4、动态规划（背包问题）
 - 背包问题（填表法）

 <img src="https://img-blog.csdnimg.cn/20210401175433956.png#pic_center"   width="85%" >

 - 思路分析

 <img src="https://img-blog.csdnimg.cn/20210401174435701.png#pic_center"   width="85%" >

# 5、迪杰斯特拉算法（最短路径之一点到其他各点）

 - 应用场景：最短路径（如图，求G点【指定点】到其他【各点】的最短路径）
 <img src="https://img-blog.csdnimg.cn/20210401211300209.png#pic_center"   width="50%" >
 - 思路分析：
以起始点为中心向外层层扩展( 广度优先搜索思想)，直到扩展到终点为止。上图中先找到G相邻的点A、B、E、F，然后在其中找到最小的边是2，即GA，然后以A为中心，找到A相邻的点，再在其中找到最小的边......
 - 举例
 <img src="https://img-blog.csdnimg.cn/20210401212059999.jpg#pic_center"   width="85%" >

# 6、弗洛伊德算法（最短路径之每一点到其他各点）

 - 弗洛伊德 VS 迪杰斯特拉：迪算法通过指定一点，求出从该点到其他顶点的最短路径；弗算法中每一个顶点都是出发访问点，求出从每一个顶点到其他顶点的最短路径。
 - 思路分析：找到中转点K，使得经过中转的路径小于直达的路径.如图，若中转点是V2，则从V1到V4的最短路径是3+1=4.

 
 <img src="https://img-blog.csdnimg.cn/20210401220608893.jpg#pic_center"   width="60%" >
 

 - 分析过程：找到一个起始点，一个中转点，一个结束点。然后比较中转路径和直达路径，选小的。 
   找到所有情况只需3层遍历循环：1层、所有点依次为起始点。2层、所有点依次为中转点。3层、所有点依次为结束点。

# 7、KMP模式匹配算法（字符串匹配）

 - 目的：从字符串中查找子串。不用暴力匹配算法。
 - 暴力匹配算法：如图，一个元素挨个比较，相同则继续比较，不同则子串右移再重新比较。其中右移后从g开始比较，g已经在之前的比较中知道和o,o,d,不一样，但是还是会进行比较。
<img src="https://img-blog.csdnimg.cn/2021040122401255.jpg#pic_center"   width="60%" >
 - KMP匹配算法：使暴力匹配中的重复比较去掉，即省去上面的g和o,o,d比较的步骤。因此创造了“部分匹配值“，以此值来跳过那些重复的长度。

 <img src="https://img-blog.csdnimg.cn/20210401224749541.jpg#pic_center"   width="80%" >