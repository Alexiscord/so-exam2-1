### Examen 2
**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Nombre:** Alexis Córdoba.  
**Código:** A00232548.  
**Correo:** alexiscord1@gmail.com  

### Descripción
En este documento se muestra en una serie de pasos, la manera en que se crean servicios a partir de Scripts y la manera de controlar algunos recursos de la CPU gracias a CPUQuote y CPUShares. Esto, ayudando a la creación y entendimiento del concepto de asignación de recursos.

### Actividades

## Primera Actividad:  
1.  En primer lugar creamos los Scripts que usaermos. En este caso son contador.sh y laHora.sh. Estos están ubicados en el directorio /root/parcialDos/Scripts y sus respectivos códigos son:  
![contador.sh](images/2_contador.png)  
![laHora.sh](images/3_lahora.png)  



```
# adduser operativos
# passwd operativos
# su operativos
```

Realice una prueba de concepto empleando systemd y el recurso de control CPUQuota teniendo en cuenta los requerimientos que se describen a cotinuación. Incluya evidencias del funcionamiento de lo solicitado.

 * Las pruebas se realizaran sobre un solo núcleo de la CPU
 * Se deben ejecutar dos procesos
 * Cada proceso debe poder acceder solo al 50% de la CPU
 * Cuando uno de los procesos se cancela, el que continua ejecutándose no debe acceder a mas del 50% de la CPU
4.  Realice una prueba de concepto empleando systemd y el recurso de control CPUShares teniendo en cuenta los requerimientos que se describen a continuación. Incluya evidencias del funcionamiento de lo solicitado (30%):
 * Las pruebas se realizaran sobre un solo núcleo de la CPU
 * Se deben ejecutar dos procesos
 * Uno de los procesos tendrá el 25% de la CPU mientras que el otro tendrá el 75% de la CPU
 * Cuando uno de los procesos se cancela, el que continua ejecutándose debe poder llegar al 100% de la CPU
5. Por medio de las evidencias obtenidas en los puntos anteriores y de fuentes de consulta en Internet, elabore las definiciones para los grupos de control CPUQuota y CPUShares, además concluya acerca de cuando es preferible usar un recurso de control sobre otro (20%)
6. El informe debe ser entregado en formato pdf a través del moodle y el informe en formato README.md debe ser subido a un repositorio de github. El repositorio de github debe ser un fork de https://github.com/ICESI-Training/so-exam2 y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (10%)  

### Referencias
https://docs.docker.com/engine/admin/resource_constraints/#configure-the-realtime-scheduler
https://www.freedesktop.org/software/systemd/man/systemd.resource-control.html
