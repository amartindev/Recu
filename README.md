#   Proyecto de Ventas - Backend con Django y Frontend con React y Vue

Este proyecto es una solución completa para la gestión y visualización de ventas. Incluye un backend desarrollado con Django y dos frontends separados, uno implementado con React y otro con Vue. Ambos frontends consumen la API GraphQL proporcionada por el backend.

---

##   Explicación Técnica General

###   Backend

* **Framework:** Django 5.2
* **Base de Datos:** MySQL
* **API:** GraphQL implementado con `graphene-django`
* **Características principales:**
    * Gestión de productos, clientes y ventas.
    * Consultas avanzadas como ventas por producto, ventas por mes, y cliente con más compras.
    * Migraciones para la creación de tablas en la base de datos.
    * Archivo SQL (`datosprueba.sql`) para poblar la base de datos con datos de prueba.

###   Frontend

* **React:**
    * Implementado con Vite para un desarrollo rápido.
    * Uso de `react-router-dom` para la navegación.
    * Gráficos interactivos con `react-chartjs-2` y `chart.js`.
    * Animaciones con `framer-motion`.
    * Estilizado con Tailwind CSS.
* **Vue:**
    * Implementado con Vite y Vue 3.
    * Uso de `vue-router` para la navegación.
    * Gráficos interactivos con `vue-chartjs` y `chart.js`.
    * Animaciones con `@vueuse/motion`.
    * Estilizado con Tailwind CSS.

---

##   Librerías/Frameworks Externos Usados

###   Backend

* `Django`: Framework principal para el backend.
* `graphene-django`: Para implementar la API GraphQL.
* `mysqlclient`: Conector para MySQL.
* `corsheaders`: Para permitir solicitudes CORS desde los frontends.

###   Frontend React

* `react`: Biblioteca principal para la interfaz de usuario.
* `react-router-dom`: Para la navegación entre páginas.
* `react-chartjs-2` y `chart.js`: Para gráficos interactivos.
* `framer-motion`: Para animaciones.
* `tailwindcss`: Para estilizado.

###   Frontend Vue

* `vue`: Framework principal para la interfaz de usuario.
* `vue-router`: Para la navegación entre páginas.
* `vue-chartjs` y `chart.js`: Para gráficos interactivos.
* `@vueuse/motion`: Para animaciones.
* `tailwindcss`: Para estilizado.

---

##   Cómo Correr el Proyecto

###   Requisitos Previos

* **Backend:**
    * Python 3.10+
    * MySQL
    * Node.js y npm (para los frontends)

###   Opción 1: Correr Manualmente

####   Backend

1.  Clonar el repositorio:

    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd backend
    ```
2.  Crear y activar un entorno virtual:

    ```bash
    python -m venv venv
    source venv/bin/activate # En Windows: venv\Scripts\activate
    ```
3.  Instalar dependencias:

    ```bash
    pip install -r requirements.txt
    ```
4.  Configurar la base de datos:

    * Crear una base de datos en MySQL llamada `datosprueba`.
    * Actualizar la configuración de la base de datos en `backend/settings.py` con sus credenciales de MySQL (por ejemplo, `NAME`, `USER`, `PASSWORD`, `HOST`, `PORT`).
    * Es posible que necesite crear un usuario de MySQL y otorgarle privilegios para acceder a la base de datos `datosprueba`.
    * Aplicar migraciones:

        ```bash
        python manage.py migrate
        ```
    * Poblar la base de datos con datos de prueba:

        ```bash
        mysql -u root -p datosprueba < backend/datosprueba.sql
        ```
5.  Iniciar el servidor:

    ```bash
    python manage.py runserver
    ```

####   Frontend React

1.  Navegar al directorio del frontend de React:

    ```bash
    cd FrontendReact
    ```
2.  Instalar las dependencias:

    ```bash
    npm install
    ```
3.  Iniciar el servidor de desarrollo:

    ```bash
    npm run dev
    ```

####   Frontend Vue

1.  Navegar al directorio del frontend de Vue:

    ```bash
    cd FrontendVue
    ```
2.  Instalar las dependencias:

    ```bash
    npm install
    ```
3.  Iniciar el servidor de desarrollo:

    ```bash
    npm run dev
    ```

###   API Endpoint

El endpoint de la API GraphQL se encuentra en `http://localhost:8000/graphql/`.