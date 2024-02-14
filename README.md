salary = [int(s) for s in open('/home/student/Рабочий стол/salary.txt')] #разделяем данные по спискам
company = [s for s in open('/home/student/Рабочий стол/Company.txt')]
role = [s for s in open('/home/student/Рабочий стол/role.txt')]
ma1 = 0 #задаем переменные для поиска максимумов
ma2 = 0
ma3 = 0

top_1 = '' #задаем перменные для названия компаний
top_2 = ''
top_3 = ''

ind_ma_1 = 0 #переменные для индексов максимумов в списках
ind_ma_2 = 0
ind_ma_3 = 0

for x in range(len(salary)): #начинаем перебор по списку зарплат
    if ma1 < salary[x]: #находим максимальную
        ma1 = salary[x]
        ind_ma_1 = x #запоминаем инедекс макс заплаты
top_1 = str(company[ind_ma_1]) + '-' + str(role[ind_ma_1]) + '-' + str(salary[ind_ma_1]) #по найденному индексу ищем в других списках соответствующие этой зарплае данные
salary.remove(salary[ind_ma_1]) #удаляем максимум, чтобы найти второй максимум
company.remove(company[ind_ma_1])
role.remove(role[ind_ma_1])

for x in range(len(salary)): #аналогичный перебор второй раз
    if ma2 < salary[x]:
        ma2 = salary[x]
        ind_ma_2 = x
top_2 = str(company[ind_ma_2]) + '-' + str(role[ind_ma_2]) + '-' + str(salary[ind_ma_2])
salary.remove(salary[ind_ma_2])
company.remove(company[ind_ma_2])
role.remove(role[ind_ma_2])

for x in range(len(salary)):
    if ma3 < salary[x]:
        ma3 = salary[x]
        ind_ma_3 = x
top_3 = str(company[ind_ma_3]) + '-' + str(role[ind_ma_3]) + '-' + str(salary[ind_ma_3])
salary.remove(salary[ind_ma_3])
company.remove(company[ind_ma_3])
role.remove(role[ind_ma_3])
print(top_1) #выводим результат
print(top_2)
print(top_3)
    
