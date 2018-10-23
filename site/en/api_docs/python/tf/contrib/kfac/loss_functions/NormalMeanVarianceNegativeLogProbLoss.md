

page_type: reference


<!-- DO NOT EDIT! Automatically generated file. -->


# tf.contrib.kfac.loss_functions.NormalMeanVarianceNegativeLogProbLoss

## Class `NormalMeanVarianceNegativeLogProbLoss`

Inherits From: [`DistributionNegativeLogProbLoss`](../../../../tf/contrib/kfac/loss_functions/DistributionNegativeLogProbLoss)



Defined in [`tensorflow/contrib/kfac/python/ops/loss_functions.py`](https://www.github.com/tensorflow/tensorflow/blob/r1.5/tensorflow/contrib/kfac/python/ops/loss_functions.py).

Negative log prob loss for a normal distribution with mean and variance.

This class parameterizes a multivariate normal distribution with n independent
dimensions. Unlike `NormalMeanNegativeLogProbLoss`, this class does not
assume the variance is held constant. The Fisher Information for n = 1
is given by,

F = [[1 / variance,                0],
     [           0, 0.5 / variance^2]]

where the parameters of the distribution are concatenated into a single
vector as [mean, variance]. For n > 1, the mean parameter vector is
concatenated with the variance parameter vector.

See https://www.ii.pwr.edu.pl/~tomczak/PDF/[JMT]Fisher_inf.pdf for derivation.

## Properties

<h3 id="dist"><code>dist</code></h3>



<h3 id="fisher_factor_inner_shape"><code>fisher_factor_inner_shape</code></h3>



<h3 id="fisher_factor_inner_static_shape"><code>fisher_factor_inner_static_shape</code></h3>



<h3 id="hessian_factor_inner_shape"><code>hessian_factor_inner_shape</code></h3>



<h3 id="hessian_factor_inner_static_shape"><code>hessian_factor_inner_static_shape</code></h3>



<h3 id="input_minibatches"><code>input_minibatches</code></h3>

A `list` of inputs to the loss function, separated by minibatch.

Typically there will be one minibatch per tower in a multi-tower setup.
Returns a list consisting of `self.inputs` by default; `LossFunction`s
supporting registering multiple minibatches should override this method.

#### Returns:

A `list` of `Tensor`s representing

<h3 id="inputs"><code>inputs</code></h3>



<h3 id="num_registered_minibatches"><code>num_registered_minibatches</code></h3>

Number of minibatches registered for this LossFunction.

Typically equal to the number of towers in a multi-tower setup.

#### Returns:

An `int` representing the number of registered minibatches.

<h3 id="params"><code>params</code></h3>



<h3 id="targets"><code>targets</code></h3>





## Methods

<h3 id="__init__"><code>__init__</code></h3>

``` python
__init__(
    mean,
    variance,
    targets=None,
    seed=None
)
```



<h3 id="evaluate"><code>evaluate</code></h3>

``` python
evaluate()
```

Evaluate the loss function on the targets.

<h3 id="evaluate_on_sample"><code>evaluate_on_sample</code></h3>

``` python
evaluate_on_sample(seed=None)
```

Evaluates the log probability on a random sample.

#### Args:

* <b>`seed`</b>: int or None. Random seed for this draw from the distribution.


#### Returns:

Log probability of sampled targets, summed across examples.

<h3 id="multiply_fisher"><code>multiply_fisher</code></h3>

``` python
multiply_fisher(vecs)
```



<h3 id="multiply_fisher_factor"><code>multiply_fisher_factor</code></h3>

``` python
multiply_fisher_factor(vecs)
```



<h3 id="multiply_fisher_factor_replicated_one_hot"><code>multiply_fisher_factor_replicated_one_hot</code></h3>

``` python
multiply_fisher_factor_replicated_one_hot(index)
```



<h3 id="multiply_fisher_factor_transpose"><code>multiply_fisher_factor_transpose</code></h3>

``` python
multiply_fisher_factor_transpose(vecs)
```



<h3 id="multiply_hessian"><code>multiply_hessian</code></h3>

``` python
multiply_hessian(vector)
```



<h3 id="multiply_hessian_factor"><code>multiply_hessian_factor</code></h3>

``` python
multiply_hessian_factor(vector)
```



<h3 id="multiply_hessian_factor_replicated_one_hot"><code>multiply_hessian_factor_replicated_one_hot</code></h3>

``` python
multiply_hessian_factor_replicated_one_hot(index)
```



<h3 id="multiply_hessian_factor_transpose"><code>multiply_hessian_factor_transpose</code></h3>

``` python
multiply_hessian_factor_transpose(vector)
```



<h3 id="sample"><code>sample</code></h3>

``` python
sample(seed)
```




