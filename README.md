
# Ultrasonic-Sensor-And-Bluetooth-Module-Circuit


```
const int trigPin = 3; const int echoPin = 2; long duration, cm;

void setup() {
  Serial.begin(9600);  pinMode(trigPin, OUTPUT);  pinMode(echoPin, INPUT);
}

void loop()
{
   
  digitalWrite(trigPin, LOW); 
  delayMicroseconds(2);  
  digitalWrite(trigPin, HIGH);  
  delayMicroseconds(10);  
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);
 
  cm = (duration/2)/29.1;
  if(cm < 20)
  {
    Serial.print("d"); delay(400);
  }
  else
  {
    Serial.print("n"); delay(400);
  }  
}
```
![schematic_2](https://user-images.githubusercontent.com/67175109/126713994-18b287f3-c1a3-48bc-aa2a-67d00f91d666.png)

