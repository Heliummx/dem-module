# dem-module
Modulo para sistema de distribuidores en Odoo

Este modulo es el encargado de las siguientes funciones:
- Cada que hay cambio de precio o stock se envia un post al ws
- Una acción en cada producto que envia un post con la info del producto
- Una acción en cada contacto que envia sus datos:
- Endpoint que recibe un post para generar orden. Lo que recibe el post es el contenido del webhook de shopify "Order payment" más el id del distribuidor ()

Se debe definir un parner "dummy" en company para que el modulo lo asigne a una orden en caso de que no cuente con id. /create_dem_order

You have to call the endpoint /web/session/authenticate with specific data (the data base and the user login and password ), this endpoint return s a json with a key "session_id", this session_id key must be used to call the /create_sale_order_connector with the data to create the sale order.

El endpoint a donde se mandarán los posts se define en la compañia.

El endpoint que recibe la orden está en algun lugar del código.
