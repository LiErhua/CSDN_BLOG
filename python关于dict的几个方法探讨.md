# python关于dict的几个方法探讨



```python
import json
```


```python
d = {
    'a': 1,
    'b': 2,
    'c': [3,4],
}

print(json.dumps(d))
```

```python
{"c": [3, 4], "a": 1, "b": 2}
```

```python
c = {"c": [3, 4], "a": 1, "b": 2}
list(c.keys())
#python3中keys,values,items方法不能再直接返回列表，需要一个转换
```

其中keys方法输出所有的键


```Python
['a', 'c', 'b']
```
values方法输出所有的值
```python
list(c.values())
```
    [1, [3, 4], 2]

  items（）方法输出对应的键值对的touple
```python
list(c.items())
```


    [('a', 1), ('c', [3, 4]), ('b', 2)]

