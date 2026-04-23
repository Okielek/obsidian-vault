## Centralne Twierdzenie Graniczne (CTG)

Niech $X_1, X_2, \dots, X_n$ będą niezależnymi zmiennymi losowymi o tym samym rozkładzie, takich że
$\mathbb{E}[X_i] = \mu$ oraz $Var(X_i) = \sigma^2 < \infty$.

Wtedy:
$$
\frac{X_1 + X_2 + \dots + X_n - n\mu}{\sigma \sqrt{n}} \xrightarrow{d} \mathcal{N}(0,1)
$$
### Przykład zastosowania CTG

Załóżmy, że rzucamy uczciwą kostką $n = 100$ razy.  
Niech $X_i$ oznacza wynik $i$-tego rzutu.

Mamy:
$$
\mu = \mathbb{E}[X_i] = 3.5, \quad \sigma^2 = Var(X_i) = \frac{35}{12}
$$

Rozważamy średnią:
$$
\overline{X} = \frac{1}{100}\sum_{i=1}^{100} X_i
$$

Z CTG:
$$
\overline{X} \approx \mathcal{N}\left(3.5, \frac{35}{12 \cdot 100}\right)
$$


## Wzór Bayesa
Jeśli 
$$
\mathbb{P}(A) > 0 \;\land\; \mathbb{P}(B)>0
$$
to:
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(B|A)\mathbb{P}(A)}{\mathbb{P}(B)}
$$

### Przykład
Wśród 100 monet jedna ma 2 orły (reszta normalna) losujemy monete i rzucamy nią 10 razy wypadło 10 orłów. Jakie jest $\mathbb{P}$(wylosowaliśmy monetę z dwoma orłami). 

$A$ - Wypadło 10 orłów,  $D_1$ - rzucono monetą fałszywą, $D_2$ - rzucono monetą prawdziwą
$$
\mathbb{P}(D_1 \mid A) = \frac{\mathbb{P}(A \mid D_1)\,\mathbb{P}(D_1)}{\mathbb{P}(A \mid D_1)\,\mathbb{P}(D_1) + \mathbb{P}(A \mid D_2)\,\mathbb{P}(D_2)}
$$

$$  
\mathbb{P}(D_1 \mid A)  
=  
\frac{1\cdot \frac{1}{100}}{1\cdot \frac{1}{100} + (\frac{1}{2})^{10} \cdot \frac{99}{100}}  
=  
\frac{1024}{1123}  
$$  
  
Ostatecznie:  
$$  
\mathbb{P}(D_1 \mid A) = \frac{1024}{1123} \approx 0.912  
$$
## Niezależność zdarzeń
Zdarzenia $A$ i $B$ nazywamy niezależne, jeżeli:
$$
\mathbb{P}(A\land B)=\mathbb{P}(A)\cdot\mathbb{P}(B)
$$
## Lemat Borela–Cantellego

Niech $(A_n)_{n\ge 1}$ będzie ciągiem zdarzeń.

### I lemat Borela–Cantellego
Jeśli
$$
\sum_{n=1}^{\infty} \mathbb{P}(A_n) < \infty,
$$
to
$$
\mathbb{P}\big(\limsup_{n\to\infty} A_n\big) = 0.
$$

---

### II lemat Borela–Cantellego (dla zdarzeń niezależnych)
Jeśli zdarzenia $A_n$ są niezależne oraz
$$
\sum_{n=1}^{\infty} \mathbb{P}(A_n) = \infty,
$$
to
$$
\mathbb{P}\big(\limsup_{n\to\infty} A_n\big) = 1.
$$

---

### 📌 Definicja $\limsup$
$$
\limsup_{n\to\infty} A_n
=
\bigcap_{n=1}^{\infty} \bigcup_{k=n}^{\infty} A_k
$$

---

### 🧠 Interpretacja
$\limsup A_n$ oznacza, że zdarzenie $A_n$ zachodzi nieskończenie wiele razy.

## `Prawo Wielkich Liczb (LLN)`

Niech $X_1, X_2, \dots, X_n$ będą niezależnymi zmiennymi losowymi o tym samym rozkładzie, takich że
$$
\mathbb{E}[X_i] = \mu < \infty
$$

### Słabe prawo wielkich liczb (WLLN)

Wtedy:
$$
\frac{X_1 + X_2 + \dots + X_n}{n} \xrightarrow{\mathbb{P}} \mu
$$

czyli:
$$
\overline{X}_n \xrightarrow{\mathbb{P}} \mu
$$

---

### Silne prawo wielkich liczb (SLLN)

Jeśli dodatkowo $\mathbb{E}|X_i| < \infty$, to:
$$
\frac{X_1 + X_2 + \dots + X_n}{n} \xrightarrow{p.n.} \mu
$$

czyli:
$$
\overline{X}_n \xrightarrow{p.n.} \mu
$$

---

## 🔥 Intuicja

Średnia z próby:
$$
\overline{X}_n = \frac{1}{n}\sum_{i=1}^n X_i
$$

zbiega do wartości oczekiwanej:
$$
\mu = \mathbb{E}[X]
$$

czyli:

> częstość / średnia z danych $\to$ prawdziwa wartość

---

## 📌 Przykład zastosowania

Rzucamy uczciwą monetą.  
Niech $X_i$ oznacza wynik:
- $1$ — orzeł
- $0$ — reszka

Wtedy:
$$
\mathbb{E}[X_i] = 0.5
$$

Średnia:
$$
\overline{X}_n = \frac{1}{n}\sum_{i=1}^n X_i
$$

Z prawa wielkich liczb:
$$
\overline{X}_n \xrightarrow{p.n.} 0.5
$$

czyli:

> częstość orłów zbiega do $0.5$