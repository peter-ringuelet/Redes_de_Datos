## Resumen Completo

### 1. **Modelo OSI (Open Systems Interconnection):**
   - **Capas del Modelo OSI:**
     - **Capa Física (Physical Layer):** Se encarga de la transmisión de bits a través de un medio físico (cable, fibra óptica, aire, etc.). Maneja señales eléctricas, ópticas o de radiofrecuencia.
     - **Capa de Enlace de Datos (Data Link Layer):** Proporciona un enlace confiable entre nodos en la misma red física. Gestiona el control de acceso al medio (MAC), la detección de errores y la formación de tramas.
     - **Capa de Red (Network Layer):** Responsable del direccionamiento lógico (por ejemplo, direcciones IP) y el enrutamiento de paquetes a través de diferentes redes. Determina las rutas que los paquetes deben seguir.
     - **Capa de Transporte (Transport Layer):** Proporciona una comunicación confiable entre nodos finales. Se encarga de la segmentación y reensamblaje de datos, control de flujo y recuperación de errores (TCP y UDP).
     - **Capa de Sesión (Session Layer):** Establece, gestiona y termina las sesiones entre aplicaciones en diferentes dispositivos.
     - **Capa de Presentación (Presentation Layer):** Traduce datos entre la aplicación y la red. Se ocupa de la codificación de datos, compresión y encriptación.
     - **Capa de Aplicación (Application Layer):** Proporciona servicios de red a las aplicaciones del usuario. Incluye protocolos como HTTP, FTP, SMTP, etc.

   - **Encapsulamiento de Datos:**
     - Proceso mediante el cual los datos se preparan para ser transmitidos a través de la red, añadiendo cabeceras y trailers en cada capa.
     - **Orden del encapsulamiento:** Datos → Segmentos → Paquetes → Tramas → Bits.
   
   - **Eficiencia de Transmisión en el Modelo OSI:**
     - **Eficiencia de Transmisión:**
       - Cuando se agregan cabeceras en cada capa del modelo OSI, la eficiencia de transmisión se calcula como la proporción de los datos útiles (payload) en comparación con el total de datos transmitidos (payload + cabeceras).
       - **Fórmula para la eficiencia:**
         Eficiencia = (Datos útiles) / (Datos útiles + Cabeceras)

### 2. **Conceptos Clave de Red:**
   - **Segmento:** Unidad de datos en la capa de transporte.
   - **Paquete:** Unidad de datos en la capa de red.
   - **Trama:** Unidad de datos en la capa de enlace de datos.
   - **Bits:** Unidad de datos en la capa física.

### 3. **Modelo TCP/IP:**
   - **Capa de Aplicación:** Combina las funciones de las capas de aplicación, presentación y sesión del modelo OSI.
   - **Capa de Transporte:** Equivalente a la capa de transporte del modelo OSI. Gestiona la transmisión confiable de datos.
   - **Capa de Internet:** Similar a la capa de red del modelo OSI, se encarga del enrutamiento de paquetes.
   - **Capa de Acceso a la Red:** Combina las capas de enlace de datos y física del modelo OSI.

### 4. **Conceptos de Redes:**
   - **Causalidad:** Un sistema es causal si la salida en un momento dado depende solo de las entradas presentes y pasadas, no de futuras.
   - **Invarianza en el Tiempo:** Un sistema es invariante en el tiempo si su comportamiento no cambia cuando se desplaza la entrada en el tiempo.
   - **Linealidad:** Un sistema es lineal si cumple con las propiedades de homogeneidad (escalabilidad) y aditividad (superposición).
   - **Memoria:** Un sistema tiene memoria si la salida en un instante depende de entradas pasadas; si depende solo de la entrada actual, es sin memoria.
   - **Estabilidad:** Un sistema es estable si para una entrada acotada produce una salida acotada.

### 5. **Dispositivos de Red:**
   - **Tarjetas de Red (NIC):** Implementan las funciones de la capa física y de enlace de datos para gestionar la transmisión y recepción de datos en una red.

### 6. **Frecuencia y Período:** 
   - La frecuencia (f) es el número de ciclos de una señal por segundo, medida en Hertz (Hz).
   - El período (T) es el tiempo que toma un ciclo completo de la señal, y se relaciona con la frecuencia por T = 1/f.

### 7. **Señales Electromagnéticas:**
   - Una señal electromagnética puede sufrir atenuación a medida que viaja a través de un medio, lo que resulta en una disminución de la potencia de la señal en el receptor.
   - **Atenuación (en dB):** 
     Atenuación (dB) = 10 * log10(P_transmitida / P_recibida)

### 8. **Velocidad de Transmisión:**
   - Se mide en bits por segundo (bps) y se calcula usando la frecuencia de transmisión (en baudios) y el número de elementos de señal (V):
     Velocidad de transmisión (bps) = Baudios * log2(V)

### 9. **Teoremas Clave en Comunicaciones**

- **Teorema de Nyquist:**
  - En un canal sin ruido, la máxima velocidad de transmisión es:
    C = 2 * B * log2(V)
  - Donde B es el ancho de banda y V es el número de niveles de señal distintos.

- **Teorema de Shannon:**
  - La capacidad máxima de un canal con ruido se da por:
    C = B * log2(1 + S/N)
  - Donde S/N es la relación señal a ruido.

### 10. **Relación Señal/Ruido (S/N) y Conversión entre dB y Forma Lineal**

- **Conversión de dB a relación lineal:**
  Relación S/N = 10^(S/N (dB)/10)
  - Ejemplo: Una relación S/N de 30 dB se convierte a S/N = 1000.

- **Cálculo de S/N en dB:**
  Relación S/N (dB) = 20 * log10(A_señal / A_ruido)

### 11. **Cálculo de Potencia y Ancho de Banda**

- **Potencia de Ruido Térmico:**
  P_ruido = kTB
  - Donde k es la constante de Boltzmann, T es la temperatura en Kelvin, y B es el ancho de banda.
  
- **Potencia de Ruido Térmico en dBm:**
  - La potencia de ruido térmico se puede calcular en dBm utilizando la fórmula:
    P_ruido (dBm) = 10 * log10(P_ruido (W)) + 30

### 12. **Latencia y RTT (Round Trip Time)**

- **Latencia:** 
  - Es el tiempo que tarda una señal en viajar desde el transmisor al receptor. Para ondas viajando a la velocidad de la luz:
    Latencia = Distancia / Velocidad de la luz

- **RTT (Round Trip Time):**
  - Es el tiempo total para que una señal vaya y vuelva entre dos puntos. Se calcula como el doble de la latencia más los tiempos de transmisión:
    RTT = 2 * (Latencia + Tiempo de transmisión)

### 13. **Bandwidth-Delay Product (Producto de Ancho de Banda por Retardo):**

- **Definición:**
  - El producto de la latencia por la velocidad de transmisión es conocido como Bandwidth-Delay Product. Representa la cantidad de datos que pueden estar "en tránsito" en un canal en un momento dado.
  
- **Cálculo:**
  Producto = Latencia * Velocidad de transmisión
  
- **Significado:**
  - Este valor indica cuántos bits pueden estar "en vuelo" en un enlace de comunicaciones en un momento dado, y es crucial para determinar el tamaño óptimo de las ventanas de transmisión en protocolos como TCP.

### 14. **Cálculo de Velocidad de Transmisión en un Canal Telefónico**

- **Canal Telefónico:**
  - Ancho de banda típico: 4 kHz.
  - Relación señal/ruido y capacidad calculada usando el Teorema de Shannon.

### 15. **Transmisión de Imágenes y Vídeo**

- **Transmisión de Imágenes:**
  - Para imágenes de televisión, se necesita calcular la cantidad de datos transmitidos por imagen y la velocidad total de transmisión, considerando el número de puntos por línea, líneas por imagen, niveles de brillo, y la tasa de imágenes por segundo.