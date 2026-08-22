# 🌐 DevDomain Studio — Gestor Personal de Subdominios `.is-a.dev`

<p align="center">
  <img src="https://raw.githubusercontent.com/is-a-dev/register/main/media/banner.png" alt="is-a.dev Banner" width="100%" style="border-radius: 12px; max-height: 280px; object-fit: cover;">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Activo-00F5D4?style=for-the-badge&logo=statuspage&logoColor=black" alt="Status">
  <img src="https://img.shields.io/badge/Service-is--a.dev-5c46eb?style=for-the-badge&logo=github" alt="is-a.dev">
  <img src="https://img.shields.io/badge/Panel-DevDomain_Studio-10B981?style=for-the-badge&logo=cloudflare" alt="DevDomain Studio">
  <img src="https://img.shields.io/badge/Licencia-GPL_v3-blue?style=for-the-badge" alt="Licencia">
</p>

---

## 📌 ¿Qué es este repositorio?

Este repositorio es una bifurcación (*fork*) personalizada y activa de [is-a-dev/register](https://github.com/is-a-dev/register), utilizada para:

1. **Administrar y registrar subdominios gratuitos `.is-a.dev`** para proyectos personales y profesionales.
2. **Proveer una interfaz gráfica interactiva ([`DevDomain Studio`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/index.html))** que permite verificar la disponibilidad de nombres de subdominios en tiempo real, generar configuraciones JSON válidas de DNS (CNAME, A, AAAA, TXT, etc.) y gestionar registros existentes de manera intuitiva.

---

## 🚀 Subdominios Activos Registrados

En la carpeta [`domains/`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/domains) se encuentran las configuraciones DNS oficiales de los proyectos activos:

| Subdominio | Archivo de Configuración | Tipo de Registro | Destino / Propósito |
| :--- | :--- | :---: | :--- |
| **`portafolio.is-a.dev`** | [`domains/portafolio.json`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/domains/portafolio.json) | `CNAME` | Portafolio profesional en GitHub Pages (`frankusqabant.github.io/portafolio-adaptable-bootstrap`) |
| **`aurea-dental.is-a.dev`** | [`domains/aurea-dental.json`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/domains/aurea-dental.json) | `CNAME` | Sitio web de Áurea Dental en GitHub Pages (`frankusqabant.github.io/aurea-dental`) |

---

## 💻 Panel de Control Web: DevDomain Studio

El archivo [`index.html`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/index.html) contiene una aplicación web completa y moderna (sin dependencias externas pesadas) que incluye:

- **Buscador de Disponibilidad:** Comprueba instantáneamente si un subdominio `.is-a.dev` está libre u ocupado consultando directamente la API del repositorio de *is-a-dev*.
- **Generador de JSON DNS:** Asistente visual paso a paso para crear el archivo `.json` requerido con la estructura oficial (propietario, descripción, registros CNAME/A/URL).
- **Validador de Esquema:** Verifica que los campos requeridos cumplan las políticas de *is-a-dev* antes de enviar cualquier solicitud.
- **Visualizador de Subdominios Registrados:** Lista rápida de los dominios vinculados a tu cuenta y sus destinos.

---

## 🛠️ Ejecución Local

Para abrir y probar la aplicación web localmente:

```bash
# Opción 1: Usando npx serve
npx -y serve -p 3000

# Opción 2: Usando Python
python -m http.server 3000
```

Luego abre tu navegador en **[http://localhost:3000](http://localhost:3000)**.

---

## 🚀 Despliegue en GitHub Pages

El proyecto cuenta con un flujo automatizado en [`.github/workflows/deploy.yml`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/.github/workflows/deploy.yml). Cada vez que realizas un `push` a la rama `main`:

1. GitHub Actions empaqueta los archivos estáticos.
2. Despliega automáticamente la versión actualizada del panel a GitHub Pages.
3. Cuenta con etiquetas `<meta name="robots" content="noindex, nofollow">` en [`index.html`](file:///C:/Users/fran_/.gemini/antigravity-ide/scratch/register/index.html) para mantener el panel fuera de los índices públicos de motores de búsqueda.

> **Nota para activar GitHub Pages:**  
> Ve a **Configuración del repositorio en GitHub** (`Settings`) ➔ **Pages** ➔ En **Source / Fuente**, selecciona **GitHub Actions**.

---

## 📁 Estructura del Repositorio

```text
├── .github/
│   └── workflows/
│       └── deploy.yml        # Pipeline de despliegue continuo para GitHub Pages
├── domains/                  # Archivos JSON con las configuraciones DNS de cada subdominio
│   ├── portafolio.json       # Configuración para portafolio.is-a.dev
│   └── aurea-dental.json     # Configuración para aurea-dental.is-a.dev
├── index.html                # Interfaz web de DevDomain Studio (Panel de control)
├── package.json              # Scripts de validación y utilidades del ecosistema is-a-dev
└── README.md                 # Documentación del proyecto
```

---

## 📜 Licencia

Este proyecto está bajo la licencia [GNU General Public License v3.0](LICENSE).  
El servicio base es proporcionado por [is-a.dev](https://is-a.dev) con el respaldo de la infraestructura de Cloudflare.
