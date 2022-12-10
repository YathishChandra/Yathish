input_array=[[3,3,3,3,3,5,6],[2.5, 2.5 ,2.5, 2.5, 2.5, 4, 4],[4,4,4,4,4,4,10],[1.5, 1.5, 1.5, 1.5, 1.5, 1.5, 1.5],[2, 2, 2, 2, 2, 4 ,4]]
d={}
d["TOI"]=sum(input_array[0])
d["Hindu"]=sum(input_array[1])
d["ET"]=sum(input_array[2])
d["BM"]=sum(input_array[3])
d["HT"]=sum(input_array[4])
weekly_budget=int(input())
lst=["TOI","Hindu","ET","BM","HT"]
answer=[]
for i in range(len(lst)):
    for j in range(i+1,len(lst)):
        if d[lst[i]]+d[lst[j]]<weekly_budget:
            tmp=[]
            tmp.append(lst[k])
            tmp.append(lst[l])
            answer.append(tmp)
print(answer)
