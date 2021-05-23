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
  pinMode(temperaturepin,INPUT);//pin for temperature sensor
  pinMode(bloodpressurepin,INPUT);//pin for blood pressure sensor
  pinMode(pulseratepin,INPUT);//pin for pulse sensor
  pinMode(breathingratepin, INPUT);//pin for breathing sensor
  pinMode(buzzerpin, OUTPUT);//pin for piezo buzzer
 }
   
   void loop()
   {
     temperature=analog Read(temperature pin);
     bloodpressure=analog Read(bloodpressurepin);
     pulserate=analog Read(pulseratepin);
     breathingrate=analog Read(breathingratepin);
     
     if(temperature<=98.5 && bloodpressure<120 && pulserate>60 && breathingrate>12)
     {
       digitalWrite(13,HIGH);//alert sound from piezo buzzer
     }
     else
     {
       digitalWrite(13,Low);//no sound from piezo buzzer
     }
    } 
