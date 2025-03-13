
#define BUZZER_PIN 3
#define LED_PIN 6
void setup() {
  // put your setup code here, to run once:
  pinMode(BUZZER_PIN,OUTPUT);
  pinMode(LED_PIN,OUTPUT);
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  int sensorValue = analogRead(A0);
  Serial.println(sensorValue);
  if(sensorValue > 40)
  {
    analogWrite(BUZZER_PIN,50);
    analogWrite(LED_PIN,50);
  }
  else
  {
    analogWrite(BUZZER_PIN,0);
    analogWrite(LED_PIN,0);
  }
  delay(1000);

}
