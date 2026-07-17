#define BLYNK_PRINT Serial
#define BLYNK_TEMPLATE_ID   "TUKAR"

#include <WiFi.h>
#include <WiFiClient.h>
#include <BlynkSimpleEsp32.h>

char auth[] = "TUKAR";
char ssid[] = "TUKAR";
char pass[] = "TUKAR";
BlynkTimer timer;

#include "DHT.h"
#define DHTPIN D7    
#define DHTTYPE DHT11   
DHT dht(DHTPIN, DHTTYPE);*/

BLYNK_WRITE(V1)
{ int pb=param.asInt();
  if(pb==1) digitalWrite(D0,HIGH);
  if(pb==0) digitalWrite(D0,LOW);
}

int status=0;
void kelip()
{ digitalWrite(D1,status);
  if(status==1) Blynk.virtualWrite(V0,HIGH);
  if(status==0) Blynk.virtualWrite(V0,LOW);
  status =! status;
}

/*void readTe()
{ Blynk.virtualWrite(V2,dht.readTemperature());
  Blynk.virtualWrite(V3,dht.readHumidity());
  Serial.print(dht.readTemperature());
  Serial.print("  ");
  Serial.println(dht.readHumidity());
}*/

void readPB()
{ int pbD5 = digitalRead(D5);
  if(pbD5==1) Blynk.virtualWrite(V4,HIGH);
  if(pbD5==0) Blynk.virtualWrite(V4,LOW);
}

void setup()
{ pinMode(D0,OUTPUT);
  pinMode(D1,OUTPUT);
  pinMode(D5,INPUT);
  Serial.begin(9600);
 // dht.begin();
  Blynk.begin(auth, ssid, pass);
  timer.setInterval(500L,kelip);
 // timer.setInterval(1000L,readDHT);
  //timer.setInterval(10L,readPB);
}

void loop()
{ Blynk.run();
  timer.run();
}
