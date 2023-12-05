## PROCESOS

- ps: Muestra información de los procesos activos.
    
    1. ps a
    2. pa au
    3. ps aux 
    4. ps -C nano
    5. ps -U "usuario"

- top: Proporciona una visión en tiempo real de los procesos que consumen más recursos,como la CPU y la memoria.

- Ordenar:
    1. shift M (memoria)
    2. shift P (CPU)
    3. shift T (tiempo)
    4. shift N (PID)
    5. f (seleccionar que campos quiero en pantalla)
    6. top -b -n 3 > top.info(mandar informacion del top a un archivo)
    7. top -n 3 -o %CPU -b | head -n 17(10 procesos que consumen mas CPU, durante 3 periodos)

- htop: Similar a top, pero con una interfaz más visual y funciones adicionales, como la
capacidad de desplazarse y filtrar procesos de manera más intuitiva.

- atop: Registra e informa de la actividad de todos los procesos del servidor.Toma datos desde el momento en el que se inicia.
    1. systemctl status atop
    2. /etc/default/atop (LOGINTERUAL=600, 60)
    3. /var/log/atop_FECHA
    4. atop -r /var/log/
    atop_FECHA 
    5. g, m , c, d, t, T, b
## MEMORIA
- free: Muestra la cantidad de memoria libre y utilizada en el sistema.
- df: Muestra el espacio utilizado y disponible en los sistemas de archivos montados.

    1. df -h (muestra lo que esta montado)
    2. df -hT (aparece el tipo de fichero)
    3. lsblk ()
- du: Muestra el espacio ocupado por un fichero o directorio.
- iostat: Se utiliza para rastrear los problemas de rendimiento de los dispositivos de
almacenamiento.
    1. iostat "nombre disco"
    2. iostat "nombre disco" "segundos" "nº veces">"nombre archivo" copiar algun archvio a el directorio /dev/null
    3. cat "nombre archivo"
## RED
- tcpdump: Analiza el tráfico que circula por la red.
    1. tcpdump -n -i "nombre tarjeta"
    2. tcpdump -n -i "nombre tarjeta" net "red+mascara"
- tcptrack: Nos muestra las conexiones establecidas, su origen, destino, estado, el tiempo
de iddle y la velocidad de transferencia.
- iptraf: Intercepta paquetes en la red y muestra información sobre el tráfico.
- bandwidthd: una herramienta específica de monitorización del ancho de banda
## PUERTOS

- netstat (ss): Muestra las conexiones activas de una computadora, tanto entrantes como
salientes.