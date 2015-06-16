練習問題 8.1 

def back(word):
	i = 0
	length = len(word) - 1
	while i < len(word):
		letter = word[length - i]
		print letter
		i = i + 1

back("Hello")

実行結果
o
l
l
e
H

練習問題 8.2 

prefixes = "JKLMNOPQ"
sufix = "ack"

for letter in prefixes:
	if letter == "O" or letter =="Q":
		print letter +"u"+ sufix
	else:
		print letter + sufix

以下実行結果
Jack
Kack
Lack
Mack
Nack
Ouack
Pack
Quack

練習問題 8.3 
fruit[x:y]としたときにxを省略すると先頭の文字からとなり、
yを省略すると文字列の最後の文字となる。そのためfruit[:]は
文字列の最初から最後までつまり文字列そのものを表す。

練習問題 8.4 

def find(word, letter, index):
	while index < len(word):
		if word[index] == letter:
			return index
		index = index + 1
	return -1

練習問題 8.5 

def count(word,letter):
	index = 0
	for i in word:
		if i == letter :
			index = index + 1
	print index


count("Hello", "l")

実行結果
2

練習問題 8.6

def count(word,letter):
	index = 0
	print find(word,letter,index)

count("Hello", "l")
実行結果
2

練習問題 8.7 

word = "banana"
print word.count("a")

実行結果
3


練習問題 8.9

def is_reverse(word1, word2):
	if len(word1) != len(word2):
		return False
	i = 0
	j = len(word2) -1
	while j >= 0:
		print i,j
		if word1[i] != word2[j]:
			return False
		i = i + 1
		j = j - 1
	return True


print is_reverse("pots","stop")

以下実行結果

0 3
1 2
2 1
3 0
True
