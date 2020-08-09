# 栈

LeetCode试题

## 难度:简单

#20 有效的括号

思路：使用栈来存放每个左括号，右括号根据栈顶左括号匹配则弹出，不匹配则失败，最后栈为空则成功

#155 最小栈

思路1：pop为弹出数组最后一个元素，top为数组最后一个元素，可以使用length-1操作。push则直接吧length作为索引存入数组。getMin使用for循环找最小值

思路2：getMin在每次push的时候压入2个值，一个是当前需要压入的元素，另一个是当前最小值。当pop的时候pop2个值，偶数index为当前值，奇数index为当前最小值，所以getMin时直接取最后一个索引值

#225 用队列实现栈

思路1：使用单队列时，push、top、empty直接根据数组length操作即可，对于pop要求是在对头取出，这样一来，单队列的pop就需要反转队列，然后再取队首元素，之后再反转回来

思路2：使用双队列，一个队列用于正常push、top、empty。另一个队列在pop时候使用，当pop时，有元素的队列依次取队首元素插入另一个空队列，直到旧队列只剩一个元素，这个元素就是最近插入队尾元素，把这个元素取出即可，这样一来新旧队列互换了，但是新队列少插入了一个opo的元素

#232 用栈实现队列

思路1：使用单栈，主要问题在取队首时：栈反转之后pop，再反转回去

思路2：使用双栈，同#225思路，其中一个栈pop到另一个栈中，取出最后一个元素作为队首元素，之后再把另一个栈push回来

#496 下一个更大元素I(注意审题)

思路：循环弹出nums1中的元素，nums2按顺序pop到另一个栈中，当遇到当前pop的值与nums1中pop的值相等时，说明找到对应位置。再队刚才保存pop元素的栈循环pop找到第一个大于nums1中pop的值即可，依此类推

#682 棒球比赛

思路：遍历数组，把整数push入栈，之后遇到非整数就去栈中操作数据，使用switch判断类型

#844 比较含退格的字符串

思路1：使用传统栈操作，循环字符串，按顺序入栈，遇到#则pop一个，直到循环结束，使用数组拼接字符串比较

思路2：使用字符串replace正则匹配#以及前一个字符，递归替换直到2个字符串都没有#，最后做对比

#1021 删除最外层的括号

思路：使用栈，依次入栈，当栈元素只有1时，说明是最外层的括号，大于1时说明是需要拼接的原语，需注意判断位置，在push之后，pop之前，与#20思路类似

#1047 删除字符串中的所有相邻重复项

思路1：挨个进栈，如果当前进制栈元素与栈顶相同，则栈pop，最后返回栈内元素拼接字符串

思路2：使用递归replace正则替换相邻2个字符串为空，直到没有相邻相同字符

#1441 用栈操作构建数组

思路：循环n次，当`target[i]`与当前循环i相等时说明没有pop，如果不等说明有pop操作进入下一轮判断，不相等继续pop，直到相等