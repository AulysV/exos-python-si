# Exos de python en SI

Version en ligne : https://aulysv.github.io/exos-python-si/

Version PDF : [Exos python si.pdf](https://github.com/AulysV/exos-python-si/files/8337227/Exos.python.si.pdf)


# Exercices de python

Aulys VINAY, 1G1 - 03/2022 (push : 04/222)

## Présentation :

```python
# Ici un commentaire en Python précédé d'un hashtag. 
largeur = int(input("Entrez largeur : "))
longueur = int(input("Entrez longueur : "))

surf = largeur * longueur
peri = 2 * largeur + 2 * longueur

print("La surface =", surf)
print("Le périmètre =", peri)

if peri < surf : 
    print("Le périmètre est inférieur à la surface")

else : 
    print("le périmètre est inférieur à la surface")
```

## Exercice 2 :

```python
# Demande des valeurs
a = float(input("Entrez a : "))
b = float(input("Entrez b : "))
c = float(input("Entrez c : "))
d = float(input("Entrez d : "))

x = (d - b) / (a - c)

y = a * x + b
print("x =", x)
print("y =", y)
```

## Exercice 3

```python
a = 5
b = 10

print("Au début : a =", a, "et b =", b, ".")

tmp = a # tmp = 5
a = b # a = 10 & b = 10
b = tmp # b = tmp = 5

print("A à fin : a =", a, "et b =", b, ".") # a = 10 et b = 5
```

## Exercice 4 :

```python
n = int(input("Entrez un nombre entier n : "))

S = 1

for i in range (n) :
    S = S * 2

print("S =", S)
```

## Exercice 5 :

```python
n = int(input("Entrer un nombre n (10 et 100) : "))

l = 1
p = 1

for i in range (n) :
    l = l + 1
    p = p*l

print("S =", p )
```

## Exercice 6 :

```python
n = int(input("Entrez un nombre entier n : "))

S = 0
l = 0

for i in range (n) : 
    l = l + 1
    S = S + l

print("S =", S)

S2 = int(n * (n + 1) / 2)

print("S =", S2)

# Les deux résultats sont égaux (S = S2)
```

## Exercice 7 :

```python
s = float(input("Entrez une somme initiale en € : s = "))
u = s # La variable u sauvegarde la somme initiale
t = float(input("Entrez un taux d'intérêt en % : t = "))
n = int(input("Entrez un nombre entier d'années :  "))

for i in range (n) :
    s = s + (s * (t/100))
    print("Intérêts percus de l'année", i, " :", s - u, "€ ")

print("Au bout de", n, "années, le montant total sur le livret est de :", s, ".")
```

## Exercice 8 :

Version "double"

```python
n = int(input("Entrez un nombre entier : "))
for i in range(1, n + 1):
    if n % i == 0:
            print(i)
print(n)
```

Version "éco"

```python
n = int(input("Entrez un nombre entier : "))
for i in range(1, n//2 + 1):
    if n % i == 0:
            print(i)
print(n)
```

## Exercice 9 :

```python
n = int(input('Entrez un nombre entier : '))

i = 2

while i < n and n % i != 0 :
    i = i + 1

if i == n :
    prem = True
else :
    prem = False

if prem :
    print('Le nombre', n, 'est premier.')
else :
    print('Ce n\'est pas un nombre premier.')
```

## Exercice 10 :

```python
ax = int(input("Enrez les coordonnées x du point a : "))
ay = int(input("Enrez les coordonnées y du point a : "))

bx = int(input("Enrez les coordonnées x du point b : "))
by = int(input("Enrez les coordonnées y du point b : "))

cx = int(input("Enrez les coordonnées x du point c : "))
cy = int(input("Enrez les coordonnées y du point c : "))

xab = bx-ax
yab = by-ay
xac = cx-ax
yac = cy-ay

if (xab * xac - xac * yab == 0) :
    print("Les points sont alignés.")

else :
    print("Les points ne sont pas alignés.")
```

## Exercice 11 :

```python
n1 = float(input("Entrez un premier nombre : "))
n2 = float(input("Entrez un deuxième nombre : "))

dis = abs(n1 - n2)

print("La distance entre les deux nombres est de :", dis)
```

## Exercice 12 :

```python
from math import *

a = float(input("Entrez a : "))
b = float(input("Entrez b : "))
c = float(input("Entrez c : "))

delta = b**2 - 4*a*c

if delta < 0 :
    print("Pas de solution")

else :
    x1 = (-b-sqrt(delta))/2*a
    x2 = (-b+sqrt(delta))/2*a
    print("x1 =", x1)
    print("x2 =", x2)
```

## Exercice 13 :

```python
import sys # Importation de la bibliothèque pour terminer le programme en cas de a nul.
from math import *

a = float(input("Entrez a : "))

if a == 0:
    print("Ce n'est pas une équation du second degré")
    sys.exit()

b = float(input("Entrez b : "))
c = float(input("Entrez c : "))

delta = b**2 - 4*a*c

if delta < 0 :
    print("Pas de solution")

else :
    x1 = (-b-sqrt(delta))/2*a
    x2 = (-b+sqrt(delta))/2*a
    print("x1 =", x1)
    print("x2 =", x2)
```

## Exercice 14 :

```python
from math import *

a = float(input("Entrez a : "))
b = float(input("Entrez b : "))
c = float(input("Entrez c : "))

if a == 0 :
    print("Ceci n'est pas une equation du second degré")
    x = -c/b
    print("La solution est", x)

else : 
    delta = b**2 - 4*a*c

    if delta < 0 :
        print("Pas de solution")

    else :
        x1 = (-b-sqrt(delta))/2*a
        x2 = (-b+sqrt(delta))/2*a
        print("x1 =", x1)
        print("x2 =", x2)
```

## Exercice 15 :

```python
from math import *

a = float(input("Entrez a : "))
b = float(input("Entrez b : "))
c = float(input("Entrez c : "))

if a == 0:
    print("Ceci n'est pas une equation du second degré")
    sol = -c / b
    print("La solution est", sol)

else:
    delta = b**2 - 4 * a * c

    if delta < 0:
        print("Pas de solution")

    else:
        x1 = (-b - sqrt(delta)) / 2 * a
        x2 = (b - sqrt(delta)) / 2 * a
        print("x1 =", x1)
        print("x2 =", x2)

x = int(
    input("Borne début : ")
)  # On appelle x la borne de début pour faciliter le calcul plus bas.
fin = int(input("Borne fin : "))
pas = float(input("Entrez le pas : "))

for t in range(fin - x):
    print("x =", x, "y=", a * x**2 + b * x + c)
    x = x + pas
```

## Exercice 16 :

```python
n = int(input("Entrez un nombre entier : "))

while n != 1:
    if n%2 == 0:
        n = n/2
        print(n)
    else :
        n = (n*3)+1
        print(n)
```

## Exercice 17 :

```python
n = int(input("Entrez un nombre entier : "))

p = 0  # Compteur d'étapes.
m = 0  # Variable qui augmente pour chaque nombre supérieur au précédent.

while n != 1:

    if n % 2 == 0:
        if n > m:  # Boucle permettant d'augmenter m à chaque nombre supérieur rencontré
            m = n
        n = n / 2
        p = p + 1
        print(n)

    else:
        if n > m:
            m = n
        n = (n * 3) + 1
        p = p + 1
        print(n)

print("Nombres d'étapes :", p)
print("Le plus grand nombre rencontré est :", m)

```

## Exercice 18 :

### Version 1 :

```python
n = 0

fib = [0, 1]

while max(fib) <= 500:
    fib.append(fib[n - 1] + fib[n - 2])

del fib[-1]

print(fib)
```

### Version 2 :

```python
n = 0
deb = int(input("Entrez une borne de début : "))  # 500 dans l'énoncé
fin = int(input("Entrez une borne de fin : "))  # 1000 dans l'énoncé

fib = [0, 1]  # Deux premiers termes de la liste

while max(fib) <= fin:
    fib.append(fib[n - 1] + fib[n - 2])

del fib[
    -1
]  # Supression du dernier élément de la liste qui est en trop (dépasse la borne fin)

x = [
    i for i in fib if i > deb
]  # Création d'une nouvelle liste qui ne prend que les nombres supérieurs à 500 (de la 1ère liste)

print(x)  # Affichage des valeurs de la liste qui vient d'être créer

```

## Exercice 19 :

### Version 1 :

```python
n = int(input("Entrez un nombre entier à convertir en binaire : "))
d = n
res = []

while n != 0 :
    q = n // 2
    r = n % 2
    res.append(str(r))
    n = q

x = res[::-1]
x = ''.join(x)

print("le nombre décimal", d, "est égal à", x, "en binaire.")
```

#### Version 1 (avec fonction) :

```python
def dec_to_bin(d):

    if d//2 in [0,1]: return str(d//2) + str(d%2)
    else: return dec_to_bin(d//2) + str(d%2)

a = int(input("Entrez d : "))
print(dec_to_bin(a))
```

#### Version 1 (récursive) :

```python
def b(d):
    return (
        b(d // 2) * 10 + d % 2 if d else 0
    )  # La fonction s'appelle elle-même. Si la condition a lieu, affiche 1, sinon 0.


a = int(input("Entrez un nombre à convertir en binaire : "))
print(f"Le nombre décimal {a} est égal à {b(a)} en binaire.")
```

#### Version 1 (opérateurs binaires) :

```python
def b(d):
  if d == 0: return '0'

  r = [0]*d.bit_length()
  i = 0
  while d:
      r[-i] = d & 1
      d >>= 1
      i += 1
  return ''.join(r)

a = int(input("Entrez un nombre à convertir en binaire : "))
print(f"Le nombre décimal {a} est égal à {b(a)} en binaire.")
```

### Version 2 :

```python
n = int(input("Entrez un nombre entier à convertir en binaire : "))
d = n
res = []  # Liste vide

while n != 0:
    q = n // 2
    r = n % 2
    res.append(str(r))  # Ajout de la valeur du reste à la liste
    n = q

bit = 8 - len(res)
for i in range(bit):
    res.append(str(0))

res = res[
    ::-1
]  # Inversion des termes de la suite (bit de poids fort et bit de poids faible)
res = "".join(
    res
)  # "Colle" les termes de la suite, au lieu d'obtenir un truc comme "[1, 0, 0, 1, 0]"

print("le nombre décimal", d, "est égal à", res, "en binaire.")
```

### Version 3 :

```python
n = int(input("Entrez un nombre entier à convertir en binaire : "))
d = n
res = []
k = 0

while n != 0:

    q = n // 2
    r = n % 2
    res.append(str(r))
    n = q

if d < 10:  # Bug pour les nombres à un chiffre, donc condition avec if

    bit = 8 - (len(res))
    for i in range(bit):
        res.append(str(0))

else:

    for k in range(1, (len(str(d)))):  # Vérifie chaque octet entre 1 et len(d)

        if d / 256 <= k and d / 256 > k - 1:  # Si division par 256 <= nombre étudié
            bit = k * 8 - (len(res))  # Calcule le nombre de 0 qu'il faut ajouter

            for i in range(bit):
                res.append(str(0))

print("Nombre d'octets :", k)


res = res[::-1]
res = "".join(res)

print(f"Le nombre décimal {d} est égal à {res} en binaire.")
```
