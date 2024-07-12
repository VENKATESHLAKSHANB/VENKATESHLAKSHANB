
1. Gradient Descent: The Mountain Climber*
 
 *Code: Gradient Descent*

```import numpy as np

def gradient_descent(start, gradient, learn_rate, n_iter=100, tolerance=1e-06):
    vector = start
    for _ in range(n_iter):
        diff = -learn_rate * gradient(vector)
        if np.all(np.abs(diff) <= tolerance):
            break
        vector += diff
    return vector

# Example usage for finding the minimum of f(x) = x^2 + 5 \\
def gradient(x):
    return 2 * x

minimum = gradient_descent(start=10.0, gradient=gradient, learn_rate=0.1)
print(f"The minimum occurs at: {minimum}")```
 *
