---
tags:
  - contare
  - punti
  - poligoni
  - aggregare
---

# Conta  i punti nel poligono

Contare i features di un layer puntuale che ricadono dentro poligoni, e ‘appendere’ i valori nella tabella attributi del layer poligonale.

Esiste una geo-algoritmo in processing (Conta i punti nel poligono) che fa questo lavoro in modo brillante ma crea un altro strato.

Un modo rapido per evitare la creazione di un nuovo layer è quello di utilizzare il calcolatore di campi:

1. creare un nuovo campo '_nro_' nel layer poligonale;
2. popolarlo utilizzando la seguente espressione: 

```   
aggregate(
 layer:='punti', 
 aggregate:='count', 
 expression:=$id, 
 filter:=intersects( $geometry, geometry(@parent))
 )
```

[![](../img/esempi/conta_punti_in_poligono/conta_01.png)](../img/esempi/conta_punti_in_poligono/conta_01.png)

risultato:

[![](../img/esempi/conta_punti_in_poligono/conta_02.png)](../img/esempi/conta_punti_in_poligono/conta_02.png)

NB: i due layer devono avere stesso SR, altrimenti restituirà sempre zero.

 Geopackage è [qui](../prova_tu/dati_esempi.zip)
 
 [QUI VIDEO](https://youtu.be/vlmnmI6sjAg)

---

Funzioni e variabili utilizzate:

* [aggregate](../gr_funzioni/aggrega/aggrega_unico.md#aggregate)
