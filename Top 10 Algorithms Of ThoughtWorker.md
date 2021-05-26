Top 10 Algorithms Of ThoughtWorker: 

```
1) 二分查找(非递归算法) 针对有序数组: 
2) 分治算法——汉诺塔的最佳实践
3) 动态规划算法——背包问题
4) KMP算法——字符串匹配 区别于暴力匹配
5) 贪心算法——集合覆盖问题
6) 普里姆算法——修路问题 最小生成树与极小连通子图
7) 克鲁斯卡尔算法——公交站问题 加权连通图的最小生成树算法
8) 迪杰斯特拉算法——最短路径 
9) 弗洛伊德算法——与迪杰斯特拉算法的比较
10) 马踏棋盘算法——回溯法
```

| 应用场景               | 相关的数据结构和算法    | 原理剖析                                                     | 实现步骤(图解)                                               | 代码实现                                                     |
| ---------------------- | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 有序数组的值target查找 | 二分查找                |                                                              |                                                              | int left = 0 ;int right = arr.length - 1;<br/>										while(left < right){<br/>											int med = (left + right )/2;	if(arr[med] == target ){return med;}else if(arr[med] < target){	left = med + 1;}else{	right = med - 1;}}return -1;<br/>									} |
| 合并排序、快速排序     | 分治算法                |                                                              |                                                              |                                                              |
| 背包问题               | 动态规划                | 列表找到状态转换方程(列表找规律) 类似数组中根据目标和选元素  | dp[i] = dp[i - j* j] + 1;                                    | 将v[0][j]=0;v[i][j] = 0;if(w[i] > j){ v[i][j] = v[i -1][j]}else{ v[i][j] = max(v[i - 1][j] ,v[i] + v[i - 1][j - w[i]]); |
| 覆盖问题               | 贪心算法                | 每次选择当前覆盖电台与all电台中的最大值，然后将最大覆盖的添加到select电台中 |                                                              |                                                              |
| 修路问题(最小生成树)   | Prim算法	(顶点)      |                                                              |                                                              |                                                              |
| 公交站台问题           | 克鲁斯卡尔算法 (边排序) |                                                              |                                                              |                                                              |
| 邮差派送问题(最短路径) | Dijkstra迪杰斯特拉算法  | 广度优先 + 贪心                                              | 选择并确定下一个访问顶点                                     | public void dijkstra(){ VertexVisited vv = new VertexVisited(); update(index); for(int i = 1;i < vertex.length;i ++){		int index = vv.updateIsvisited();update(index);} |
| 最短路径               | Floyd佛洛依德算法       |                                                              | 区别于dijkstra算法，以每个顶点计算到其余顶点的距离，时间复杂度高于前者 |                                                              |
| 马踏棋盘(骑士周游问题) | 回溯算法                | 找到每个点可以走的point集合，然后依次遍历  + 优化(贪心算法)  | 优化：每次优先选择 当前point可走的下一个point中的可走步数最小的点 |                                                              |

基础: 数据结构
	线性结构 + 非线性结构
	线性结构: 顺序存储结构(数组) + 链式存储结构(链表、队列、栈 )
	非线性结构: 二维数组、多维数组、广义表、树结构、图结构
1. KMP算法
	基本思路: 
	代码实现: 
	应用场景: 字符串匹配、
	
2. 分治算法
	基本思路: 
	代码实现: 
	应用场景: 汉诺塔游戏(三塔n圆盘移动)、求数组的最大子序列和、八皇后问题(非同行、同列、同对角) 归并排序
	
3. 回溯算法: 
	基本思路: 
	代码实现: 
	应用场景: Hot100-子集(方法的递归实现、参数列表的确定)
	
4. 图的深度遍历 + 贪心算法: 
	
5. 排序算法: Sort Algorithm
	
	内部排序: 
	
	| 插入排序         | 直接插入排序 (逐个插入)    | 有序插入 无序复制                            |
	| ---------------- | -------------------------- | -------------------------------------------- |
	|                  | 希尔排序 (分组)            | 步进减半 逐步后移 发现交换(发现移位)         |
	| 选择排序         | 简单选择算法               | 逆序交换 最小置前                            |
	|                  | 堆排序                     |                                              |
	| 交换排序         | 冒泡排序                   | 逆序交换 最大置后                            |
	|                  | 快速排序                   | 找中轴值 左增右减 左右交换 等值减增 左右递归 |
	| 归并排序         | 分而治之 链表合并 填充数组 |                                              |
	| 基数排序(桶排序) |                            |                                              |
	
	外部排序: 
	时间频度: T(n) = 3n + 1 忽略常数项、忽略系数、忽略低阶项
	时间复杂度: O(n) = n 
	常见的时间复杂度: 
	
	> ​	1) 常数阶O(1)
	> ​	2) 对数阶O(log2 n)
	> ​	3) 线性阶O(n)
	> ​	4) 线性对数阶阶O(n*log N)
	> ​	5) 平方阶O(n^2)
	> ​	6) 立方阶O(n^3)
	> ​	7)k次方阶O(n^k)
	> ​	8) 指数阶O(2^n) < O(n! )



6. 查找算法

  > 线性查找: O(n)
  > 二分查找: 	针对有序数组的查找、对多重复值的查找	mid = (left + right)/2
  > 插值查找: 针对均匀分布的有序数组查找，自适应查找，有优势	mid =low + (high - low)* (findVal - arr[low])/(arr[right] -arr[low]);
  > 斐波那契(黄金分割)查找: 	mid = low + f[k] -1; 



DataStructure: 
1)稀疏数组: 
	应用：棋盘的存盘与读取、地图的存盘与读取
	实现：第一行存储棋盘的行(row)、列(col)、非零的数据个数(n)
		第二行至第n+1行存储的是非零数据的行号、列号、数据值
2)队列与环形队列: 
	类变量: 

```
private int front; private int rear; private int maxSize; private int[] arrQueue;
```


​	构造器: 

```
public ArrayQueue(int maxSize){
			//front表示队列的头指针，即队列的第一个元素的前一个元素索引；rear表示的是队列的尾指针，即队列的最后一个元素的索引	
			arrQueue = new int[maxSize]; front = -1; rear = -1;
			//环形队列时的front与rear表示的含义不同: 
			//front表示队列的头指针，即队列的第一个元素索引；rear表示的是队列的尾指针，即队列的最后一个元素的下一个元素的索引
			//arrQueue = new int[maxSize]; front =0; rear =0; 其实可不写，类变量在默认初始化中已赋值为0
		}
```

​	成员方法: 
​		

```
public void enQueue(int num){ 
			if(isFull()){ 
				throws new RuntimeException("队列已满，不能添加数据");
			} 
			rear++;//指针后移
			arrQueue[rear] = num;
			//环形队列中: 顺序有所不同，判断队列为空条件不变: rear == front; 
			//判断队列为满条件由: rear == maxSize -1 ; -> (rear + 1) % maxSize == front; 
			//读取有效数据的个数由rear - front ; -> (rear + maxSize - front) % maxSize
			//arrQueue[rear] = num;
			//rear = (rear + 1) % maxSize ;//指针后移，注意索引需求模
		}
		public int deQueue(){ 
			if(isEmpty){ 
				throws new RuntimeException("队列为空，不能移出数据");
			} 
			front++;//指针后移
			return arrQueue[front];
			//循环队列：
			//int value = arrQueue[front];
			//front = (front + 1) % maxSize ;//指针后移，注意索引需求模
			//return value;
		}
		peek(); showQueue();isFull();isEmpty();exist();size();
3)单链表SingleLinkedList:	与双链表DoubleLinkedList: 
	class MySingleLinkedList{
		//构造器: 
		public MySingleLinkedList(){
		}
		public void add(HeroNode heroNode){
			//因头结点不能移动，故需要借助一个辅助变量进行添加
			HeroNode temp = heroNode;
			while(true){
				if(temp == null){
					break;
				}
				temp = temp.next;
			}
			temp.next = heroNode;
		}
		public void addByOrder(HeroNode heroNode){
			//因头结点不能移动，故需要借助一个辅助变量进行添加
			HeroNode temp = heroNode;
			boolean flag = false;//此标志用于记录是否存在编号一致的节点
			while(true){
				//根据具体需求实现
				if(temp.next.no > heroNode.no){
					break;
				}else if(temp.next.no == heroNode.no){
					flag = true;
					break;
				}
				temp = temp.next;
			}
			if(flag){
				System.out.printf("编号为%d 的英雄已经存在，不能添加重复的英雄", heroNode.no);
				return;
			}
			heroNode.next = temp.next;
			temp.next = heroNode;
		}
	}
```

结点类：

	class HeroNode{	
		private int no;
		private String name;
		private int age;
		private String nickname;
		private HeroNode next;
		//构造器
		public HeroNode(int no,String name,int age,String nickname){
			this.no = no;
			this.name = name;
			this.age = age;
			this.nickname = nickname;
		}
		public int getNo(){
			return this.no;
		}
		public void setNo(int no){
			this.no = no;
		}
	}
双向链表DoubleLinkedList: 
	
		
	Class MyDoubleLinkedList{
		private HeroNodeD head = new HeroNodeD(0,"","");
		public MyDoubleLinkedList(){
		}
		
		//增加结点(直接添加结点到链表的尾部)
		public void add(HeroNodeD node){
			//因头指针不能移动，需要借助辅助结点
			HeroNodeD temp = this.head;
			while(true){
				if(temp.next == null){
					temp.next = node;	
					node.pre = temp;
					break;
				}
				temp = temp.next;
			}
		}
		// 增加结点(按照结点的no增序)
		public void addByOrder(HeroNodeD node){
			//因头指针不能移动，需要借助辅助结点
			HeroNodeD temp = this.head;
			while(true){
				if(temp.next.no > node.no){
					node.next = temp.next;
					node.pre = temp;
					temp.next = node;
					temp.next.pre = node;
					break;
				}
				temp = temp.next;
			}
		}
		//删除结点
		public void delete(int no){
			//因头指针不能移动，需要借助辅助结点
			HeroNodeD temp = this.head;
			while(true){
				if(temp == null){//查找到链表的尾部
					System.out.println("结点序号为 %d 的结点不存在" + no);
					break;
				}else if(temp..no == no){
					temp.pre.next = temp.next;
					if(temp.next != null){
						temp.next.pre = temp.pre;//若删除的结点是最后一个结点，此处可能报空指针异常
					}	
					break;
				}
				temp = temp.next;
			}
		}
	
	}
	Class HeroNodeD(){
		private int no;
		private String name;
		private String nickName;
		private HeroNodeD next;
		private HeroNodeD pre;
	
		public HeroNodeD(int no, String name, String nickname){
			this.no = no;
			this.name = name;
			this.nickName = nickname;
		}
	
		public int getNo(){
			return this.no;
		}
		public void setNo(int no){
			this.no = no;
		}
	}

4) 栈MyStack	(数组实现栈的功能)
	

```
Class MyStack{
		private int maxSize;
		private int[] arrayStack;
		private int top;
		public MyStack(int maxSize){
			this.top = -1;
			this.maxSize = maxSize;
			this.arrayStack = new int[maxSIze];
		}
		//显示栈数据
		public void show(){
			if(isEmpty()){
				System.out.println("栈为空，没有数据");
			}
			for(int i = top ;i >= 0; i--){
				System.out.printf("arrayStack[%d] = %d\n" ,i ,arrayStack[i]);
			} 
		}
		public void push(int value){
			if(isFull()){
				System.out.println("栈已满，不能压入数据！");
				return;
			}
			top++;
			arrayStack[top] = value;
		}
		public int pop(){
			if(isEmpty()){
				throw new RuntimeException("栈为空，无法弹出数据！");
			}
			int value = arrayStack[top];
			top --;
			return value;
		}
		public boolean isFull(){
			return top == maxSize - 1;
		}
		public boolean isEmpty(){
			return top ==  - 1;
		}
	}
```

// 练习: 用链表实现栈
*栈的应用场景：

> ​	1) 子程序的调用: 存储下一个指令的地址
> ​	2) 处理递归调用: 存储下一个指令的地址外 + 参数和区域变量等数据存储到堆栈中
> ​	3) 表达式的转换(中缀表达式转后缀表达式) + 求值(实际解决)
> ​	4) 二叉树的遍历
> ​	5) 图形的深度优先遍历(depth - first)搜索算法

5) 前缀表达式、中缀表达式、后缀表达式(逆波兰表达式)：
eg: 计算表达式：(3+4)*5-6
前缀表达式：从表达式的右边开始，从右至左开始遍历，最后有-减法 从栈顶元素减去次栈顶元素			- * + 3 4 5 6
中缀表达式：人们最为习惯的方式遍历，从左至右依次遍历，判断符号的优先级计算，但是计算机计算麻烦，一般转为后缀表达式	3 4 + 5 * 6 -
后缀表达式：从表达式的左边开始，从左至右开始遍历，最后有-减法 从次栈顶元素减去栈顶元素			3 4 + 5 * 6 -

难点(面试常问)：
	Q: 如何将中缀表达式转换为后缀表达式？1+((2+3)*4) -5
	A: 思路如下: 
	1.建立两个栈：一个运算符栈s1 一个中间过程栈s2 分别用于存储操作符及小括号等；另一个栈用于存储中间过程；
	2.依次遍历字符串的每个字符，然后判断是数字、操作符、括号

 	3. 若该字符是数字，则直接入栈s2;
 	4. 若字符为操作符，则分情况讨论: 
     	4.1 若s1为空，或s1栈顶元素为"("，直接入栈s1;
     	4.2 否则该字符的优先级与s1栈顶元素的优先级高，则直接压入栈s1;
     	4.3 否则将s1出栈并将出栈元素压入栈s2，重复执行4.1与新栈顶元素的运算符进行比较
 	5. 若该字符为括号"("或")"
     	5.1若为"("，则直接入栈s1；
     	5.2 若为")"，则依次弹出s1中栈顶元素，直到遇到"("为止，此时将一对括号丢弃；
 	6. 重复步骤2-5直到遍历到表达式的末尾，
 	7. 然后将s1中的元素依次弹出入栈s2;
 	8. 最后将栈s2中的元素依次弹出，然后逆序输出则为后缀表达式
     6) 递归调用Recursion : 
     def: 方法自己调用自己的方式
     *递归的应用场景: 
     1) 数学问题：8皇后问题，汉诺塔问题，阶乘问题，迷宫问题，球和篮子问题
     2) 算法问题：快排，归并排序，二分查找，分治算法
     3) 将用栈解决的问题 -> 归并排序较为简洁

> ```
> 递归需要遵循的重要规则: 
> 1) 执行一个方法时，就创建一个新的受保护的独立空间(栈空间)；
> 2) 方法的局部变量是独立的，互不影响；
> 3) 如果方法中使用的是引用类型变量，就会共享该引用类型变量的数据；
> *4) 递归必须向退出递归的条件递进，否则出现无限递归，出现StackOverflowError;
> 5) 当一个方法执行完毕，或遇到return就会返回，遵守谁调用，就将结果返回给谁，同时当方法执行完毕或者返回，该方法就执行完毕。
> ```

7) 排序算法: 

> ​	冒泡排序、选择排序——max后移 相邻交换 	min前置 
> ​	插入排序、希尔排序——
> ​	快速排序、归并排序——找中轴值 左增右减 
> ​	基数排序、堆排序——
> ​	
> 8) 哈希表Hashtable: 
> ​	实现: 数组 + 链表
> ​	数组的特点: 查找快，增删慢	——copy()一个数组副本，ArrayList底层维护了一个object[] 数组，动态适应数组长度capcity，需要扩容时，调用grow方法扩容elementData为*1.5
> ​	链表的特点: 增删快，查找慢	LinkedList
> ​	树的特点: 既可以保证检索速度，也可以保证增删速度；	如 排序二叉树

9) 树Tree：

​	树的结构: 
​		节点；根节点；父节点；子节点；叶子节点；
​		结点的权(节点的值)；路径(root节点到该节点的路径)；层；子树；树的高度；森林
​	二叉树: 每个节点最多只能有两个子节点
​		满二叉树: 所有的叶子节点都在最后一层；且所有节点的个数为2^n -1
​		完全二叉树: 所有的叶子节点都是最后一层或倒数第二层, 且最后一层的叶子节点在左边连续，倒数第二层的节点在右边连续
​	二叉树的遍历: 

> ​		前序遍历: 先输出父节点；在判断左子节点是否为空，再对左节点中序递归输出；再输出右节点
> ​		中序遍历: 先判断左子节点是否为空，再对左节点中序递归输出；再输出父节点；再输出右节点
> ​		后序遍历: 先判断左子节点是否为空，再对左节点中序递归输出；再输出右节点；再输出父节点；

		前序搜索: 先判断当前节点id是否是所搜索的节点id
	
		删除节点: 先判断当前节点的下一个节点id是否是所搜索的节点id

顺序存储二叉树: 
	针对完全二叉树: 将二叉树存储为数组或	将数组转换为二叉树(前序遍历、中序遍历、后序遍历)
	索引为2*n + 1;2*n +2
应用场景: 堆排序

线索化二叉树: 

> ​	中序线索二叉树: left 可能指向左子树，也可能指向前驱节点; 
> ​	遍历线索化二叉树: 原来的遍历方式不能使用，需要和中序遍历结果相同	

堆排序: 

> ​	大顶堆: arr[i] >= arr[2*i + 1]; arr[i] >= arr[2*i - 1];
> ​	小顶堆: arr[i] <= arr[2*i + 1]; arr[i] <= arr[2*i - 1];
> 堆排序思想: 

> ​	1)将无序序列构建成一个堆，根据升序或者降序需求选择大顶堆或者小顶堆；	即 先将首个非叶子结点及其左右节点构建为大顶堆
> ​	2) 将栈顶元素与末尾元素交换，使最大元素下沉到数组末端；
> ​	3) 重新调整结构adjustHeap()使其满足大顶堆，继续交换栈顶元素与当前元素；直到整个序列有序

WPL最长带权路径: 
	哈夫曼树: 

```
create HuffmanTree(){	
			//step1: 将string转为byte[],然后利用map计算每个字符出现的次数，然后创建list存储节点node信息
			//利用list先对节点的value或weight排序后，以从list中取出最小的两个节点的value或weight之和创建parent节点，
			//将最小的两个节点连接在父节点的左右子树下；然后将parent节点加入到list中，删除左右节点；返回list.get(0);
			List<Node> list = new ArrayList<>();
			for(Map.Entry entry: map.entrySet()){
				list.add(new Node(map.getKey(),map.getValue));
			}
			while(list.size() > 1){
				Collections.sort(list);
				Node leftNode = list.get(0);
				Node rightNode = list.get(1);
				Node parent =new Node(null, leftNode.getWeight + rightNode.getWeight);
				parent.setLeft(leftNode);
				parent.setRight(rightNode);
				list.add(parent);
				list.remove(leftNode);
				list.remove(rightNode);
			}
			return list.get(0);
	}
```

​	定长编码；变长编码；哈夫曼编码(func: 无损压缩)
​	哈夫曼编码压缩文件:
​		1) 获取原始数据的byte[] (toBinaryBytes()),将其转换为哈夫曼树结构后的byte[]，和哈夫曼编码表HashMap<String,Byte>
​		2) 文件输入流与文件输出流(对象输入流可以read()和write())
BST二叉排序树: 
​	def: 一颗二叉树满足，该二叉树上所有的结点，其左子树上所有节点的值都小于父节点的值，其右子树上的值均大于父结点的值；
​	二叉排序树的add(); delete(); infixOrder(); search(); searchParent(); 
多叉树: 
​	def: 每个节点有多个数据项(>2).通过重新组织节点，降低树的高度，提高检索效率
​	func:  B树，广泛引用于数据库和文件系统，
B树、B+树、B*树: 多路搜索树
​	B-tree的阶: 节点的最多子节点个数, eg: 2-3树
​	

> ​	*B-tree: 关键字分布在整棵树，故数据可以存储在叶子节点，也可以存储在非叶子节点。搜索性能相当于每次都做二分查找
> ​	B+树: 所有数据均存储在叶子节点；不可能在非叶子节点命中数据，稠密索引；func： 适合文件索引系统
> ​	B*树: 在非叶子节点中增加了指向兄弟节点的索引，块的最低使用率为2/3，而B+树的块的最低使用率为1/2；分配新节点的概率低于B+树，空间分配率更高。
> 对比：	与HashMap和Hashtable的优劣对比: 
> ​		hash表的优点是: 	索引定位快，能够在很短的时间内，利用hash函数定位到数据的位置。
> ​		但缺点是: 		hash索引不支持顺序和范围查找。
> ​		而B+树因有序的特点，对于这种范围查找优势很明显。

(10)图:
	func：处理多对多的关系；而链表是只有前驱和后继节点，树中只能有一个前驱节点即父节点。
	相关概念: 顶点、边、路径、无向图、有向图、带权图、
	图的表示方式: 二维数组(邻接矩阵)、链表(邻接表) 
	

图: 
	构造:  insertVertexs(int vertex){};	insertEdges(int weight){} 	
	获取图中的某顶点的相邻顶点: getFirstAdjacent(int vertex){};	getNextVertex(int vertex1,int w){};
	dfs深度优先遍历: 
		

```java
public void dfs(int vertex,boolean[] flag){ 
			if(!isVisited[vertex]){
				isVisited[vertex] = true;
				System.out.println(vertexs.get(vertex));
				int w = getFirstAdjacent(vertex);
				while(w != -1){
					if(!isVisited[w] ){
						isVisited[w] = true;	
						System.out.print(vertexs.get(w) + " -> ");
						dfs(w,flag);
					}	
					w = getNextAdjacent(w,w );
				}
			}
		}
		//方法的重载，在于遍历非连通图
		public void dfs(){
			boolean[] isVisited = new boolean[vertexs.size()];
			for(int i = 0; i < vertexs.size(); i++){
				if(!isVisited[i]){
					dfs(i,isVisited);
				}
			}
		}
```

​	bfs广度优先遍历: 