# Rozkład $X$
## `Zbieżności zmiennych losowych`

Niech $X_n$ $-$  ciąg zmiennych losowych na $(\Omega,\,\mathbb{F},\,\mathbb{P})$. Mówimy,  żę $X_n$ zbiega do $X$.
### Zbieżność prawie na pewno $X_n\xrightarrow{p.n}X$
$$
\lim_{n\to \infty}X_n(\omega)=X(\omega)
$$
### Zbieżność według prawdopodobieństwa $X_n\xrightarrow{\mathbb{P}}X$
$$
\large \forall_{\varepsilon > 0} \quad \lim_{n \to \infty} P(|X_n - X| \ge \varepsilon) = 0
$$
### Zbieżność według rozkładu $X_n\xrightarrow{d}X$
$$
\large \lim_{n \to \infty} F_{X_n}(x) = F_X(x) \quad \text{dla każdego punktu ciągłości } F_X
$$
### Zbieżność w $L^p$ $X_n \xrightarrow{L^p} X$
$$
\large \lim_{n \to \infty} \mathbb{E}\big(|X_n - X|^p\big) = 0
$$

---
## `Relacje między zbieżnościami`

### Implikacje

$$
\large X_n \xrightarrow{p.n.} X \;\Rightarrow\; X_n \xrightarrow{P} X \;\Rightarrow\; X_n \xrightarrow{d} X
$$

$$
\large X_n \xrightarrow{L^p} X \;\Rightarrow\; X_n \xrightarrow{P} X
$$

---

### Ważne uwagi

* Odwrotne implikacje **nie zachodzą** (ogólnie)
* Jeśli $X_n \xrightarrow{d} c$, gdzie $c$ jest stałą, to:
  $$
  \large X_n \xrightarrow{P} c
  $$
* Jeśli $X_n \xrightarrow{P} X$, to istnieje podciąg $(X_{n_k})$ taki, że:
  $$
  \large X_{n_k} \xrightarrow{p.n.} X
  $$

---

### Intuicja

* $p.n.$ → „najsilniejsza” zbieżność  
* $P$ → „średnia siła”  
* $d$ → „najsłabsza” (tylko rozkłady)  
* $L^p$ → kontrola momentów (silna, ale innego typu)
## `Jednoznaczność rozkładu według dystrybuanty`
Dystrybuanta zmiennej losowej jednoznacznie wyznacza jej rozkład.

---
## `Dystrybuanta rozkładu ciagłego`
* Musi być **ciągła**
* Musi być r**óżniczkowalna** (Poza pewnym zbiorem przeliczalnym)

---
## `Wyprowadzanie dystrybuanty zależnej od innego rozkładu`
załóżmy że:
$$
X\sim U([-1, 1]), \quad Y=X^2
$$
Wtedy:
$$
F_y(t)=\mathbb{P}(X^2\le t)=\mathbb{P}(-\sqrt{t}\le X\le \sqrt{t})=\mathbb{P}(X\le \sqrt{t})-\mathbb{P}(X\ge \sqrt{t})
$$
W taki sposób możemy wyprowadzić dystrybuante dowolnego rozkładu $Y=g(X)$

# Wartość oczekiwana $\mathbb{E}$
## `Definicja`
Niech $X$ - zmienna losowa na $(\Omega ,\mathbb{F}, \mathbb{P})$
Mowimy, że X ma **wartość oczekiwaną**, jeśli istnieje:
$$
\int_{\Omega}X\,d\mathbb{P} 
$$

---
## `Najważniejsze własności`
1. Jeśli $X\ge 0$ , to $\mathbb{E}X\ge$ 0
2. $|{\mathbb{E}X}|\le \mathbb{E}|X|$
3. dla a, b$\in\mathbb{R}$ : $\mathbb{E}(aX+bY)=a\mathbb{E}X+b\mathbb{E}Y$
### Jeżeli $X_1,...., X_n$ niezależne
1. $\mathbb{E}(X_1,...,X_n)=\mathbb{E}X_1,.....,\,\mathbb{E}X_n$

---
## `Sposób liczenia`
Niech $X$ będzie zmienną losową, a $g:\mathbb{R}\rightarrow\mathbb{R}$ funkcją borelowską, wtedy:
$$
\mathbb{E}[g(X)] =\int_\mathbb{R} g(x)\,d\mu_x(x)
$$
dla $g(x)=x$, to
$$
\mathbb{E}[X] =\int_\mathbb{R} x\,d\mu_x(x)
$$
Dla rozkładów **dyskretnych**:
$$
\mathbb{E}[g(X)] =\sum_\mathbb{R} g(x)\mathbb{P}(X=x)
$$
Dla rozkładów **ciągłych**:
$$
\mathbb{E}[g(X)] =\int_\mathbb{R} g(x)f_x(x)\,dx
$$
Ponieważ gęstość to pochodna miary względem miary Lebesgue’a:
$$
f(x)=\frac{d\mu_X}{dx}
$$

---
# Wariancja $Var$
## `Definicja`
Wariancja pozwala nam określic jak bardzo wartości $X$ rożnią się od $\mathbb{E}X$.
Liczbę $\mathbb{E}(X-\mathbb{E}X)^2$ nazywamy wariancja zmiennej losowej $X$ i oznaczamy $VarX$ tzn.
$$
VarX=\mathbb{E}(X-\mathbb{E}X)^2=\mathbb{E}X^2-(\mathbb{E}X)^2
$$

---
## `Własności`
1. $VarX\ge 0$
2. $Var(cX)=c^2VarX$
3. $Var(X+c)=VarX$
4. $VarX=0\iff$ $P(X=c)=1$
### Jeżeli $X_1,...., X_n$ niezależne
1. $Var(X_1,....,X_n)=VarX_1+.....+VarX_n$

---

# Funkcje charakterystyczne $\varphi_X(t)$
## `Definicja`
Niech $X$ będzie zmienną losową. 
**Funkcją charakterystyczną** nazywamy:
$$
\varphi_X(t)=\mathbb{E}e^{iXt} \quad t\in\mathbb{R}
$$

---
# Odchylenie standardowe $\sigma$
## `Definicja`
**Odchyleniem standradowym** (inaczej depresją) nazywamy $\sqrt{VarX}$.

---
# Nierówności probabilistyczne

## `Nierówność Markowa`

Niech $X \ge 0$ oraz $\mathbb{E}(X) < \infty$. Wtedy dla każdego $a > 0$:

* $\large P(X \ge a) \le \frac{\mathbb{E}(X)}{a}$

---

## `Nierówność Czebyszewa`

Niech $\mathbb{E}(X)=\mu$ oraz $Var(X)<\infty$. Wtedy dla każdego $a > 0$:

* $\large P(|X - \mu| \ge a) \le \frac{Var(X)}{a^2}$

---

