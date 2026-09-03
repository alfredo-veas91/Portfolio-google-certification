# Aplicar filtros a consultas SQL

  

## Descripción del proyecto

  

Usted es un profesional de seguridad en una gran organización. Parte de su trabajo es investigar problemas de seguridad para ayudar a mantener el sistema seguro. Recientemente descubrió algunos problemas potenciales de seguridad que involucran intentos de inicio de sesión y máquinas de empleados.

  

Su tarea es examinar los datos de la organización en sus tablas **employees** y **log_in_attempts**. Deberá utilizar filtros SQL para recuperar registros de diferentes conjuntos de datos e investigar los posibles problemas de seguridad.

  

## Recuperar intentos de inicio de sesión fallidos fuera del horario laboral

  

```
SELECT *  

FROM log_in_attempts  

WHERE login_time > ‘18:00’ AND success = 0;

```
  

Esta consulta recupera los registros de la tabla log_in_attempts correspondientes a intentos de inicio de sesión fallidos (success = 0) realizados después del horario laboral (login_time > '18:00').

  

## Recuperar intentos de inicio de sesión en fechas específicas

  

```
SELECT *  

FROM log_in_attempts  

WHERE login_date = ‘2022-05-09’ OR login_date = ‘2022-05-08’;
```

  

Esta consulta filtra la tabla log_in_attempts para obtener todos los intentos de inicio de sesión registrados en las fechas específicas del 8 y 9 de mayo de 2022 (login_date = '2022-05-09' OR login_date = '2022-05-08').

  

## Recuperar intentos de inicio de sesión fuera de México

  

```
SELECT *  

FROM log_in_attempts  

WHERE NOT country LIKE ‘MEX%’;
```

  

Esta consulta extrae los registros de la tabla log_in_attempts correspondientes a inicios de sesión realizados fuera de México, aplicando la condición NOT country LIKE 'MEX%' para excluir variantes de dicho país.

  

## Recuperar empleados de Marketing

  
```

SELECT *  

FROM employees  

WHERE department = ‘Marketing’ AND office LIKE ‘East%’;
```

  

Esta consulta recupera la información de los empleados de la tabla employees pertenecientes al departamento de Marketing y asignados a oficinas de la región Este (department = 'Marketing' AND office LIKE 'East%').

  

## Recuperar empleados de Finanzas o Ventas

  

```
SELECT *  

FROM employees  

WHERE department = ‘Finance’ OR department = ‘Sales’;

```
  

Esta consulta consulta la tabla employees para seleccionar a los empleados que pertenecen a los departamentos de Finanzas o Ventas (department = 'Finance' OR department = 'Sales').

  

## Recuperar todos los empleados que no pertenecen a TI

  

```
SELECT *  

FROM employees  

WHERE NOT department = ‘Information technology’;
```

  

Esta consulta extrae de la tabla employees a todos los empleados excluyendo a aquellos que forman parte del departamento de Tecnología de la Información (NOT department = 'Information technology').

  

## Resumen

  

En esta actividad se aplicaron conceptos clave de filtrado AND, NOT y OR en consultas de base de datos. Aplicados a la necesidad de buscar información con respecto a inicios de sesión sospechosos fuera del horario laboral, en determinados lugares así como también datos de empleados de determinados departamentos.



---

# English version

# Apply Filters to SQL Queries

## Project Description

You are a security professional at a large organization. Part of your job is to investigate security issues to help keep the system secure. Recently, you discovered some potential security issues involving login attempts and employee machines.

Your task is to examine the organization's data in the **employees** and **log_in_attempts** tables. You will need to use SQL filters to retrieve records from different datasets and investigate potential security issues.

## Retrieve Failed Login Attempts After Work Hours

```sql
SELECT * 
FROM log_in_attempts 
WHERE login_time > '18:00' AND success = 0;
```

This query retrieves records from the `log_in_attempts` table corresponding to failed login attempts (`success = 0`) that occurred after work hours (`login_time > '18:00'`).

## Retrieve Login Attempts on Specific Dates

```sql
SELECT * 
FROM log_in_attempts 
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

This query filters the `log_in_attempts` table to obtain all login attempts recorded on the specific dates of May 8 and May 9, 2022 (`login_date = '2022-05-09' OR login_date = '2022-05-08'`).

## Retrieve Login Attempts Outside of Mexico

```sql
SELECT * 
FROM log_in_attempts 
WHERE NOT country LIKE 'MEX%';
```

This query extracts records from the `log_in_attempts` table corresponding to logins originating outside of Mexico, applying the condition `NOT country LIKE 'MEX%'` to exclude variants for that country.

## Retrieve Employees in Marketing

```sql
SELECT * 
FROM employees 
WHERE department = 'Marketing' AND office LIKE 'East%';
```

This query retrieves employee information from the `employees` table for personnel belonging to the Marketing department and assigned to East region offices (`department = 'Marketing' AND office LIKE 'East%'`).

## Retrieve Employees in Finance or Sales

```sql
SELECT * 
FROM employees 
WHERE department = 'Finance' OR department = 'Sales';
```

This query searches the `employees` table to select employees who belong to either the Finance or Sales departments (`department = 'Finance' OR department = 'Sales'`).

## Retrieve All Employees Not in IT

```sql
SELECT * 
FROM employees 
WHERE NOT department = 'Information technology';
```

This query extracts all employees from the `employees` table while excluding those who are part of the Information Technology department (`NOT department = 'Information technology'`).

## Summary

In this activity, key filtering concepts using `AND`, `NOT`, and `OR` operators were applied to database queries. These were used to investigate suspicious login attempts outside of business hours and from specific locations, as well as to retrieve employee data across designated departments.
