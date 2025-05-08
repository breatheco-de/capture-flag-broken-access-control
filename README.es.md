# Customer Service - Descubrimiento de rutas y cracking de contraseñas

En este laboratorio deberás explorar una aplicación web alojada en un servidor Apache, identificar accesos indebidos y descifrar contraseñas cifradas para obtener acceso a información sensible. Aprenderás a:

- Detectar rutas ocultas mediante fuerza bruta
- Reconocer un caso de Broken Access Control
- Analizar y descifrar contraseñas MD5
- Simular inicios de sesión para usuarios reales

<how-to-start>
   
## 🌱 Cómo iniciar este laboratorio

Sigue las siguientes instrucciones para comenzar:

1. **Descarga la máquina virtual** desde este [enlace](https://storage.googleapis.com/cybersecurity-machines/customer-service-lab.ova).
2. **Importa la máquina** en tu gestor de virtualización preferido (VirtualBox, VMware, etc.).
3. Una vez iniciada la máquina, ¡ya puedes comenzar con el laboratorio!
</how-to-start>


## 📄 Instrucciones

Estás frente al sitio web de una empresa de servicios de hosting, dominios y VPS llamada **Customer Service**. Tu misión es descubrir si existe alguna sección del sistema que esté mal protegida o expuesta indebidamente.


1. **Descubre la dirección IP de la máquina.**
   - La máquina está conectada a la misma red que tú, pero su IP no ha sido proporcionada.
   - Usa herramientas como `nmap`, `netdiscover` o `arp-scan` para escanear la red.

2. **Explora el sitio web visible.**
   - Abre tu navegador y visita la IP detectada.
   - Analiza la página principal, intenta detectar si hay directorios o rutas ocultas.

3. **Realiza fuerza bruta de rutas.**
   - Utiliza herramientas como `gobuster`, `dirb` o `ffuf` para descubrir recursos ocultos.
   - El objetivo es encontrar un panel oculto.

4. **Analiza los usuarios y contraseñas.**
   - Utiliza herramientas como `john`, `hashcat` o servicios online para descifrar los hashes.

5. **Simula el inicio de sesión como distintos usuarios.**


**Recuerda:** los sistemas no siempre fallan por fallos complejos. A veces, basta con omitir un control básico de acceso.

¡Buena suerte!