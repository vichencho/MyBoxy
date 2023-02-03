# DOCUMENTATION OF PROYECT MYBOXY

## Proyect Purpose
	Build an application that serves as a dynamic repository that can be configured by the user owner so they can upload, publish, privatize, group and maintain different types of documents.

## Database Design

### 1. Definition and Analisis of Requirments:
	- The database can be capable of storing information about users and their documents in any type of file format that can be previously established.
	- The upload of files could be restricted by size and file type, based on parameters that are set for each user.
	- Users can group their documents by profiles established by the system or created by themselves.
	- The system can be capable of generating URIs for each document or profile, which can be public or private.
	- Users must belong to a specific role,that determine what actions or functions they can do inside the application.
	- Users could download documents (files) as long as their role has permission for that action.

### 2. Conceptual Data Model: 
	Based on the definition and analysis of requirements, the following entities can be identified in the data model:

### Data Model Entities

1. User
2. Role
3. File
4. File_Format
5. Group
6. Group_Type


### Relationships

	1. User - File (N to 1)
		- User can have multiple files
		- File belongs to one user
	2. User - Role (1 to N)
		- User belongs to one role
		- Role can have multiple users
	3. Group - File (N to M)
		- Group can have multiple files
		- File can belongs to multiple groups
	4. File - File_Format (1 to N)
		- File belongs to one File_Format
		- File_Format can have multiple Files
	5. User - Group (N to 1)
		- User can have multiple groups
		- Group belongs to one user
    6. Group - Group_Type (1 to N)
	    - Group have one Group_Type
	    - Group_Type can have multiple Group



3. Creación de tablas: Crea tablas en Oracle para representar entidades y relaciones identificadas en el modelo conceptual.

4. Definición de claves: Define claves primarias y foráneas para las tablas para garantizar la integridad referencial.

5. Normalización: Normaliza las tablas para evitar la redundancia y mejorar el rendimiento.

6. Creación de índices: Crea índices para optimizar la velocidad de búsqueda y mejorar el rendimiento.

7. Pruebas y validación: Prueba la base de datos para asegurarte de que cumpla con los requerimientos y objetivos.

8. Implementación: Implementa la base de datos en un ambiente de producción y comienza a utilizarla.

