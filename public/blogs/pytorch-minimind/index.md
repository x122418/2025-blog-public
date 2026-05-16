<details>
	<summary>torch.arange</summary>
  	用于创建一个一维张量（Tensor），其值是一个等差数列。

```python
# 从0开始 到10结束（不包含） 步长为2
torch.arange(0, 10, 2)
# tensor([0, 2, 4, 6, 8])
	
# 步长可以为浮点数
torch.arange(0, 1, 0.25)
# tensor([0, 0.25, 0.5, 0.75])

# 步长可以为负数
torch.arange(5, 0, -1)
# tensor([5, 4, 3, 2, 1])
```
</details>




<details>
	<summary>torch.div</summary>
  	用于完成张量之间的逐元素相除。

```python
a = torch.tensor([[1, 2, 3], 
                  [4, 5, 6]])
b = torch.tensor([[1, 1, 1], 
                  [2, 2, 2]])
c = torch.div(a, b)
# c = torch.tensor([[1.0, 2.0, 3.0],
#                 [2.0, 2.5, 3.0]])
	
```
</details>




<details>
	<summary>torch.repeat_interleave</summary>
  	用于完成张量保留原本顺序的复制（而非整块的复制 区别于torch.repeat。

```python
a = torch.tensor([1,2,3])
b = torch.repeat_interleave(a, repeats=2)
# b = torch.tensor([1, 1, 2, 2, 3, 3])
	
```
</details>



<details>
	<summary>torch.argsort</summary>
  	获取张量的顺序索引。

```python
a = torch.tensor([3, 1, 2])
b = torch.argsort(a)  # indexes of the sorted elements
# b = torch.tensor([1, 2, 0])
	
```
</details>



<details>
	<summary>torch.bincount</summary>
  	获取数组中各个数字的统计数量（按升序）

```python
a = torch.tensor([0, 1, 1, 2, 2, 2])
b = torch.bincount(a)
# b = torch.tensor([1, 2, 3])  # counts of each integer in the input tensor
	
```
</details>