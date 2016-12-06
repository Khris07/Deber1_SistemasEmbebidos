# Deber3_SistemasEmbebidos
//Password
#include <LiquidCrystal.h>
LiquidCrystal lcd (12,11,5,4,3,2);
char txt [10];
int cont=0; 
String dato;
int tamano;

void setup() {
  lcd.begin(16,2);
  Serial.begin(9600);
  Serial.println("INGRESE EL TEXTO");
  lcd.clear();
}

void loop() {
  if (Serial.available()>0){
    dato=Serial.readString();  
    tamano=dato.length(); 
    Serial.println(dato);
    delay(400); 
    lcd.clear();       
  }   
  for(;cont<tamano;cont++){
    lcd.setCursor(cont+6, cont-2); 
    lcd.print(dato);
    delay(400);
    lcd.clear(); 
    }    
    lcd.clear();
    cont=0;
}
