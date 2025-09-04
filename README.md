# Tarea 2
# Comunicación RS232 y Código ASCII

Este documento contiene una descripción del código ASCII, los conectores RS232 (DB9 y DB25) y el formato del protocolo RS232.

---

## 1.![Descripción de la imagen](image.png) 
**Código ASCII**
**Historia:**  
El código ASCII (American Standard Code for Information Interchange) fue desarrollado en 1963 por el comité ANSI. Su propósito fue unificar la representación de caracteres en computadoras, reemplazando distintos códigos propietarios que usaban los fabricantes.

**Funcionamiento:**  
ASCII representa letras, números y símbolos como números binarios de 7 bits (0-127). Cada carácter corresponde a un valor decimal, hexadecimal y binario. Ejemplo:  
- Letra **A** → Decimal: 65 → Binario: 01000001  
- Letra **a** → Decimal: 97 → Binario: 01100001  

**Importancia:**  
- Permite la comunicación entre diferentes dispositivos y sistemas.  
- Es la base para otros estándares modernos como Unicode.  

---

## 2. 
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

**Referencia:**  
[RS232 Pinout](https://www.electronicshub.org/rs232-pinout/)

---

## 3. Formato del protocolo RS232

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

Ejemplo de transmisión a 8 bits con paridad:  


