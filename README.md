# Proyecto SQL – Análisis de la Base de Datos DVD Rental

## Descripción del proyecto

Este proyecto consiste en la resolución de una serie de consultas SQL utilizando la base de datos **DVD Rental (Sakila)**.

El objetivo del proyecto es practicar el uso de **SQL para análisis de datos**, trabajando con una base de datos relacional que simula el funcionamiento de un sistema de alquiler de películas.

A lo largo del proyecto se han resuelto **más de 60 consultas SQL**, aplicando diferentes técnicas para extraer información relevante de la base de datos y comprender mejor la estructura y relaciones entre sus tablas.

---

# Base de datos utilizada

La base de datos utilizada es **DVD Rental**, que representa el sistema de gestión de un videoclub.

Esta base de datos contiene información sobre:

- Películas  
- Actores  
- Clientes  
- Alquileres  
- Categorías  
- Inventario  
- Tiendas  
- Empleados  

El archivo utilizado para importar la base de datos es:

```
BBDD_Proyecto_shakila_sinuser.sql
```

Este archivo contiene todas las instrucciones necesarias para crear las tablas y cargar los datos en PostgreSQL.

---

# Esquema de la base de datos

La base de datos está formada por múltiples tablas relacionadas entre sí mediante claves primarias y foráneas.

Algunas de las relaciones más importantes son:

```
film
 ├── film_actor
 │     └── actor
 │
 ├── film_category
 │     └── category
 │
 └── inventory
       └── rental
             └── payment

customer
 └── rental

store
 └── staff
```

Estas relaciones permiten realizar consultas complejas combinando información de diferentes tablas mediante **JOIN**.

---

# Metodología seguida

Para la realización del proyecto se siguieron los siguientes pasos:

1. Importación de la base de datos en **PostgreSQL** mediante **DBeaver**.
2. Exploración de la estructura de la base de datos y análisis de las relaciones entre tablas.
3. Resolución progresiva de las consultas SQL planteadas en el proyecto.
4. Uso de diferentes técnicas de SQL para obtener información relevante de los datos.
5. Documentación de cada consulta mediante comentarios que incluyen el número de consulta y el enunciado correspondiente.

---

# Consultas realizadas

El proyecto incluye más de **60 consultas SQL**, que cubren diferentes niveles de complejidad.

Algunos ejemplos de análisis realizados son:

- Listado de películas según diferentes criterios.
- Búsqueda de actores que participan en determinadas categorías de películas.
- Identificación de clientes con mayor número de alquileres.
- Cálculo de alquileres por categoría.
- Análisis de duración de alquileres.
- Uso de subconsultas para comparar valores dentro de la base de datos.
- Creación de tablas temporales para almacenar resultados intermedios.

---

# Conceptos SQL utilizados

Durante el proyecto se han aplicado diversos conceptos fundamentales de SQL.

## Consultas básicas

- SELECT  
- WHERE  
- ORDER BY  
- LIMIT  

## Funciones de agregación

- COUNT()  
- SUM()  
- AVG()  
- MIN()  
- MAX()  

## Agrupación de datos

- GROUP BY  
- HAVING  

## Joins

- INNER JOIN  
- LEFT JOIN  
- CROSS JOIN  

## Subconsultas

Ejemplo:

```sql
SELECT *
FROM film
WHERE length > (SELECT AVG(length) FROM film);
```

## Tablas temporales

Uso de:

```
CREATE TEMP TABLE
```

para almacenar resultados intermedios durante el análisis.

---

# Estructura del repositorio

El repositorio contiene los siguientes archivos:

```
proyecto-sql-dvd-rental
│
├── README.md
├── consultas_dvd_rental.sql
├── BBDD_Proyecto_shakila_sinuser.sql
└── esquema_bbdd.png
```

Descripción de los archivos:

- **README.md** → documentación del proyecto  
- **consultas_dvd_rental.sql** → archivo con todas las consultas SQL realizadas  
- **BBDD_Proyecto_shakila_sinuser.sql** → script para crear la base de datos  
- **esquema_bbdd.png** → diagrama de la estructura de la base de datos  

---

# Herramientas utilizadas

- PostgreSQL  
- DBeaver  
- SQL  
- GitHub  

---

# Autor

**Juan Manuel Agudo Cruz**

Estudiante del Grado en ADE con interés en **Data Analytics y análisis de datos**.
