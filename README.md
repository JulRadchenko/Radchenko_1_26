print("Введите нужную цифру для K:", end=" ")
k = int(input())
file = open("text.txt",'r')
buffer = ''
chisl = ''
maxim = '0'
colich_1 = 0
colich_2 = 0
slovar = {0:'ноль', 1:'один', 2:'два',  3:'три', 4:'четыре', 5:'пять', 6:'шесть', 7:'семь', 8:'восемь', 9:'девять', 10:'A', 11:'B', 12:'C', 13:'D', 14:'E', 15:'F'}
buffer = file.read(1)
if not buffer:
    print("Файл является пустым")
    colich_2 += 1
elif buffer:
    print("Все числа:", end=" ")
    while buffer:
        if buffer != ' ':
            chislo = chislo + buffer
            buffer = file.read(1)
        else:
            if len(chsilo) > k and int(chislo,16) % 2 == 0 and int(chislo,16) < 2048:
                colich_1 += 1
                if int(maxim,16) < int(chislo,16):
                    maxim = chislo
                print(chislo, end=' ')
            chislo = ''
            buffer = file.read(1)
if colich_1 == 0 and colich_2 == 0:
        print("Чисел не найдено", end=" ")
print('')
if colich_1 > 0:
    print('Количество чисел:', colich_1)
    print('Максимальное из чисел:',end=' ')
    for j in range(len(maxim)):
        for l in range(len(slovar)):
            if str(l) == maxi[j]:
                print(slovar[l], end=' ')
                break
            elif slovar[l] == maxim[j]:
                print(slovar[l], end=' ')
