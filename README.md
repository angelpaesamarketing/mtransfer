# M Transfer Ibiza — versión blanca

Sitio estático de una sola página (`index.html` + `img/`). No necesita
proceso de build.

## Despliegue en Cloudflare Pages

Workers & Pages → Create → Pages → Connect to Git → este repositorio.

| Ajuste                    | Valor                   |
| ------------------------- | ----------------------- |
| Framework preset          | None                    |
| Build command             | *(vacío)*               |
| Build output directory    | `/`                     |
| Root directory            | `/`                     |

Cada push a la rama de producción publica una nueva versión; el resto de
ramas generan previews.

`_headers` define el cacheado: las imágenes son inmutables durante un año
y el HTML se revalida en cada visita.

## Hero showroom

El hero es una órbita de vehículos movida por el scroll nativo dentro de
una sección con `position:sticky`. Se controla con scroll, arrastre,
flechas, los botones numerados y el teclado.

El pie incluye un conmutador «Reducir movimiento / Activar animaciones».
Respeta `prefers-reduced-motion`, pero permite activar las animaciones
igualmente (en Windows es habitual tener «Mostrar animaciones» apagado) y
recuerda la elección en `localStorage`.
