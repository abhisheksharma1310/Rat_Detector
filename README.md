# Rat_Detector
This can detect Rat using Laser and Photodiode Sensor

Arduino Code

<pre>
<code>
int ldrPin = A0;
int buzzer = 3;

void setup() 
{
  Serial.begin(9600);
  pinMode(ldrPin,INPUT);
  pinMode(buzzer,OUTPUT);
}

void loop() 
{
  int ldrValue = analogRead(ldrPin);
  //Serial.print("LDR Value:");
  //Serial.println(ldrValue);
  if (ldrValue > 1000)
  {
    Serial.println("Rat Detected");
    digitalWrite(buzzer,HIGH);
  }
  else
  {
    digitalWrite(buzzer,LOW);
  }
}
</code>
</pre>

<p>Schematic</p>

<img src = "https://github.com/abhisheksharma1310/Rat_Detector/blob/main/Rat%20Detector.png>
