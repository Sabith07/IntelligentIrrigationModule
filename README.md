# IntelligentIrrigationModule
S5EEEProject

#define Temperature and Humidity sensor A0 // Analog pin A0 of Arduino Uno
int sensor_pin = A0;
int output_value ;
int ledPin1 = 13;
int ledPin2 = 12;
int ledPin3 = 11;
int pos = A1; // Define motor position
——————————————————————————————————————————————
#define Sensor_PIN No.
void setup()
{
(ledPin1, OUTPUT); (ledPin2, OUTPUT); (ledPin3, OUTPUT); // Define the pinModes
pinMode(motorPin, OUTPUT); // set A1 to an output so we can use it to turn on the transistor
Serial.begin(9600); // Baud Rate
Serial.println(“Reading From the Sensor …”);
}
—————————————————————————————————————————————-
void loop()
{
// READ DATA
Serial.print(“Define Sensor, \t”);
int chk = Read the Output of Sensor;
switch (chk)
{
case SensorNameLIB_OK:
Serial.print(“OK,\t”);
break;
case SensorNameLIB_ERROR_CHECKSUM:
Serial.print(“Checksum error,\t”);
break;
case SensorNameLIB_ERROR_TIMEOUT:
Serial.print(“Time out error,\t”);
break;
default:
Serial.print(“Unknown error,\t”);
break;
}
——————————————————————————————————————————————
// DISPLAY DATA
Serial.print(“Humidity:”);
Serial.print(sensorname.humidity, 1);
Serial.print(“%”);
Serial.println(“,\t”);
Serial.print(“Temperature:\t”);
Serial.print(sensorname.temperature, 1);
Serial.println(“`C”);
value= analogRead(sensor_pin);
value = map(value,550,0,0,100);
Serial.print(“Mositure : “);
Serial.print(output_value);
Serial.println(“%”);
if (Humidity value>10)
{
Sensorinput gets HIGH; //green LED ON
}
else {
Sensorinput gets LOW; //Digital Output
}
if (Sensor value>31)
{
Sensorinput gets HIGH; // Digital output
Serial.println(“Tempearture is HIGH”); //yellow LED ON
}
else {
Sensorinput gets Low;
}
if (value>50)
{
Sensorinput gets HIGH;
Serial.println(“Moisture is high”);// RED
}
else {
Sensorinput gets LOW;
}
if (output_value<10) { Serial.println(“output value is low”); Sensorinput gets HIGH; // Digital output delay(x); Sensorinput gets LOW; // Digital output delay(x); } else { Sensorinput gets HIGH; //Digital output } if(Serial.available()>0)
{
char data = Serial.read();
if (data == ‘a’)
{
Motorinp pin gets HIGH; //Digital output
}
else if(data == ‘b’)
{
Motorinp pin gets LOW; //Digital output
}
}
delay(x);
}
//
// END OF FILE
//————————————————————
