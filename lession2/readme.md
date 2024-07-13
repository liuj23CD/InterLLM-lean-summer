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


from collections import Counter

import re

text = """
Got this panda plush toy for my daughter's birthday,
who loves it and takes it everywhere. It's soft and
super cute, and its face has a friendly look. It's
a bit small for what I paid though. I think there
might be other options that are bigger for the
same price. It arrived a day earlier than expected,
so I got to play with it myself before I gave it
to her.
"""
#print (text)

words = re.findall(r'\b\w+\b',text.lower())

words_count = Counter(words)

#print(words)

print(words_count)




The OUTPUT is 
Counter({'it': 7, 'i': 4, 'for': 3, 's': 3, 'and': 3, 'a': 3, 'got': 2, 'to': 2, 'this': 1, 'panda': 1, 'plush': 1, 'toy': 1, 'my': 1, 'daughter': 1, 'birthday': 1, 'who': 1, 'loves': 1, 'takes': 1, 'everywhere': 1, 'soft': 1, 'super': 1, 'cute': 1, 'its': 1, 'face': 1, 'has': 1, 'friendly': 1, 'look': 1, 'bit': 1, 'small': 1, 'what': 1, 'paid': 1, 'though': 1, 'think': 1, 'there': 1, 'might': 1, 'be': 1, 'other': 1, 'options': 1, 'that': 1, 'are': 1, 'bigger': 1, 'the': 1, 'same': 1, 'price': 1, 'arrived': 1, 'day': 1, 'earlier': 1, 'than': 1, 'expected': 1, 'so': 1, 'play': 1, 'with': 1, 'myself': 1, 'before': 1, 'gave': 1, 'her': 1})

![image](https://github.com/user-attachments/assets/35814b46-33ff-45b3-8a19-be6b41b159cd)
