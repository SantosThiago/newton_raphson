#Thiago dos Santos
import time
from sympy import *

inicio=time.time()
x=var("x")
x0=1
erro=10**-6
f = Lambda(x, pow(x,12)*5224.05-((pow(x,11)+pow(x,10)+pow(x,9)+pow(x,8)+pow(x,7)+pow(x,6)+pow(x,5)+pow(x,4)+pow(x,3)+pow(x,2)+x+1)*692.89))
fd=Lambda(x,diff(f(x),x))
n=0

while (True):
    if (fd(x0)==0):
        print("Digite outro valor inicial")
        break
    n=n+1
    x1=x0-(f(x0)/fd(x0))

    if (f(x1)==0):
        print("Valor de x:",x1)
        break

    Er=abs(f(x1))
    Ex=abs(x1-x0)
    x0 = x1
    print("iteração",n,":","Valor de x=",x1,",Er",Er,",Ex",Ex,",Taxa=",x1-1)
    if (Er<=erro and Ex<=erro):
        break

fim=time.time()
print(f"\nTempo de Execução: {fim-inicio}")
