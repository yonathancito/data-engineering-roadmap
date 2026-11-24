La empresa recibe los siguientes registros:

id_venta	cliente	ciudad	fecha	importe
1001	Ana	Arequipa	09/11/2026	250
1002	Luis	Lima	2026-11-09	400
1003	Pedro	Cusco	09/11/2026	-100
1001	Ana	Arequipa	09/11/2026	250
1004	María	Lima	2026-11-09	350

Tenemos problemas:
- Fechas con formatos diferentes.
- Un importe negativo que necesita validación.
- Un registro posiblemente duplicado.

Ejercicio 3.1 — Bronze
Responde:
1. ¿Guardarías los cinco registros?
Si los guardaria
2. ¿Modificarías las fechas?
No
3. ¿Eliminarías el registro duplicado?
No
4. ¿Por qué es importante conservar la información original?
Para poder hacer un rastreo si es necesario sobre todo cuando hay una auditoria

Ejercicio 3.2 — Silver
Supongamos que la empresa determina que:
- Las fechas deben estar en formato YYYY-MM-DD.
- No se permiten importes negativos en ventas.
- Los duplicados deben identificarse y tratarse.

Diseña cómo debería quedar la información validada.

id_venta	cliente	ciudad	fecha	importe
1001	Ana	Arequipa	2026-11-09	250
1002	Luis	Lima	2026-11-09	400
1004	María	Lima	2026-11-09	350

Indica qué sucede con el registro de importe negativo y el duplicado. No los elimines sin explicar tu decisión.

Registro 1001: se identifica como posible duplicado. Se verifica su origen y se determina si corresponde a una duplicación accidental. Si se confirma, se conserva una sola ocurrencia en Silver y se registra la incidencia para auditoría.

correccion, en el caso de importe negativo lo primero que se tiene que hacer el llevarlo a datos cuarentena para poder averiguar el porque de esa negatividad y una vez descubierto poder o corregirlo o eliminarlo

**Tratamiento de registros no válidos:**

- Registro 1003: se envía a cuarentena porque presenta un
  importe negativo. Se investigará si corresponde a una
  devolución u otro evento legítimo.

- Registro 1001 duplicado: se identifica como posible
  duplicado. Se verifica su origen antes de determinar
  si corresponde a una duplicación accidental. Si se
  confirma, se conserva una sola ocurrencia en Silver
  y se registra la incidencia para auditoría.

Ejercicio 3.3 — Gold
La gerencia quiere conocer las ventas por ciudad.

Diseña una tabla que contenga:
- Ciudad.
- Número de ventas válidas.
- Importe total vendido.

ciudad      Numero de ventas validas    importe total
Arequipa            1                       250
Lima                2                       750
Cusco               0                        0
