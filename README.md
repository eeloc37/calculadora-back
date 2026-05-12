# Calculator App - Monorepo DevOps

API Calculadora. 
Guia de Integracion y Despliegue DevOps para soportar CI/CD y contenedorizacion

## Estructura del proyecto

```
calculator-app/
├── backend/                  # API REST (FastAPI + Python 3.12)
│   ├── main.py               # Aplicacion con prefijo /api
│   ├── requirements.txt      # Deps con versiones pinneadas
│   ├── Dockerfile            # Non-root, cache optimizado
│   ├── .dockerignore
│   └── README.md
├── .github/
│   ├── workflows/            # CI/CD pipelines
│   └── CODEOWNERS
├── docker-compose.yml        # Desarrollo local
└── .gitignore
```

## Inicio rapido

```bash
# Levantar todo en local
docker compose up --build

# Acceder
# API docs: http://localhost/api/docs
# Health:   http://localhost/api/health
```

## Endpoints del backend

| Metodo | Ruta                | Descripcion                  |
|--------|---------------------|------------------------------|
| GET    | `/api/health`       | Health check                 |
| GET    | `/api/sumar`        | Suma `?a=2&b=3`             |
| GET    | `/api/restar`       | Resta `?a=10&b=4`           |
| POST   | `/api/multiplicar`  | `{"a": 3, "b": 4}`          |
| POST   | `/api/dividir`      | `{"a": 10, "b": 2}`         |


## Equipo y CODEOWNERS

- **Global:** @jluisquf
- **Backend:** @eeloc37, @Bxtto
- **Frontend:** @mau-m
- **Infraestructura:** @MMCJUAREZ, @hernandev96
