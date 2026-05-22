# El Marco Legal y la Estructura del "Relato"

## Pablo Garcia Rojas

## 1º DESARROLLO DE APLICACIONES MULTIPLATAFORMA

## FECHA: 15/05/2026

[**1\. Análisis de necesidades	3**](#análisis-de-necesidades)

[2\. ¿Qué problema de la empresa resolvemos con Guacamole y Docker?	3](#¿qué-problema-de-la-empresa-resolvemos-con-guacamole-y-docker?)

[3\. ¿Por qué elegimos esta solución y no conectar directamente por RDP a cada máquina?	3](#¿por-qué-elegimos-esta-solución-y-no-conectar-directamente-por-rdp-a-cada-máquina?)

[**2. Estimación de Costes de Infraestructura 3**](#análisis-de-necesidades)

## 

## 1.  Análisis de necesidades

   

**2.  ¿Qué problema de la empresa resolvemos con Guacamole y Docker?**

   Podemos resolver problemas como el acceso y el orden a las máquinas de nuestra empresa. Antes nos conectabamos por RDP directamente al equipo entonces hacia que tuviéramos problemas como los siguientes: demasiados puertos abiertos, credenciales repartidas por todas partes, cero control sobre quién entra a qué máquina y una experiencia de uso nada unificada.  
     
   Para solucionarlo, usamos Apache Guacamole en docker. Apache Guacamole hace que el usuario solo entra a una ulr y desde ahi el usuario pueda acceder a todas las máquinas que tenga permitidas. No necesita instalar clientes RDP, ni guardar credenciales, ni abrir puertos en cada equipo. Todo pasa por un único punto controlado.  
     
   Usando Apache Guacamole podemos ganar diferentes ámbitos como:  
* **Mayor centralización total:** un único portal para todas las conexiones remotas.  
* **Más seguridad:** dejamos de exponer puertos RDP máquina por máquina; solo se expone Guacamole.  
* **Gestión de permisos más seria:** usuarios, grupos y accesos controlados desde un único sitio.  
* **Ahorro de tiempo y recursos:** menos configuraciones, menos mantenimiento, menos problemas.  
* **Escalabilidad:** al estar en Docker, podemos actualizar, mover o duplicar el servicio sin complicaciones.  
  


**3. ¿Por qué elegimos esta solución y no conectar directamente por RDP a cada máquina?**

Porque es inseguro, difícil de gestionar y también es muy poco práctico. Cada máquina tendría que abrir su puerto, cada técnico tendría que guardar credenciales y no habría forma real de auditar accesos. Además, cada cliente RDP funciona distinto según el sistema operativo, lo que complica el soporte.

Con Guacamole todo se estandariza: una sola interfaz, una sola puerta de entrada y un control centralizado de quién accede a qué.


## 2. Estimación de Costes de Infraestructura
En la siguiente imagen, se muestra el presupuesto realizado en una hoja de calculo, realizado con diferentes funciones de esta como pueden ser calcular el subtotal, IVA, etc...
![ImagenPresupuesto](../assets/presupuestoInfraestructura.png)
