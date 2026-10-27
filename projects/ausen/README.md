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

<img src="screenshots/inicio.png" alt="Inicio de AUSEN" width="100%">

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

### Inicio y Bandeja de Aprobaciones
| Inicio | Bandeja de aprobaciones |
| :---: | :---: |
| <img src="screenshots/inicio.png" alt="Inicio" width="100%"> | <img src="screenshots/bandeja.png" alt="Bandeja de aprobaciones" width="100%"> |

### Mapa de Ausencias y Reportes
| Mapa de ausencias | Reportes |
| :---: | :---: |
| <img src="screenshots/mapa.png" alt="Mapa de ausencias" width="100%"> | <img src="screenshots/reportes.png" alt="Reportes" width="100%"> |

### Gestión del Personal y Perfiles
| Nómina de empleados | Legajo del empleado |
| :---: | :---: |
| <img src="screenshots/nomina.png" alt="Nómina de empleados" width="100%"> | <img src="screenshots/legajo.png" alt="Legajo del empleado" width="100%"> |

### Configuración, Modo Oscuro y Móvil
| Configuración | Portal en modo oscuro |
| :---: | :---: |
| <img src="screenshots/configuracion.png" alt="Configuración" width="100%"> | <img src="screenshots/portal_oscuro.png" alt="Portal en modo oscuro" width="100%"> |

<div align="center">
  <img src="screenshots/pedir_movil.png" alt="Pedido de ausencia desde el celular" width="30%">
  <p><i>Solicitud de ausencia desde el celular</i></p>
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

## 👤 Autor

**Emanuel Sequeira**
* Full Stack Developer
* [LinkedIn](https://www.linkedin.com/in/emanuel-sequeria-a8360b231?utm_source=share_via&utm_content=profile&utm_medium=member_ios)
* [GitHub](https://github.com/Manuseq94)

---
<div align="center">
  <sub>Desarrollado con ❤️ para la gestión eficiente de equipos.</sub>
</div>
