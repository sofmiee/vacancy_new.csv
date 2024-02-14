salary=[int(s) for s in open('/home/student/Рабочий стол/salary.txt')]
company=[s for s in open('/home/student/Рабочий стол/Company.txt')]
role=[s for s in open('/home/student/Рабочий стол/role.txt')]
ma1=0
ma2=0
ma3=0

top_1=''
top_2=''
top_3=''

ind_ma_1=0
ind_ma_2=0
ind_ma_3=0

for x in range(len(salary)):
    if ma1<salary[x]:
        ma1=salary[x]
        ind_ma_1=x
top_1=str(company[ind_ma_1])+'-'+str(role[ind_ma_1])+'-'+str(salary[ind_ma_1])
salary.remove(salary[ind_ma_1])
company.remove(company[ind_ma_1])
role.remove(role[ind_ma_1])

for x in range(len(salary)):
    if ma2<salary[x]:
        ma2=salary[x]
        ind_ma_2=x
top_2=str(company[ind_ma_2])+'-'+str(role[ind_ma_2])+'-'+str(salary[ind_ma_2])
salary.remove(salary[ind_ma_2])
company.remove(company[ind_ma_2])
role.remove(role[ind_ma_2])

for x in range(len(salary)):
    if ma3<salary[x]:
        ma3=salary[x]
        ind_ma_3=x
top_3=str(company[ind_ma_3])+'-'+str(role[ind_ma_3])+'-'+str(salary[ind_ma_3])
salary.remove(salary[ind_ma_3])
company.remove(company[ind_ma_3])
role.remove(role[ind_ma_3])
print(top_1)
print(top_2)
print(top_3)
    
