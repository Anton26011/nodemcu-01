# Kod med förklaring
När man skriver kod för till exempel mikro kontrollers så använder man C++ alltså en språkvariant av source kod (käll kod)

Denna kod som man skriver måste man sedan omvandla till språk så att datorn förstår det (1:or och 0:or), denna omvadnling heter kompilera

## Setup
Först startar man med en så kallad "setup".

Kopierbart exempel:
```html
void setup() {

}
```

En setup gör följande:
- Körs en gång för att förbereda programmet
- Talar om hur de olika pinnarna är konfigurerade på kontrollen med hjälp av pinMode()
- Startar kommunikation mellan datorn och NodeMCU med hjälp av Serial.begin()

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