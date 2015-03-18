Aula-2
========================================================
author: Wilson Freitas

Tudo é Objeto
=============
type: sub-section

Objetos
=======

Tudo, absolutamente tudo, no R é objeto.

Os objetos possuem tipos físicos e tipos abstratos:

- tipos físicos: tipo que indica como o objeto é armazenado na memória
  - retornado pela função `mode`
- tipos abstratos: tipo que define o comportamento do objeto
  - retornado pela função `class`

Tipos Físicos
=============
incremental:true

Podem ser: numeric, character, list, function, logical


```r
c(mode(2), mode("a"), mode(c), mode(list(1,2)))
```

```
[1] "numeric"   "character" "function"  "list"     
```



```r
c(mode(TRUE), mode(data.frame(a=2, b=3)))
```

```
[1] "logical" "list"   
```



```r
mode(as.Date('2000-01-01'))
```

```
[1] "numeric"
```

Tipos Abstratos
===============

Definem o comportamento.


```r
c(class(2), class("a"), class(c), class(list(1,2)))
```

```
[1] "numeric"   "character" "function"  "list"     
```



```r
c(class(TRUE), class(data.frame(a=2, b=3)))
```

```
[1] "logical"    "data.frame"
```



```r
class(as.Date('2000-01-01'))
```

```
[1] "Date"
```
