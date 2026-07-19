# API de Proyectos - TechSolutions

API REST en Laravel 12 para la gestión de proyectos.

## Configuración rápida

1. Configurar y levantar el proyecto con Laragon (`http://techsolutions.test`) o con Artisan:
   ```bash
   php artisan serve
   ```
2. Ejecutar las migraciones de la base de datos:
   ```bash
   php artisan migrate
   ```

## Rutas y Endpoints (`/api/proyecto`)

| Acción | Método | Endpoint | Estructura JSON (Body) |
| :--- | :--- | :--- | :--- |
| **Listar todos** | `GET` | `/api/proyecto` | (Vacío) |
| **Obtener uno** | `GET` | `/api/proyecto/{id}` | (Vacío) |
| **Agregar** | `POST` | `/api/proyecto` | Estructura JSON de ejemplo |
| **Actualizar** | `PUT` | `/api/proyecto/{id}` | Estructura JSON de ejemplo (Parcial) |
| **Eliminar** | `DELETE` | `/api/proyecto/{id}` | (Vacío) |

### Estructura JSON de ejemplo (Proyecto)
```json
{
  "nombre": "Desarrollo de Software",
  "fecha_inicio": "2026-03-10",
  "estado": "Activo",
  "responsable": "Jaime Bodaleo",
  "monto": 10000000.00
}
```
*(Nota: `fecha_inicio` también soporta formatos como `DD-MM-YYYY` gracias a un parseo automático).*

## Pruebas
Ejecutar las pruebas automatizadas:
```bash
php artisan test
```
