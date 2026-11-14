# spec.md · Simulador de inventario EOQ

## 1. Objetivo y problema que resuelve
Que estudiantes de Gestión de Operaciones entiendan cómo la cantidad de pedido y el punto de reorden afectan costos y quiebres de stock cuando la demanda varía.

## 2. Usuarios
Estudiantes de pregrado de Ingeniería Industrial, en clase o en casa, sin instalar nada.

## 3. Funcionalidades
1. Parámetros editables: demanda anual, costo de pedir, costo de mantener, lead time y variabilidad de la demanda.
2. Cálculo y muestra de la EOQ y el punto de reorden sugerido.
3. Simulación de 52 semanas con demanda aleatoria y gráfico del nivel de inventario.
4. Indicadores: costo total, número de pedidos y semanas con quiebre de stock.
5. Botón "nueva simulación" para comparar escenarios.

## 4. Fuera de alcance
Múltiples productos, descuentos por volumen, guardar resultados en servidor.

## 5. Datos de entrada y salida
Entrada: 5 parámetros numéricos. Salida: EOQ, punto de reorden, gráfico e indicadores.

## 6. Diseño de la interfaz
Una página: panel de parámetros a la izquierda, gráfico y tarjetas de indicadores a la derecha.

## 7. Criterios de aceptación
- Dado D=12000, S=50, H=2, cuando calculo, entonces la EOQ mostrada es 775 (redondeada).
- Dado cualquier cambio de parámetro, cuando pulso "nueva simulación", entonces el gráfico se actualiza en menos de 1 segundo.
- Dado un punto de reorden muy bajo, cuando simulo, entonces el indicador de quiebres es mayor que cero y se resaltan esas semanas.
- La página funciona abriendo un solo archivo HTML, sin conexión a servidor.
