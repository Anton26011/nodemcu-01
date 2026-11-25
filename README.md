# Kod med förklaring
När man skriver kod för till exempel mikro kontrollers så använder man C++ alltså en språkvariant av __source kod__ (käll kod).

Denna kod som man skriver måste man sedan omvandla till språk så att datorn förstår det (1:or och 0:or), denna omvadnling heter __compile__ (kompilera).

Här kommer en enkel förklaring till hur man kodar en LED-lampa via en mikrokontroller.

## Setup
Först startar man med en så kallad "setup".

En __setup()__ gör följande:
- Körs en gång vid start.
- Ställer in pinnar med pinMode().
- Startar kommunikation med Serial.begin().

Kopierbart exempel:
```html
void setup() {
    pinMode(LED_BUILTIN, OUTPUT);
    Serial.begin(115200);

}
```

pinMode = 
LED_BUILTIN = Inbyggda LED-lampan
OUTPUT = Skickar ut signalen

## Loop
Sedan följs det upp med en så kallad "loop".

Kopierbart exempel:
```html
void loop() {

}
```

En loop gör följande:
- Körs om och om igen
- Innehåller programmets huvudfunktioner
- Gör att LED-lampan kan forsätta blinka



Här är det också såklart viktigt vid slutet av ett kommando att sluta med " ; "