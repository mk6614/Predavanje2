# Predavanje2

Pogledali si bomo nova osnovena tipa - boolean in seznam, if stavek in pa zanke - while in for.

## Boolean

Tip boolean ima lahko samo eno izmed dveh vrednosti: `True` ali `False` (pazimo na veliko začetnico):

```
b1 = True
b2 = False
```

Nad booleanom alko izvajamo osnovne operacije:
```
#AND
a = b1 and b2           #a <- False
a = True and True       #a <- True
#OR
a = b1 or b2            #a <- True
a = False or False      #a <- False
#NOT
a = not False           #a <- True
#EQUALS
a = (False == False)    #a <- True
#DOES NOT EQUAL
a = (False != False)    #a <- False
#IS LESS/LESS OR EQUAL TO
a = (3 < 4)             #a <- True 
a = (3 <= 4)            #a <- True 
#IS MORE/MORE OR EQUAL TO
a = (3 > 4)             #a <- False 
a = (3 <= 4)            #a <- False 

```

Pazimo tudi na prednostne funkcije; tako kot ima potenciranje prednost pred množenjem in množenje pred seštevanjem, velja da ima `not` prednost pred `and` in ta pred `or`:
```
c = (not a or b1 and b2 ==  (not a) or (b1 and b2)  #c <- True
```

Funkcija za pretvorbo tipa v boolean je naslednja:
```
a = bool(1)         #a <- True
a = bool(1.0)       #a <- True
a = bool(-1)        #a <- True
a = bool(-1.0)      #a <- True
a = bool("Mojca")   #a <- True
a = bool([1,2,3])   #a <- True
a = bool(0)         #a <- False

a = bool(0.0)       #a <- False
a = bool("")        #a <- False
a = bool([])        #a <- False
```


## Seznami

Pogledali si bomo nov tip: seznam (ang. list/array). 

### Možni seznami:
```
seznam = []                     #prazen seznam
seznam = [1,2,3,4]              #seznam celih števil
oseba = ["Mojca", "Kolšek", 24] #mešani seznam
matrika = [ [1,0,0,0], [0,1,0,0], [0,0,1,0], [0,0,0,1] ]                     #seznam seznamov
```

### Dostop do elementa v seznamu:
```

a = seznam[0]                   #a <- 1
a = seznam[-1]                  #a <- 4
a = seznam[4]                   #a <- ERROR

vrstica1 = matrika[0]           #vrstica <- [1,0,0,0]
vrstica2 = matrika[1]

stolpec1 = [ matrika[0][0], matrika[1][0], matrika[2][0], matrika[3][0] ]  #seznam elementov: stolpec1 = [1,0,0,0]
```

### Funkcije na seznamih:
```
seznam.append(5)                #seznam <- [1,2,3,4,5]
seznam.insert(5,6)              #seznam <- [1,2,3,4,5,6]
length = len(seznam)            #length <- 6
```
### operacije na seznamih:
```
a = seznam[1:3]                 #a <- [2,3]
a = seznam[0:]                  #a <- [1,2,3,4,5,6]
a = seznam[3:]                  #a <- [4, 5, 6]
a = seznam[:3]                  #a <- [1, 2, 3]
a = seznam[0:]                  #a <- [1,2,3,4,5,6]
```



# If stavek
If stavek razveji program glede na nek pogoj:

```
if (a > b):                     # pogoj: a < b
    print("a je večji od b")
else if (a = b):
    print("a je enak b")
else:
    print("a je manjši od b")
```
Možni pogoji so vse vrednosti, ki se lahko opredelijo kot boolean:
```
if (True and False)
```




# Zanke
```

```


## While
Naslednji kratek program izpiše števila od ena do vključno 9
```
i = 0
while(i < 10):                  #0....9
    print(i)
    i = i + 1
```
In naslednji izpiše samo soda števila, manjša od 9:
```
i = 0
while(i < 10):                  #0,2,4,6,8
    print(i)
    i = i + 2
```

## For
Naslednja programa seštejeta števila iz seznama

```
seznam = [1,2,3,4,5,6]
sum = 0
int i = 0
while (i < len(seznam)):
    sum += seznam[i]              
#sum <- 21
```

```
seznam = [1,2,3,4,5,6]
sum = 0
for stevilo in seznam:
    sum += stevilo              
#sum <- 21
```


# Vaje

## Fibonačijevo zaporedje:
Fibonačijevo zaporedje je definirano z prvima dvema členoma $a_0$ in $a_1$ in z $a_i$ za vsako naslednji člen i:

$a_0 = 0$ 

$a_1 = 1$

$a_i$ = $a_{i-2}$  + $a_{i-1}$

Tretji člen je torej $a_2$ = $a_0$ + $a_1$ = 0 + 1 = 2.

Zapiši prvih 100 členov v spremenljivko tipa seznam in ga na koncu programa izpiši. Začni s spodnjim osnovnim seznamom:
```
fib = [0, 1]
i = 0
while(i < 100):
    ai =  
    fib.append(ai)
    i +=1

print(fib)
```

## Iskanje največjega števila v seznamu

Napiši progra, ki v neurejenem seznamo najde in izpiše največje število iz seznama.

```
seznam = [20,654,684,20,3,2,0,-59,416,1,9*10,95,35,67,8,2,6,426,-42,641,-33,259,5**9,4,1100,355546,20251,46,31203,51,354131,351384,684,351,351,313+788,339,121,020,351,35,1684,684684,313*976,1351,354,8468464,6846+4186468,846531,21,57,59,365965,68746,845313,7,41,5135468*61,4684**2,684,6,1351,3,84684,684,15135353,6846,33337,8431,35,18,4864,86468,4,684-789,31,684684,684*5,684,6,135,135183,4684,4,97,987,864,1531**2,53,46,4697**5,9789,789,78,6465468,7,87,97,68,46,584,684,84,9*577,97*97,86,4,6854,6884,684*654,0,23]
```
## Soda števila
I prejšnjega seznama izpiši števila, ki so soda (deljiva z 2).

## Praštevila
Napiši program, ki ugotovi, ali je neko pozitivno število $n$ praštevilo.
Praštevilo je število, ki je deljivo samo z 1 in samim sabo.
Spomni se na opreacijo `%`: 
```
a = 10 % 2      #a <- 0 ostanek pri deljenju z 2
a = 10 % 3      #a <- 1 ostanek pri deljenju s 3
```

Napiši program, ki iz prejšnjega seznama izpiše praštevila.


## Diagonala matrike
Napiši program, ki izpiše diagonalne elemente matrike.
```
matrika = [ [1,0,0,0], [0,1,0,0], [0,0,1,0], [0,0,0,1] ]                     #seznam seznamov

"""
0 1 2 3
- - - - 
1 0 0 0 | matrika[0]
0 1 0 0 | matrika[1]
0 0 1 0 | matrika[2]
0 0 0 1 | matrika[3]
"""

```







