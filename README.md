import numpy as np
def calculate(a):
 if(len(a)<9):
  print("List must contain nine numbers")
 else:
  a1=a.reshape(3,3)
  mean=np.mean(a1,axis=1)
  mean1=np.mean(a1,axis=0)
  mean2=np.mean(a1)
  v=np.var(a1,axis=1)
  v1=np.var(a1,axis=0)
  v2=np.var(a1)
  std=np.std(a1,axis=1)
  std1=np.std(a1,axis=0)
  std2=np.std(a1)
  ma=np.max(a1,axis=1)
  ma1=np.max(a1,axis=0)
  ma2=np.max(a1)
  mi=np.min(a1,axis=1)
  mi1=np.min(a1,axis=0)
  mi2=np.min(a1)
  sum=np.sum(a1,axis=1)
  sum1=np.sum(a1,axis=0)
  sum2=np.sum(a1)
  r={
   'mean':[mean,mean1,mean2],
    'variance':[v,v1,v2],
    'standard deviation':[std,std1,std2],
    'max':[ma,ma1,ma2],'min':[mi,mi1,mi2],
    'sum':[sum,sum1,sum2]
    }
  print(r)

a=np.array([0,1,2,3,4,5,6,7,8])
calculate(a)
