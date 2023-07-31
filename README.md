# connect-two-arduino-

link tp tenkercad "https://www.tinkercad.com/things/2DNeIRk1FUp-connect-two-arduino/editel"

this code for the first arduino :
const int inPin = 3;


void setup()
{
  pinMode(inPin, INPUT);
  Serial.begin(9600);
}

void loop()
{
  Serial.print( digitalRead(inPin));
  delay(1000);
}

this code fot the second arduino :
const int OUT_PIN = 2;

int buttonState ;

void setup()
{
  pinMode(OUT_PIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  if(Serial.available() == 1) {
    buttonState = bitRead(Serial.read(), 0);
  }
  digitalWrite(OUT_PIN, buttonState);
  delay(1000);
}
![لقطة شاشة 2023-07-31 164320](https://github.com/Ammaralaseri/connect-two-arduino-/assets/140005774/ddb9893b-8346-41ba-82b5-fd9d9f664233)

