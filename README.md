# CAMBIAR HOSTNAME
# Cómo Cambiar el Hostname en Ubuntu 22.04  

El **hostname** es el nombre que identifica tu computadora en una red. En Ubuntu 22.04, se puede cambiar de varias maneras.  

---

## 1. Ver el Hostname Actual  

Para ver el **hostname** actual del sistema, ejecuta:  

```bash
hostnamectl
```
2. Cambiar el Hostname Temporalmente
Para cambiar el hostname sin necesidad de reiniciar, usa:

```
sudo hostnamectl set-hostname nuevo-nombre
```
Nota: Este cambio es temporal y se perderá después de reiniciar el sistema.

4. Cambiar el Hostname de Forma Permanente
Para cambiarlo de manera permanente, sigue estos pasos:

Paso 1: Cambiar el Hostname con hostnamectl
Ejecuta el siguiente comando:
```
sudo hostnamectl set-hostname nuevo-nombre
```
Reemplaza nuevo-nombre con el hostname deseado.

Paso 2: Editar el Archivo Hosts
Abre el archivo /etc/hosts con un editor de texto, como nano:
```
sudo nano /etc/hosts
```
Busca la línea que contiene el hostname anterior y cámbiala por el nuevo nombre:
127.0.0.1    localhost
127.0.1.1    nuevo-nombre
Guarda los cambios y cierra el editor (CTRL + X, luego Y y Enter).

Paso 3: Reiniciar el Sistema
Para aplicar los cambios de forma permanente, reinicia tu servidor con:
```
sudo reboot
```
4. Verificar el Cambio
Después de reiniciar, confirma que el hostname se ha actualizado correctamente ejecutando:
```
hostnamectl
```
Si todo se realizó correctamente, verás el nuevo hostname reflejado en la salida del comando
