# Selecciones Historicas app

# Sistema de Gestión de Equipos y Jugadores de Fútbol

Este proyecto es una aplicación web desarrollada con **Python (Flask)** para la lógica interna, **PostgreSQL** para la base de datos, y **HTML, CSS y JavaScript** para la interfaz de usuario. Su objetivo es gestionar equipos de fútbol, permitiendo la creación, edición y eliminación de jugadores, así como la asignación de posiciones en una formación táctica.

## Tecnologías Utilizadas
- **Backend:** Flask (con Flask-CORS para manejar peticiones de diferentes orígenes)
- **Base de datos:** PostgreSQL con SQLAlchemy como ORM
- **Frontend:** HTML, CSS y JavaScript
- **API REST:** Para la comunicación entre el frontend y el backend

## Funcionalidades Principales
### 1. Gestión de Equipos
- Listar todos los equipos disponibles.

### 2. Gestión de Jugadores
- Crear nuevos jugadores asignados a un equipo.
- Obtener jugadores según su equipo y posición.
- Eliminar jugadores.

### 3. Formaciones y Posiciones
- Asignar jugadores a posiciones en una formación de 11 jugadores.
- Reemplazar jugadores en una posición de la formación.

## Estructura del Backend
- Se han definido rutas API REST en Flask para realizar las operaciones CRUD sobre **jugadores** y **equipos**.
- Se usa SQLAlchemy para interactuar con la base de datos PostgreSQL.
- Flask-CORS permite que el frontend pueda hacer peticiones sin restricciones de origen.

## Ejecución del Proyecto
1. Crear y activar un entorno virtual (opcional pero recomendado):
 ```bash
python3 -m venv venv
source venv/bin/activate
```

2. Instalar dependencias:
   ```sh
   pip install -r requirements.txt
   ```

3. Configurar la base de datos en PostgreSQL:
- Crea la base de datos en PostgreSQL usando el siguiente comando:
  ```sh
CREATE DATABASE seleccioneshistoricas;
```
- Si deseas otro nombre, recuérdalo para el siguiente paso.

4. Modificar la conexión a la base de datos:
- En el archivo app.py, busca esta línea:
```sh
app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql+psycopg2://postgres:postgres@localhost:5432/seleccioneshistoricas'
```
- Modifícala con tus datos:
```sh
app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql+psycopg2://usuario:contraseña@servidor:puerto/basedatos'
```
5. Activa el entorno virtual y ejecuta el backend:
```bash
source venv/bin/activate
cd backend
python3 main.py
```

4. El frontend se comunica con este backend mediante las API REST definidas:
```bash
cd frontend
python3 -m http.server
```
