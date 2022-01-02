/*
 *  PROJECT NAME   : SMART FLOWERPORT
 *  AUTHOR         : DEVRIM CAN DIVIT
 *  DATE           : 29.12.2021
 */


int soilMoistureValue = 0;    //soil moisture 
int percentage=0;             //soil mousture percentage

//setup code area 
void setup() {
  pinMode(3,OUTPUT);          //3 pin defined as OUTPUT
  Serial.begin(9600);         // sets the baut rate for serial data transmission
}

//main code area
void loop() {
soilMoistureValue = analogRead(A0);
if(percentage < 10)  
{
  digitalWrite(3,LOW);        //water pump is off
}
else if(percentage >80)
{
  digitalWrite(3,HIGH);       //water pump is on
}
}
