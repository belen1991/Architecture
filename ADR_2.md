# Título:
Usar una arquitectura basada en eventos para garantizar un flujo en paralelo de la solicitud de pedidos.
# Estado:
Propuesta
# Contexto:
Esta solución va a garantizar el rendimiento de las peticiones al momento de realizar un pedido, ya que el flujo es sencillo siempre y cuando se tenga definido el identificador del pedido en curso, y esto se lo puede realizar en paralelo de acuerdo al número de usuarios que realicen solicitudes.
# Decisión:
La arquitectura basada en eventos nos va a permitir generar un Message Broker, para comunicarnos mediante mensajes y solicitudes de acuerdo a los eventos, de esta manera somos capaces de enviar solicitudes que van a ser atendidas en el siguiente procesador cuando le llegue un mensaje, la respuesta a este mensaje será enviada por un nuevo canal de mensajería al usuario final, y así recibirá actualizaciones sobre su pedido según el operador cambie los estados. Se puede garantizar con esto un óptimo tiempo de respuesta y una gran capacidad de crecimiento y actualización de funcionalidades.
# Consecuencia:
No podemos garantizar la consistencia de los datos, ya que es posible que alguno de los mensajes se pueda perder en el transcurso del envío, por lo que tampoco se puede garantizar la recuperación de la información perdida. El tiempo de implementación de esta solución requiere más tiempo de desarrollo que el establecido y una inversión más grande de capital.
