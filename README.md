# intersection

```
def intersection(n1,n2,n3,arr1,arr2,arr3):
  xloc = 0
  yloc = 0
  zloc = 0
  
  res = []
  
  while xloc!=n1 and yloc!=n2 and zloc!=n3:
    
    x = arr1[xloc]
    y = arr2[yloc]
    z = arr3[zloc]
    
    if x==y and x==z:
      res.append(x)
      xloc+=1
      yloc+=1
      zloc+=1
    elif x<=y and x<=z:
      xloc+=1
    elif y<=x and y<=z:
      yloc+=1
    else:
      zloc+=1
  return res
 
n1 = int(input())
n2 = int(input())
n3 = int(input())

arr1 = list(map(int, input().split()))
arr2 = list(map(int, input().split()))
arr3 = list(map(int, input().split()))

final = intersection(n1,n2,n3,arr1,arr2,arr3)

print(final)


```
