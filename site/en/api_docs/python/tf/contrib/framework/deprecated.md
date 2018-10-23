

page_type: reference


<!-- DO NOT EDIT! Automatically generated file. -->
# tf.contrib.framework.deprecated

### `tf.contrib.framework.deprecated`

``` python
deprecated(
    date,
    instructions
)
```



Defined in [`tensorflow/python/util/deprecation.py`](https://www.github.com/tensorflow/tensorflow/blob/r1.1/tensorflow/python/util/deprecation.py).

See the guide: [Framework (contrib) > Deprecation](../../../../../api_guides/python/contrib.framework#Deprecation)

Decorator for marking functions or methods deprecated.

This decorator logs a deprecation warning whenever the decorated function is
called. It has the following format:

  <function> (from <module>) is deprecated and will be removed after <date>.
  Instructions for updating:
  <instructions>

<function> will include the class name if it is a method.

It also edits the docstring of the function: ' (deprecated)' is appended
to the first line of the docstring and a deprecation notice is prepended
to the rest of the docstring.

#### Args:

* <b>`date`</b>: String. The date the function is scheduled to be removed. Must be
    ISO 8601 (YYYY-MM-DD).
* <b>`instructions`</b>: String. Instructions on how to update code using the
    deprecated function.


#### Returns:

  Decorated function or method.


#### Raises:

* <b>`ValueError`</b>: If date is not in ISO 8601 format, or instructions are empty.