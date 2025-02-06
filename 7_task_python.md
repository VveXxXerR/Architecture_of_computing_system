# Architecture_of_computing_system
Kudrya_Yuriy_I-1-24


num = str(input("Enter float number >> "))
int_part = list()
float_part = list()
k = 0
while num[k] != '.':
    int_part.append(num[k])
    k += 1
int_part = "".join(int_part)
float_part = num.replace(int_part, '', 1).replace('.', '')

res1 = int(int_part, 2)
res2 = 0
for i in range(1, len(float_part) + 1):
    res2 = res2 + int(float_part[i-1], 2)*2**(-i)
print(f'binary {num} -> decimal {res1 + res2}')
