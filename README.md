 #!/bin/python3

import math
import os
import random
import re
import sys




first_multiple_input = input().rstrip().split()

n = int(first_multiple_input[0])

m = int(first_multiple_input[1])

matrix = []

for _ in range(n):
....matrix_item = input()
....matrix.append(matrix_item)import re

def decode_matrix_script(rows, columns, matrix):
    # Transpose the matrix to read characters column-wise
    transposed_matrix = [''.join(row[i] for row in matrix) for i in range(columns)]
    
    # Join the characters column by column and replace symbols or spaces with a single space
    decoded_script = ''.join(re.sub(r'(?<=[A-Za-z0-9])[^A-Za-z0-9]+(?=[A-Za-z0-9])', ' ', col) for col in transposed_matrix)
    
    return decoded_script

# Read input (number of rows and columns)
n, m = map(int, input().split())

# Read the matrix script into a list of strings
matrix_script = []
for _ in range(n):
    matrix_item = input()
    matrix_script.append(matrix_item)

# Decode the matrix script
decoded_script = decode_matrix_script(n, m, matrix_script)

# Print the decoded script
print(decoded_script)


