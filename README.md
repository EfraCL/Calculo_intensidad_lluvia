## Finalidad y fundamento 
El objetivo principal de esta función es calcular la lluvia caída durante un intervalo de tiempo cualquiera, es decir, para calcular la intensidad de la lluvia.

El fundamento matemático de la función es el siguiente: un conjunto de datos (o vector) de longitud N puede ser subdivido en [N-(A-1)] 
subconjuntos consecutivos de amplitud A.

## Argumentos de la función
La función **intensidad()** admite dos argumentos:
- **x**: es el vector a utilizar para realizar los subconjuntos sobre los que se aplicará una función determinada.
- **amplitud**: este argumento hace referencia a, como su propio nombre indica, a la amplitud de los subconjuntos sobre los que
queremos aplicar una función concreta. Por ejemplo, si queremos aplicar la función sum() en subconjuntos de 3, 4 o 5 elementos.

## Observaciones
Por defecto la función aplica la función sum() a cada subconjunto de datos, ya que es la función necesaria para
calcular la intensidad de lluvia.

## Ejemplo:

Copia y pega las siguientes líneas de código y observa cómo trabaja la función:
~~~
intensidad<-function(x,amplitud){
  c<-c()
  i<-1
  a<-amplitud-1
  lon<-length(x)-a
  while(i<=lon){
    c[i]<-sum(x[i:(i+a)])
    i<-i+1}
  return(c)}

a<-1:5
intensidad(a,amplitud=2)
~~~
