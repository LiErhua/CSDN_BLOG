# Python中总结出的处理不同问题的方法（数据处理）

1. 统计sequence列表中item出现的次数，并按照多少降序排列

   ```python
   #方法一
   def get_counts(sequence):
       counts = {}
       for item in sequence:
           if item in counts:
               count[item] += 1
           else:
               count[item] = 1
       return counts
   #方法二
   from collections import defaultdict
   def get_counts(sequence):
       count = dafaultdict{int}
       for item in sequence:
           count[item] += 1
       return counts
   ```

   ​

