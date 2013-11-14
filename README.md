Dedupe-Function
===============

Dedupe function

import csv

reader1= csv.reader(open('firstlist.csv', 'r'), delimiter=',')
reader2=csv.reader(open('secondList.csv', 'r'), delimiter=',')
newFile=csv.writer(open('newFile.csv', 'wb'), delimiter=',')

name = []
for row in reader2: 
   if row not in reader1:
      name.append(row)

print name
newFile.writerows(name)

