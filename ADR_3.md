# Título:
Utilizar módulos sencillos para desplegar un monolito que resuelva la solicitud de pedidos.
# Estado:
Propuesta
# Contexto:
Se requiere una aplicación sencilla y liviana que cumpla con los requisitos de realizar un pedido y recibir notificaciones, para lo cual se sugiere levantar una arquitectura monolito por modelos que va a ser realizada en un corto tiempo y que puede ser fácilmente mantenible por un grupo pequeño de desarrolladores, lo que no provocará costos innecesarios.
# Decisión:
Dividir cada requerimiento en un módulo específico que cumpla su función, para realizar un pedido, receptar un pedido, actualizar un pedido y notificar la información del estado del pedido. Como tenemos un solo repositorio donde tenemos todos los modelos incluidos para interactuar, tenemos una comunicación directa y un repositorio de datos verás, que siempre va a reflejar el estado real de la información.
# Consecuencia:
No se puede garantizar la reacción ante fallos, y si algo falla en el proceso, probablemente todo el sistema se va a ver afectado hasta que se resuelva el problema. No se puede garantizar una concurrencia alta y tampoco un crecimiento ordenado y mejorado para agregar nuevas características.