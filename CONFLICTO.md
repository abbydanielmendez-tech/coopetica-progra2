# Documentación del conflicto de fusión

## 1. ¿Qué archivo entró en conflicto y por qué?

El conflicto ocurrió en README.md durante una práctica realizada por Abby. Modifiqué la misma línea de dos formas distintas en mis ramas trabajo-abby y practica-conflicto. Al ejecutar git merge practica-conflicto desde trabajo-abby, Git no pudo elegir automáticamente cuál conservar.

## 2. ¿Qué mostraba Git exactamente?

El archivo mostraba este bloque:

```text
    <<<<<<< HEAD
    <!-- Practica de fusion: revisar diagramas -->
    =======
    <!-- Practica de fusion: revisar documentacion -->
    >>>>>>> practica-conflicto
```

## 3. ¿Cómo resolví el conflicto?

Combiné las dos ideas, eliminé los marcadores del README y dejé esta línea:

```html
<!-- Practica de fusion: revisar diagramas y documentacion -->
```

Después agregué el archivo con git add y confirmé la resolución mediante un commit.

## 4. ¿Qué haríamos distinto para evitar un conflicto similar?

Nos pondríamos de acuerdo sobre qué sección del README editará cada integrante. Antes de trabajar, revisaríamos e incorporaríamos los cambios compartidos a nuestras ramas y compararíamos las diferencias antes de integrarlas. Esto reduce la posibilidad de modificar la misma línea de formas distintas.