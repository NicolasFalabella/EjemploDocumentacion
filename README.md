#  Dojos: EQUIPO ROJO 26/9/22


## Integrantes 
- bruno castagnola
- luca bovone
- nicolas falabella
- melina ochoa
- leonardo figueroa
- lucas dieguez

## Proyecto: Camara frigorifica con leds.

## Descripción
Descripcion: Simula el funcionamiento de un medidor de la temperatura de una cámara frigorífica, convirtiendo los valores del sensor de temperatura a los rangos válidos propios de un frigorífico, e indicando en un display LED de 7 segmentos si la temperatura está en Frio, Calor o Normal, y prendiendo un led Azul, Verde o Rojo según estos parametros.

## Función principal
Esta funcion se encarga de encender y apagar los leds.

es una funcion que permite mediante el sensor de temperatura ver los diferentes leds prendidos, cuando la temperatura esta alta sale rojo y en el display se ve una C, cuando la temperatura es baja sale azul y en el display se ve una F y cuando no es ni frio ni calor se prende la verde y en el display se ve un - .

(Breve explicación de la función)

~~~ c (lenguaje en el que esta escrito)
void loop()
{
  
tecla = digitalRead(A1);
  
if(tecla == 0)
{
  
 temperatura = analogRead(A0);
 temp2 = map(temperatura, 20, 358, -40, 125);
 
  
  
  if(temp2 > 30)
  {
    digitalWrite(AZUL, LOW);
    digitalWrite(VERDE, LOW);
    printDigit('c');
    digitalWrite(ROJO, HIGH);
  } 
     
  else if(temp2 < 10)
  {
    digitalWrite(ROJO, LOW);
    digitalWrite(VERDE, LOW);
    printDigit('f');
    digitalWrite(AZUL, HIGH);
  }
     
  else
  {
    digitalWrite(ROJO, LOW);
    digitalWrite(AZUL, LOW);
    printDigit('d');
    digitalWrite(VERDE, HIGH);
  }  
}else{
  digitalWrite(ROJO, LOW);
  digitalWrite(AZUL, LOW);
  digitalWrite(VERDE, LOW);
  digitalWrite(G, LOW);
}
}
~~~

## :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/eUmyjlDAxmT)
## :tv: Link al video del proceso
- [video](https://www.youtube.com/watch?v=VyGjE8kx-O0)

---








