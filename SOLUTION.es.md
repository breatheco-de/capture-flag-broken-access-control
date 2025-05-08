# Customer Service

Este laboratorio pone a prueba la capacidad del alumno para descubrir rutas ocultas en aplicaciones web, analizar contraseñas cifradas y detectar accesos indebidos, logrando así comprender:

- Reconocimiento de rutas web no documentadas (Broken Access Control)
- Análisis de contraseñas MD5 y uso de diccionarios para descifrarlas
- Simulación de inicio de sesión en formularios inseguros
- Lectura condicional de flags a partir de credenciales específicas


## Especificaciones de la máquina 🖥️

- **Sistema:** Ubuntu Server sin GUI
- **Servidor web:** Apache
- **Ruta del sitio principal:** `/var/www/html/index.html`
- **Ruta oculta vulnerable:** `/var/www/html/admin/admin.php`
- **Tipo de vulnerabilidad:** Broken Access Control (ruta no protegida)
- **Formulario:** login con comparación de hashes MD5 en PHP

- **Usuarios disponibles (con contraseña en MD5):**

    | Nombre | Apellido   | Email                     | Contraseña en texto plano |
    |--------|------------|---------------------------|----------------------------|
    | Romeo  | Rodriguez  | romeo@fake.4geeks         | starwars                   |
    | Alex   | Wilson     | alexwilson@fake.4geeks    | sunshine                   |
    | Elisa  | Smith      | elismith94@fake.4geeks    | bubbles                    |
    | John   | Logan      | jlogan@fake.4geeks        | g0dmode                    |

- **Flag visible solo si se inicia sesión correctamente como `john`:**

    ```text
    4GEEKS{Th1s_1s_p455w0rd_cr4ck!ng}
    ```

### Credenciales de la máquina

```bash
servername: customer-service-lab
username: student
password: 4geeks-lab
```

## Pasos esperados por el alumno

1. **Realiza reconocimiento de red para identificar la máquina.**
   - Utiliza herramientas como `nmap`, `netdiscover` o `arp-scan`.
   - Debe detectar una IP con el puerto **80 (HTTP)** abierto.

2. **Accede al sitio web desde el navegador.**
   - Introduce la IP detectada en el navegador para cargar la landing page pública.

3. **Descubre rutas ocultas mediante fuerza bruta.**
   - Usa herramientas como `gobuster`, `ffuf` o `dirb` para detectar `/admin/`.

4. **Accede al archivo vulnerable `admin.php`.**
   - Revisa el código del formulario y la tabla de usuarios con contraseñas MD5.

5. **Descifra los hashes de contraseña.**
   - Utiliza `john`, `hashcat`, `crackstation` o diccionarios como `rockyou.txt`.

6. **Simula inicios de sesión.**
   - Prueba loguear como cada usuario hasta lograr acceso exitoso.

7. **Identifica la flag al loguearte como `john`.**
   - Solo ese usuario mostrará la flag al ingresar la contraseña correcta.
