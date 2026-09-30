<div align="center">

# 🍃 AUSEN
### Sistema de Gestión de Vacaciones y Licencias

**🌐 Web Oficial:** [www.ausen.com.ar](https://www.ausen.com.ar)

---

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-5.0-092E20?style=for-the-badge&logo=django&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Apto-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Alpine.js](https://img.shields.io/badge/Alpine.js-3.x-8BC0D0?style=for-the-badge&logo=alpine.js&logoColor=white)
![Status](https://img.shields.io/badge/Status-En_Producción-success?style=for-the-badge)

<br>

<img src="screenshots/light_mode.png" alt="Dashboard Principal Light" width="100%" style="border-radius: 10px; box-shadow: 0 10px 20px rgba(0,0,0,0.1);">

</div>

---

## 📋 Descripción

**AUSEN** es una solución integral desarrollada para optimizar la gestión de recursos humanos en cooperativas y PyMES. El sistema digitaliza el proceso de solicitud, aprobación y seguimiento de vacaciones y licencias, reemplazando las planillas manuales por una interfaz web intuitiva, reactiva y automatizada.

El objetivo principal es brindar transparencia a los empleados sobre sus días disponibles y facilitar a la administración el control del ausentismo mediante métricas en tiempo real.

## ✨ Características Principales

* **📊 Dashboard Interactivo:** Visualización de métricas clave (ausentismo mensual, distribución diaria, empleados activos) para la toma de decisiones.
* **📅 Motor Inteligente de Feriados:** Integración con API de feriados nacionales para importación automática al calendario.
* **⚡ Cálculo Flexible de Días:** El empleado solicita únicamente el período. Al aprobar, RRHH define si corresponde descontar **"Días Corridos"** o **"Solo Días Hábiles"**, y el sistema recalcula automáticamente fines de semana y feriados según el régimen elegido.
* **🧮 Cálculo Automático (LCT):** Algoritmo que determina los días de vacaciones correspondientes según la antigüedad del empleado (basado en la Ley de Contrato de Trabajo Argentina).
* **👥 Gestión de Empleados:** Sistema completo de administración de perfiles (ABM) con historial laboral y datos personales.
* **📩 Notificaciones Automáticas:** Envío de correos electrónicos a RRHH y supervisores cada vez que se genera o aprueba una solicitud.
* **📄 Reportes PDF:** Generación instantánea de reportes de saldos y solicitudes listos para imprimir y firmar.
* **🎨 Interfaz Moderna y Reactiva:** Diseño basado en componentes utilitarios con soporte nativo para **Modo Oscuro**, modales reactivos con Alpine.js y diseño adaptativo a dispositivos móviles.
* **🔐 Seguridad:** Sistema de autenticación robusto con panel de configuración protegido para administradores.

---

## 📸 Tour del Sistema

### Gestión del Personal y Perfiles
| Nómina de Empleados | Portal del Empleado (Legajo) |
| :---: | :---: |
| <img src="screenshots/nomina_empleados.png" alt="Nomina Empleados" width="100%" style="border-radius: 8px;"> | <img src="screenshots/portal_empleado.png" alt="Portal Empleado" width="100%" style="border-radius: 8px;"> |

### Motor de Ausencias y Configuración
| Cálculo Inteligente de Fechas | Panel de Configuración de Sistema |
| :---: | :---: |
| <img src="screenshots/calculo_inteligente.png" alt="Cálculo Inteligente" width="100%" style="border-radius: 8px;"> | <img src="screenshots/config.png" alt="Configuración" width="100%" style="border-radius: 8px;"> |

### Herramientas y Visualización
| Motor de Feriados | Interfaz Adaptativa (Modo Oscuro) |
| :---: | :---: |
| <img src="screenshots/feriados.png" alt="Gestión de Feriados" width="100%" style="border-radius: 8px;"> | <img src="screenshots/dark_mode.png" alt="Modo Oscuro" width="100%" style="border-radius: 8px;"> |

<br>

<div align="center">
  <img src="screenshots/login.png" alt="Login Screen" width="50%" style="border-radius: 10px; box-shadow: 0 10px 20px rgba(0,0,0,0.1);">
  <p><i>Pantalla de Acceso Seguro (Autenticación)</i></p>
</div>

---

## 🛠️ Stack Tecnológico

* **Backend:** Python 3.10, Django Framework 5.x.
* **Frontend:** HTML5, CSS3, **Tailwind CSS 3.x** (Compilado vía PostCSS), **Alpine.js 3.x**, JavaScript.
* **Servidor de Producción:** Gunicorn (WSGI HTTP Server).
* **Contenedores:** Docker (Imagen base `python:3.10-slim` optimizada con dependencias nativas para Cairo).
* **Librerías Clave:** `holidays` (Cálculo de fechas), `xhtml2pdf` / `pycairo` (Generación de reportes PDF).
* **Base de Datos:** PostgreSQL (Producción en Neon.tech) / SQLite (Local).
* **Gráficos y Calendarios:** Chart.js, FullCalendar.
* **Despliegue e Infraestructura:** Render (Web Service basado en Docker + WhiteNoise para estáticos).
* **Control de Versiones:** Git & GitHub.

---

## 🚀 Instalación y Desarrollo Local

### Opción A: Desarrollo Local con Entorno Virtual 💻

1. **Crear y activar entorno virtual**
   ```bash
   python -m venv venv
# En Windows:
venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate

2. **Instalar dependencias de Python**
   ```bash
   pip install -r requirements.txt

3. **Instalar dependencias Frontend y compilar estilos**
   ```bash
   npm install
   npm run build:css

4. **Configurar variables de entorno**
   Crea un archivo `.env` en la raíz del proyecto (puedes copiar el `.env.example`) y configura tus claves:
   ```env
   SECRET_KEY=tu_clave_secreta_aqui
   DEBUG=True
   EMAIL_HOST_PASSWORD=tu_clave_app_gmail

5. **Migrar base de datos y correr servidor**
   ```bash
   python manage.py migrate
   python manage.py runserver

### Opción B: Despliegue Rápido con Docker 🐳
Al estar el proyecto dockerizado, no necesitas preocuparte por instalar dependencias locales de C (requeridas por pycairo) ni versiones específicas de Python/Node.

1. **Construir y levantar el contenedor**
```bash
   docker build -t ausen-app .
   docker run -d -p 8000:8000 --env-file .env ausen-app



## 👤 Autor

**Emanuel Sequeira**
* Full Stack Developer
* [LinkedIn](https://www.linkedin.com/in/emanuel-sequeria-a8360b231?utm_source=share_via&utm_content=profile&utm_medium=member_ios)
* [GitHub](https://github.com/Manuseq94)

---
<div align="center">
  <sub>Desarrollado con ❤️ para la gestión eficiente de equipos.</sub>
</div>
