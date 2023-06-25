# Título:
Usar servicios específicos para atender y recibir pedidos en un tiempo corto y con un presupuesto justo.
# Estado:
Propuesta
# Contexto:
Esta decisión está basada en la portabilidad, el presupuesto y el tiempo de requerimiento, para cumplir con este objetivo los servicios se pueden realizar sin mayor complicación y con la ayuda de varios desarrolladores, contemplando los servicios de manera desatendida, para que sean capaces de funcionar sin dependencia de los demás servicios. Esto nos permite instalar la solución de manera fácil y sencilla en los dispositivos que así lo requieran sin preocuparnos por los demás servicios a ser instalados.
# Decisión:
Se utilizarán servicios específicos, uno para que los usuarios puedan autenticarse y realizar sus pedidos, otro para que los operadores puedan atender y preparar los pedidos, y uno específico para enviar actualizaciones del pedido y notificaciones. Esta solución nos permite garantizar una solución portable a un costo razonable y en el tiempo ideal, adicional a esto el crecimiento a futuras características o funcionalidades queda totalmente abierto. Se puede agregar un Api Layer para garantizar la seguridad de la información que viaja en los servicios, ya que es información sensitiva del cliente.
# Consecuencias:
Al tener una arquitectura basada en servicios, no vamos a poder garantizar un rendimiento óptimo dada una concurrencia considerablemente grande, también la velocidad puede disminuir dependiendo de la comunicación entre los servicios. No se puede garantizar un manejo oportuno frente a fallas inesperadas por la arquitectura elegida. 
