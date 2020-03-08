#QR Decomposition of 3x3, 4x4 or 5x5 Matrices with User Input
#developed by Barış Berk ZORBA

import numpy as np

#input matrix and its components
P = []
a = []
b = []
c = []
d = []
e = []
aTr = []
bTr = []
cTr = []
dTr = []
eTr = []
A = []
B = []
C = []
D = []
E = []

n=int(input("For Pascal(n), Enter n where n is min 3, max 5: "))
print("Enter the elements from left to right:") 
  
# For user input 
for i in range(n):              #for row entries 
    x =[] 
    for j in range(n):          #for column entries 
         x.append(int(input()))
    P.append(x)
print("Input matrix: ",P)

#matrix a
for i in range(n):
    aTr.append(P[i][0])
a=np.transpose(aTr)
print("a: ",a)
print("Transpose of a: ",aTr)

#matrix b
for i in range(n):
    bTr.append(P[i][1])
b=np.transpose(bTr)
print("b: ",b)
print("Transpose of b: ",bTr)

#matrix c
for i in range(n):
    cTr.append(P[i][2])
c=np.transpose(cTr)
print("c: ",c)
print("Transpose of c: ",cTr)

#matrix d
if n==4 or n==5:
    for i in range(n):
        dTr.append(P[i][3])
    d=np.transpose(dTr)
    print("d: ",d)
    print("Transpose of d: ",dTr)

#matrix e
if n == 5:
    for i in range(n):
        eTr.append(P[i][4])
    e=np.transpose(eTr)
    print("e: ",e)
    print("Transpose of e: ",eTr)

#vector A
A=a
e1=np.true_divide(a,np.linalg.norm(a))
print("A: ", A)
print("e1: ",e1)

#vector B
B=b-np.matmul(b,e1)*e1
e2=np.true_divide(B,np.linalg.norm(B))
print("B: ", B)
print("e2: ",e2)

#vector C
C=c-np.matmul(c,e1)*e1-np.matmul(c,e2)*e2
e3=np.true_divide(C,np.linalg.norm(C))
print("C: ", C)
print("e3: ",e3)

#vector D
if n==4 or n==5:
    D=d-np.matmul(d,e1)*e1-np.matmul(d,e2)*e2-np.matmul(d,e3)*e3
    e4=np.true_divide(D,np.linalg.norm(D))

#vector E
if n==5:
    E=e-np.matmul(e,e1)*e1-np.matmul(e,e2)*e2-np.matmul(e,e3)*e3-np.matmul(e,e4)*e4
    e5=np.true_divide(E,np.linalg.norm(E))

#output
if n<4:
    Q=[e1, e2, e3]
    R=[[np.matmul(a,e1),np.matmul(b,e1),np.matmul(c,e1)],[0,np.matmul(b,e2),np.matmul(c,e2)],[0,0,np.matmul(c,e3)]]
    print("Q= ",Q)
    print("R= ",R)
elif n==4:
    Q=[e1,e2,e3,e4]
    R=[[np.matmul(a,e1),np.matmul(b,e1),np.matmul(c,e1),np.matmul(d,e1)],[0,np.matmul(b,e2),np.matmul(c,e2),np.matmul(d,e2)],[0,0,np.matmul(c,e3),np.matmul(d,e3)],[0,0,0,np.matmul(d,e4)]]
    print("Q= ",Q)
    print("R= ",R)
elif n==5:
    Q=np.array[e1,e2,e3,e4,e5]
    R=[[np.matmul(a,e1),np.matmul(b,e1),np.matmul(c,e1),np.matmul(d,e1),np.matmul(e,e1)],[0,np.matmul(b,e2),np.matmul(c,e2),np.matmul(d,e2),np.matmul(e,e2)],[0,0,np.matmul(c,e3),np.matmul(d,e3),np.matmul(e,e3)],[0,0,0,np.matmul(d,e4),np.matmul(e,e4)],[0,0,0,0,np.matmul(e,e5)]]
    print("Q= ",Q)
    print("R= ",R)
