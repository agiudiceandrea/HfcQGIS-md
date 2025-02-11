---
tags:
  - operatori
  - propedeutico
---

# Operatori interfaccia

!!! Abstract "Intro"
    **In questa sezione documenteremo gli operatori presenti nell'interfaccia del Field Calc.**

L'interfaccia del calcolatore rende immediatamente disponibili alcuni operatori:

![operatori](../img/operatori_calc1.png)

## uguale

    - uguaglianza tra numeri 10 = 10;
    - uguaglianza tra lettere 'A' = 'A' ;
    - uguaglianza tra parole 'Ciao' = 'Ciao';
    - ugualgianza tra stringhe 'Viva QGIS' = 'Viva QGIS';
    - uguaglianza tra campi "field1" = "field2";
    - uguaglianza tra espressioni $area = area($geometry);

## somma

    - somma di numeri 10 + 15.4 ;
    - somma di stringhe (unione) 'QGIS' + '3.0' ;
    - somma di campi "fied1" + "field2"
    - somma di espressioni $perimeter + 500;

## differenza

    - differenza tra numeri 250 -200;
    - differenza tra campi "field1"-"field2"
    - differenza tra espressioni length("field1") - length("field2");

## divisione

    - divisione tra numeri 125/5;
    - divisione tra campi "field1"/"field2";
    - divisione tra espressioni $area/$perimeter;

## moltiplicazione

    - moltiplicazione tra numeri 12*22;
    - moltiplicazione tra campi "field1"*"field2";
    - moltiplicazione tra espressioni $perimeter*length($area);

## potenza

    - potenza tra numeri 10^2;
    - potenza tra campi "field1"^"field2";
    - potenza tra espressioni $area^length($area);

## unione di stringhe

    - unione di numeri (che trasforma in stringhe) 12 || 24 → '1224';
    - unione tra lettere 'A'||'b' → 'Ab';
    - unione tra parole 'Ciao' || 'Mondo' → 'CiamoMondo' ;
    - unione tra stringhe 'Viva QGIS' || 'Viva Pigreco' → 'Viva QGISViva Pigreco';
    - unione tra campi "field1" = "field2";
    - unione tra espressioni \$area || area($geometry);
    - unione tra simboli 'A'||'=>'||'B' → 'A=>B';

## parentesi aperta

    - il calcolatore indica se una parentesi è rimasta aperta;

## parentesi chiusa

    - il calcolatore indica se una parentesi è rimasta chiusa;

## nuova riga

    - aggiunge una nuova riga:  
    (12 || 24 ) ||'\n' ||( '12' || '24' ) → stamperà '1224' su 1224' in due righe;
    - molto utile per le etichette su due o più righe;

Un altro operatore nascosto è `'\t'` tabulazione:

utile per esempio nelle legende, leggi [qui](https://geoobserver.wordpress.com/2021/07/19/qgis-tipp-tabellenartige-legenden-mit/)

