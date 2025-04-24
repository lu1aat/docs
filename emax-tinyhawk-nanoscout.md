# EMAX Tinyhawk Nanoscout (espanol)

## Especificaciones del Tinyhawk Nanoscout

*   **Distancia entre ejes:** 65mm
*   **Tamaño máximo (L*An*Al):** 84x84x35mm
*   **Peso (excluyendo batería):** 23g
*   **Motor:** 08015(22000KV)
*   **Hélice:** Avia 31mm
*   **FC (Controlador de Vuelo):** STM32F411 (100MHz) - Es parte de la placa AIO. Firmware stock: Betaflight 4.4.3 target STM32F411SX1280. Soporta protocolos D-Shot y otros.
*   **ESC (Controlador Electrónico de Velocidad):** Integrado 4-en-1-6A-8 bit. Corriente continua: 6A. Corriente pico: 6.7A (10S). MCU: EFM8BB21F16G(50MHz). Firmware: Bluebird / JESC_SH90_48_2_3.HEX. Es parte de la placa AIO.
*   **Receptor:** Onboard ELRS (2.4G) receiver (SPI communication). RF chip: SX1280 (SPI support). Protocolo: CRSF. Es parte de la placa AIO.
*   **Cámara:** RunCam Nano 3. Proporciona visuales analógicos.
*   **Transmisión de Imagen (VTX):** EMAX-32-bit open-source simulation image transmission. Frecuencia: 5.8G 40CH. Potencia RF: 25mW/100mW/200mW/400mW. Soporta protocolo Smartaudio. Antena: Omnidireccional, ganancia 2db. Es parte de la placa AIO.
*   **Batería (Stock):** 1S HV 320mAh(EM2.0). El conector EM 2.0 ofrece mejor eficiencia y durabilidad.

## Hélices y Motores Brushless

### Hélices del Tinyhawk Nanoscout

Las hélices tienen dos direcciones de rotación: en sentido horario (CW) y en sentido antihorario (CCW). Al comprar un set, se deben adquirir 2 CW y 2 CCW. Las hélices rotan a lo largo del borde romo.

*   **Instalación de Hélices:** Alinea los 3 ejes de la hélice con los 3 ejes del motor, apoyando detrás del motor. Presiona las palas de la hélice con la mano hasta que estén al ras con el eje del motor.
    *   **Advertencia:** La instalación incorrecta puede causar que el Tinyhawk Nanoscout no vuele correctamente y se vuelva incontrolable. Verifica cuidadosamente que la dirección de la hélice sea correcta. La falta de apoyo detrás del motor puede provocar la rotura del frame. ¡Asegura precauciones de seguridad al instalar hélices!
*   **Remoción de Hélices:** Usa una herramienta pequeña (como una llave hexagonal de 1.5mm o un destornillador pequeño) para presionar entre el metal en la parte inferior del motor y el Tinyhawk Nanoscout. Sostén las palas de la hélice con los dedos hasta que la hélice salte del motor.
    *   **Advertencia:** Solo retira las palas de la hélice cuando las reemplaces por unas nuevas. ¡Practica precauciones de seguridad al remover hélices y usar herramientas!

### Motor Brushless del Tinyhawk Nanoscout

El modelo del motor brushless es: **08015 (22000KV)**.
Las terminales del conector entre el motor y la placa de control principal son: **P = 1.25mm, conector plug 1x3p**.

## VTX (Transmisor de Video)

El Tinyhawk Nanoscout utiliza un transmisor de imagen analógico de código abierto EMAX de 32 bits.
*   **Frecuencia:** 5.8G 40 canales.
*   **Potencia RF:** 25mW/100mW/200mW/400mW.
*   **Voltaje/Corriente de entrada:** 5V.
*   **Protocolo Soportado:** Smartaudio.
*   **Interfaz de señal de alimentación:** P=0.8mm, 1x4p.
*   **Actualización de Firmware:** Soporta actualización de firmware VTX a través del controlador de vuelo.
*   **Antena:** Omnidireccional, ganancia 2db.
*   **Interfaz de Antena:** IPEX 1ª generación o soldadura.
El SmartAudio del transmisor de video analógico está en UART2 TX.

## AIO (Todo en Uno)

La placa Tinyhawk Nanoscout PLUS-AIO integra un receptor ELRS (2.4G), un ESC BlHeliSuite de 6A y un controlador de vuelo F411 en una sola placa.

### Parte del Controlador de Vuelo (FC)

*   **MCU (Microcontrolador):** STM32F411CEU6 (100MHz).
*   **Giroscopio y Acelerómetro (MPU):** ICM42688 (conexión SPI).
*   **Superposición de Caracteres (OSD):** AT74569E (conexión SPI).
*   **Voltaje de entrada:** 1S.
*   **Voltaje de salida (BEC):** 5V@2A, 3.3V@1A.
*   **Firmware (Betaflight):** EMAX_TINYHAWKF4SX1280.
*   **Protocolos de ajuste eléctrico soportados:** Shot150, D-Shot300, D-Shot600, Multishoth, OneShot125, PWM.
*   **Luces de color RGB programables:** Soporta.
*   **Puertos seriales:** 2 (UART1, UART2).
*   **Protocolo SBUS:** Soporte (UART1).

### Parte del Ajuste Eléctrico (ESC)

*   **Corriente continua:** 6A.
*   **Corriente pico:** 6.7A (10S).
*   **MCU (Microcontrolador):** EFM8BB21F16G (50MHz).
*   **Voltaje de entrada:** 1S.
*   **Firmware (Bluebird):** JESC_SH90_48_2_3.HEX.

### Parte del Receptor

*   **Chip RF:** SX1280 (soporte SPI).
*   **Banda de frecuencia:** 2400-2480MHz.
*   **Protocolo:** CRSF.

## Operación Básica de Vuelo

### Inicio Rápido de la Aeronave

Remueve la batería e insértala en el compartimiento de la batería de la aeronave. Conecta la interfaz de energía de la aeronave a la interfaz de la batería. Verás las luces roja y azul de la aeronave parpadeando. Coloca la aeronave en el suelo en una posición nivelada y espera unos 3 segundos. La luz indicadora roja de la aeronave parpadeará y luego se mantendrá encendida fijamente, mientras que la luz indicadora azul parpadeará y luego se apagará. Esto indica que la inicialización de la aeronave está completa y se ha emparejado exitosamente con el control remoto.

### Verificación del Estado de Despegue

Con el drone conectado a la batería y emparejado (luz roja fija, azul apagada):
*   Si usas el interruptor "ARM" en tu control remoto (típicamente AUX 1 es el interruptor ARM en la configuración pre-configurada), muévelo a la posición que **desbloquea** (ARM) el drone. Observarás que las hélices de la aeronave giran a baja velocidad.
*   Mueve el interruptor "ARM" a la posición **BLOQUEADO** (ULOCK). Las hélices de la aeronave dejarán de girar.

### Control de la Aeronave

Tras desbloquear la aeronave para que los motores giren a baja velocidad:
*   Usa el joystick izquierdo para controlar el ascenso y descenso (Throttle).
*   Usa el joystick izquierdo para controlar la rotación izquierda y derecha (Yaw).
*   Usa el joystick derecho para controlar la inclinación de nariz arriba y abajo (Pitch).
*   Usa el joystick derecho para controlar la inclinación izquierda y derecha (Roll).
Se recomienda priorizar la práctica de estas operaciones básicas, dominando estos controles fundamentales y familiarizándote con la sensibilidad de los joysticks.

### Vuelo Visual

Primero, asegúrate de que el vuelo sea dentro de la línea de visión (sin usar gafas FPV). Enciende el Tinyhawk Nanoscout y colócalo en una habitación segura y abierta. Enciende el Tinyhawk Nanoscout y usa el joystick izquierdo para subir el acelerador a la posición de flotar. Comienza intentando mantener una altitud estable. Usa tus pulgares en los joysticks izquierdo y derecho para controlar el pitch y roll del Tinyhawk Nanoscout y mantener un vuelo normal. Practica varias veces para adquirir habilidad.

*   **Nota:** Después de aterrizar la aeronave de manera segura en el suelo, mueve el interruptor "ARM" en tu control remoto a la posición ULOCK para bloquear la aeronave.

### Vuelo FPV

Una vez que tengas una comprensión básica de las operaciones de vuelo, puedes intentar volar con gafas FPV. Asegúrate de que el Tinyhawk Nanoscout y las gafas FPV estén en el mismo canal VTX. Elige un área espaciosa y segura. Basado en tu experiencia volando en modo normal, controla el acelerador para mantener un vuelo lento y nivelado. Este enfoque facilita el aprendizaje del vuelo FPV.

El OSD (On-Screen Display) en las gafas FPV muestra la transmisión de video de la cámara del Tinyhawk Nanoscout. El OSD muestra información importante como el tiempo de vuelo y el voltaje de la batería. Durante el vuelo, monitorea siempre estos números para entender el voltaje restante de la batería. El Tinyhawk Nanoscout puede volar por hasta **4 minutos** con la batería incluida. Cuando la batería alcance **3.2 voltios**, aterriza el Tinyhawk Nanoscout. Evita que el voltaje de la batería caiga por debajo de 3.2 voltios, ya que podría dañar la batería.

*   **Advertencia:** Mantén una altitud controlada durante el vuelo. Evita mover los joysticks agresivamente, ya que esto puede hacer que la aeronave sea difícil de controlar. No permitas que el voltaje de la batería caiga por debajo de 3.2 voltios. Activa la función de pitido del motor si pierdes de vista la aeronave para ayudar a localizarla.

## Modos de Vuelo

El Tinyhawk Nanoscout tiene tres modos de vuelo, generalmente asignados a un interruptor de 3 posiciones (AUX 2 en la configuración por defecto):

1.  **Simple Mode (Modo Estabilizado ARM):** Este es un modo de control de vuelo simple donde el ángulo máximo del Tinyhawk Nanoscout está limitado durante el vuelo para ayudar a restringir la velocidad y facilitar el vuelo. En este modo, el control de la aeronave se basa en la actitud. Las entradas de pitch y roll desde el control remoto ajustan los ángulos de pitch y roll de la aeronave. Por ejemplo, una inclinación de 20 grados del joystick corresponderá a una inclinación de roll de 20 grados del Tinyhawk Nanoscout.
2.  **Intermediate Mode (Modo Semi-estabilizado Horizon):** Este modo tiene un límite de ángulo más alto para un vuelo más rápido, con control de actitud similar. La principal diferencia es que en el punto final de pitch y roll, la aeronave se volteará hacia esa dirección.
3.  **Advanced Mode (Modo Manual Acro):** Este modo te da control completo de la aeronave. No hay límites de ángulo; el control se basa en la velocidad (rate-based). Esto significa que las entradas de control desde el joystick establecen una velocidad de rotación alrededor del eje descrito.

## Carga de la Batería de la Aeronave

Una sola batería puede volar aproximadamente 4 minutos. Cuando la pantalla OSD en tus gafas FPV muestre "LOW VOL", indica que la batería está baja y necesita cargarse.

*   **Pasos para cargar:**
    1.  Saca el cargador e inserta la batería en la interfaz de batería del cargador.
    2.  Inserta el enchufe USB del cargador en un adaptador de corriente USB (se recomienda 5V-1A).
    3.  La luz indicadora del cargador estará **verde fijo** durante la carga, **apagada** cuando la carga esté completa y **parpadeando** si no se detecta batería.

## Funciones Avanzadas y Configuración

### Calibración de Nivelación de la Aeronave

Después de múltiples despegues y aterrizajes, los datos del giroscopio de la aeronave pueden desviarse, causando problemas de actitud durante el vuelo. En este punto, puedes calibrar los datos del giroscopio de la aeronave con los siguientes pasos:
1.  Conecta el controlador de vuelo a la computadora usando un cable de datos Type-C y asegúrate de que esté en una posición nivelada.
2.  Abre el software Betaflight Configurator.
3.  Haz clic en "Calibrate Accelerometer" (Calibrar Acelerómetro) y luego haz clic en "Reset Z-axis" (Reiniciar Eje Z).
4.  Verifica en el software Betaflight Configurator si el estado de la aeronave vuelve a la normalidad. Un mensaje indicará que la calibración del acelerómetro ha sido completada.

### Re-emparejamiento (Binding) de la Aeronave con el Control Remoto

El emparejamiento se refiere al proceso de conexión entre el receptor y el control remoto. Un receptor solo puede emparejarse con un control remoto.

*   **Tinyhawk Nanoscout Entra en Modo de Emparejamiento (Binding):** Enciende el Tinyhawk Nanoscout. Después de que se inicie, presiona y mantén presionado el **botón Bind** para poner el Tinyhawk Nanoscout en modo de emparejamiento. La luz indicadora azul del controlador de vuelo del Tinyhawk Nanoscout parpadeará y luego se volverá fija, indicando que está en modo de emparejamiento. Este botón Bind es el mismo botón BOOT y el único botón en la placa del controlador de vuelo.

*   **Otros Métodos de Emparejamiento para Tinyhawk Nanoscout:**
    *   **Primer Método (CLI en Betaflight):** Puedes poner el receptor en modo de emparejamiento usando un comando en el Betaflight Configurator. Abre Betaflight Configurator, ve a la pestaña CLI. Escribe el comando: `bind_rx` y presiona Enter. El receptor entrará en modo de emparejamiento.
    *   **Segundo Método (GUI en Betaflight):** También puedes usar el Betaflight Configurator para iniciar el modo de emparejamiento directamente desde la sección del receptor. Abre Betaflight Configurator, ve a la pestaña Receiver (Receptor). Haz clic en "Bind Receiver" (Emparejar Receptor). El receptor entrará en modo de emparejamiento.

*   **Salir del Modo de Emparejamiento:** Desconecta la batería del Tinyhawk Nanoscout para apagarlo y salir del modo de emparejamiento.

### Cambio de Clave de Emparejamiento para el Controlador de Vuelo

Puedes cambiar la clave de emparejamiento del controlador de vuelo a través del Betaflight Configurator.
*   **Cambio de Clave de Emparejamiento del Controlador de Vuelo a través de Betaflight Configurator:** Introduce el siguiente comando en la línea de comando de Betaflight Configurator (usando `0, 1, 2, 3, 4, 5` como ejemplo para la clave). Debes guardar los cambios. Presiona Enter. Espera a que el controlador de vuelo se reinicie y vuelva a entrar en Betaflight Configurator. Esto indica que la modificación de la clave de emparejamiento fue exitosa.

### Ajuste de la Configuración de Modos de Vuelo

El Tinyhawk Nanoscout viene con configuraciones de modos pre-configuradas. En la configuración típica, AUX 1 es el interruptor ARM (Desbloqueo), AUX 2 es para los modos de vuelo (Acro, Horizon, Angle) y AUX 4 es para el Beeper. Si deseas modificar estas configuraciones, localiza los canales correspondientes para los interruptores en el software Betaflight Configurator, realiza los cambios deseados y luego guarda y reinicia.

### Cambio de Configuración de OSD (On-Screen Display)

El Tinyhawk Nanoscout viene pre-configurado con los ajustes de OSD. Para cambiar los ajustes de OSD usando el software Betaflight Configurator:
1.  En Betaflight Configurator, localiza la pestaña OSD.
2.  Configura la superposición de la pantalla OSD según los caracteres e información que deseas mostrar en tus gafas FPV.
3.  Haz clic en "Save" (Guardar) para aplicar los cambios.
4.  Después de guardar, reinicia el sistema para implementar los ajustes de OSD actualizados.

### Cambio de Configuración de VTX (Transmisor de Video)

El Tinyhawk Nanoscout viene con la configuración de VTX por defecto de R:4:25mW. Puedes modificar la configuración del VTX de dos maneras:

*   **Modificación de la Configuración del VTX Usando Betaflight Configurator:**
    1.  Abre el software Betaflight Configurator.
    2.  Localiza la pestaña VTX.
    3.  Modifica los parámetros deseados como canal, frecuencia, potencia y habilita el bloqueo de baja potencia.
    4.  Haz clic en "Save" (Guardar) para aplicar los cambios.
    5.  Después de guardar, reinicia el sistema para implementar los ajustes de VTX actualizados.
    *   **Nota:** La función de bloqueo de baja potencia asegura que el VTX opere a baja potencia hasta que se desbloquee. Una vez desbloqueado, opera al nivel de potencia configurado.

*   **Cambio de Configuración del VTX Usando el OSD de las Gafas de Video:** El Tinyhawk Nanoscout está equipado con SmartAudio, que ya está configurado. El SmartAudio está en UART2 TX. Con el Tinyhawk Nanoscout encendido:
    1.  Sigue las instrucciones en pantalla para entrar al menú de configuración principal.
    2.  Centra el acelerador, mueve el stick izquierdo a la izquierda y el pitch hacia arriba (THROTTLE MID + YAW LEFT + PITCH UP) para entrar al menú de ajuste de parámetros OSD.
    3.  En la interfaz del menú, usa pitch (arriba/abajo) para navegar y seleccionar opciones de menú. Mueve el cursor a "FEATURES" y luego empuja el stick de roll (derecha) para entrar al siguiente menú.
    4.  Usa pitch (arriba/abajo) para mover el cursor a "VTX SA". Empuja el stick de roll (derecha) para entrar al menú de configuración VTX.
    5.  En el menú VTX SA, puedes configurar BAND, CHAN y POWER. Usa el stick de pitch (arriba/abajo) para mover el cursor y seleccionar las opciones de VTX deseadas.
    6.  Una vez que los parámetros estén configurados, mueve el cursor a "SET" y empuja el stick de roll (derecha) para entrar en "SET" y seleccionar "YES". Empuja el stick de roll (derecha) nuevamente para guardar la configuración.
    7.  En el menú VTX SA, mueve el cursor a "CONFIG" para entrar al menú. Mueve el cursor a "PIT FMODE" y luego empuja el stick de roll (derecha) para apagar la potencia del VTX (modo pit).