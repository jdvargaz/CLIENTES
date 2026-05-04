# JDVARGAZ — Clientes: Dashboards & Propuestas Digitales

## Propósito
Este repositorio contiene dashboards y propuestas digitales para clientes de JDVARGAZ.
Cada cliente tiene su propia carpeta con un `index.html` autocontenido.

## Estructura estándar
```
Clientes/
├── DonEli/
│   └── index.html
├── NombreCliente/       ← una carpeta por cliente
│   └── index.html       ← archivo único, todo embebido (CSS + JS inline)
└── README.md
```

## Reglas para crear un dashboard de cliente

### Nombre de carpeta
- Usar PascalCase sin espacios ni tildes
- Ejemplos: `DonEli`, `HerPlast`, `CafePrimo`, `StudioNova`

### El archivo `index.html` debe ser:
- **Autocontenido**: todo el CSS y JS va inline o en `<style>` / `<script>` dentro del mismo HTML
- **Sin dependencias externas** de archivos locales (imágenes, fonts, etc. deben venir de CDN o base64)
- **Responsive**: funcionar bien en móvil y desktop

### Branding JDVARGAZ
- Firma/logo del autor: Juan David Vargas | jdvargaz.com@gmail.com
- Colores primarios: negro (#0a0a0a), blanco (#ffffff), azul eléctrico (#0066ff)
- Tipografías sugeridas: Inter, Space Grotesk, o similares vía Google Fonts CDN

## Flujo de despliegue (OBLIGATORIO después de crear o editar)

Después de crear o modificar cualquier archivo de cliente, ejecutar:

```bash
git add .
git commit -m "Cliente [NombreCliente]: [descripción breve del cambio]"
git push origin main
```

Netlify desplegará automáticamente en ~30 segundos.

## URLs en producción
- Base: `https://jdvargaz-clientes.netlify.app/`
- Por cliente: `https://jdvargaz-clientes.netlify.app/NombreCliente/`
- Ejemplo: `https://jdvargaz-clientes.netlify.app/DonEli/`

## Clientes activos
| Cliente | Carpeta | URL |
|---|---|---|
| Don Elí Café | `DonEli/` | [/DonEli/](https://jdvargaz-clientes.netlify.app/DonEli/) |
| Laboratorio Dermatológico Saderma | `Saderma/` | [/Saderma/](https://jdvargaz-clientes.netlify.app/Saderma/) |

## Notas por cliente

### Saderma
La carpeta `Saderma/` no sigue la convención de un solo `index.html` autocontenido. Contiene un hub `index.html` que enlaza 7 dashboards independientes (análisis 360, Meta Ads, comparativa períodos, e-commerce, GA4, retorno/ROAS, infografía de marca). Cada dashboard es autocontenido y usa Chart.js vía CDN cuando aplica.
