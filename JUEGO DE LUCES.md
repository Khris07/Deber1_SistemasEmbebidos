int led_1=13;
int led_2=12;
int led_3=11;
int led_4=10;
int led_5=9;
int led_6=8;
int led_7=7;
int led_8=6;
int led_9=5;
int led_10=4;

int sw_1=3;
int sw_2=2;
int sw_3=1;

int contador=0;
int aleatorio;

int led_par [5]={led_2,led_4,led_6,led_8,led_10};
int led_imp [5]={led_1,led_3,led_5,led_7,led_9};
int led_ram [10]={led_1,led_2,led_3,led_4,led_5,led_6,led_7,led_8,led_9,led_10};
int leds [2]={led_1,led_2};
int led [2]={led_3,led_4};
int le [1]={led_5};
int e [1]={led_6};
int l [2]={led_8,led_7};
int f [2]={led_10,led_9};
void setup() {
  pinMode(led_1,OUTPUT);
  pinMode(led_2,OUTPUT);
  pinMode(led_3,OUTPUT);
  pinMode(led_4,OUTPUT);
  pinMode(led_5,OUTPUT);
  pinMode(led_6,OUTPUT);
  pinMode(led_7,OUTPUT);
  pinMode(led_8,OUTPUT);
  pinMode(led_9,OUTPUT);
  pinMode(led_10,OUTPUT);
  pinMode(sw_1,INPUT);
  pinMode(sw_2,INPUT);
  pinMode(sw_3,INPUT);

}

void loop() {
  
 if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==LOW)
  {
  for(;contador<5;contador++)  
    {
     digitalWrite(led_par[contador],HIGH);
     delay(100);
     digitalWrite(led_par[contador],LOW);
     delay(100);
    }   
   contador=0;  
 }
 contador=0; 
  
 if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==HIGH)
  {
  for(;contador<5;contador++)  
    {
     digitalWrite(led_imp[contador],HIGH);
     delay(100);
     digitalWrite(led_imp[contador],LOW);
     delay(100);
    }   
   contador=0;  
 }
 contador=0;

 if(digitalRead(sw_1)==LOW&&digitalRead(sw_2)==LOW&&digitalRead(sw_3)==HIGH)
  {
    aleatorio=random(0,10);
     digitalWrite(led_ram[aleatorio],HIGH);
     delay(100);
     digitalWrite(led_ram[aleatorio],LOW);
     delay(100);
      
  }
  if(digitalRead(sw_1)==HIGH&&digitalRead(sw_2)==HIGH&&digitalRead(sw_3)==LOW)
  {
  for(;contador<2;contador++)  
    {
     digitalWrite(leds [contador],HIGH);
     digitalWrite(f[contador],HIGH);
     delay(100);
     digitalWrite(leds [contador],LOW);
     digitalWrite(f[contador],LOW);
     delay (100);
    }   
   contador=0;  
 }
 contador=0;

  for(;contador<2;contador++)  
    {
    digitalWrite(led [contador],HIGH);
     digitalWrite(l[contador],HIGH);
     delay(100);
     digitalWrite(led [contador],LOW);
     digitalWrite(l[contador],LOW);
     delay (100);
    }   
   contador=0;  

    for(;contador<1;contador++)  
    {
    digitalWrite(le [contador],HIGH);
    digitalWrite(e [contador],HIGH);
     delay(100);
     digitalWrite(le [contador],LOW);
     digitalWrite(e [contador],LOW);
     delay (100);
    }   
   contador=0;  
 }
