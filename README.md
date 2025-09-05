# Electrical-Circuit-Design-and-Simulation-Lesson-12

<img width="825" height="690" alt="image" src="https://github.com/user-attachments/assets/baf725d6-1530-4b19-937a-e985ee110373" />
<img width="871" height="837" alt="image" src="https://github.com/user-attachments/assets/1a25e18c-76cb-4b16-8616-6e9157bcb6ef" />
<img width="1486" height="729" alt="image" src="https://github.com/user-attachments/assets/d331ee66-ed42-4dc3-b1f0-dde7b11bd76f" />
------------------------
<img width="1612" height="773" alt="image" src="https://github.com/user-attachments/assets/0951d884-e3ed-4063-b92d-96c57889fac2" />
    // C++ code
    //
    
    int ldr = A0;
    int kirmizi =3;
    int yesil=6;
    int mavi=5;
    
    void setup()
    {
    pinMode(ldr,INPUT);
    pinMode(kirmizi,OUTPUT);
    pinMode(yesil,OUTPUT);
    pinMode(mavi ,OUTPUT);
    Serial.begin(9600);
      
    }
    
    void loop()
    {
      double aydinlik = analogRead(ldr);
      Serial.println(aydinlik);
      if(aydinlik<26 && aydinlik>0){
      	analogWrite(kirmizi,aydinlik);
        digitalWrite(yesil,LOW);
         digitalWrite(mavi,LOW);
       
      }
      else if(aydinlik<452 && aydinlik>=226){
        analogWrite(kirmizi,aydinlik);
        analogWrite(yesil,aydinlik);
        digitalWrite(mavi,LOW);
        
      }else  {
        analogWrite(yesil,aydinlik);
         digitalWrite(mavi,LOW);
         digitalWrite(kirmizi,LOW);
      }
      
    }





    
