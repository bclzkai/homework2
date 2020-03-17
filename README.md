# homework2
homework2
def count_char(fn): 
2 	import os.path 
3 	if os.path.isfile(fn): 
4 		with open(fn,'r') as fh: 
5 			total = 0 
6 			for line in fh: 
7 				for char in ('#','/','\n',':'): 
8 					line = line.replace(char," ") 
9 				total += len(line.strip().split()) 
10 			return total  
11 print(count_char('./readme.md')) 
