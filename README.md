# ApiNotaVenta
Integración de Software Propio con ERP Factronica

Por medio de esta API se puede realizar la conexión entre su software propio con el ERP Factronica.
<br>En este caso utilizaremos Prestashop como plataforma comercial.
<br>El Objetivo es que al momento de ser Enviado un Pedido en Prestashop de forma instantanea se genere una Nota de Venta en el Sistema ERP Factronica.
<br>Para realizar este proceso se requiere un Token y Datos del Pedido.
<br>Los datos deben ser enviados a una Url Especifica por medio de datos POST[.
<br>Las variables requeridas se encuentran en el manual en el siguiente apartado.
<br>
<br>Pasos a seguir:
<br>Generar el envio de datos POST.
<br>
<br>Variables requeridas:
<pre>
<BR>// TOKEN DE ACCESO AL SISTEMA
<br>$_POST["TOKEN"]="7XW453SJ339F";
<BR>// ID DEL PEDIDO CREADO EN PRESTASHOP
<br>$_POST["PEDIDO"]="23";
<BR>// ID CLIENTE
<br>$_POST["CLIENTE_ID"]="2";
<BR>// CANTIDAD DE ITEMS DEL PEDIDO
<br>$_POST["ITEMS_CANTIDAD"]="2";
<BR>// ------ ITEM 1 --------
<BR>// ITEM 1 CODIGO
<br>$_POST["ITEMS_CODIGO_1"]="22040";
<BR>// ITEM 1 NOMBRE ITEM
<br>$_POST["ITEMS_NOMBRE_1"]="ZOOM DUAL INFRAROJO WEST7";
<BR>// ITEM 1 CANTIDAD
<br>$_POST["ITEMS_CANTIDAD_1"]="4";
<BR>// ITEM 1 UNITARIO
<br>$_POST["ITEMS_PRECIO_1"]="2500";
<BR>// ITEM 1 SUBTOTAL
<br>$_POST["ITEMS_SUBTOTAL_1"]="10000";
<BR>// ------ ITEM 2 --------
<BR>// ITEM 2 CODIGO
<br>$_POST["ITEMS_CODIGO_2"]="13031";
<BR>// ITEM 2 NOMBRE ITEM
<br>$_POST["ITEMS_NOMBRE_2"]="CAMARA PRO Z20";
<BR>// ITEM 2 CANTIDAD
<br>$_POST["ITEMS_CANTIDAD_2"]="5";
<BR>// ITEM 2 UNITARIO
<br>$_POST["ITEMS_PRECIO_2"]="5000";
<BR>// ITEM 2 SUBTOTAL
<br>$_POST["ITEMS_SUBTOTAL_2"]="10000";
</pre>

El envío de datos debe apuntar a la siguiente url:
<pre>
http://190.107.177.113/~apifactronica/index.php
</pre>
