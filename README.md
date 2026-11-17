const int in_1 = 5;
const int in_2 = 6;
const int in_3 = 9;
const int in_4 = 10;
void setup()
{
Serial.begin(9600);
pinMode(5, OUTPUT);
pinMode(6, OUTPUT);
pinMode(9, OUTPUT);
pinMode(10, OUTPUT);
}
void loop()
{
if (( Serial.read() == ‘F’))
{
digitalWrite(in_1, HIGH);
digitalWrite(in_2, LOW);
digitalWrite(in_1, HIGH);
digitalWrite(in_2, LOW);
}
if (( Serial.read() == ‘B’))
{
digitalWrite(in_1, LOW);
digitalWrite(in_2, HIGH);
digitalWrite(in_1, LOW);
digitalWrite(in_2, HIGH);
}
if (( Serial.read() == ‘L’))
{
digitalWrite(in_1, HIGH);
digitalWrite(in_2, LOW);
digitalWrite(in_1, LOW);
digitalWrite(in_2, HIGH);
}
if (( Serial.read() == ‘R’))
{
digitalWrite(in_1, LOW);
digitalWrite(in_2, HIGH);
digitalWrite(in_1, HIGH);
digitalWrite(in_2, LOW);
}
if (( Serial.read() == ‘S’))
{
digitalWrite(in_1, LOW);
digitalWrite(in_2, LOW);
digitalWrite(in_1, LOW);
digitalWrite(in_2, LOW);
}
}
