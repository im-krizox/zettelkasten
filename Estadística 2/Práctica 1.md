import numpy as np

from scipy import stats

  

def LinearRegression(X, y, alpha=0.05):

    # Agregar una columna de unos para el término independiente (intercepto)

    X = np.column_stack((np.ones(X.shape[0]), X))

  

    # Calcular los coeficientes usando la fórmula de mínimos cuadrados

    XtX_inv = np.linalg.inv(X.T @ X)

    beta_hat = XtX_inv @ (X.T @ y)

  

    # Predicciones

    y_hat = X @ beta_hat

  

    # Residuos

    residuals = y - y_hat

  

    # Grados de libertad

    n = len(y)

    p = X.shape[1]

  

    # Estimación de la varianza de los residuos

    sigma_squared_hat = (residuals.T @ residuals) / (n - p)

  

    # Varianza de los coeficientes estimados

    var_beta_hat = np.diagonal(sigma_squared_hat * XtX_inv)

  

    # Error estándar de los coeficientes

    se_beta_hat = np.sqrt(var_beta_hat)

  

    # Intervalos de confianza para los coeficientes

    t_critical = stats.t.ppf(1 - alpha/2, n - p)

    ci_beta_hat = [(beta - t_critical * se, beta + t_critical * se) for beta, se in zip(beta_hat, se_beta_hat)]

  

    # Tabla ANOVA

    SSR = np.sum((y_hat - np.mean(y)) ** 2)

    SSE = np.sum((residuals) ** 2)

    SST = SSR + SSE

  

    MSR = SSR / (p - 1)

    MSE = SSE / (n - p)

  

    F_statistic = MSR / MSE

    p_value = 1 - stats.f.cdf(F_statistic, p - 1, n - p)

  

    anova_table = {

        'Source': ['Regression', 'Residual', 'Total'],

        'DF': [p - 1, n - p, n - 1],

        'SS': [SSR, SSE, SST],

        'MS': [MSR, MSE, None],

        'F': [F_statistic, None, None],

        'P-value': [p_value, None, None]

    }

  

    # Construir intervalos de confianza para las predicciones

    X_new = np.column_stack((np.ones(X.shape[0]), X[:, 1:]))

    y_pred = X @ beta_hat

    SE_pred = np.sqrt(MSE * (1 + np.sum(X_new @ XtX_inv * X_new, axis=1)))

  

    ci_pred = [(y_pred[i] - t_critical * SE_pred[i], y_pred[i] + t_critical * SE_pred[i]) for i in range(len(y_pred))]

  

    results = {

        'beta_hat': beta_hat,

        'var_beta_hat': var_beta_hat,

        'ci_beta_hat': ci_beta_hat,

        'anova_table': anova_table,

        'ci_pred': ci_pred

    }

  

    return results

  

# Ejemplo de uso

X = np.array([[0], [1], [2]])

y = np.array([2, 10, 28])

  

results = LinearRegression(X, y, alpha=0.05)

  

# Mostrar los resultados

print("Estimación puntal de los coeficientes (betas):", results['beta_hat'])

print("Varianza de los coeficientes:", results['var_beta_hat'])

print("Intervalos de confianza para los coeficientes:", results['ci_beta_hat'])

print("Tabla ANOVA:", results['anova_table'])

print("Intervalos de confianza para las predicciones:", results['ci_pred'])
- Realizada por: Kristoffer Van Steemberghe Luján
- Número de cuenta: 319206463

La práctica fue realizada en un notebook de Colab, a la cual se puede acceder mediante los siguientes enlaces:

- [Enlace 1](https://colab.research.google.com/drive/1ejhST3xOy_p8D2XWpkg_3VGiKmV3FI5F?usp=sharing)
- [Enlace 2](https://colab.research.google.com/drive/1ejhST3xOy_p8D2XWpkg_3VGiKmV3FI5F?usp=sharing)
- [Enlace 3](https://colab.research.google.com/drive/1ejhST3xOy_p8D2XWpkg_3VGiKmV3FI5F?usp=sharing)

Además, se encuentra también en un repositorio de Github disponible [aquí](https://github.com/Kristoffer-Van-Steemberghe/Practica-1-Estadistica.git).

>[!tip] Importante.
>Al momento de ejecutar el código, no olvidar revisar si es que los archivos `.csv` y `.xlsx` se encuentran en la sección de *Archivos*.

