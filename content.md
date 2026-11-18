Implement the accumulator pattern using a `for`{.python} loop with `range()`{.python} to compute:

$$
\sum_{x=1}^{100}x^2
$$

Print your final result. The expected final value is `338350`.

# Hint

>[!HIDDEN]
> Remember the second argument passed to `range`{.python} is exclusive, so to include 100 in the range, you should use `range(1, 101)`{.python}.

Write your code here:

```py-cell
# Write your code here

```

# Sample Solution

Click below to see a sample solution.

>[!HIDDEN]
> The sample solution is shown below:
>
> ```py-cell
> result = 0
> for x in range(1, 101):
>     result = result + x**2
> print(result)
> ```
>
> This should output `338350`{.python}.
>
> ## Explanation
>
> We will accumulate the sum in the variable `result`{.python}. As a result, the first step is to create this variable and set it to `0`{.python}. Next, we need to loop over all integers from 1 to 100. To do this, we loop over the range `range(1, 101)`{.python}. This will generate each integer in that range in turn. For each integer `x`{.python}, we compute its square and add it to `result`{.python}.
>
> ## Common Mistakes
>
> * Using the wrong range bounds, such as `range(1, 100)`{.python}, which would exclude 100.
> * Forgetting to initialize the accumulator variable `result`{.python} to 0 before the loop. This would lead to a `NameError`{.python} if the variable is not defined when the first iteration of the loop runs.
> * Setting the accumulator variable to the square of the loop variable (e.g., `result = x**2`{.python}) instead of adding the square of the loop variableto the accumulator value (e.g. `result = result + x**2`{.python}). This would overwrite the accumulated value each iteration of the loop, instead of adding to it.