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

| Kod namn | Förklaring |
| --- | --- |
| __pinMode__ | Bestämmer hur pinnen används |
| __LED_BUILTIN__ | Inbyggda LED-lampan |
| __OUTPUT__ | Skickar ut signalen |

__Serial.begin__ = Kommunikationen och att den startar
__(115200)__ = Kommunikationshastigheten

## Loop
Sedan följs det upp med en så kallad "loop".

En loop gör följande:
- Körs om och om igen
- Innehåller programmets huvudfunktioner
- Gör att LED-lampan kan forsätta blinka

Kopierbart exempel:
```html
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(500);
  digitalWrite(LED_BUILTIN, LOW);
  delay(500);
}
```

Här är det också viktigt att veta att HIGH och LOW är motsatsen från varann. HIGH betyder att lampan ska släckas och LOW betyder att lampan ska tändas.

Här är det också såklart viktigt vid slutet av ett kommando att sluta med " ; "