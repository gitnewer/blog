
遍历
forEach  从ie9开始普遍支持
indexOf  从ie9开始普遍支持

判断

Array.isArray从ie9开始支持
  Object.prototype.toString.call(arg) === '[object Array]';

方法
reverse  反向
concat 连接两个数组，返回新的数组
every  传入函数，全true返回true，否则返回false
filter 返回符合函数的元素
indexOf 找到元素的索引
join  连接
lastIndexOf
map  对每个元素执行
reduce  递归执行，前一个结果和后一个元素作为下一次的结果
reduceRight  从右执行
pop
push
shift
slice 方法返回一个从开始到结束（不包括结束）选择的数组的一部分浅拷贝到一个新数组对象。且原始数组不会被修改。
some  任一为truthy值，则true
sort，不一定稳定
splice
toLocaleString
toString
unshift

# 以下不一定可用

## IE不支持

from 从一个类数组对象复制
of  同上，从一系列元素创建数组
copyWithin  复制修改数组内部一段元素
fill  填充一段元素
entries() 方法返回一个新的Array Iterator对象
find 返回第一个符合的元素
findIndex  返回索引
includes
keys 返回迭代器
values
