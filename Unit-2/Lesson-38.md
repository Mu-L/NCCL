
## Lesson 38 - 堆排序问题

### 课程任务
堆是一个近似完全二叉树的结构，并同时满足堆的性质：即子结点的键值或索引总是小于（或者大于）它的父节点。如果根节点是大值，则称为最大堆。

堆排序算法的基本思想是，将数组A创建为一个最大堆，然后交换堆的根(最大元素)和最后一个叶节点x，将x从堆中去掉形成新的堆A1，然后重复以上动作，直到堆中只有一个节点。

通常堆是通过一维数组来实现的。在起始数组为 0 的情形中：

* 父节点i的左子节点在位置 (2*i+1);
* 父节点i的右子节点在位置 (2*i+2);

#### 堆、二叉树和数组下标的对应关系
![heap-array](../images/heap-array.png)

#### 堆排序算法
* 数组的起始状态（随机排列）  
![heap-random](../images/heap-random.png)

* 最大堆调整（Max_Heapify），将堆的末端子节点作调整，使得子节点永远小于父节点  
![heap-0-max-heapify](../images/heap-0-max-heapify.png)

* 建立最大堆树（Build_Max_Heap）：将堆所有数据重新排序  
![heap-1-build-max](../images/heap-1-build-max.png)

* 交换根节点（最大值）和数组最后那个位置的元素，然后对 size-1 重新进行“建立最大堆树”  
![heap-2-swap-max-to-last](../images/heap-2-swap-max-to-last.png)
![heap-3-swap-max-to-next](../images/heap-3-swap-max-to-next.png)

* 重复以上动作，直到堆中只有一个节点  
![heap-4-swap-to-first](../images/heap-4-swap-to-first.png)


### 参考资料
* 堆排序 <http://zh.wikipedia.org/wiki/堆排序>
* 经典排序算法 - 堆排序Heap sort <http://www.cnblogs.com/kkun/archive/2011/11/23/2260286.html>

