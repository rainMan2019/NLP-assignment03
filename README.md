# NLP-assignment03
- 实现旅行家问题
- 梯度下降(修改损失函数)
- 编辑距离

# answer questions:
## Part 5-1: review machine learning
1)	Why do we use Derivative / Gredient to fit a target function?¶
Ans: 让预测函数的参数值朝着让损失函数的值减少的方向运动，通过计算损失函数对未知参数的导数可以知道目标函数的自变量的变化方向，从而以最快速度来最小化损失函数的值
2)	In the words 'Gredient Descent', what's the Gredient and what's the Descent?¶
Ans: 梯度就是导数的意思，下降是指让损失函数的值变小，即最小化损失函数的值

3)	What's the advantages of the 3rd gradient descent method compared to the previous methods?
Ans: 有方向性，预测函数的参数一直朝着损失函数值减少的方向运动，并且可以控制学习率，因此可以加快求解最小损失函数所对应的最优参数
4)	Using the simple words to describe: What's the machine leanring.¶
Ans: 根据历史数据，学习得到一个预测函数，并且最小化损失函数来调参，从而可以预测未知数据

## Part 5: Answer following questions:
1.	Why do we need dynamic programming? What's the difference of dynamic programming and previous talked searchproblme?

1：遇到重复子问题时，递归求解时会有大量的重复计算，所以用一个数组存储中间结果，当遇到重复子问题时只要访问数组就行，而不需要重复计算一次，从而提高了运行速度，这是一种以空间换时间的应用。
2：搜索问题只要访问每一个状态就行，不需要计算这个状态的值，而动态规划将一个大问题分解为小问题时，也就是从一个状态转移到另外一个状态时需要计算这种状态，才能做出转移策略，通过访问数组保存了这个状态值从而避免重复计算

2.	Why do we still need dynamic programming? Why not we train a machine learning to fit a function which could get the rightanswer based on inputs?

因为后一个状态依赖于前面的状态，最终结果只能从一个状态转移到另外一个状态，最终到达最优状态，不能直接从输入就得到最优状态，因此需要动态规划来解决。
3.	Can you catch up at least 3 problems which could solved by Dynamic Programming?

01背包问题，旅行家问题，编辑距离（edit distance）
4.	Can you catch up at least 3 problems wich could sloved by Edit Distance?

字符串相似度，子串匹配，最长公共子序列
5.	Please summarize the three main features of Dynamic Programming, and make a concise explain for each feature.

- 最优子结构：当问题的最优解包含了其子问题的最优解时，称该问题具有最优子结构性质。
- 重叠子问题：在用递归算法自顶向下解问题时，每次产生的子问题并不总是新问题，有些子问题被反复计算多次。动态规划算法正是利用了这种子问题的重叠性质，对每一个子问题只解一次，而后将其解保存在一个表格中，在以后尽可能多地利用这些子问题的解。

- 描述最优解的结构
- 递归定义最优解的值
- 按自底向上的方式计算最优解的值
- 由计算出的结果构造一个最优解
6.	What's the disadvantages of Dynamic Programming? (You may need search by yourself in Internet)

1.	没有统一的标准模型；
2.	数值方法求解时存在维数灾。
3.	不同问题的阶段划分、状态识别等内容常需要不同的方法，无统一方法
4.	对于复杂问题，不同的处理方法得到的最优策略可能不同
5.	约束条件的存在，增加了问题的求解难度
