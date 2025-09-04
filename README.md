# Tarea 2
# Código ASCII, Pines de los conectores y Profundizacion 

Revisar, describir y profundizar acerca de código ASCII, los conectores RS232 (DB9 y DB25) y el formato del protocolo RS232.

---

## 1.
![Descripción de la imagen](Screenshot_2025-09-03_223624.png) 
**Código ASCII**
**Historia:**  
El código ASCII (American Standard Code for Information Interchange) nació en los años 60 como una solución a un problema: cada fabricante de computadoras usaba sus propios códigos para representar caracteres, lo que hacía muy difícil que diferentes equipos se entendieran. ASCII unificó esto creando un estándar que todos podían seguir.  

**Funcionamiento:**  
Para su funcionamiento lo que se haces es que el codigo ASCII asigna un número a cada letra, número o símbolo. Por ejemplo, la letra **A** corresponde al número 65 y la letra **a** al 97. Estos números se convierten a binario, que es el lenguaje que entiende la computadora. De esta forma, cuando escribimos en un teclado, en realidad lo que enviamos al sistema son números binarios que van a representar un caracteres especifico. 
Por ejemplo:  
- Letra **A** → Decimal: 65 → Binario: 01000001  
- Letra **a** → Decimal: 97 → Binario: 01100001  

**Importancia:**  

Lo más relevante de ASCII es que permitió que diferentes dispositivos pudieran comunicarse sin importar la marca o el modelo del equipo. Además, sirvió de base para estándares más modernos como Unicode, que hoy permite representar no solo letras inglesas, sino también caracteres de otros idiomas como el chino, árabe o emojis.  

---

## 2.![Descripción de la imagen](image.png)  

**Pines de los conectores RS232 (DB9 y DB25)**

### Conector DB9
| Pin | Nombre | Descripción |
|-----|---------|-------------|
| 1   | DCD     | Data Carrier Detect |
| 2   | RXD     | Receive Data |
| 3   | TXD     | Transmit Data |
| 4   | DTR     | Data Terminal Ready |
| 5   | GND     | Tierra |
| 6   | DSR     | Data Set Ready |
| 7   | RTS     | Request To Send |
| 8   | CTS     | Clear To Send |
| 9   | RI      | Ring Indicator |

### Conector DB25
| Pin | Nombre | Descripción |
|-----|---------|-------------|
| 1   | GND     | Tierra |
| 2   | TXD     | Transmit Data |
| 3   | RXD     | Receive Data |
| 4   | RTS     | Request To Send |
| 5   | CTS     | Clear To Send |
| 6   | DSR     | Data Set Ready |
| 7   | GND     | Tierra |
| 8   | DCD     | Data Carrier Detect |
| 20  | DTR     | Data Terminal Ready |
| 22  | RI      | Ring Indicator |

---

## 3.![Descripción de la imagen](Screenshot_2025-09-03_230355.png) 
Formato del protocolo RS232

El protocolo RS232 define cómo se transmiten los bits entre dispositivos.  

**Características principales:**  
- Comunicación **serial** (un bit a la vez).  
- Velocidades comunes: 9600, 19200, 115200 bps.  
- Señales eléctricas:  
  - Lógico 1 → voltaje entre -3V y -15V  
  - Lógico 0 → voltaje entre +3V y +15V  

**Formato de trama (frame):**  
1. **Bit de inicio (Start bit):** siempre `0`, indica el comienzo de transmisión.  
2. **Bits de datos:** normalmente 7 u 8 bits que representan el carácter.  
3. **Bit de paridad (opcional):** usado para detección de errores.  
4. **Bits de parada (Stop bits):** uno o dos `1` que indican el fin de la trama.  

