### 基于用户的协同过滤算法
- 基于用户的协同过滤算法主要包括两个步骤：
   - 找到和目标用户兴趣相似的用户集合;
   - 找到这个集合中的用户喜欢的，且目标用户没有听说过的物品推荐给目标用户.

**寻找第一步的用户集合**
> 采用Pearson相关系数用户x和y的相似度：
> ```python
>(np.sum(x_.T*y))/(np.sqrt(np.sum(x.T*x)*np.sum(y.T*y)))
```

**第二部的推荐部分**
> 导入了*numpy*中的transpose---find and return index (type=numpy.ndarray) 以及nonzero return 非零tuple
>```python
p = np.transpose(np.nonzero(this_one))
l = np.transpose(np.nonzero(user))
if p not in l:  # Then I can find that different quickly.
```

-----------------------------------------------------------------------------------  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;made by ZhangJin 
