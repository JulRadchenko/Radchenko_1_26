#Шестнадцатиричные четные числа, не превышающие 2048в10 и содержащие более К цифр. Вывести числа и их количество. Максимальное число вывести прописью.

print("Введите нужную цифру для K:", end=" ")
k = int(input())
buffer = ''
chislo = ''
maxim = '0'
colich_1 = 0
colich_2 = 0
slovar = {0:'ноль',1:'один',2:'два',3:'три',4:'четыре',5:'пять',6:'шесть',7:'семь',8:'восемь',9:'девять',\
     'A':'десять','B':'одинадцать','C':'двенадцать','D':'тринадцать','E':'четырнадцать','F':'пятнадцать'}
with open("text.txt",'r') as f:
    buffer = f.readline(1)
    if not buffer:
        print("Файл является пустым")
        colich_2 +=1
    while buffer:
        while buffer in ['1','2','3','4','5','6','7','8','9','0','A','B','C','D','E','F']:
            chislo += buffer
            buffer = f.readline(1)
        if len(chislo) > 0:
            if len(chislo) > k and int(chislo,16) % 2 ==0 and int(chislo,16) <= 2048:
                colich_1 += 1
                if int(maxim,16) < int(chislo,16):
                    maxim = chislo
                print(chislo, end=' ')
        chislo = ''
        buffer = f.read(1)
if colich_1 == 0 and colich_2 == 0:
        print("Чисел не найдено", end=" ")
print('')
if colich_1 >0:
    print('Количество чисел:', colich_1)
    print('Максимальное из чисел:',end=' ')
    for j in range(len(maxim)):
        for l in slovar:
            if str(l) == maxim[j]:
                print(slovar[l], end=' ')
                break
            elif str(l) == maxim[j]:
                print(slovar[l], end=' ')
