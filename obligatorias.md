---
title: Las etiquetas obligatorias
---

Antes de poder escribir los movimientos que pertenecen a una partida, es necesario escribir unas etiquetas obligatorias que la identifiquen, ya que en el mismo fichero puede haber tantas partidas como nos interese tener.

La forma en la que se deben definir estas etiquetas es la siguiente:


```[Event "Torneo"]
[Site "Ciudad"]
[Date "AAAA.MM.DD"]
[Round "ronda"]
[White "Jugador de blancas"]
[Black "Jugador de negras"]
[Result "Resultado"]
```

## Significado y contenido de las etiquetas

Event nos identifica el torneo en el que se jugó la partida. Si desconocemos este dato deberemos escribir un signo de interrogación entre las comillas.

Site identifica el nombre de la ciudad en la que se disputó la partida. Si desconocemos el dato también escribimos interrogación.

Date sirve para indicar la fecha. El formato correcto, como se puede apreciar, consiste en escribir el año con cuatro cifras y el mes y el día con dos cifras. Cada componente de la fecha se separa del anterior por un punto. Si alguno de los datos fuese desconocido, habría que escribir tantos signos de interrogación como cifras hubiese que poner.

Por ejemplo, supongamos que una partida se disputó el 17 de abril de 2016. En ese caso esta etiqueta quedaría así:

```
[Date "2016.04.17"]
```

Sin embargo, supongamos que queremos editar una partida de 1935, pero no conocemos más datos sobre la fecha. Entonces, esta etiqueta quedaría así:

```
[Date "1935.??.??"]
```

Como último ejemplo, si no supiésemos la fecha en la que se jugó la partida, la etiqueta quedaría así:

```
[Date "????.??.??"]
```

La etiqueta Round indica la ronda del torneo a la que pertenece la partida. Si se quisiera indicar la subronda se usaría un punto. Por ejemplo, si la partida pertenece a la quinta ronda del torneo se escribiría:

```
[Round "5"]
```

En cambio, si hubiese que indicar ronda 11 subronda 3 se escribiría de esta forma:

```
[Round "11.3"]
```

De nuevo, al igual que en las etiquetas Event y Site, si se desconoce este dato, habrá que escribir un signo de interrogación.

En las etiquetas White y Black se indican, respectivamente, los nombres de quienes jugaron la partida con blancas y negras usando el formato "apellidos, nombre" o bien un signo de interrogación para indicar que se desconoce el dato.

Por último, La etiqueta Result indica cómo terminó la partida. La siguiente tabla recoge sus posibles valores.

Resultado | Significado
--------- | -----------
1-0 | Ganan las blancas.
1/2-1/2 | Tablas.
0-1 | Ganan las negras.
* | Cualquier otro resultado.