## 6. Field at a Point from a System of Charges

### Useful definitions and formulas

Electric field from a point charge:

$$\vec E=kq\frac{\vec r-\vec r_0}{|\vec r-\vec r_0|^3}$$

where:

- $\vec r$ is the observation point
- $\vec r_0$ is the position of the charge
- $q$ is the charge
- $k=8.99\times10^9\text{ N m}^2/\text{C}^2$

The total field is the vector sum:

$$\vec E_{\text{total}}=\vec E_1+\vec E_2$$

---

### Given system

There are two charges:

$$+q\text{ at }(-a,0)$$

$$+2q\text{ at }(a,0)$$

Observation point:

$$(x,y)$$

---

### 1) General field $\vec E(x,y)$

For charge $+q$ at $(-a,0)$:

$$\vec r_1=(x+a,y)$$

$$r_1=\sqrt{(x+a)^2+y^2}$$

So:

$$\vec E_1=kq\frac{(x+a)\hat i+y\hat j}{\left((x+a)^2+y^2\right)^{3/2}}$$

For charge $+2q$ at $(a,0)$:

$$\vec r_2=(x-a,y)$$

$$r_2=\sqrt{(x-a)^2+y^2}$$

So:

$$\vec E_2=k(2q)\frac{(x-a)\hat i+y\hat j}{\left((x-a)^2+y^2\right)^{3/2}}$$

Therefore:

$$\vec E(x,y)=kq\frac{(x+a)\hat i+y\hat j}{\left((x+a)^2+y^2\right)^{3/2}}+2kq\frac{(x-a)\hat i+y\hat j}{\left((x-a)^2+y^2\right)^{3/2}}$$

Components:

$$E_x=kq\frac{x+a}{\left((x+a)^2+y^2\right)^{3/2}}+2kq\frac{x-a}{\left((x-a)^2+y^2\right)^{3/2}}$$

$$E_y=kq\frac{y}{\left((x+a)^2+y^2\right)^{3/2}}+2kq\frac{y}{\left((x-a)^2+y^2\right)^{3/2}}$$

---

### Field at $(0,y)$

Put $x=0$.

The distances are equal:

$$r=\sqrt{a^2+y^2}$$

Then:

$$E_x=kq\frac{a}{(a^2+y^2)^{3/2}}+2kq\frac{-a}{(a^2+y^2)^{3/2}}$$

$$E_x=-\frac{kqa}{(a^2+y^2)^{3/2}}$$

For $E_y$:

$$E_y=kq\frac{y}{(a^2+y^2)^{3/2}}+2kq\frac{y}{(a^2+y^2)^{3/2}}$$

$$E_y=\frac{3kqy}{(a^2+y^2)^{3/2}}$$

So:

$$\vec E(0,y)=\frac{kq}{(a^2+y^2)^{3/2}}\left(-a\hat i+3y\hat j\right)$$

---

### Field at $(x,0)$

Put $y=0$.

Then:

$$E_y=0$$

and:

$$E_x=kq\frac{x+a}{|x+a|^3}+2kq\frac{x-a}{|x-a|^3}$$

So:

$$\vec E(x,0)=\left(kq\frac{x+a}{|x+a|^3}+2kq\frac{x-a}{|x-a|^3}\right)\hat i$$

---

### 2) Conditions for $E_x=0$, $E_y=0$, and $\vec E=0$

From the general expression:

$$E_y=kqy\left[\frac{1}{r_1^3}+\frac{2}{r_2^3}\right]$$

Since the bracket is always positive, we get:

$$E_y=0\Rightarrow y=0$$

So a zero total field can only happen on the x-axis.

On the x-axis between the charges, $-a<x<a$, the fields point in opposite directions.

Set $E_x=0$:

$$kq\frac{1}{(x+a)^2}=2kq\frac{1}{(a-x)^2}$$

Cancel $kq$:

$$\frac{1}{(x+a)^2}=\frac{2}{(a-x)^2}$$

Take square root:

$$\frac{1}{x+a}=\frac{\sqrt2}{a-x}$$

Cross multiply:

$$a-x=\sqrt2(x+a)$$

$$a-x=\sqrt2x+\sqrt2a$$

$$a-\sqrt2a=x+\sqrt2x$$

$$a(1-\sqrt2)=x(1+\sqrt2)$$

$$x=a\frac{1-\sqrt2}{1+\sqrt2}$$

This is negative, so the zero point is closer to the smaller charge $+q$.

---

### 3) Numerical field for $a=0.2\text{ m}$, $y=0.3\text{ m}$, $q=2\mu\text{C}$

We calculate $\vec E(0,y)$:

$$\vec E(0,y)=\frac{kq}{(a^2+y^2)^{3/2}}\left(-a\hat i+3y\hat j\right)$$

Values:

$$a=0.2\text{ m}$$

$$y=0.3\text{ m}$$

$$q=2\times10^{-6}\text{ C}$$

First:

$$a^2+y^2=0.2^2+0.3^2=0.04+0.09=0.13$$

$$(a^2+y^2)^{3/2}=0.13^{3/2}\approx0.0469$$

Also:

$$kq=(8.99\times10^9)(2\times10^{-6})=17980$$

So:

$$\frac{kq}{(a^2+y^2)^{3/2}}=\frac{17980}{0.0469}\approx3.83\times10^5$$

Now components:

$$E_x=(3.83\times10^5)(-0.2)$$

$$E_x\approx-7.67\times10^4\text{ N/C}$$

$$E_y=(3.83\times10^5)(3\cdot0.3)$$

$$E_y=(3.83\times10^5)(0.9)$$

$$E_y\approx3.45\times10^5\text{ N/C}$$

So:

$$\vec E(0,0.3)\approx(-7.67\times10^4\hat i+3.45\times10^5\hat j)\text{ N/C}$$

---

### 4) Limit $y\gg a$

For point $(0,y)$:

$$\vec E(0,y)=\frac{kq}{(a^2+y^2)^{3/2}}\left(-a\hat i+3y\hat j\right)$$

If $y\gg a$, then:

$$(a^2+y^2)^{3/2}\approx y^3$$

So:

$$E_x\approx-\frac{kqa}{y^3}$$

$$E_y\approx\frac{3kqy}{y^3}=\frac{3kq}{y^2}$$

Therefore, far away, the system behaves mainly like one total charge:

$$q_{\text{total}}=q+2q=3q$$

---

### Final answer

$$\vec E(x,y)=kq\frac{(x+a)\hat i+y\hat j}{\left((x+a)^2+y^2\right)^{3/2}}+2kq\frac{(x-a)\hat i+y\hat j}{\left((x-a)^2+y^2\right)^{3/2}}$$

$$\vec E(0,0.3)\approx(-7.67\times10^4\hat i+3.45\times10^5\hat j)\text{ N/C}$$

For $y\gg a$:

$$E_y\approx\frac{3kq}{y^2}$$

The field looks like the field of one charge $3q$ far away.
