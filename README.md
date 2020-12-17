# euler-problem-4
import math
list1=[]

for i in range(100,1000):
    for j in range(100,1000):
        t=0
        a=i*j
        a=str(a)
        l=len(a)
        if l%2:
            k=math.trunc(l/2)+1
            for m in range(k):
                if a[m]==a[l-1-m]:
                    t+=1
            if k==t:
                a=int(a)
                list1.append(a)
        else:
            k=math.trunc(l/2)
            for m in range(k):
                if a[m]==a[l-1-m]:
                    t+=1
            if k==t:
                a=int(a)
                list1.append(a)
list1=set(list1)
list2=sorted(list1)
print(max(list2))
