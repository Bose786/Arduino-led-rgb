# Arduino-led-rgb
char amn;//amn is my global variable
void setup()
{
pinMode(13,OUTPUT);
pinMode(12,OUTPUT);
pinMode(11,OUTPUT);
Serial.begin(9600);
}
 void loop()
{
if(Serial.available() >0)
{
  amn = Serial.read();//read as input
  if(amn == 'H')
  {
    digitalWrite(13,HIGH);
  }
  if(amn == 'L')
  {
    digitalWrite(13,LOW);
  }
  if(amn == 'A')
  {
    digitalWrite(12,HIGH);
  }
  if(amn == 'B')
  {
    digitalWrite(12,LOW);
  }
  if(amn == 'Y')
  {
    digitalWrite(11,HIGH);
  }
  if(amn == 'Z')
  {
    digitalWrite(11,LOW);
  }
}
}
