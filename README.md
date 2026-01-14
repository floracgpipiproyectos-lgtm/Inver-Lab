# Bearlytics — Market Analyzer Pro

Repositorio con la especificación, planificación y artefactos de diseño para construir Bearlytics: una plataforma web de análisis de mercados financieros que permite subir imágenes de carteras (OCR), conectarse a APIs de mercado en tiempo real y ejecutar análisis técnico y predictivo (MACD, RSI, Bollinger, simulaciones).

## Propósito
Servir como guía práctica y base de requisitos para desarrolladores, diseñadores y equipos de producto. Contiene sitemap, user flows, wireframes, diagramas técnicos, modelos de datos y un plan de implementación para un MVP.

## Características clave
- Subida de cartera por imagen (OCR) y extracción automática de activos.
- Integración con APIs de mercado (Yahoo Finance / Alpha Vantage / Finnhub).
- Visualizaciones interactivas: velas, MACD, RSI, Bollinger.
- Recomendaciones automatizadas y exportación de informes.

## Tech stack sugerido
- Frontend: React (+ Chart.js / D3)
- Backend: Node.js (API) + Python (análisis técnico, TA-Lib / Pandas)
- Base de datos: MongoDB o PostgreSQL
- Cache: Redis
- Infra: Docker, CI/CD en GitHub Actions / Azure / AWS

## Cómo usar este repositorio
1. Revisa `2025-10-07.md` para la especificación funcional y técnica.
2. Usa este repo como fuente de verdad para diseñar el `scaffold` del frontend/backend y los endpoints necesarios.

## Quick start (ejemplo mínimo)
Estos son comandos de ejemplo para un entorno de desarrollo local en Windows (PowerShell).

1) Frontend (React) — ejemplo:

```powershell
cd frontend
npm install
npm start
```

2) Backend (Node.js) — ejemplo:

```powershell
cd backend
npm install
npm run dev
```

3) Backend (Python) — ejemplo para procesos de análisis:

```powershell
cd analysis
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python analyze.py --example
```

Estas rutas son orientativas; adapta la estructura a tu scaffold real.

## Desarrollo y testing
- Añade tests unitarios para los cálculos (p. ej. MACD, RSI) y para la integración del OCR.
- Cachea peticiones frecuentes a APIs externas (Redis) y maneja rate limits.

## Seguridad y cumplimiento
- Autenticación: JWT.
- Almacena solo los hashes de imagen si retienes uploads; pide consentimiento para datos personales.
- Incluir disclaimer legal: "No es consejo financiero".

## Próximos pasos sugeridos
- Generar el scaffold inicial con `create-react-app` y un template de Express.
- Añadir un ejemplo funcional mínimo (endpoints mock, ejemplo de OCR con Tesseract).
- Preparar `docker-compose` para desarrollo local.

## Contribuir
Abre issues o PRs con mejoras a la especificación, wireframes o implementaciones de referencia.

---
Si quieres, transformo este `README.md` en una guía más detallada (comandos completos, `docker-compose`, `requirements.txt` y ejemplo mínimo ejecutable).
