# dem-module
Modulo para sistema de distribuidores en Odoo

Este modulo es el encargado de las siguientes funciones:
- Cada que hay cambio de precio o stock se envia un post al ws
- Una acción en cada producto que envia un post con la info del producto
- Una acción en cada contacto que envia sus datos:
- Endpoint que recibe un post para generar orden

Se debe definir un parner "dummy" en company para que el modulo lo asigne a una orden en caso de que no cuente con id.
Hay que realizar una autenticacion con cookies antes de crear una orden por cuestiones de seguridad.
El endpoint a donde se mandarán los posts se define en la compañia
El endpoint que recibe la orden está en algun lugar del código
