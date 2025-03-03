# C语言课程设计

## C语言实现通讯录
实现一个通讯录；  
通讯录可以用来存储1000个人的信息，每个人的信息包括：姓名、性别、年龄、电话、住址。

提供方法：  

- 添加联系人信息
- 删除指定联系人信息
- 查找指定联系人信息
- 修改指定联系人信息
- 显示所有联系人信息
- 清空所有联系人
- 以名字排序所有联系人

🌿🌿注：这是一个简单的通讯录，实现方案是初级版。  
只能在程序运行期间存在（没有写入文件）。

![C语言实现通讯录实现](https://github.com/summerjava/awosome-cs/blob/main/C%E8%AF%AD%E8%A8%80/C%E8%AF%AD%E8%A8%80%E8%AF%BE%E7%A8%8B%E8%AE%BE%E8%AE%A1/C%E8%AF%AD%E8%A8%80%E5%AE%9E%E7%8E%B0%E9%80%9A%E8%AE%AF%E5%BD%95.pdf)


## C语言实现计算器
### 简单版本
实现简单的加减乘除。

### 用栈实现稍复杂的四则运算
为了达到目的，首先自学了栈：按照先进后出的原则存储数据，先进入的数据被压入栈底，最后的数据在栈顶，需要读数据的时候从栈顶开始弹出数据。允许进行插入和删除操作的一端称为栈顶(top)，另一端为栈底(bottom)；栈底固定，而栈顶浮动；栈中元素个数为零时称为空栈。插入一般称为进栈（PUSH），删除则称为退栈（POP）。允许进行插入和删除操作的一端称为栈顶(top)，另一端为栈底(bottom)；栈底固定，而栈顶浮动；栈中元素个数为零时称为空栈。插入一般称为进栈（PUSH），删除则称为退栈（POP）。

![C语言实现计算器](https://github.com/summerjava/awosome-cs/blob/main/C%E8%AF%AD%E8%A8%80/C%E8%AF%AD%E8%A8%80%E8%AF%BE%E7%A8%8B%E8%AE%BE%E8%AE%A1/C%E8%AF%AD%E8%A8%80%E5%AE%9E%E7%8E%B0%E8%AE%A1%E7%AE%97%E5%99%A8.pdf)


## C语言实现LRU缓存
请你设计并实现一个满足  LRU (最近最少使用) 缓存 约束的数据结构。

实现 LRUCache 类：

LRUCache(int capacity) 以 正整数 作为容量 capacity 初始化 LRU 缓存  
int get(int key) 如果关键字 key 存在于缓存中，则返回关键字的值，否则返回 -1 。  
void put(int key, int value) 如果关键字 key 已经存在，则变更其数据值 value ；如果不存在，则向缓存中插入该组 key-value 。如果插入操作导致关键字数量超过 capacity ，则应该 逐出 最久未使用的关键字。  
函数 get 和 put 必须以 O(1) 的平均时间复杂度运行。

![C语言实现LRU缓存](https://github.com/summerjava/awosome-cs/blob/main/C%E8%AF%AD%E8%A8%80/C%E8%AF%AD%E8%A8%80%E8%AF%BE%E7%A8%8B%E8%AE%BE%E8%AE%A1/C%E8%AF%AD%E8%A8%80%E5%AE%9E%E7%8E%B0LRU%E7%BC%93%E5%AD%98.pdf)

## 生命游戏
用结构类型编写一个程序，完成生命游戏的功能：（选做）

20世纪70年代，一种被称作“生命游戏”的小游戏曾风靡一时。这种游戏相当简单，假
设有一个像棋盘一样的方格网，每个方格中放置一个生命细胞，生命细胞只有两种状态：“生”
或“死”。游戏规则如下：

- 如果一个细胞周围有3个细胞为生（一个细胞周围共有8个细胞），则该细胞为生，即该细胞若原先为死，则转为生，若原先为生，则保持不变；
- 如果一个细胞周围有2个细胞为生，则该细胞的生死状态保持不变；
- 在其他情况下，该细胞为死，即该细胞若原先为生，则转为死，若原先为死，则保持不变。

依此规则进行迭代变化，使细胞生生死死，会得到一些有趣的结果。该游戏之所以被称
为“生命游戏”，是因为其简单的游戏规则，反映了自然界中的生存规律：如果一个生命，
其周围的同类生命太少的话，会因为得不到帮助而死亡；如果太多，则会因为得不到足够的
资源而死亡。

写一个程序，模拟生命游戏过程。

## 最佳运动员评选问题
从100名优秀运动员中评选出10名最佳运动员。具体规则如下：

- 运动员按1，2，3，…，100顺序编号；
- 由键盘输入所收到的选票，每张选票至多可写10个不同的编号；
- 对应名次的运动员编号可以有空缺，但必须用0表示；
- 若编号超出规定的范围，或编号重复出现，作废票处理；
- 按选票中所列最佳运动员顺序给他们计分，计分标准如下：从第一名至第十名所得分数依次为：15，12，9，7，6，5，4，3，2，1； 
- 按各运动员所得分数高低进行排队，列出最佳运动员前10名排名表，格式为：  
名次 运动员编号 合计得分 合计得票数  
如果得分相同，则得票多的排名在前；如果得分和得票都相同，则编号小的在前。

（提示：评选过程分为3个步骤：接收选票、选票检查看是否为废票，以及有效票统计。）

## 五子棋游戏
试编制一个五子棋游戏，要求每一颗棋子放在棋盘上时有相应的伴音，每一局棋结束时播放一段音乐