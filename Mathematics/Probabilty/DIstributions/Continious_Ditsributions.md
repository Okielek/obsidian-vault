## `Rozkład Jednostajny`

$\Large X \sim U(a,b)$
**Rozkład jednostajny ciągły** to rozkład, w którym zmienna losowa przyjmuje wartości z przedziału **$[a, b]$**, a gęstość prawdopodobieństwa jest stała na tym przedziale.
* Gęstość rozkładu: $\large f(x) = \frac{1}{b-a}$ 
* Dystrybuanta: $\large F(x) = \frac{x-a}{b-a}$
* Wartość oczekiwana: $\large\mathbb{E}(X) = \frac{b+a}{2}$
* Wariancja rozkładu: $\large Var(X) = \frac {(b-a)^2}{12}$
## `Rozkład Normalny`

$\Large \mathcal{N}(\mu, \sigma^2)$
**Rozkład normalny** to rozkład ciągły, w którym wartości zmiennej losowej skupiają się wokół średniej $\mu$, a prawdopodobieństwo maleje wraz z oddalaniem się od niej.
* Gęstość rozkładu: $\large f(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$  
* Dystrybuanta: $\large F(x) = P(X \le x)$  
* Wartość oczekiwana: $\large \mathbb{E}(X) = \mu$  
* Wariancja rozkładu: $\large Var(X) = \sigma^2$
* Standaryzacja: $\large Z = \frac{X - \mu}{\sigma} \sim \mathcal{N}(0,1)$
## `Rozkład Wykładniczy`

$\Large X \sim Exp(\lambda)$

**Rozkład wykładniczy** to rozkład ciągły opisujący czas oczekiwania na zajście zdarzenia, przy założeniu stałej intensywności $\lambda$.

* Gęstość rozkładu: $\large f(x) = \lambda e^{-\lambda x}$ dla $x \ge 0$  
* Dystrybuanta: $\large F(x) = 1 - e^{-\lambda x}$ dla $x \ge 0$  
* Wartość oczekiwana: $\large \mathbb{E}(X) = \frac{1}{\lambda}$  
* Wariancja rozkładu: $\large Var(X) = \frac{1}{\lambda^2}$
## `Rozkład Gamma`

$\Large X \sim \Gamma(\alpha, \lambda)$

**Rozkład gamma** to ciągły rozkład opisujący czas oczekiwania na zajście $\alpha$ zdarzeń w procesie Poissona o intensywności $\lambda$.

* Gęstość rozkładu: $\large f(x) = \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x}$ dla $x \ge 0$  
* Dystrybuanta: $\large F(x) = \int_0^x f(t)\,dt$  
* Wartość oczekiwana: $\large \mathbb{E}(X) = \frac{\alpha}{\lambda}$  
* Wariancja rozkładu: $\large Var(X) = \frac{\alpha}{\lambda^2}$
* * $\Gamma(\alpha)$ — funkcja gamma (uogólnienie silni): $\Gamma(n) = (n-1)!$
## `Rozkład Beta`

$\Large X \sim Beta(\alpha, \beta)$

**Rozkład beta** to ciągły rozkład na przedziale $[0,1]$, często używany do modelowania prawdopodobieństw.

* Gęstość rozkładu: $\large f(x) = \frac{1}{B(\alpha,\beta)} x^{\alpha-1}(1-x)^{\beta-1}$ dla $x \in [0,1]$  
* Dystrybuanta: $\large F(x) = \int_0^x f(t)\,dt$  
* Wartość oczekiwana: $\large \mathbb{E}(X) = \frac{\alpha}{\alpha+\beta}$  
* Wariancja rozkładu: $\large Var(X) = \frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$
* * $B(\alpha,\beta)$ — funkcja beta (stała normalizacyjna)