# Animated Video

This video has been made for an History of Science course at École polytechnique (France) to showcase this amazing machine, one of the masterpiece of the school museum.

<iframe width="1280" height="720" src="https://www.youtube.com/embed/yVqqV-p2aEE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


# Mathematical details:

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

French mathematician Joseph Fourier demonstrated 200 years ago the following principle: given a periodic function of period $$T$$, one can decompose it using cosine and sine components of different order:

$$f(t) = \sum\limits_{n = -\infty}^{+\infty}c_n(f)e^{int\frac{2\pi}{T}}$$

with $a_0$ being a constant value, $a_n$ the cosine component of order $n$, and $b_n$ the sine component of order $n$. These components can themselve be calculated thanks to the function:

$$a_n(f) = \frac{2}{T}\int_0^T f(t)cos(nt\frac{2\pi}{T})dt$$

$$b_n(f) = \frac{2}{T}\int_0^T f(t)sin(nt\frac{2\pi}{T})dt$$
