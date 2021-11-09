## PWM (Pulse Width Modulation)

Problema tengo un Adruino que suministra SV a un LED.

A mayor intensidad de corriente (A) el LED brilla más.

A menor intensidad de corriente el LED brilla menos (Ver ley de OHM)

I=V/R Si subimos o bajamos el voltaje, haremos lo mismo con la intensidad 
Suponiendo que la resistencia del circuito es la misma. 

Entonces si conecto un led co su resistencia de 220VL.

A un voltaje de SV ó de 3'3V
El LED brilla más con SV 

### Qué es un pulso

Un pulso eléctrico es una señal de voltaje medida en el tiempo.

Los ojos humanos podemos detectar cambio hasta en torno a 12HZ

A partir de 24-30HZ no somos capaces visualmente

Los pulsos modulados en ancho crean la ilusión de voltajes interemedios entre o y SV para ello usan pulsos muy cortos.

Que usaremos a través de función

AnalogWrite(Pin,0-255) esta función solo funsiona en pines con PWM.

Los pines con PWM están marcados con el símbolo ~ (la tilde de la eñe)

La función nos pide 2 cosas "Por un lado (y lo primero) El número de PIN

Por otro lado un número entre 0y255

0-0% De Voltaje 

255-100% de voltae(Su)

int= integer
(número entero)

Significa que nuestra variable es un tipo de dato numérilo no decimal

Le asigma un espacio en memoria otros tipos

sting=cadena de caracteres 

bool=booleno y es verdadero o falso

char= 1 unico caracter

float= número decimales

### Trabajo

const int greenLEDPin= 9;
const int redLEDPin= 11;
const int blueLEDPin= 10;

const int redSensorPin= A0;
const int greenSensorPin= A1;
const int blueSensorPin= A2;

int redValue= 0;
int greenValue= 0;
int blueValue= 0;

int redSensorValue= 0;
int greenSensorValue= 0;
int blueSensorValue= 0;

void setup() {
  Serial.begin(9600);

  pinMode(greenLEDPin, OUTPUT);
  pinMode(redLEDPin, OUTPUT);
  pinMode(blueLEDPin, OUTPUT);
  
}


void loop () {
  redSensorValue= analogRead(redSensorPin);
  delay(5);
  greenSensorValue= analogRead(greenSensorPin);
  delay(5);
  blueSensorValue= analogRead(blueSensorPin);

 Serial.print("Raw Sensor Values \t Red: ");
 Serial.print(redSensorValue);
 Serial.print("\t Green: ");
 Serial.print(greenSensorValue);
 Serial.print("\t Blue: ");
 Serial.println(blueSensorValue);

 redValue= redSensorValue/4;
 greenValue= greenSensorValue/4;
 blueValue= blueSensorValue/4;

 Serial.print("Mapped Sensor Value \t Red: ");
 Serial.print(redValue);
 Serial.print("\t Green:");
 Serial.print(greenValue);
 Serial.print("\t Blue:");
 Serial.println(blueValue);

 analogWrite(redLEDPin, redValue);
 analogWrite(greenLEDPin, greenValue);
 analogWrite(blueLEDPin, blueValue);
 
}
