coopetica-progra2
Modelado del Dominio CoopeTica R.L. - BIS04 Programación II

Universidad Latina de Costa Rica
Integrantes:
Integrante 1: Abby Daniel Mendez - GitHub: @abbydanielmendez-tech
Integrante 2: Jeremy Angulo Ovares - GitHub: @JeremAng

1. Descripción del Dominio
CoopeTica R.L. es una cooperativa costarricense de ahorro y crédito que actualmente gestiona sus operaciones con hojas de cálculo dispersas. Este sistema de modelado permite a la organización administrar toda la información que corresponde a sus clientes, sus diversas cuentas financieras (Ahorros, Cheques y Certificados a Plazo) junto con un historial de transacciones (depósitos, retiros, cobro de comisiones y aplicación de intereses) de manera inmutable, garantizando que en ningún momento el saldo quedará desbalanceado.
Resumen del Modelo:
1. Asociado: Representa al cliente. Guarda cédula, nombre, teléfono, correo, fecha de ingreso y estado.
2. Cuenta:Clase base con número de cuenta, saldo, fecha de apertura y estado.
3. CuentaAhorro: Especialización de cuenta con tasa de interés de ahorro y comisión de mantenimiento.
4. CuentaCorriente: Especialización de cuenta con tasa de interés corriente y comisión por transacción.
5.CertificadoPlazo: Especialización con tasa de interés a plazo, plazo en meses y fecha de vencimiento.
6. Movimiento: Registra la fecha/hora, el tipo de movimiento, el monto y el saldo resultante después de cada transacción.

2. Justificación del Modelo

Clases escogidas y criterio de selección:
Asociado: Necesaria para encapsular los datos de la persona física y gestionar su estado (activo/inactivo) sin eliminar su historial.
Cuenta, CuentaAhorro, CuentaCorriente y CertificadoPlazo: Se diferenciaron debido a que cada producto calcula intereses y cobra comisiones bajo reglas de negocio distintas. El Certificado a Plazo, además, añade restricciones de retiro antes de la fecha de vencimiento.
Movimiento: Indispensable para auditar el historial financiero de cada cuenta con la fecha, hora y saldo resultante.
Elementos descartados del enunciado:"Hojas de cálculo dispersas": Se descartó por ser parte de la problemática previa de la cooperativa y no un objeto del sistema.
"Tipos de movimiento" (Depósito, Retiro, Intereses, Comisión): Se modeló como un atributo de tipo `String` dentro de la clase `Movimiento` en lugar de una clase separada, ya que no poseen métodos ni comportamientos complejos independientes.
"Reporte de movimientos": Se descartó como entidad del dominio porque corresponde a una operación o función de consulta, no a un objeto persistente.


3. Bitácora de Uso de Inteligencia Artificial

Consulta 1: Se consultó a una herramienta de IA sobre el criterio para diferenciar cuándo un sustantivo del enunciado debe modelarse como una clase o como un atributo. La explicación indicó que si no tiene comportamiento propio ni atributos adicionales, debe ser un atributo. Se usó este criterio para mantener `tipoMovimiento` como un atributo dentro de `Movimiento`.
Uso directo: No se utilizó inteligencia artificial para la elaboración del diagrama UML ni para redactar la justificación técnica del modelo.
