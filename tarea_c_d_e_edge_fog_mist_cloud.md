# Tarea (c+d+e) · Edge, Fog, Mist y Cloud (DAW 1º)

## 🅲 Tarea C — Edge Computing y relación con Cloud
**Definición (3–5 líneas):**
Edge Computing es una forma de procesar datos cerca del lugar donde se generan, como sensores o dispositivos IoT.
En vez de enviar toda la información a la nube, parte del trabajo se hace en el propio dispositivo o cerca de él.
Así se consigue una respuesta más rápida y se usan menos datos de Internet.

**Relación Edge ↔ Cloud (5–8 líneas):**
Edge y Cloud trabajan juntos.
El Edge se encarga de las tareas rápidas y urgentes, como tomar decisiones en el momento.
La Cloud se utiliza para guardar datos, analizarlos con más detalle y gestionarlo todo desde un punto central.
El Edge envía solo la información importante a la Cloud.
De esta forma se mejora el rendimiento y se reduce la latencia.
Es muy común en sistemas IoT.

**Ejemplo real:**
En una fábrica con sensores, el Edge detecta si una máquina falla y actúa al momento.
Después, los datos se envían a la Cloud para analizar fallos a largo plazo.
**Fuentes oficiales (mín. 2):**
- IBM
- Google Cloud: https://docs.cloud.google.com/distributed-cloud/edge/latest/docs?hl=es

## 🅳 Tarea D — Fog vs Mist (niveles y zonas de aplicación)
**Definición Fog (2–4 líneas):**
Fog Computing es una capa entre el Edge y la Cloud.
Se encarga de procesar datos de varios dispositivos cercanos antes de enviarlos a la nube.
Ayuda a reducir el tráfico de datos y mejora la velocidad.

**Definición Mist (2–4 líneas):**
Mist Computing es el nivel más cercano al sensor.
El propio sensor hace pequeñas tareas como filtrar datos o detectar eventos simples.
Solo envía información cuando es necesario.

**Esquema (ASCII o Mermaid recomendado):**
```
+------------+
|  Sensores  |
+------------+
       |
     (Mist)
       |
+------------+
|    Edge    |
+------------+
       |
     (Fog)
       |
+------------+
|   Cloud    |
+------------+
```


**Zonas de aplicación (qué hace cada capa):**
- Mist → Filtra datos simples y ahorra energía.
- Edge → Toma decisiones rápidas en tiempo real.
- Fog → Junta datos de varios Edge y los procesa.
- Cloud → Guarda datos y hace análisis grandes.
## 🅴 Tarea E — Ventajas de la Cloud en sistemas conectados
Incluye mínimo 3 ventajas (recomendado 5), con explicación + ejemplo.

1) Ventaja: Escalabilidad
   Explicación: La Cloud permite aumentar o reducir recursos fácilmente.
   Ejemplo: Una aplicación puede crecer sin comprar nuevos servidores.

2) Ventaja: Acceso desde cualquier lugar
   Explicación: Los datos están disponibles desde cualquier dispositivo con Internet.
   Ejemplo: Controlar una casa inteligente desde el móvil.

3) Ventaja: Almacenamiento de datos
   Explicación: La Cloud puede guardar muchos datos durante mucho tiempo.
   Ejemplo: Guardar datos de sensores durante años.

4) Ventaja: Menor coste
   Explicación: No hace falta comprar servidores propios.
   Ejemplo: Se paga solo por lo que se usa cada mes.
   
5) Ventaja: Seguridad y copias de seguridad automáticas

   Explicación: La Cloud suele incluir medidas de seguridad avanzadas y realiza copias de seguridad automáticas de los datos. Esto protege la información frente a fallos del hardware, pérdidas o ataques.
   Ejemplo: Si un sensor industrial falla y borra datos, la información ya está respaldada en la Cloud y se puede recuperar fácilmente.   

**Fuente oficial (mín. 1):**
- Microsoft Azure

## 📚 Fuentes (enlaces oficiales)
(Recopila aquí todos los enlaces oficiales usados)
Google Cloud
https://cloud.google.com/distributed-cloud/edge

Microsoft Azure
https://learn.microsoft.com/azure/architecture/guide/architecture-styles/edge-computing

Red Hat
https://www.redhat.com/en/topics/edge-computing

Intel
https://www.intel.com/content/www/us/en/edge-computing/overview.html

Cisco
https://www.cisco.com/c/en/us/solutions/what-is-edge-computing.html
