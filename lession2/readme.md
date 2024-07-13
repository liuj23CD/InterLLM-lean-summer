任务一
请实现一个wordcount函数，统计英文字符串中每个单词出现的次数。返回一个字典，key为单词，value为对应单词出现的次数。
使用 Counter及re可以简单实现

from collections import Counter
import re
text = """Hello world!  
This is an example.  
Word count is fun.  
Is it fun to count words?  
Yes, it is fun!"""
#print (text)
words = re.findall(r'\b\w+\b',text.lower())
words_count = Counter(words)
#print(words)
print(words_count)

![image](https://github.com/user-attachments/assets/1f865a43-f8ea-487a-b2b8-dc3ee4ce0ec4)
仅要结果的输出：
![image](https://github.com/user-attachments/assets/6412aa66-3aca-4d15-9490-d9699d2ac2f8)


