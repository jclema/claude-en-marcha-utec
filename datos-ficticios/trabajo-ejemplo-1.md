# Informe: Boticas Andinas (estudiante ficticio A)

El problema principal es que Boticas Andinas pide siempre la misma cantidad, sin considerar que la demanda de suero oral y paracetamol sube entre junio y agosto. En los datos, la demanda de suero oral en julio de 2025 fue cerca de 30% mayor que el promedio anual.

Clasificación ABC: los productos A son paracetamol y suero oral, B ibuprofeno y alcohol en gel, y C mascarillas y vitamina C.

Para el suero oral calculé una demanda anual aproximada de 4300 unidades. Con S = 120 y H = 0.25 x 4.5 = 1.125, la EOQ es raíz de (2 x 4300 x 120 / 1.125) = 958 unidades. El punto de reorden con lead time de 10 días es 4300/365 x 10 = 118 unidades, más un stock de seguridad de 60 unidades para la temporada alta.

Recomiendo usar un pronóstico estacional, revisar la EOQ cada trimestre y medir el número de días sin stock por local cada mes, con una meta de cero quiebres en productos A.
