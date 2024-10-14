import math
def find_columns(matrix):
return [i + 1 for i, col in enumerate(zip(*matrix)) 
if any(x < 0 for x in col) and math.prod(x for x in col if x < 0) > 0]
matrix1 = [[1, -2, 3], [-4, 5, -6], [7, -8, 9]]
matrix2 = [[-1, 2, -3], [4, -5, 6], [-7, 8, -9]]
print("Номера столбцов для матрицы 1:", find_columns(matrix1) or "Нет таких столбцов")
print("Номера столбцов для матрицы 2:", find_columns(matrix2) or "Нет таких столбцов")
