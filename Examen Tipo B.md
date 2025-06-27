# Examen Tipo B

## Sección 1: JOINs (5 problemas)

**Obtener el nombre del empleado, su sucursal y el departamento donde trabaja.**

Solucion

```
SELECT e.nombre AS empleado, s.nombre AS sucursal, d.nombre AS departamento
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN municipio m ON s.municipioid = m.id
JOIN departamento d ON m.depid = d.id;
```

Resultado Esperado

```
+-------------------+------------------+-----------------+
| empleado          | sucursal         | departamento    |
+-------------------+------------------+-----------------+
| Laura Rodríguez   | Sucursal Zona 1  | Tolima          |
| Ana Pérez         | Sucursal Zona 1  | Tolima          |
| Sofía Gómez       | Sucursal Zona 1  | Tolima          |
| Pedro Pérez       | Sucursal Zona 1  | Tolima          |
| Ana Gómez         | Sucursal Zona 1  | Tolima          |
| Laura Torres      | Sucursal Zona 1  | Tolima          |
| Carlos Torres     | Sucursal Zona 1  | Tolima          |
| Pedro Rodríguez   | Sucursal Zona 1  | Tolima          |
| Pedro Torres      | Sucursal Zona 1  | Tolima          |
| Laura Torres      | Sucursal Zona 1  | Tolima          |
| Laura Rodríguez   | Sucursal Zona 2  | Cundinamarca    |
| Luis Torres       | Sucursal Zona 2  | Cundinamarca    |
| Luis Rodríguez    | Sucursal Zona 2  | Cundinamarca    |
| Ana Pérez         | Sucursal Zona 2  | Cundinamarca    |
| Ana Gómez         | Sucursal Zona 2  | Cundinamarca    |
| Sofía Torres      | Sucursal Zona 2  | Cundinamarca    |
| Sofía Gómez       | Sucursal Zona 2  | Cundinamarca    |
| Luis Rodríguez    | Sucursal Zona 2  | Cundinamarca    |
| Laura Pérez       | Sucursal Zona 2  | Cundinamarca    |
| Sofía Gómez       | Sucursal Zona 2  | Cundinamarca    |
| Sofía Pérez       | Sucursal Zona 3  | Antioquia       |
| Pedro Gómez       | Sucursal Zona 3  | Antioquia       |
| Carlos Gómez      | Sucursal Zona 3  | Antioquia       |
| Ana Gómez         | Sucursal Zona 3  | Antioquia       |
| Sofía Rodríguez   | Sucursal Zona 3  | Antioquia       |
| Sofía Rodríguez   | Sucursal Zona 3  | Antioquia       |
| Pedro Gómez       | Sucursal Zona 3  | Antioquia       |
| Laura Gómez       | Sucursal Zona 3  | Antioquia       |
| Carlos Pérez      | Sucursal Zona 3  | Antioquia       |
| Carlos Pérez      | Sucursal Zona 3  | Antioquia       |
| Luis Pérez        | Sucursal Zona 4  | Atlántico       |
| Laura Gómez       | Sucursal Zona 4  | Atlántico       |
| Carlos Rodríguez  | Sucursal Zona 4  | Atlántico       |
| Sofía Torres      | Sucursal Zona 4  | Atlántico       |
| Laura Pérez       | Sucursal Zona 4  | Atlántico       |
| Laura Gómez       | Sucursal Zona 4  | Atlántico       |
| Sofía Rodríguez   | Sucursal Zona 4  | Atlántico       |
| Carlos Torres     | Sucursal Zona 4  | Atlántico       |
| Luis Torres       | Sucursal Zona 4  | Atlántico       |
| Pedro Rodríguez   | Sucursal Zona 4  | Atlántico       |
| Sofía Torres      | Sucursal Zona 5  | Atlántico       |
| Ana Gómez         | Sucursal Zona 5  | Atlántico       |
| Sofía Torres      | Sucursal Zona 5  | Atlántico       |
| Luis Pérez        | Sucursal Zona 5  | Atlántico       |
| Luis Rodríguez    | Sucursal Zona 5  | Atlántico       |
| Luis Gómez        | Sucursal Zona 5  | Atlántico       |
| Laura Torres      | Sucursal Zona 5  | Atlántico       |
| Laura Torres      | Sucursal Zona 5  | Atlántico       |
| Carlos Rodríguez  | Sucursal Zona 5  | Atlántico       |
| Luis Rodríguez    | Sucursal Zona 5  | Atlántico       |
| Sofía Rodríguez   | Sucursal Zona 6  | Valle del Cauca |
| Luis Rodríguez    | Sucursal Zona 6  | Valle del Cauca |
| Luis Gómez        | Sucursal Zona 6  | Valle del Cauca |
| Ana Torres        | Sucursal Zona 6  | Valle del Cauca |
| Pedro Rodríguez   | Sucursal Zona 6  | Valle del Cauca |
| Luis Pérez        | Sucursal Zona 6  | Valle del Cauca |
| Ana Rodríguez     | Sucursal Zona 6  | Valle del Cauca |
| Laura Pérez       | Sucursal Zona 6  | Valle del Cauca |
| Pedro Rodríguez   | Sucursal Zona 6  | Valle del Cauca |
| Ana Gómez         | Sucursal Zona 6  | Valle del Cauca |
| Carlos Torres     | Sucursal Zona 7  | Cundinamarca    |
| Laura Gómez       | Sucursal Zona 7  | Cundinamarca    |
| Luis Gómez        | Sucursal Zona 7  | Cundinamarca    |
| Sofía Pérez       | Sucursal Zona 7  | Cundinamarca    |
| Sofía Rodríguez   | Sucursal Zona 7  | Cundinamarca    |
| Pedro Gómez       | Sucursal Zona 7  | Cundinamarca    |
| Ana Pérez         | Sucursal Zona 7  | Cundinamarca    |
| Ana Pérez         | Sucursal Zona 7  | Cundinamarca    |
| Sofía Torres      | Sucursal Zona 7  | Cundinamarca    |
| Ana Rodríguez     | Sucursal Zona 7  | Cundinamarca    |
| Carlos Pérez      | Sucursal Zona 8  | Cundinamarca    |
| Ana Torres        | Sucursal Zona 8  | Cundinamarca    |
| Ana Rodríguez     | Sucursal Zona 8  | Cundinamarca    |
| Luis Rodríguez    | Sucursal Zona 8  | Cundinamarca    |
| Luis Torres       | Sucursal Zona 8  | Cundinamarca    |
| Sofía Gómez       | Sucursal Zona 8  | Cundinamarca    |
| Laura Rodríguez   | Sucursal Zona 8  | Cundinamarca    |
| Ana Gómez         | Sucursal Zona 8  | Cundinamarca    |
| Ana Torres        | Sucursal Zona 8  | Cundinamarca    |
| Luis Pérez        | Sucursal Zona 8  | Cundinamarca    |
| Sofía Gómez       | Sucursal Zona 9  | Nariño          |
| Luis Gómez        | Sucursal Zona 9  | Nariño          |
| Sofía Rodríguez   | Sucursal Zona 9  | Nariño          |
| Carlos Rodríguez  | Sucursal Zona 9  | Nariño          |
| Sofía Gómez       | Sucursal Zona 9  | Nariño          |
| Ana Rodríguez     | Sucursal Zona 9  | Nariño          |
| Carlos Pérez      | Sucursal Zona 9  | Nariño          |
| Luis Torres       | Sucursal Zona 9  | Nariño          |
| Laura Pérez       | Sucursal Zona 9  | Nariño          |
| Pedro Torres      | Sucursal Zona 9  | Nariño          |
| Carlos Torres     | Sucursal Zona 10 | Cundinamarca    |
| Sofía Rodríguez   | Sucursal Zona 10 | Cundinamarca    |
| Sofía Torres      | Sucursal Zona 10 | Cundinamarca    |
| Sofía Pérez       | Sucursal Zona 10 | Cundinamarca    |
| Ana Gómez         | Sucursal Zona 10 | Cundinamarca    |
| Pedro Rodríguez   | Sucursal Zona 10 | Cundinamarca    |
| Pedro Torres      | Sucursal Zona 10 | Cundinamarca    |
| Luis Rodríguez    | Sucursal Zona 10 | Cundinamarca    |
| Luis Pérez        | Sucursal Zona 10 | Cundinamarca    |
| Sofía Gómez       | Sucursal Zona 10 | Cundinamarca    |
+-------------------+------------------+-----------------+
```

**Listar los clientes junto con el nombre del país en el que residen.**

Solucion

```
SELECT c.nombre AS cliente, p.nombre AS pais
FROM clientes c
JOIN municipio m ON m.id = c.municipioid
JOIN departamento d ON d.id = m.depid
JOIN pais p ON p.id = d.paisid;
```



```
+----------------------+----------+
| cliente              | pais     |
+----------------------+----------+
| Valentina Mendoza    | Colombia |
| Andrés Mendoza       | Colombia |
| Daniela López        | Colombia |
| Andrés Vargas        | Colombia |
| Camila García        | Colombia |
| Andrés Romero        | Colombia |
| Valentina Hernández  | Colombia |
| David Vargas         | Colombia |
| Valentina López      | Colombia |
| Julián López         | Colombia |
| Sofía Martínez       | Colombia |
| Andrés Mendoza       | Colombia |
| Julián Hernández     | Colombia |
| Daniela Vargas       | Colombia |
| Daniela Hernández    | Colombia |
| Sofía Rodríguez      | Colombia |
| Valentina García     | Colombia |
| Camila Vargas        | Colombia |
| Daniela López        | Colombia |
| Sofía López          | Colombia |
| Julián García        | Colombia |
| David García         | Colombia |
| Andrés Mendoza       | Colombia |
| Daniela Vargas       | Colombia |
| David Rodríguez      | Colombia |
| Daniela García       | Colombia |
| Andrés García        | Colombia |
| David Romero         | Colombia |
| Julián Romero        | Colombia |
| Julián Mendoza       | Colombia |
| David Martínez       | Colombia |
| Andrés Rodríguez     | Colombia |
| David Rodríguez      | Colombia |
| Juan Rodríguez       | Colombia |
| Sofía López          | Colombia |
| Camila López         | Colombia |
| Camila López         | Colombia |
| Andrés García        | Colombia |
| Julián Rodríguez     | Colombia |
| Julián Martínez      | Colombia |
| Julián Mendoza       | Colombia |
| Andrés López         | Colombia |
| David Romero         | Colombia |
| Daniela García       | Colombia |
| Daniela Mendoza      | Colombia |
| Daniela García       | Colombia |
| Valentina Mendoza    | Colombia |
| Andrés Vargas        | Colombia |
| David García         | Colombia |
| Sofía Hernández      | Colombia |
| Valentina Mendoza    | Colombia |
| Andrés Hernández     | Colombia |
| Camila Hernández     | Colombia |
| David Martínez       | Colombia |
| Valentina Martínez   | Colombia |
| Daniela Mendoza      | Colombia |
| Andrés Martínez      | Colombia |
| Sofía Mendoza        | Colombia |
| Daniela Hernández    | Colombia |
| Daniela García       | Colombia |
| Sofía Martínez       | Colombia |
| Juan Hernández       | Colombia |
| David García         | Colombia |
| Daniela Rodríguez    | Colombia |
| Daniela Martínez     | Colombia |
| Daniela Romero       | Colombia |
| Daniela Martínez     | Colombia |
| Andrés Romero        | Colombia |
| Andrés Romero        | Colombia |
| Valentina García     | Colombia |
| Juan Vargas          | Colombia |
| Andrés López         | Colombia |
| Andrés López         | Colombia |
| Julián Vargas        | Colombia |
| Julián Mendoza       | Colombia |
| David García         | Colombia |
| David Hernández      | Colombia |
| Daniela Mendoza      | Colombia |
| Juan Vargas          | Colombia |
| Julián García        | Colombia |
| Camila Rodríguez     | Colombia |
| Valentina Vargas     | Colombia |
| Camila Vargas        | Colombia |
| Sofía Hernández      | Colombia |
| Andrés López         | Colombia |
| Andrés Hernández     | Colombia |
| Andrés Romero        | Colombia |
| Valentina Rodríguez  | Colombia |
| Valentina López      | Colombia |
| Camila Vargas        | Colombia |
| Valentina López      | Colombia |
| Camila Romero        | Colombia |
| Julián Rodríguez     | Colombia |
| David Mendoza        | Colombia |
| Daniela López        | Colombia |
| Camila Mendoza       | Colombia |
| Sofía García         | Colombia |
| Valentina Romero     | Colombia |
| Daniela Martínez     | Colombia |
| Andrés Vargas        | Colombia |
| Valentina López      | Colombia |
| Julián Martínez      | Colombia |
| Daniela García       | Colombia |
| Camila Rodríguez     | Colombia |
| Andrés Mendoza       | Colombia |
| Juan López           | Colombia |
| Juan Romero          | Colombia |
| David García         | Colombia |
| Camila Romero        | Colombia |
| Sofía Martínez       | Colombia |
| David López          | Colombia |
| Julián Mendoza       | Colombia |
| Camila Hernández     | Colombia |
| Sofía Romero         | Colombia |
| Juan Hernández       | Colombia |
| Andrés Vargas        | Colombia |
| Valentina Mendoza    | Colombia |
| Andrés Romero        | Colombia |
| Sofía Vargas         | Colombia |
| Julián Romero        | Colombia |
| Camila Vargas        | Colombia |
| Daniela Vargas       | Colombia |
| Valentina Mendoza    | Colombia |
| David Romero         | Colombia |
| David Vargas         | Colombia |
| David Romero         | Colombia |
| Camila López         | Colombia |
| Sofía Hernández      | Colombia |
| Julián Rodríguez     | Colombia |
| Julián García        | Colombia |
| Sofía Hernández      | Colombia |
| Juan García          | Colombia |
| David Vargas         | Colombia |
| Andrés Hernández     | Colombia |
| Daniela García       | Colombia |
| Julián Vargas        | Colombia |
| Valentina Romero     | Colombia |
| Sofía López          | Colombia |
| Sofía García         | Colombia |
| Valentina Hernández  | Colombia |
| Valentina López      | Colombia |
| Camila Martínez      | Colombia |
| Juan Romero          | Colombia |
| Sofía Hernández      | Colombia |
| Julián García        | Colombia |
| Julián Mendoza       | Colombia |
| David Vargas         | Colombia |
| Andrés Vargas        | Colombia |
| Juan López           | Colombia |
| Juan López           | Colombia |
| Valentina Mendoza    | Colombia |
| Camila García        | Colombia |
| David Martínez       | Colombia |
| Sofía Martínez       | Colombia |
| Daniela Vargas       | Colombia |
| Juan Vargas          | Colombia |
| Julián Hernández     | Colombia |
| Valentina García     | Colombia |
| Valentina Rodríguez  | Colombia |
| Camila Martínez      | Colombia |
| Julián López         | Colombia |
| Valentina Romero     | Colombia |
| Julián Hernández     | Colombia |
| Daniela Hernández    | Colombia |
| Sofía Rodríguez      | Colombia |
| Daniela López        | Colombia |
| Andrés Rodríguez     | Colombia |
| Daniela Rodríguez    | Colombia |
| Valentina Rodríguez  | Colombia |
| Daniela Vargas       | Colombia |
| David Hernández      | Colombia |
| Sofía Rodríguez      | Colombia |
| David Mendoza        | Colombia |
| Daniela Romero       | Colombia |
| Sofía García         | Colombia |
| Juan Rodríguez       | Colombia |
| Valentina García     | Colombia |
| Camila Rodríguez     | Colombia |
| David Mendoza        | Colombia |
| Valentina Romero     | Colombia |
| David Hernández      | Colombia |
| Camila López         | Colombia |
| Valentina Hernández  | Colombia |
| David Hernández      | Colombia |
| Valentina Mendoza    | Colombia |
| Julián Hernández     | Colombia |
| Juan López           | Colombia |
| David García         | Colombia |
| Julián Vargas        | Colombia |
| Julián Hernández     | Colombia |
| Sofía Vargas         | Colombia |
| Sofía López          | Colombia |
| Sofía Vargas         | Colombia |
| Valentina Mendoza    | Colombia |
| Julián Rodríguez     | Colombia |
| Julián Vargas        | Colombia |
| Juan López           | Colombia |
| Juan Mendoza         | Colombia |
| Valentina Romero     | Colombia |
| Sofía Martínez       | Colombia |
| Andrés Martínez      | Colombia |
| Camila García        | Colombia |
| Valentina Romero     | Colombia |
| Andrés López         | Colombia |
| Daniela López        | Colombia |
| Julián Romero        | Colombia |
| David López          | Colombia |
| Camila Rodríguez     | Colombia |
| Julián Martínez      | Colombia |
| Juan Rodríguez       | Colombia |
| Sofía Rodríguez      | Colombia |
| David Rodríguez      | Colombia |
| Daniela Hernández    | Colombia |
| Daniela Mendoza      | Colombia |
| David Romero         | Colombia |
| Julián Rodríguez     | Colombia |
| Daniela Romero       | Colombia |
| Sofía Rodríguez      | Colombia |
| Andrés Rodríguez     | Colombia |
| Andrés Rodríguez     | Colombia |
| Julián Rodríguez     | Colombia |
| Andrés Mendoza       | Colombia |
| Juan Vargas          | Colombia |
| David Hernández      | Colombia |
| Andrés Mendoza       | Colombia |
| Daniela Martínez     | Colombia |
| Daniela Hernández    | Colombia |
| Juan Mendoza         | Colombia |
| Julián Mendoza       | Colombia |
| Julián López         | Colombia |
| Andrés Martínez      | Colombia |
| Andrés López         | Colombia |
| Camila Mendoza       | Colombia |
| Daniela Martínez     | Colombia |
| Camila Romero        | Colombia |
| Valentina Rodríguez  | Colombia |
| Sofía Romero         | Colombia |
| Juan Rodríguez       | Colombia |
| Daniela Romero       | Colombia |
| Valentina García     | Colombia |
| Andrés Martínez      | Colombia |
| Sofía Martínez       | Colombia |
| Camila López         | Colombia |
| Daniela García       | Colombia |
| Daniela Vargas       | Colombia |
| David Martínez       | Colombia |
| Daniela Vargas       | Colombia |
| Juan Vargas          | Colombia |
| Daniela García       | Colombia |
| Andrés Hernández     | Colombia |
| David Vargas         | Colombia |
| David Hernández      | Colombia |
| Julián Romero        | Colombia |
| Andrés Vargas        | Colombia |
| Andrés Rodríguez     | Colombia |
| Valentina Hernández  | Colombia |
| Valentina Romero     | Colombia |
| David Hernández      | Colombia |
| Julián García        | Colombia |
| Daniela Vargas       | Colombia |
| Sofía Vargas         | Colombia |
| Valentina Romero     | Colombia |
| Juan Vargas          | Colombia |
| Juan López           | Colombia |
| Juan Mendoza         | Colombia |
| Julián López         | Colombia |
| Daniela Romero       | Colombia |
| Daniela Romero       | Colombia |
| Andrés Rodríguez     | Colombia |
| Daniela Vargas       | Colombia |
| Sofía Rodríguez      | Colombia |
| Juan Mendoza         | Colombia |
| Valentina Vargas     | Colombia |
| Andrés García        | Colombia |
| David Mendoza        | Colombia |
| Julián García        | Colombia |
| Andrés Hernández     | Colombia |
| Andrés López         | Colombia |
| Valentina Vargas     | Colombia |
| Valentina López      | Colombia |
| Juan Mendoza         | Colombia |
| Juan Hernández       | Colombia |
| Valentina Vargas     | Colombia |
| Julián Vargas        | Colombia |
| David Vargas         | Colombia |
| Valentina Vargas     | Colombia |
| David López          | Colombia |
| Daniela Romero       | Colombia |
| Valentina Mendoza    | Colombia |
| Camila Vargas        | Colombia |
| Julián Romero        | Colombia |
| Valentina García     | Colombia |
| Sofía Rodríguez      | Colombia |
| Julián García        | Colombia |
| Camila Mendoza       | Colombia |
| Sofía Martínez       | Colombia |
| Andrés Rodríguez     | Colombia |
| Valentina López      | Colombia |
| David Hernández      | Colombia |
| Sofía Hernández      | Colombia |
| Camila Hernández     | Colombia |
| Valentina Vargas     | Colombia |
| Valentina Hernández  | Colombia |
| Andrés Romero        | Colombia |
| Julián Vargas        | Colombia |
| Andrés Romero        | Colombia |
| David Hernández      | Colombia |
| Julián Vargas        | Colombia |
| Julián Martínez      | Colombia |
| Daniela Rodríguez    | Colombia |
| Sofía García         | Colombia |
| Valentina Martínez   | Colombia |
| Andrés García        | Colombia |
| Juan Mendoza         | Colombia |
| Daniela López        | Colombia |
| Andrés García        | Colombia |
| Valentina López      | Colombia |
| Julián Vargas        | Colombia |
| Julián Rodríguez     | Colombia |
| David Romero         | Colombia |
| Juan Hernández       | Colombia |
| Juan Romero          | Colombia |
| Daniela García       | Colombia |
| Camila Vargas        | Colombia |
| David López          | Colombia |
| Camila Hernández     | Colombia |
| Sofía Romero         | Colombia |
| Valentina Hernández  | Colombia |
| Valentina Vargas     | Colombia |
| Daniela Rodríguez    | Colombia |
| Julián Martínez      | Colombia |
| Camila López         | Colombia |
| Sofía López          | Colombia |
| David Romero         | Colombia |
| Andrés Mendoza       | Colombia |
| Valentina Vargas     | Colombia |
| Juan Martínez        | Colombia |
| David Romero         | Colombia |
| Juan Vargas          | Colombia |
| David García         | Colombia |
| Camila Romero        | Colombia |
| Andrés Mendoza       | Colombia |
| Sofía Rodríguez      | Colombia |
| Juan López           | Colombia |
| David Martínez       | Colombia |
| Andrés Rodríguez     | Colombia |
| Valentina Hernández  | Colombia |
| David Mendoza        | Colombia |
| Valentina Romero     | Colombia |
| Valentina Rodríguez  | Colombia |
| David Mendoza        | Colombia |
| Andrés López         | Colombia |
| Daniela García       | Colombia |
| Julián Hernández     | Colombia |
| Juan Vargas          | Colombia |
| Camila Hernández     | Colombia |
| Juan García          | Colombia |
| Camila Rodríguez     | Colombia |
| Sofía García         | Colombia |
| Andrés Vargas        | Colombia |
| Daniela Romero       | Colombia |
| David Rodríguez      | Colombia |
| Camila Rodríguez     | Colombia |
| Julián Martínez      | Colombia |
| Juan Rodríguez       | Colombia |
| Julián Mendoza       | Colombia |
| Sofía López          | Colombia |
| Sofía Martínez       | Colombia |
| Juan López           | Colombia |
| Camila Rodríguez     | Colombia |
| Juan Vargas          | Colombia |bre) VA
| David López          | Colombia |
| Valentina Mendoza    | Colombia |
| Camila Mendoza       | Colombia |
| David López          | Colombia |
| Valentina García     | Colombia |
| Andrés Vargas        | Colombia |
| Julián Vargas        | Colombia |
| Juan López           | Colombia |
| Valentina Martínez   | Colombia |
| Valentina Vargas     | Colombia |
| Julián López         | Colombia |
| David López          | Colombia |
| Camila Hernández     | Colombia |
| Sofía García         | Colombia |
| Daniela López        | Colombia |
| Daniela García       | Colombia |
| Julián García        | Colombia |
| Sofía García         | Colombia |
| Andrés García        | Colombia |
| Daniela López        | Colombia |
| David Rodríguez      | Colombia |
| Sofía Hernández      | Colombia |
| Julián López         | Colombia |
| Sofía Mendoza        | Colombia |
| Sofía García         | Colombia |
| Julián Hernández     | Colombia |
| David Romero         | Colombia |
| Julián Mendoza       | Colombia |
| Valentina García     | Colombia |
| Juan Martínez        | Colombia |
| Juan Mendoza         | Colombia |
| Valentina García     | Colombia |
| Juan López           | Colombia |
| Valentina Hernández  | Colombia |
| Daniela Vargas       | Colombia |
| Daniela García       | Colombia |
| Andrés García        | Colombia |
| David Romero         | Colombia |
| Julián Martínez      | Colombia |
+----------------------+----------+
```

**Mostrar todas las sucursales que pertenecen a la empresa 'RedElectro S.A.' junto con el municipio y departamento donde están ubicadas.**

Solución

```
SELECT 
    s.nombre AS sucursal, m.nombre AS municipio, d.nombre AS  departamento
FROM sucursal s
JOIN municipio m ON s.municipioid = m.id
JOIN departamento d ON m.depid = d.id
JOIN empresa e ON d.empresaid = e.id
WHERE e.nombre = 'RedElectro S.A.';
```



```
+------------------+--------------+-----------------+
| sucursal         | municipio    | departamento    |
+------------------+--------------+-----------------+
| Sucursal Zona 1  | Ibagué       | Tolima          |
| Sucursal Zona 2  | Zipaquirá    | Cundinamarca    |
| Sucursal Zona 3  | Bello        | Antioquia       |
| Sucursal Zona 4  | Malambo      | Atlántico       |
| Sucursal Zona 5  | Barranquilla | Atlántico       |
| Sucursal Zona 6  | Cartago      | Valle del Cauca |
| Sucursal Zona 7  | Facatativá   | Cundinamarca    |
| Sucursal Zona 8  | Chía         | Cundinamarca    |
| Sucursal Zona 9  | Samaniego    | Nariño          |
| Sucursal Zona 10 | Soacha       | Cundinamarca    |
+------------------+--------------+-----------------+
```

**Mostrar los nombres de empleados que trabajan en el mismo municipio donde hay más de una sucursal.**(y Subconsultas)

Solución

```
SELECT DISTINCT e.nombre
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
WHERE s.municipioid IN (
    SELECT municipioid
    FROM sucursal
    GROUP BY municipioid
    HAVING COUNT(*) > 1
);
```

**Obtener el número total de empleados por empresa.**

Solucion

```
SELECT 
  emp.id AS empresa_id,
  emp.nombre AS empresa_nombre,
  COUNT(e.empleado_id) AS total_empleados
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN empresa emp ON s.empresaid = emp.id
GROUP BY emp.id, emp.nombre
ORDER BY total_empleados DESC;

```

```
+-----------------+-----------------+
| empresa         | total_empleados |
+-----------------+-----------------+
| RedElectro S.A. |             100 |
+-----------------+-----------------+
```

## Sección 2: Funciones Agregadas (5 problemas)

**Calcular el salario promedio de empleados por municipio.**

Solución

```
SELECT 
  m.nombre AS municipio,
  AVG(e.salario) AS salario_promedio
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN municipio m ON s.municipioid = m.id
GROUP BY m.id, m.nombre
ORDER BY salario_promedio DESC;

```

```
+--------------+------------------+
| municipio    | salario_promedio |
+--------------+------------------+
| Bello        |   1807789.417000 |
| Soacha       |   1902034.541000 |
| Chía         |   1730699.521000 |
| Zipaquirá    |   1769330.543000 |
| Facatativá   |   1854213.800000 |
| Cartago      |   1842813.252000 |
| Barranquilla |   1847349.308000 |
| Malambo      |   1929583.595000 |
| Samaniego    |   1708567.175000 |
| Ibagué       |   1916484.849000 |
+--------------+------------------+
```

**Listar los tres departamentos con más clientes registrados.**

Solución

```
SELECT 
  d.nombre AS departamento,
  COUNT(c.cliente_id) AS total_clientes
FROM clientes c
JOIN municipio m ON c.municipioid = m.id
JOIN departamento d ON m.depid = d.id
GROUP BY d.id, d.nombre
ORDER BY total_clientes DESC
LIMIT 3;

```

```
+-----------------+----------------+
| departamento    | total_clientes |
+-----------------+----------------+
| Antioquia       |             50 |
| Cundinamarca    |             50 |
| Valle del Cauca |             50 |
+-----------------+----------------+
```

**Mostrar el puesto con el mayor número de empleados en toda la empresa.**

Solución

```
SELECT 
  puesto,
  COUNT(*) AS total_empleados
FROM empleados
GROUP BY puesto
ORDER BY total_empleados DESC
LIMIT 1;

```

```
+----------+----------+
| puesto   | cantidad |
+----------+----------+
| Vendedor |       25 |
+----------+----------+
```

**Calcular el total de salarios pagados por cada empresa.**

Solución

```
SELECT 
  emp.nombre AS empresa,
  SUM(e.salario) AS total_salarios
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN empresa emp ON s.empresaid = emp.id
GROUP BY emp.id, emp.nombre
ORDER BY total_salarios DESC;

```

```
+-----------------+----------------+
| empresa         | total_salarios |
+-----------------+----------------+
| RedElectro S.A. |   183088660.01 |
+-----------------+----------------+
```

 **Obtener el promedio de empleados por municipio.**

Solución

```

```

```
+--------------+-----------------+
| municipio    | total_empleados |
+--------------+-----------------+
| Bello        |              10 |
| Soacha       |              10 |
| Chía         |              10 |
| Zipaquirá    |              10 |
| Facatativá   |              10 |
| Cartago      |              10 |
| Barranquilla |              10 |
| Malambo      |              10 |
| Samaniego    |              10 |
| Ibagué       |              10 |
+--------------+-----------------+
```

## Sección 3: Subconsultas (5 problemas)

**Listar empleados cuyo salario es mayor al salario promedio general de la empresa.**

Solucion

```
SELECT e.nombre, e.salario
FROM empleados e
WHERE e.salario > (
    SELECT AVG(salario)
    FROM empleados
    WHERE salario IS NOT NULL
);
```

```
+-------------------+------------+
| nombre            | salario    |
+-------------------+------------+
| Laura Rodríguez   | 2040075.24 |
| Sofía Gómez       | 2274750.60 |
| Carlos Torres     | 2034335.51 |
| Pedro Rodríguez   | 2196507.16 |
| Pedro Torres      | 2286928.91 |
| Laura Torres      | 2126954.47 |
| Laura Rodríguez   | 1989423.28 |
| Sofía Torres      | 2216180.29 |
| Luis Rodríguez    | 1892042.62 |
| Sofía Gómez       | 2035760.98 |
| Sofía Pérez       | 2378794.18 |
| Pedro Gómez       | 1920831.18 |
| Carlos Gómez      | 2253536.49 |
| Pedro Gómez       | 2015158.50 |
| Luis Pérez        | 2360108.22 |
| Carlos Rodríguez  | 2298828.77 |
| Sofía Torres      | 1951307.65 |
| Laura Pérez       | 2149728.97 |
| Sofía Rodríguez   | 2012297.58 |
| Pedro Rodríguez   | 2152105.60 |
| Sofía Torres      | 1843737.15 |
| Luis Rodríguez    | 2071302.13 |
| Laura Torres      | 2133981.12 |
| Laura Torres      | 2172226.15 |
| Carlos Rodríguez  | 2060965.87 |
| Luis Rodríguez    | 1884014.12 |
| Luis Rodríguez    | 2093412.76 |
| Ana Torres        | 1948545.60 |
| Luis Pérez        | 2078820.33 |
| Ana Rodríguez     | 1908694.86 |
| Laura Pérez       | 2259991.71 |
| Carlos Torres     | 1934723.27 |
| Laura Gómez       | 2192256.28 |
| Luis Gómez        | 1913880.34 |
| Pedro Gómez       | 2342349.22 |
| Ana Rodríguez     | 2245567.40 |
| Carlos Pérez      | 1948768.55 |
| Luis Torres       | 1893979.72 |
| Sofía Gómez       | 2278365.18 |
| Luis Pérez        | 1998263.19 |
| Ana Rodríguez     | 1987949.62 |
| Laura Pérez       | 1905922.91 |
| Pedro Torres      | 2391482.85 |
| Carlos Torres     | 2215357.49 |
| Sofía Torres      | 1906391.58 |
| Sofía Pérez       | 2120921.80 |
| Pedro Rodríguez   | 2098656.08 |
| Pedro Torres      | 1892438.64 |
| Sofía Gómez       | 2075750.67 |
+-------------------+------------+
```

**Mostrar los municipios que no tienen ninguna sucursal.**

Solucion

```
SELECT m.nombre
FROM municipio m
LEFT JOIN sucursal s ON m.id = s.municipioid
WHERE s.id IS NULL;

```

```
+-----------------------+
| nombre                |
+-----------------------+
| Medellín              |
| Itagüí                |
| Envigado              |
| Rionegro              |
| Girardot              |
| Cali                  |
| Palmira               |
| Buenaventura          |
| Tuluá                 |
| Soledad               |
| Puerto Colombia       |
| Sabanalarga           |
| Cartagena             |
| Magangué              |
| Turbaco               |
| El Carmen de Bolívar  |
| Arjona                |
| Bucaramanga           |
| Floridablanca         |
| Giron                 |
| Piedecuesta           |
| Barrancabermeja       |
| Pasto                 |
| Tumaco                |
| Ipiales               |
| Túquerres             |
| Manizales             |
| Villamaría            |
| Chinchiná             |
| La Dorada             |
| Riosucio              |
| Espinal               |
| Melgar                |
| Honda                 |
| Líbano                |
| Tunja                 |
| Duitama               |
| Sogamoso              |
| Chiquinquirá          |
| Moniquirá             |
+-----------------------+
```

**Listar los clientes que viven en municipios donde no hay empleados.**

Solucion

```
SELECTc.nombre
FROM clientes c
WHERE NOT EXISTS (
    SELECT 1
    FROM empleados e
    JOIN sucursal s ON e.sucursalid = s.id
    WHERE s.municipioid = c.municipioid
);
```

```
+----------------------+
| nombre               |
+----------------------+
| Valentina Mendoza    |
| Andrés Mendoza       |
| Daniela López        |
| Andrés Vargas        |
| Camila García        |
| Andrés Romero        |
| Valentina Hernández  |
| David Vargas         |
| Valentina López      |
| Julián López         |
| Julián García        |
| David García         |
| Andrés Mendoza       |
| Daniela Vargas       |
| David Rodríguez      |
| Daniela García       |
| Andrés García        |
| David Romero         |
| Julián Romero        |
| Julián Mendoza       |
| David Martínez       |
| Andrés Rodríguez     |
| David Rodríguez      |
| Juan Rodríguez       |
| Sofía López          |
| Camila López         |
| Camila López         |
| Andrés García        |
| Julián Rodríguez     |
| Julián Martínez      |
| Julián Mendoza       |
| Andrés López         |
| David Romero         |
| Daniela García       |
| Daniela Mendoza      |
| Daniela García       |
| Valentina Mendoza    |
| Andrés Vargas        |
| David García         |
| Sofía Hernández      |
| Valentina López      |
| Camila Romero        |
| Julián Rodríguez     |
| David Mendoza        |
| Daniela López        |
| Camila Mendoza       |
| Sofía García         |
| Valentina Romero     |
| Daniela Martínez     |
| Andrés Vargas        |
| Valentina López      |
| Julián Martínez      |
| Daniela García       |
| Camila Rodríguez     |
| Andrés Mendoza       |
| Juan López           |
| Juan Romero          |
| David García         |
| Camila Romero        |
| Sofía Martínez       |
| David López          |
| Julián Mendoza       |
| Camila Hernández     |
| Sofía Romero         |
| Juan Hernández       |
| Andrés Vargas        |
| Valentina Mendoza    |
| Andrés Romero        |
| Sofía Vargas         |
| Julián Romero        |
| Camila Vargas        |
| Daniela Vargas       |
| Valentina Mendoza    |
| David Romero         |
| David Vargas         |
| David Romero         |
| Camila López         |
| Sofía Hernández      |
| Julián Rodríguez     |
| Julián García        |
| Sofía Hernández      |
| Juan García          |
| David Vargas         |
| Andrés Hernández     |
| Daniela García       |
| Julián Vargas        |
| Valentina Romero     |
| Sofía López          |
| Sofía García         |
| Valentina Hernández  |
| Julián López         |
| Valentina Romero     |
| Julián Hernández     |
| Daniela Hernández    |
| Sofía Rodríguez      |
| Daniela López        |
| Andrés Rodríguez     |
| Daniela Rodríguez    |
| Valentina Rodríguez  |
| Daniela Vargas       |
| David Hernández      |
| Camila López         |
| Valentina Hernández  |
| David Hernández      |
| Valentina Mendoza    |
| Julián Hernández     |
| Juan López           |
| David García         |
| Julián Vargas        |
| Julián Hernández     |
| Sofía Vargas         |
| Sofía López          |
| Sofía Vargas         |
| Valentina Mendoza    |
| Julián Rodríguez     |
| Julián Vargas        |
| Juan López           |
| Juan Mendoza         |
| Valentina Romero     |
| Sofía Martínez       |
| Andrés Martínez      |
| Camila García        |
| Valentina Romero     |
| Andrés López         |
| Daniela López        |
| Julián Romero        |
| David López          |
| Camila Rodríguez     |
| Julián Martínez      |
| Juan Rodríguez       |
| Sofía Rodríguez      |
| David Rodríguez      |
| Daniela Hernández    |
| Daniela Mendoza      |
| David Romero         |
| Julián Rodríguez     |
| Daniela Romero       |
| Sofía Rodríguez      |
| Andrés Rodríguez     |
| Andrés Rodríguez     |
| Julián Rodríguez     |
| Andrés Mendoza       |
| Juan Vargas          |
| David Hernández      |
| Andrés Mendoza       |
| Daniela Martínez     |
| Daniela Hernández    |
| Juan Mendoza         |
| Julián Mendoza       |
| Julián López         |
| Andrés Martínez      |
| Andrés López         |
| Camila Mendoza       |
| Daniela Martínez     |
| Camila Romero        |
| Valentina Rodríguez  |
| Sofía Romero         |
| Juan Rodríguez       |
| Daniela Romero       |
| Valentina García     |
| Andrés Martínez      |
| Sofía Martínez       |
| Camila López         |
| Daniela García       |
| Daniela Vargas       |
| David Martínez       |
| Daniela Vargas       |
| Juan Vargas          |
| Daniela García       |
| Andrés Hernández     |
| David Vargas         |
| David Hernández      |
| Julián Romero        |
| Andrés Vargas        |
| Andrés Rodríguez     |
| Valentina Hernández  |
| Valentina Romero     |
| David Hernández      |
| Julián García        |
| Daniela Vargas       |
| Sofía Vargas         |
| Valentina Romero     |
| Juan Vargas          |
| Juan López           |
| Juan Mendoza         |
| Julián López         |
| Daniela Romero       |
| Daniela Romero       |
| Andrés Rodríguez     |
| Daniela Vargas       |
| Sofía Rodríguez      |
| Juan Mendoza         |
| Valentina Vargas     |
| Andrés García        |
| David Mendoza        |
| Julián García        |
| Andrés Hernández     |
| Andrés López         |
| Valentina Vargas     |
| Valentina López      |
| Juan Mendoza         |
| Juan Hernández       |
| Valentina Vargas     |
| Julián Vargas        |
| David Vargas         |
| Valentina Vargas     |
| David López          |
| Daniela Romero       |
| Valentina Mendoza    |
| Camila Vargas        |
| Julián Romero        |
| Valentina García     |
| Sofía Rodríguez      |
| Julián García        |
| Camila Mendoza       |
| Sofía Martínez       |
| Andrés Rodríguez     |
| Valentina López      |
| David Hernández      |
| Sofía Hernández      |
| Camila Hernández     |
| Valentina Vargas     |
| Valentina Hernández  |
| Andrés Romero        |
| Julián Vargas        |
| Andrés Romero        |
| David Hernández      |
| Julián Vargas        |
| Julián Martínez      |
| Daniela Rodríguez    |
| Sofía García         |
| Valentina Martínez   |
| Andrés García        |
| Juan Mendoza         |
| Daniela López        |
| Andrés García        |
| Valentina López      |
| Julián Vargas        |
| Julián Rodríguez     |
| David Romero         |
| Juan Hernández       |
| Juan Romero          |
| Daniela García       |
| Camila Vargas        |
| David López          |
| Camila Hernández     |
| Sofía Romero         |
| Valentina Hernández  |
| Valentina Vargas     |
| Daniela Rodríguez    |
| Julián Martínez      |
| Camila López         |
| Sofía López          |
| David Romero         |
| Andrés Mendoza       |
| Valentina Vargas     |
| Juan Martínez        |
| David Romero         |
| Juan Vargas          |
| David García         |
| David Mendoza        |
| Andrés López         |
| Daniela García       |
| Julián Hernández     |
| Juan Vargas          |
| Camila Hernández     |
| Juan García          |
| Camila Rodríguez     |
| Sofía García         |
| Andrés Vargas        |
| Daniela Romero       |
| David Rodríguez      |
| Camila Rodríguez     |
| Julián Martínez      |
| Juan Rodríguez       |
| Julián Mendoza       |
| Sofía López          |
| Sofía Martínez       |
| Juan López           |
| Camila Rodríguez     |
| Juan Vargas          |
| David López          |
| Valentina Mendoza    |
| Camila Mendoza       |
| David López          |
| Valentina García     |
| Andrés Vargas        |
| Julián Vargas        |
| Juan López           |
| Valentina Martínez   |
| Valentina Vargas     |
| Julián López         |
| David López          |
| Camila Hernández     |
| Sofía García         |
| Daniela López        |
| Daniela García       |
| Julián García        |
| Sofía García         |
| Andrés García        |
| Daniela López        |
| David Rodríguez      |
| Sofía Hernández      |
| Julián López         |
| Sofía Mendoza        |
| Sofía García         |
| Julián Hernández     |
| David Romero         |
| Julián Mendoza       |
| Valentina García     |
+----------------------+
```

**Obtener los empleados cuyo salario supera al salario más alto registrado en su mismo municipio.**

Solucion

```

```

**Mostrar los puestos que existen en al menos 3 sucursales distintas.**

Solucion

```
SELECT e.puesto
FROM empleados e
GROUP BY e.puesto
HAVING COUNT(DISTINCT e.sucursalid) >= 3;

```

```
+------------+
| puesto     |
+------------+
| Bodeguero  |
| Cajero     |
| Supervisor |
| Técnico    |
| Vendedor   |
+------------+
```

