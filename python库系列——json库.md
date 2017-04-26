# python库系列——json库

Python自带的json库，可以将json对象转化为普通的dict来处理

```python
import json
a_string = '{"a":1,"b":2}'
a_dict = json.loads(a_string)
#json.loads（）会将一个string类转化为一个标准的字典格式
print(a_dict)
输出：{'a': 1, 'b': 2}
```

```python
import json
d = {
    'a': 1,
    'b': 2,
    'c': [3,4],
}
#json.dumps()会讲一个如上格式的dict转化为一个标准的字典文件
print(json.dumps(d))
输出：{"c": [3, 4], "a": 1, "b": 2}
```

