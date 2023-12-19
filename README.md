# Solarpowered_trashcollector
int motorSpeed = 200;  // Set the initial motor speed (0-255)
int motorA1 = 4;       // IN1
int motorA2 = 5;       // IN2
int motorB1 = 6;       // IN3
int motorB2 = 7;       // IN4

void setup() {
  pinMode(motorA1, OUTPUT);
  pinMode(motorA2, OUTPUT);
  pinMode(motorB1, OUTPUT);
  pinMode(motorB2, OUTPUT);
}

void loop() {
  // Move Motor A Forward
  digitalWrite(motorA1, HIGH);
  digitalWrite(motorA2, LOW);
  analogWrite(2, motorSpeed);  // Enable Motor A (ENA pin)

  // Move Motor B Forward
  digitalWrite(motorB1, HIGH);
  digitalWrite(motorB2, LOW);
  analogWrite(3, motorSpeed);  // Enable Motor B (ENB pin)

  // Delay for a while
  delay(2000);

  // Stop both motors
  digitalWrite(motorA1, LOW);
  digitalWrite(motorA2, LOW);
  digitalWrite(motorB1, LOW);
  digitalWrite(motorB2, LOW);

  // Delay again
  delay(1000);

  // Move Motors A and B backward
  digitalWrite(motorA1, LOW);
  digitalWrite(motorA2, HIGH);
  analogWrite(2, motorSpeed);  // Enable Motor A (ENA pin)
  digitalWrite(motorB1, LOW);
  digitalWrite(motorB2, HIGH);
  analogWrite(3, motorSpeed);  // Enable Motor B (ENB pin)

  // Delay
  delay(2000);

  // Stop both motors
  digitalWrite(motorA1, LOW);
  digitalWrite(motorA2, LOW);
  digitalWrite(motorB1, LOW);
  digitalWrite(motorB2, LOW);

  // Delay again
  delay(1000);
}
