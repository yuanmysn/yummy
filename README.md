# yummy
自己随便玩玩吧
# -*- coding:utf-8 -*-
import xlrd
x=[]
file = 'abc.xlsx'
data=xlrd.open_workbook(filename=file)
table=data.sheets()[0]
for i in range(table.nrows):
    ty=table.row_values(i)
    tablestr=str(ty)
    x.append(tablestr[1:5])#1:5，其中0是[,且并不到5

for m in range(len(x)):
    for n in range(len(x)-m):
        if x[m] == x[m+n] and (n != 0):
            print m,m+n,table.row_values(m),table.row_values(m+n)#真实的序号表示的时候应该+1


