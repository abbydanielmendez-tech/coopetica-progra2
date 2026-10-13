# \#coopetica-progra2

\## Integrantes

\-Abby Daniel Mendez Alvarez- GitHub:@abbydanielmendez-tech

\-Jeremy Angulo Ovares- GitHub:@JeremyAng



\## Descripción del proyecto



Este proyecto presenta el diseño inicial de un sistema para la cooperativa CoopeTica. Su propósito es organizar la información de los asociados, sus cuentas y los movimientos de dinero.



El sistema contempla cuentas de ahorro, cuentas corrientes y certificados a plazo. Permite representar depósitos, retiros, intereses y comisiones, además de consultar las cuentas de un asociado y sus movimientos entre fechas.



Esta entrega incluye el diseño de clases y el trabajo colaborativo mediante Git y GitHub. Todavía no incluye una aplicación funcional en Java.





\## Diagrama de clases — avance



\### AsociadoCooperativa



!\[Clase AsociadoCooperativa](diagramas/AsociadoCooperativa.png)



\### Cuenta

!\[Clase cuenta](diagramas/Cuenta.png)



\### Movimiento

!\[Clase Movimiento](diagramas/Movimiento.png)



\### Cuenta de ahorro

!\[Clase CuentaAhorro](diagramas/CuentaAhorro.png)



\### Cuenta Corriente

!\[Clase CuentaCorriente](diagramas/CuentaCorriente.png)



\###Certificado a plazo

!\[Clase certificadoPlazo](diagramas/CertificadoPlazo.png)



\### Nota de diseño

Las consultas devuelven información sin modificar los saldos. La consulta de cuentas incluye su estado abierto o cerrado. La consulta de movimientos incluye las fechas inicial y final del período solicitado. Cuenta representa las características comunes de los tres productos; en esta etapa se presentan sus clases sin dibujar relaciones.







\## Justificación de las clases



\- \*\*AsociadoCooperativa:\*\* representa a la persona afiliada. Guarda sus datos personales y su estado. Permite desactivarla sin eliminar su historial.



\- \*\*Cuenta:\*\* representa los datos y las operaciones comunes de las cuentas, como su número, saldo, fecha de apertura, estado, depósitos, retiros y consulta de movimientos.



\- \*\*Movimiento:\*\* representa el registro de una operación. Guarda la fecha y hora, el tipo de movimiento, el monto y el saldo posterior.



\- \*\*CuentaAhorro:\*\* representa el producto de ahorro y contempla la tasa de interés y la comisión que le correspondan.



\- \*\*CuentaCorriente:\*\* representa el producto de cuenta corriente. Aunque comparte operaciones con la cuenta de ahorro, permite distinguir las condiciones de intereses y comisiones de este producto.







\## Bitácora de uso de IA



\- Consultamos a ChatGPT la diferencia entre clases, atributos y métodos. Sus explicaciones nos ayudaron a entender cómo representar los datos y las acciones del sistema



\- Consultamos cómo utilizar Git y GitHub para crear ramas, guardar cambios y subir las imágenes al repositorio.



\- Utilizamos un borrador generado por ChatGPT para organizar el README y redactar la justificación del modelo.


<!-- Practica de fusion: revisar diagramas y documentacion -->
