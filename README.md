/*....program for wearable human health monitoring....*/

float temperature;
int temperaturepin=2;
float bloodpressure;
int bloodpressurepin=8;
float pulseratepin=4;
int pulseratepin=4;
float breathingrate;
int breathingratepin=5;
int buzzerpin=13;
void setup()
{
  pin Mode(temperaturepin,INPUT);//pin for temperature sensor
  pin Mode(bloodpressurepin,INPUT);//pin for blood pressure sensor
  pin Mode(pulseratepin,INPUT);//pin for pulse sensor
  pin Mode(breathingratepin, INPUT);//pin for breathing sensor
  pin Mode(buzzerpin, OUTPUT);//pin for piezo buzzer
 }
   
   void loop()
   {
     temperature=analog Read(temperature pin);
     blood pressure=analog Read(bloodpressurepin);
     pulse rate=analog Read(pulseratepin);
     breathing rate=analog Read(breathingratepin);
     
     if(temperature<=98.5 && bloodpressure<120 && pulserate>60 && breathingrate>12)
     {
       digital Write(13,M1GH);//alert sound from piezo buzzer
     }
     else
     {
       digital Write(13,Low);//no sound from piezo buzzer
     }
    } 
