# Esp32-Bluetooth

```c++
#include "BluetoothSerial.h"
BluetoothSerial SerialBT;

void setup()
{
  Serial.begin(9600); //puerto serial del esp32
  SerialBT.begin("Esp32"); //nombre del dispositivo
}

void loop()
{
  if(Serial.available()) //si recibe datos del puerto serial
  {
    SerialBT.write(Serial.read()); //manda los datos bluetooth
  }
  if(SerialBT.available()) //si recibe datos bluetooth
  {
    Serial.write(SerialBT.read()); //escribe los datos en el puerto serial
  }
}
```

### Puerto Serial
<img src="https://github.com/IDiegoUlises/Esp32-Bluetooth/blob/main/Images/Puerto-Serial.png" />

### Telefono
<img src="https://github.com/IDiegoUlises/Esp32-Bluetooth/blob/main/Images/Captura.jpg" width="300" height="500" />



