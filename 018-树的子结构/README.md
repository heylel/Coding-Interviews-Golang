# 题意


输入两颗二叉树A，B，判断B是不是A的子结构。

# 分析

要查找树A中是否存在和树B结构一样的子树，可以分成两步： 

1.第一步在树A中找到和B的根节点的值一样的结点R； 这实际上就是树的遍历。可以用递归实现

递归调用HasSubTree遍历二叉树A。如果发现某一结点的值和树B的头结点的值相同，则转向第2步判断两个结点为根的数是否存在父子关系

2.第二步再判断树A中以R为根结点的子树是不是包含和树B一样的结构。 这个过程其实就是要要判断两棵树对应的节点数据是否相同。这个是一个递归的过程。

首先我们先实现第2步的操作，这个操作其实就是递归判断两个树对应节是否相同， 递归的终结是如果之前的节点均相同，最后子树为空时，而父树如果也是NULL，则说明两颗树完全一样，如果父树不是NULL，则子树是父树的一部分

