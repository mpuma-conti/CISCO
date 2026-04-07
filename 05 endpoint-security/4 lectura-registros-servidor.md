# 4.2.9 Lab - Lectura de registros del servidor

En algunas situaciones, lo aconsejable es monitorear archivos de registro a medida que se les escriben las entradas de registro. El comando `tail -f` es muy útil para esos casos.

**a. Utilice `tail -f` para monitorear activamente el contenido del archivo `/var/log/syslog`:**

```bash
analyst@secOps ~$ sudo tail –f /home/analyst/lab.support.files/logstash-tutorial.log
```

### Archivos de registro y Syslog

Debido a su importancia, es común concentrar archivos de registro en una computadora de monitoreo. **Syslog** es un sistema diseñado para permitir que los dispositivos envíen sus archivos de registro a un servidor centralizado, que se conoce como servidor syslog. Los clientes se comunican con un servidor syslog por medio del protocolo syslog. Syslog es comúnmente utilizado y admite prácticamente todas las plataformas informáticas.

#### /var/log/syslog

La herramienta `journalctl` interpreta y muestra las entradas de registro almacenadas anteriormente en los archivos de registro binario de journal.

```bash
analyst@secOps ~$ journalctl
```