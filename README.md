# Proyecto
Poyecto SmartPark
SmartPark IoT — Sistema de Monitoreo y Control de Estacionamiento

Prototipo IoT desarrollado y simulado en Wokwi que automatiza el control de acceso y monitorea en tiempo real la disponibilidad de plazas de estacionamiento mediante telemetría MQTT.

Componentes y función de cada elemento:

Microcontrolador ESP32: Unidad central de procesamiento. Lee las distancias de los sensores, calcula el total de plazas disponibles, controla el accionamiento de la barrera, actualiza la pantalla local y envía los estados a la nube vía Wi-Fi mediante el protocolo MQTT.

Sensores Ultrasónicos HC-SR04 (2 unidades): Detectan la presencia o ausencia de vehículos en cada cajón de estacionamiento midiendo la distancia mediante ondas ultrasónicas.

Servomotor SG90: Actuador mecánico que funciona como barrera de acceso automatizada, permitiendo el ingreso únicamente cuando existen plazas disponibles y cerrándose cuando el estacionamiento está lleno.

Pantalla LCD 16x2 con módulo I2C: Interfaz visual local en la entrada del estacionamiento que informa al conductor la cantidad de espacios libres y el estado de acceso en tiempo real.

Broker MQTT (broker.hivemq.com): Intermediario de mensajería en la nube que recibe y distribuye los datos publicados por el ESP32 a través de los tópicos smartpark/cajon1, smartpark/cajon2 y smartpark/plazas.

Dashboard Web (dashboard.html): Interfaz de monitoreo remoto suscrita a los tópicos MQTT que visualiza en tiempo real el estado individual de cada cajón, el conteo de plazas libres, el estado de la barrera, el historial de ocupación y el registro de eventos.


ENLACE AL PROYECTO EN WOKWI:
https://wokwi.com/projects/480260152782420993

ENLACE A MQTT WEBSOCKET:
https://www.hivemq.com/demos/websocket-client/
