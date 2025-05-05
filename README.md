import math

def geometric_mean(A, n):
    product = 1
    for i in range(n):
        product *= A[i][i]
    G = product ** (1 / n)
    return G
n = int(input("Enter the size of the matrix (n): "))
A = []

print("Enter the elements of the matrix row by row (space separated):")
for i in range(n):
    row = list(map(int, input(f"Row {i+1}: ").split()))
    A.append(row)
result = geometric_mean(A, n)
print(result)
