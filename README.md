# dan-ms-usuario
repositorio microservicio usuarios

**Reglas de negocio**
* Cuando se da de alta un Cliente, se debe indicar al menos una Obra con su Tipo de Obra y la informaciòn de usuario y clave para crear el usuario.
* Para dar de alta un cliente hay que consumir un servicio "riesgo BCRA" que retorna la informaciòn de la situación crediticia de un cliente (http://www.bcra.gov.ar/BCRAyVos/Preg-Frec-Qu%C3%A9-significa-cada-situaci%C3%B3n-en-la-Central-de-deudores-considerando-s%C3%B3lo-la-mora.asp ) . Solo se puede dar de alta un cliente para comprar ONLINE, si y solo si la situación crediticia es de TIPO 1 o 2.
* Para dar de baja un cliente, no se puede eliminar si ya ha realizado algun pedido, por lo que en ese caso, debe agregar un atributo, "fechaBaja" y asignarle una fecha. Todos los clientes activos son aquellos que no tienen fechaBaja (o es null).
* Cuando consulta clientes solo puede consultar 
