## 驴Qu茅 es la Infraestructura como c贸digo (IaC)? 馃搩

Infraestructura como c贸digo es un m茅todo de aprovisionamiento y gesti贸n de infraestructura IT y servicios a trav茅s del uso de c贸digo fuente, sustituyendo el procedimiento est谩ndar de operaci贸n. B谩sicamente consiste en tratar los servidores, bases de datos, redes y otros elementos de infraestructura como si fuera software. Este c贸digo facilita el despliegue de esta infraestructura de un modo r谩pido, seguro y consistente.

## Beneficios de IaC

### Rapidez 鉁旓笍
El dise帽o de una infraestructura con c贸digo permite agilizar de manera significativa el despliegue posterior de manera r谩pida y segura. IaC permite desplegar toda una infraestructura que podr铆a llevar horas o d铆as enteros ejecutando tan s贸lo un script en cuesti贸n de unos pocos minutos.

Si bien es cierto que el desarrollo del c贸digo que permitir谩 el despliegue de la infraestructura puede ser igual de costoso que un despliegue inicial, aporta la ventaja de que es reutilizable por lo que se pueden importar snippets que automaticen partes y cuando la biblioteca de recursos est谩ndar ya est谩 poblada se reduce mucho el tiempo de desarrollo, esto sin contar que adem谩s en caso de tener que levantar varios entornos de la misma arquitectura es donde se demuestra realmente la rapidez de IaC ya que una vez desarrollado permite replicarlo en cuesti贸n de minutos.

### Automatizaci贸n 鉁旓笍
La automatizaci贸n en la replicaci贸n de infraestructura es otro punto interesante de la IaC. Es posible tomar el dise帽o de una infraestructura con c贸digo para que sea replicada exactamente igual en otro entorno 煤nicamente modificando los par谩metros que se proporcionan durante la creaci贸n.

Adem谩s las herramientas de IaC normalmente ofrecen APIs que permiten automatizar la ejecuci贸n del IaC integr谩ndola con herramientas de 鈥淐ontinuos Delivery鈥? (Jenkins, Drone) para integrar dentro de los ciclos de pruebas la creaci贸n de un entorno sobre el que ejecutar las pruebas y destruirlo a la finalizaci贸n.

Adicionalmente nos ofrece la posibilidad de automatizar la creaci贸n de entornos de Disaster Recovery, si los tiempos de RTO y RPO nos lo permiten podemos tener simplemente en una localizaci贸n alternativa las copias de seguridad de los datos y recrear la infraestructura solo en caso de desastre, con lo que se reduce al m铆nimo el coste de un entorno DR.

### Minimizaci贸n de riesgos 鉁旓笍
Otra de las ventajas que ofrece IaC es la minimizaci贸n de riesgos. Cuando se despliega infraestructura manualmente es inevitable que en alg煤n momento se cometa un error. IaC permite hacer las comprobaciones necesarias antes de desplegar para que exista una consistencia, minimizando al m谩ximo los errores anteriormente comentados. Aunque un despliegue de un servidor, por poner un ejemplo, es barato, el tiempo del ingeniero que lo despliega no lo es tanto. De modo que si se comete un error de base, como la creaci贸n de una red con datos incorrectos, y posteriormente hay que crear una cantidad concreta de servidores sobre esta red, ser谩 necesario dar marcha atr谩s a todo el proceso.

### Actualizaciones controladas y rollbacks 鉁旓笍
Los sistemas de IaC permiten la actualizaci贸n de los stacks proporcionando un fichero actualizado y pidiendo que en lugar de crear un  nuevo stack procede a actualizar uno existente, el sistema se encarga de comprar el fichero con los recursos actualmente desplegados y se encarga de hacer 煤nicamente los cambios necesarios.

Si los ficheros descriptivos los tenemos en un sistema de control de versiones adem谩s podremos hacer rollback f谩cilmente a versiones anteriores y comparar los cambios entre una versi贸n y otro.
