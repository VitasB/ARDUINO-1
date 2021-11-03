-Leer pinao

-Transforma los valores y de ergalo las pinta en pantalla

-Decidir

-Digital write es una funcion que nos pide un numero de pin y el valor HIGH (1) o LOW (0).

Si el valor es HIGH la placa subministrara 5V en ese pin

Si el valor es LOW la placa subministrara 0V en este pin

Si hay 5V se activaran los circuitos

Si es 0V no se activara

* depende del hawdred y como este conectado.



- EJERCICIO - 

Vamos a conectar 2 botones y 2 leds

Haremos diferentes programas con diferentes comportaciones.

Para poner un boton necesitamon una reistencia 10.000 (ohmnos) estas son als que tienen cuerpo beige y una linea naranja.

ejemplo:
   
 DigitalWrite ( 4 ; LOW ); o digitalWrite (4,0); se desactivaran los numeros de los pines 
  
 Si es high se activaran 5 V A los numeros de los pines.
  
  
  
} Else if (temperature >= baselineTemp +2 && temperature < baselineTemp +4){

DW ( 2,HIGH );
DW (3,LOW );
DW (4,LOW );

} Else if (temperature >= baselineTemp +4 && temperature < baselineTemp +6){

DW (2,HIGH);
DW (3,HIGH);
DW (4,LOW);


 } Else if (temperature >= baselineTemp +6) {
 
DW (2,HIGH);
DW (3,HIGH);
DW (4,HIGH);

## Conectar dos botones 

-Ejercicio 
Vamos a conectar 2 botones y 2 leds 
 
Haremos diferentes programas con diferentes comportamientos 

Para poner un boton necesitamos una resistencia de 10.000 Ohmios. Estas son las que tienen cuerpo BEIGE y una linia naranja.

Esquema de boton " Por defecto arriba o "pulled -HIGH "

Conectaremos 2 botones .UNO al Pin 2 , Pin 3 

Para poner un Led necesitamos una resistencia de 220 OHMIOS las de cuerpo azul.

Hay que tener en cuenta la polaridad del led.

La pata mas corta va hacia el GND ( o 0 V ) y la larga hacia el Voltaje.

Pin -----> led ----> 220 OHMNIOS --- GND 

Da igual si la resistencia va detras o delante del led.

Conectaremos 2 leds . Uno al Pin 4 y otro al Pin 5.

Ejercicio 1

Encender los 2 leds

sold si pulsamos 

los 2 botones(Apagar si no)

Operadores 1

Ejercicio 2

Encender los 2 leds 

Si pulsamos cualquiera de los botones(si no apagar)

Operadores 2
