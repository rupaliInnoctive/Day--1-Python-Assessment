# Day--1-Python-Assessment

Question 1: 
	Given an "out" string length 4, such as "<<>>", and a word, return a new string where the word is in the middle of the out string, e.g. "<<word>>".
	make_out_word('<<>>', 'Yay') → '<<Yay>>'
make_out_word('<<>>', 'WooHoo') → '<<WooHoo>>'
make_out_word('[[]]', 'word') → '[[word]]'
	
SOLUTION:

def make_out_word(out,word):
   print(out[:2] + word + out[2:])

make_out_word('<<>>', 'Yay')
make_out_word('<<>>', 'WooHoo')
make_out_word('[[]]', 'word')

Question 2: 
	Given an array of ints, return True if 6 appears as either the first or last element in the array. The array will be length 1 or more.
first_last6([1, 2, 6]) → True
first_last6([6, 1, 2, 3]) → True
first_last6([13, 6, 1, 2, 3]) → False
	
SOLUTION:

def first_last6 (num):
   if num [0] == 6 or num [len(num)-1] == 6:
       print('True')
   else:
       print('False')
first_last6([1, 2, 6])
first_last6([6, 1, 2, 3])
first_last6([13, 6, 1, 2, 3])


Question 3: 
Given 2 int arrays, a and b, each length 3, return a new array length 2 containing their middle elements.
middle_way([1, 2, 3], [4, 5, 6]) → [2, 5]
middle_way([7, 7, 7], [3, 8, 0]) → [7, 8]
middle_way([5, 2, 9], [1, 4, 5]) → [2, 4]

SOLUTION:

def middle_way(arr1, arr2):
   arr3 = []
   mid_value = 0
   mid_value = 0
   if len(arr1) % 2 != 0 and len(arr2) % 2 != 0:
       mid_val1 = arr1[int((len(arr1) - 1) / 2)]
       mid_val2 = arr2[int((len(arr1) - 1) / 2)]
       arr3.append(mid_val1)
       arr3.append(mid_val2)
       print(arr3)
   else:
       print('False!!')

middle_way([1, 2, 3], [4, 5, 6])
middle_way([7, 7, 7], [3, 8, 0])
middle_way([5, 2, 9], [1, 4, 5])


Question 4:
Given a Matrix, convert it into the dictionary with keys as row numbers and values as a nested list.

Input : test_list = [[5, 6, 7], [8, 3, 2]]
Output : {1: [5, 6, 7], 2: [8, 3, 2]}
Explanation: Matrix rows are paired with row numbers in order.
	
SOLUTION:

test_list = [[5, 6, 7], [8, 3, 2]]
print('The original list is : ' + str(test_list))
result = {idx + 1 : test_list[idx] for idx in range(len(test_list))}

print("The constructed dictionary : " + str(result))



 Question 5:
Write a Python program to convert them into a dictionary in a way that item from list1 is the key and item from list2 is the value

keys = ['Ten', 'Twenty', 'Thirty']
values = [10, 20, 30]

Output - {'Ten': 10, 'Twenty': 20, 'Thirty': 30}

SOLUTION:

keys =  ['Ten', 'Twenty', 'Thirty']
values = [10, 20, 30]

d = {}
for key in keys:
   for value in values:
       d[key] = value
       values.remove(value)
       break
print("Resultant dict is : " + str(d))
