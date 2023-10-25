# Regularexpression

\d 数字0,1,2,3，…,9

\w 单词，指当前区域语言的字母、数字和下划线。如果是中文区域语言，汉字也是单词。

\b 单词的开始或结束位置

[:digit:] 数字0~9

[:alpha:] 当前区域语言的字母

[:alnum:] 当前区域语言的字母和数字

[:lower:] 当前区域语言小写字母

[:upper:] 当前区域语言大写字母

[a-z] 小写英文字母a~z

[A-Z] 大写英文字母A~Z

[A-z] 所有大小写英文字母

^ 字符串的开始位置

$ 字符串的结束位置

. 除了换行符\n以外的任意字符

? 前面的项目重复最多一次

* 前面的项目重复了0次或者多次

+ 前面的项目重复了1次或更多次

{n} 前面的项目重复了n次

{n,} 前面的项目重复了n次或更多次

{n,m} 前面了项目重复了至少n次，不多于m次

\W 不是单词的字符

\D 不是数字的字符

\B 不是单词分界位置的位置，这个描述好晦涩

[^x] 不是x的字符

[^abo] 除了abo以外的任意字符


str_view(ft, "(.)\\1", match = TRUE)  #匹配 aa
str_view(ft, "(..)\\1", match = TRUE) #匹配 abab
str_view(ft, "(.)(.)\\2\\1", match = TRUE) #匹配 abba
str_view(fruit, "(.)(.)\\1", match = TRUE) #匹配aba
str_view(fruit, "(.)(.)\\1\\2", match = TRUE) #匹配abab
str_view(fruit, "(.)\\1(.)\\2", match = TRUE) #匹配aabb
str_view(fruit, "(.)(.).*\\2\\1", match = TRUE) #匹配ab()ba

