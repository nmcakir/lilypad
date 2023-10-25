The Knight rider Code
=====

.. code-block:: c

// Pin definitions
const int ledPins[] = {5, 6, 9, 10, 11, A2, A3};
const int numLeds = sizeof(ledPins) / sizeof(ledPins[0]);

// Delay between LED transitions (in milliseconds)
const int delayTime = 100;

void setup() {
  // Set all LED pins as outputs
  for (int i = 0; i < numLeds; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  // Turn on LEDs in sequence
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(ledPins[i], HIGH);
    delay(delayTime);
  }

  // Turn off LEDs in sequence
  for (int i = numLeds - 1; i >= 0; i--) {
    digitalWrite(ledPins[i], LOW);
    delay(delayTime);
  }
}

