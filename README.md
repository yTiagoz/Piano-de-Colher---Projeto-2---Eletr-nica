## Piano-de-Colher---Projeto-2---Eletrônica

## Objetivo

Construir um piano utilizando arduíno e colheres

## Vídeo no YT
[Link YT](https://youtu.be/08xDY9iudbI)

## Projeto no Tinkercad
[Link Tinkercad](https://www.tinkercad.com/things/bdmib5eNnfc-piano-de-colher?sharecode=OIaA_JvBRm8S8QFiRidHZSuT0n3t74cxiyn0jVJrh7M)

## Código utilizado

```cpp
// C++ code
//
void setup()
{
  Serial.begin(9600);
  pinMode(A0, INPUT);
  pinMode(A1, INPUT);
  pinMode(A2, INPUT);
  pinMode(A3, INPUT);
  pinMode(A4, INPUT);
  pinMode(A5, INPUT);
  pinMode(8, OUTPUT);
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  int leiA0 = map(analogRead(A0), 0, 1023, 0, 5);
  int leiA1 = map(analogRead(A1), 0, 1023, 0, 5);
  int leiA2 = map(analogRead(A2), 0, 1023, 0, 5);
  int leiA3 = map(analogRead(A3), 0, 1023, 0, 5);
  int leiA4 = map(analogRead(A4), 0, 1023, 0, 5);
  int leiA5 = map(analogRead(A5), 0, 1023, 0, 5);
  
  if(leiA5 <= 3){
    tone(8, 800, 100);
    Serial.println("A5");
  }
  else if(leiA1 <= 3){
    tone(8, 50, 100);
    Serial.println("A1");
  }
  else if(leiA2 <= 3){
    tone(8, 330, 100);
    Serial.println("A2");
  }
  else if(leiA3 <= 3){
    tone(8, 358, 100);
    Serial.println("A3");
  }
  else if(leiA4 <= 3){
    tone(8, 392, 100);
    Serial.println("A4");
  }
  else if(leiA0 <= 3){
    tone(8, 261, 100);
    Serial.println("A0");
  }
  
  digitalWrite(LED_BUILTIN, HIGH);
  delay(75); // Wait for 1000 millisecond(s)
}
```
## Alunos
### Tiago Kenzo Ogawa
### Leonardo Biondo Bertho
### Matheus Araujo Alves
