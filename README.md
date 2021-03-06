# Animated Video

This video has been made for an History of Science course at École polytechnique (France) to showcase this amazing machine, one of the masterpiece of the school museum.

<iframe width="1280" height="720" src="https://www.youtube.com/embed/yVqqV-p2aEE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br/><br/>
<br/><br/>

# More about the maths

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## The power of Fourier decompositions

French mathematician [Joseph Fourier](https://en.wikipedia.org/wiki/Joseph_Fourier) demonstrated 200 years ago the following principle: given a periodic function of period $$T$$, one can decompose it using cosine and sine components of different orders:

$$f(x) = a_0(f) + \sum\limits_{n=1}^{\infty}a_n(f)cos\left(x\frac{2n\pi}{T}\right) + \sum\limits_{n=1}^{\infty}b_n(f)sin\left(x\frac{2n\pi}{T}\right)$$

with $$a_0$$ being a constant value, $$a_n$$ the coefficient of the cosine component of order $$n$$, and $$b_n$$ of the sine component of order $$n$$. These coefficients can themselves be calculated thanks to the function:

$$a_n(f) = \frac{2}{T}\int_0^T f(x)cos\left(x\frac{2n\pi}{T}\right)dx$$

$$b_n(f) = \frac{2}{T}\int_0^T f(x)sin\left(x\frac{2n\pi}{T}\right)dx$$

These decompositions are called the [Fourier series](https://en.wikipedia.org/wiki/Fourier_series) and are the basis of a more general operation, called the [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform). This fundamental result gives the decomposition of any integrable function as a continuous sum (integral) of weighted periodic functions of different frequencies.

Conceptually, this result is very strong: any function, if decomposed enough, can be expressed as a sum of periodic basis functions. In a more practictal point of view, the Fourier transform, as part of the broader [Fourier analysis](https://en.wikipedia.org/wiki/Fourier_analysis), has been of paramount importance in the field of signal processing. These formulas are still widely used today in areas such as physics, image processing, statistics, forensics, cryptography, acoustics or optics.

Example usage: given an audio signal, find the [fundamental frequency](https://en.wikipedia.org/wiki/Fundamental_frequency) and the [harmonics](https://en.wikipedia.org/wiki/Harmonic).
<br/><br/>

## The difficulty to compute the coefficients

Fourier decompositions (in series or integrals) are only powerful if we can compute with great precision these coefficients, expressed as integrals themselves. 

However, they tend to be impossible to calculate exactly as our function can have an arbitrary shape (even for the periodic case). Consequently, the best we can do in most cases is to approximate them as close as possible to their real values but this requires computational power. Nowadays, computers alleviate this problem with great ease but this was not the case back in time. 

The Coradi analyzer is a engineering solution to this computation problem. It is a sort of mechanical calculator (like the [Pascaline](https://en.wikipedia.org/wiki/Pascal%27s_calculator)) that aims at evaluating the first coefficients of a Fourier series using directly as input the curve of our function. This ingenious invention uses physical and mathematical principles to simulate the real calculation of an integral.
<br/><br/>

## Mathematical details

Let's take a periodic function of period $$T$$ between $$0$$ and $$T$$ and scale it so it takes the whole span of the machine for the x-axis. That way, when sliding the carriage from one side to another, we go from $$x=0$$ to $$x=T$$.

When doing this full slide, the bigger pulley makes one complete rotation, the second bigger makes two etc... More precisely, the n-th pulley have a rotation angle $$\theta_n = x\dfrac{2n\pi}{T}$$. For example, for $$n=1$$ (the bigger pulley), this angle goes from $$0$$ to $$2\pi$$ (a full rotation) when $$x=T$$.

Now imagine we are at a certain value of $$x$$ and we make a small move $$dy$$ along the y-axis. This will first rotate the glass spheres by the same quantity $$dy$$. Now the dials will rotate differently, depending on their alignment (as seen in the video), which depends on angle $$\theta$$. Therefore, the first dial will only make a final rotation of $$cos(\theta)dy$$  (at $$\theta=0$$ the dial is built to be perfectly aligned with the sphere, having a move $$dy$$).

If we sum all these infinitesial moves $$dy$$ along the whole procedure, we end up with:

$$S = \int_{x=0}^{T}cos(\theta)dy$$

But we know the relation between $$x$$ and $$\theta$$ for a given pulley of order $$n$$. Furthermore, if the little moves $$dy$$ along the y-axis are done following our function $$f$$ while increasing the $$x$$ value, we have the natural relation $$dy = f'(x)dx$$ where $$f'$$ is the first-order derivative of $$f$$. It comes:

$$S = \int_0^Tcos\left(x\frac{2n\pi}{T}\right)f'(x)dx$$

An integration by parts gives:

$$S = \left[cos\left(x\frac{2n\pi}{T}\right)f(x)\right]_0^T - \int_0^Tcos'\left(x\frac{2n\pi}{T}\right)f(x)dx ~=~ \frac{2n\pi}{T}\int_0^Tsin\left(x\frac{2n\pi}{T}\right)f(x)dx$$

The first term is zero because of the periodicity. Finally, this integral value is a multiplicative constant away from our coefficient $$b_n$$:

$$S = n\pi \times b_n$$

The second dial, which makes a angle of $$\dfrac{\pi}{2}$$ with the first one, is used to integrate $$sin(\theta)$$, and gives (with an added minus sign) the same result but for coefficient $$a_n$$. 

In reality, both dials are graduated to take into account the multiplicative constant $$\pi$$. That is, if we name $$\Delta$$ and $$\Delta '$$ the differences on both dials between $$x=0$$ and $$x=T$$ for pulley $$n$$, the Fourier coefficients of order $$n$$ are given by:

$$a_n = -\frac{\Delta '}{n} ~~~~~~~~ b_n = \frac{\Delta}{n}$$

<br/><br/>

# Gallery

Click on a thumbnail for higher quality image

[![](img/small_0.png)](img/large_0.png)  [![](img/small_1.png)](img/large_1.png)  [![](img/small_2.png)](img/large_2.png)  [![](img/small_3.png)](img/large_3.png)  [![](img/small_4.png)](img/large_4.png)  [![](img/small_5.png)](img/large_5.png)  [![](img/small_6.png)](img/large_6.png)  [![](img/small_7.png)](img/large_7.png)  [![](img/small_8.png)](img/large_8.png)  [![](img/small_9.png)](img/large_9.png)  [![](img/small_10.png)](img/large_10.png)  [![](img/small_11.png)](img/large_11.png)
