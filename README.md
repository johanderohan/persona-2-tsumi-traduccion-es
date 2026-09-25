# Persona 2: Tsumi (Innocent Sin) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Persona 2: Tsumi* (ペルソナ2 罪, PlayStation, 1999),
el RPG de Atlus que en Occidente se conoce como *Innocent Sin* y cuya versión de PlayStation
nunca salió de Japón.

La traducción se distribuye como **parche**. No incluye el juego: necesitas tu propia copia
japonesa para aplicarlo.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion de eventos | 9.339 mensajes traducidos |
| Diálogos de los personajes de los mapas de la ciudad | 947 mensajes traducidos |
| Contacto con demonios | 6.258 textos traducidos |
| Menús, objetos, demonios, habilidades, avisos y tarjeta de memoria | Traducidos |
| Pantalla de nombre | Teclado en castellano con tildes, ñ y ¡¿ |
| Mapas de la ciudad y mapa automático | Traducidos |
| Placas de nombre y estados alterados de la interfaz | Redibujados en castellano |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Revisión durante una partida | Parcial (ver abajo) |

Detalles técnicos:

- Fuente proporcional nueva, con el mismo color y sombra que la original.
- El nombre del protagonista también se ve con ancho proporcional en los diálogos.
- Se admiten hasta 8 letras por nombre.

Se quedan como en el original:

- El poema del vídeo de introducción, que está grabado en la imagen.
- Los rótulos grandes que forman parte de la imagen de marca, como el logotipo, «CONTINUE» o
  «NEW GAME» y algunos títulos de menú en inglés.
- Los logotipos de las tiendas del mapa.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador desde una partida nueva hasta el patio de la primera mazmorra del
instituto Seven Sisters. Se han comprobado:

- La pantalla de nombre y el prólogo.
- La escena de Joker y la cárcel de Sumaru.
- Los mapas de Hirasaka y Rengedai, con sus diálogos.
- Una tienda (comprar y vender), los rumores, la carga y el guardado.
- Tres combates con contactos que acaban en éxito y en fracaso, pactos, magia, tácticas y
  subida de nivel.

El parche se ha aplicado sobre el BIN japonés original y el resultado se ha comparado byte a
byte con la imagen probada.

**No se ha jugado una partida completa de principio a fin** ni se ha probado en consola
real. Los distritos de Yumezaki, Aoba, Konan y el monte Katatsumuri, los jefes y el resto de
la historia no se han recorrido en las pruebas. La traducción y su revisión se han hecho con
asistencia de IA, sin revisores humanos independientes. Si encuentras un error, abre una
incidencia con una captura.

Limitaciones conocidas:

- En la cabecera de las ranuras de guardado solo caben unas 6 letras por nombre. Con
  nombres más largos, como «Tatsuya», el nombre y el apodo se solapan.
- Los estados alterados se muestran con abreviaturas de tres letras (MUE, VEN, DOR, CON…)
  sobre el nombre del personaje, en el mismo sitio que los kanji originales.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia de **Persona 2: Tsumi (Japón) (Rev 1)**, SLPS-02100, en formato
   BIN/CUE de una sola pista.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Persona 2 - Tsumi - Innocent Sin (Japan) (Rev 1).bin` |
   | Tamaño | 691.328.064 bytes |
   | MD5 | `fd0ca3c97da9f725938e087aac5a34bc` |

   ```bash
   md5sum "Persona 2 - Tsumi - Innocent Sin (Japan) (Rev 1).bin"            # Linux
   md5 "Persona 2 - Tsumi - Innocent Sin (Japan) (Rev 1).bin"               # macOS
   CertUtil -hashfile "Persona 2 - Tsumi - Innocent Sin (Japan) (Rev 1).bin" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "original.bin" parche.xdelta "Persona 2 - Tsumi (ES).bin"`
5. Comprueba que el BIN resultante tiene el MD5 **`305c8a014bd66c7ba7292ec3fa8e4fd6`** (v1.0).
6. Crea un CUE para el nuevo BIN, por ejemplo `Persona 2 - Tsumi (ES).cue`:

   ```
   FILE "Persona 2 - Tsumi (ES).bin" BINARY
     TRACK 01 MODE2/2352
       INDEX 01 00:00:00
   ```

7. Carga el CUE en tu emulador y empieza una partida nueva.

Aplica el parche sobre el **BIN japonés original**, no sobre una copia ya parcheada.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna
con Atlus ni SEGA. Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que
modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
