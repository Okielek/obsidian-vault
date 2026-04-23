# Rozkłady
## `Rozkład Poissona`

$\Large X \sim \mathrm{Poisson}(\lambda)$

**Rozkład Poissona** to rozkład dyskretny, który opisuje liczbę zdarzeń zachodzących w ustalonym przedziale czasu, przestrzeni lub na danym obszarze, przy założeniu że zdarzenia występują niezależnie i ze stałą średnią intensywnością **$\lambda > 0$**.

* Funkcja prawdopodobieństwa: $\large P(X=k)=\frac{\lambda^k e^{-\lambda}}{k!}, \quad k=0,1,2,\dots$
* Wartość oczekiwana: $\large \mathbb{E}(X)=\lambda$
* Wariancja rozkładu: $\large Var(X)=\lambda$
---
## `Rozkład dwumianowy`

$\Large X \sim Bin(n,p)$

 Liczba sukcesów w **n niezależnych próbach Bernoulliego** np. liczba trafień przy rzutach monetą.
- Funkcja prawdopodobieństwa: $P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}$
- Wartość oczekiwana: $\mathbb{E}(X)=np$
- Wariancja rozkładu: $Var(X)=np(1-p)$
---
## `Rozkład Bernoulliego`

$\Large X \sim Bern(p)$

 Zmienna losowa opisująca wynik **jednej próby Bernoulliego** (sukces/porażka).
- Przyjmuje wartości: $X \in \{0,1\}$
- Funkcja prawdopodobieństwa:
  - $P(X=1)=p$
  - $P(X=0)=1-p$
- Wartość oczekiwana: $\mathbb{E}(X)=p$
- Wariancja rozkładu: $Var(X)=p(1-p)$
---
## `Rozkład Geometryczny`

$\Large X \sim Geom(p)$

**Rozkład geometryczny** to rozkład dyskretny opisujący liczbę prób potrzebnych do uzyskania **pierwszego sukcesu** w ciągu niezależnych prób Bernoulliego o prawdopodobieństwie sukcesu **$p$**.

* Funkcja prawdopodobieństwa: $\large P(X=k)=(1-p)^{k-1}p, \quad k=1,2,3,\dots$
* Dystrybuanta: $\large F(x)=1-(1-p)^{\lfloor x \rfloor}$
* Wartość oczekiwana: $\large \mathbb{E}(X)=\frac{1}{p}$
* Wariancja rozkładu: $\large Var(X)=\frac{1-p}{p^2}$

**Własność braku pamięci:**
$\large P(X>m+n \mid X>m)=P(X>n)$
---

# Własności
