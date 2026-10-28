# ListWise — Generador de descripciones de productos con IA

**URL de producción:** https://listwise-app.onrender.com

Sube un CSV con tus productos y la IA genera automáticamente títulos optimizados para SEO, 5 bullet points de beneficios y una descripción persuasiva lista para usar en cualquier marketplace.

🎥 ## Demo en vídeo
<div align="center"> <a href="https://youtu.be/yd3wz8xNh0s"> <img src="https://drive.google.com/thumbnail?id=1mEGZOwI6ueXFlGTWxKGrVyRQtb5xesFc&sz=w1000" width="400" alt="Haz clic para ver la demo de ListWise"> </a> <br> <a href="https://youtu.be/yd3wz8xNh0s"><b>▶️ Pulsa aquí para ver la demo en vídeo</b></a> </div>

---

## Uso rápido 

1. Crea una cuenta en https://listwise-app.onrender.com/sign-up
2. Ve al Dashboard
3. Sube un archivo CSV con la columna `productName` (opcionales: `category`, `attributes`)
4. Espera unos segundos — los productos se procesan automáticamente
5. Haz clic en **Editar** para ver y modificar el contenido generado

Puedes descargar un CSV de demostración en `/demo.csv` para probar la herramienta.

### Formato del CSV

```csv
productName,category,attributes
Camiseta de algodón,Ropa,"{""color"":""Blanco"",""talla"":""M""}"
```

| Columna | Requerida | Descripción |
|---|---|---|
| `productName` | Sí | Nombre del producto |
| `category` | No | Categoría (Ropa, Electrónica, Hogar…) |
| `attributes` | No | JSON con atributos adicionales |

---

## Tecnologías

| Capa | Tecnología |
|---|---|
| Frontend | Next.js 15 (App Router), React 19, Tailwind CSS |
| Autenticación | Clerk |
| Base de datos | Turso (libSQL) + Drizzle ORM |
| IA | Groq — llama-3.3-70b-versatile |
| Jobs en background | Trigger.dev v4 |
| Pagos | Stripe |
| Rate limiting | Upstash Redis |
| Despliegue | Render |

---

## Variables de entorno necesarias

```
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY
CLERK_SECRET_KEY
TURSO_DATABASE_URL
TURSO_AUTH_TOKEN
GROQ_API_KEY
TRIGGER_SECRET_KEY
UPSTASH_REDIS_REST_URL
UPSTASH_REDIS_REST_TOKEN
STRIPE_SECRET_KEY
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY
STRIPE_WEBHOOK_SECRET
```

---

## Planes

| Plan | Productos/mes | Precio |
|---|---|---|
| Gratuito | 20 | 0€ |
| Pro | 1200 | 29€/mes |
| Empresa | 5000 | 99€/mes |
