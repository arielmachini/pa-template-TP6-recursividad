# Trabajo Práctico Nº 6: Recursividad

**UNPA-UARG**  
**Carreras:** Analista de Sistemas y Licenciatura en Sistemas  
**Asignatura:** Programación de Algoritmos  

**Profesores de Práctica:**  
- Lic. Ariel Machini  
- Mg. Fabiana Miranda  

---

## 1. Dado el siguiente método recursivo...

```
int puzzle(int base, int limite) {
    if(base > limite)
        return -1;
    else {
        if(base == limite)
            return 1;
        else
            return (base * puzzle(base + 1, limite));
    }
}
```

**a)** Identificar:
- El o los casos bases del método puzzle.
- El o los casos generales del método puzzle.

**b)** Mostrar cuál sería el resultado de las siguientes llamadas al método recursivo:
- `System.out.println(puzzle(14, 10));`
- `System.out.println(puzzle(4, 7));`
- `System.out.println(puzzle(0, 0));`

## 2. Dado el siguiente método recursivo...

```
int concurso(int base, int limite) {
    if(base == limite)
        return 1;
    else {
        if(base > limite)
            return 0;
        
        return (base + concurso(base + 1, limite));
    }
}
```

Mostrar lo que retornan las siguientes llamadas:

**a)** `int x = concurso(0, 3);` *x* es ...  
**b)** `int y = concurso(10, 7);` *y* es ...  
**c)** `int z = concurso(5, 50);` *z* es ...

## 3. En cada uno de los siguientes métodos, identificar...

- El o los casos bases,
- y una llamada recursiva a una versión más pequeña del método.
- Adicionalmente, explicar que hace cada método.

**a)**
```
int potencia(int m, int n) {
    if(n == 0)
        return 1;
    else
        return (m * potencia(m, n - 1));
}
```

**b)**
```
int factorial(int n) {
    if(n > 0)
        return (n * factorial(n - 1));
    else {
        if(n == 0)
            return 1;
        else
            return –1;
    }
}
```

## 4. Escribir un método recursivo que calcule la siguiente suma

1 + 2 + 3 + ... + (*n* - 1) + *n*

## 5. Escribir un método recursivo para encontrar la suma de los enteros pares hasta *n*

2 + 4 + 6 + ... + (*n* - 2) + *n*.

## 6. Suponer que la función G está definida recursivamente de la siguiente forma...

**G(x, y):**
- **1**, si *x* <= *y*
- **G(x, y + 1) + 1**, si *y* < *x*

### Si *x* e *y* son enteros positivos...
**a)** Escribir el método recursivo.  
**b)** Encontrar el valor de **G(8, 6)**.  
**c)** Encontrar el valor de **G(100, 10)**.

## 7. Escribir un método recursivo `int vocales(String cd)` para calcular el número de vocales de una cadena

## 8. Escribe un método recursivo que calcule la suma de los primeros *n* números naturales

Por ejemplo, si *n* = 5, el resultado debe ser 1 + 2 + 3 + 4 + 5 = 15.  
**Pista:** El caso base es cuando `n == 0`, y la suma es **0**. En caso contrario, la suma de *n* es igual a *n* + **suma(*n* - 1)**.

## 9. Escribe un método recursivo que determine si un número está presente en un arreglo

Devuelve `true` si el número se encuentra en el arreglo y `false` en caso contrario.  
**Pista:** El caso base es cuando el tamaño del arreglo es 0, en cuyo caso el número no está presente. De lo contrario, verifica el primer elemento del arreglo y llama recursivamente con el resto del arreglo.

## 10. Escribe un método recursivo que encuentre el valor mínimo en un arreglo de enteros

**Pista:** Divide el problema en dos partes: el elemento actual y el mínimo de los elementos restantes del arreglo.

## 11. Escribe un método recursivo que cuente las ocurrencias de un número dado en un arreglo de enteros

**Pista:** Compara el elemento actual con el número buscado y llama recursivamente con el resto del arreglo.