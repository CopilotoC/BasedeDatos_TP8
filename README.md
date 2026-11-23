# Especificación de Requisitos de Software[cite: 1]

* [Introducción](#introducción)[cite: 1]
* [Descripción general](#descripción-general-del-producto)[cite: 1]
* [Requisitos específicos](#requisitos-específicos)[cite: 1]
* [Verificación](#verificación)[cite: 1]

---

## Introducción[cite: 1]

* [Propósito](#propósito)[cite: 1]
* [Alcance](#alcance)[cite: 1]
* [Definiciones, Acrónimos y Abreviaturas](#definiciones-acrónimos-y-abreviaturas)[cite: 1]
* [Referencias](#referencias)[cite: 1]
* [Visión General del Documento](#visión-general-de-documento)[cite: 1]

### Propósito[cite: 1]

Este documento especifica los requisitos del sistema «Admin.Barbería», una base de datos para la gestión de barberías en general[cite: 1]. Este documento está orientado al equipo de administración, asegurando la consistencia de datos y apoyando a los stakeholders[cite: 1].

### Alcance[cite: 1]

El sistema permitirá a los usuarios:[cite: 1]

1. Gestionar sucursales: vas a poder registrar las sucursales de tu línea de barberías[cite: 1].
2. Gestión de laburantes: vas a poder manejar los registros de barberos[cite: 1].
3. Gestión de servicios: vas a poder manejar los servicios que da cada sucursal y los servicios que ofrece cada barbero[cite: 1].
4. Gestión de turnos: gestionar los turnos de cada cliente registrado[cite: 1].
5. Gestión de clientes: gestionar los clientes registrados en la Base de Datos[cite: 1].

entre otras cosas[cite: 1]. Queda fuera de alcance la integración con sistemas operativos móviles y aplicación en formato portable e instalable[cite: 1].

### Definiciones, acrónimos y abreviaturas[cite: 1]

BD es Base de datos, SRS o ERS es Software Requirements Specification o Especificación de Requisitos de Software, SQL es Structured Query Language o Lenguaje de Consultas estructuradas, Usuario es quien interactúa con el producto, Administrador es quien administra el sistema desde adentro y dueño del producto[cite: 1].

### Referencias[cite: 1]

La estructura y la guía para realizar este documento nace desde [Guía paso a paso para redactar una Especificación de Requisitos de Software (SRS)](https://classroom.google.com/c/Nzk2NDg4Mjg4MDk1/a/ODY5NDg5NTM0ODI0/details)[cite: 1]

### Visión general de documento[cite: 1]

---

## Descripción General del Producto[cite: 1]

* [Perspectiva del Producto](#perspectiva-del-producto)[cite: 1]
* [Funciones del Producto](#funciones-del-producto)[cite: 1]
* [Características de los Usuarios](#características-de-los-usuarios)[cite: 1]
* [Restricciones](#restricciones)[cite: 1]
* [Suposiciones y Dependencias](#suposiciones-y-dependencias)[cite: 1]

### Perspectiva del producto[cite: 1]

El sistema Admin.Barbería será un sistema web independiente accesible desde navegadores modernos[cite: 1].

### Funciones del producto[cite: 1]

### Características de los usuarios[cite: 1]

Administrador: Gestiona Barberos, Turnos, Servicios, Sucursales, Clientes, etcétera; Usuario: pide turnos[cite: 1].

### Restricciones[cite: 1]

Impuestas por la organización[cite: 1].

### Suposiciones y dependencias[cite: 1]

Los usuarios tienen una conexión estable a internet, usan navegadores que bancan JavaScript, la organización cuenta con servers capaces de aojar al proyecto, tanto en documentos como en Base de datos[cite: 1].

---

## Requisitos específicos[cite: 1]

* [Requisitos de Interfaces Externas](#requisitos-de-interfaces-externas)[cite: 1]
* [Requisitos Funcionales](#requisitos-funcionales)[cite: 1]
* [Requisitos no funcionales](#requisitos-no-funcionales)[cite: 1]

### Requisitos de interfaces externas[cite: 1]

La pantalla principal de la barbería tendrá dos formularios desplegables, uno para registrarse como cliente y otro para reservar un turno[cite: 1]. Si hay un error, se mostrará el Alert() de SQL o el error de JavaScript en un formato en el que cualquier persona podrá interpretar y entender[cite: 1].

### Requisitos funcionales[cite: 1]

**RF-1: Registro de usuario**  
El sistema permite a cualquier visitante registrarse o iniciar sesión para pedir un turno[cite: 1]. Para realizar esto, deberá ingresar DNI (que funciona como Identificador único en el sistema), Nombre/s y Apellido/s[cite: 1].

**RF-2: Pedir turno**  
Cuando el usuario pida turno deberá ingresar hora y fecha del mismo, método de pago, barbero que cumplirá el servicio, sucursal donde se llevará a cabo el turno y el servicio deseado[cite: 1]. Como regla de negocio, las sucursales no deben superar su capacidad máxima de clientes, por lo que si el turno es en una sucursal que está llena o que para cuando ese llevará a cabo el turno no entra más gente, entonces este será rechazado[cite: 1]. Como criterios de aceptación, la sucursal deberá estar abierta en el horario desde que inicia hasta que termina el turno, el barbero debe trabajar en esa sucursal y en ese horario a la vez, debe poder dar el servicio, la sucursal debe bancar el método de pago y tener el equipamiento para proveer el servicio solicitado[cite: 1].

**RF-3: Pedidos de turno superpuestos**  
Cuando dos usuarios piden a la vez el mismo turno, se decide por cuál servicio es más caro[cite: 1]. mientras más caro sea, más prioridad tiene[cite: 1]. Si piden dos servicios que valen lo mismo, se determina por duración; mientras menos dure más prioridad tenés[cite: 1]. Si ambos duran y valen lo mismo, se deja a disposición del barbero que va a atender[cite: 1].

### Requisitos no funcionales[cite: 1]

NFR-01: Dentro del sistema, mil (1000) personas a la vez deberían poder acceder a la página web y pedir turno[cite: 1].  
NFR-02: Tiempo de carga no debe superar los cinco (5) segundos y de respuesta no debe superar el segundo[cite: 1].  
NFR-03: El único dato sensible es el número de documento de cada usuario, barbero, etcétera, que no se muestra en la interfaz, pero internamente se maneja como ID[cite: 1].  
NFR-04: En la interfaz se muestra principalmente el nombre de las personas[cite: 1].  
NFR-05: Se dedica a usuarios casuales que desean pedir turno, asi que se considera que desde los principiantes hasta los expertos puedan usar la plataforma[cite: 1].  
NFR-06: Se cree que, al ser una plataforma chica para empresas u organizaciones de barberías, no se va a presentar una masa en gran cantidad de usuarios, solo algunos casuales que quieran arreglarse[cite: 1].

---
## Verificación[cite: 1]

Las verificaciones están pendientes[cite: 1].

# Requisitos Funcionales (Orientados a los datos)
El sistema debe: 
1. Permitir registrar un cliente y un turno las veinticuatro horas del día.
2. Impedir a un cliente registrar un barbero, sucursal, servicio, método de pago, horario, calle.
3. Permitir imprimir la tabla de turnos de un día específico junto con el monto total de dinero.
4. Impedir la existencia de un turno en un horario no laboral para el barbero, en uno donde la sucursal está cerrada, en uno cuya hora de inicio no entra dentro del rango horario 00:00-23:59. 
5. Impedir el registro de un nuevo día de la semana.
