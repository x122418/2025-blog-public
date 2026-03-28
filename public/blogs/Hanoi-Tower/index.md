今天写数据机构与算法作业，碰到一道经典的递归问题，汉诺塔。

一个古老的印度神庙里有三根柱，其中一个自上而下放置了由小到大的64个金盘。僧
侣们依照以下规则把 64 个金盘移动到另一个柱子上： 

- 一次只能移动一个金盘； 
- 金盘只能在柱子上存放； 
- 小盘必须始终放置在大盘上方

传说中，64个金盘移动完世界毁灭…… 

请设计并用Python实现算法，接收用户输入的金盘数目N，输出将金盘从柱子0移动到柱子2的全过程。输出格式为：move(a, x, y)，其中a为盘子编号（1～N），x和y为柱子编号（0～2），表示将盘子a从柱子x移动到柱子y。

解决该问题的关键在于拆分出完成金盘移动的状态，想要完成移动，需要拆分出三大步骤

- 将柱子0的n-1个上方盘子移动到1
- 将柱子0的最下方盘子移动到2
- 将柱子1的n-1个盘子移动到2

```
def hanoi(num, source, auxiliary, target):
    if num == 1:
        print(f'move(1, {source}, {target})')
    else:
        hanoi(num-1, source, target, auxiliary)
        print(f'move({num}, {source}, {target})')
        hanoi(num-1, auxiliary, source, target)

```