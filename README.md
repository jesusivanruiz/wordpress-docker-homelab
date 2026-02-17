# WordPress + MySQL con Docker Compose

Setup profesional de WordPress con MySQL usando Docker Compose para desarrollo local.

## Características

- WordPress última versión
- MySQL 8.0
- Variables de entorno seguras con `.env`
- Volúmenes persistentes para datos
- Configuración lista para producción

## Requisitos

- Docker
- Docker Compose

## Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/jesusivanruiz/wordpress-docker-homelab.git
cd wordpress-docker-homelab
```

2. Copia el archivo de ejemplo y configura tus credenciales:
```bash
cp .env.example .env
nano .env
```

3. Levanta los contenedores:
```bash
docker compose up -d
```

4. Accede a WordPress en `http://localhost:8081`

## Estructura
```
.
├── compose.yaml      # Definición de servicios Docker
├── .env.example      # Plantilla de variables de entorno
├── .gitignore        # Archivos ignorados por Git
└── wp-content/       # Contenido de WordPress (no versionado)
```

## Comandos útiles

Ver logs:
```bash
docker compose logs -f
```

Detener servicios:
```bash
docker compose down
```

Reiniciar desde cero (borra la base de datos):
```bash
docker compose down -v
```

## Autor

Jesús Iván Ruiz - [Orale Web](https://oraleweb.mx)
