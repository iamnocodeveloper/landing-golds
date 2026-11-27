# Golds — landing demo

Landing de una página para **Golds**, gimnasio en Costa Rica (WhatsApp +506 8868 8785).
Demo de referencia hecha por Nocodeveloper. **Los datos son de ejemplo**; los únicos datos
reales son el nombre del negocio, el número de WhatsApp y la calificación de Google
(4.9 con 143 reseñas).

## Contenido
- Portada con foto, CTAs a planes y a WhatsApp.
- Planes mensual / trimestral / anual con precios de ejemplo en colones.
- Clases (fuerza, funcional, cardio HIIT, spinning, pesas libres) y horario semanal de ejemplo.
- Cómo funciona la membresía: alta, pago (SINPE Móvil / tarjeta / efectivo), carné digital
  y recordatorio automático antes del vencimiento.
- Formulario de prueba gratis que arma un mensaje de WhatsApp con nombre, teléfono y día.
- Entrenadores y reseñas de ejemplo, FAQ y pie con aviso de demo.

## Estructura
```
index.html      página autocontenida (CSS y JS inline)
assets/         fotos recomprimidas con PIL (Unsplash, uso libre)
Dockerfile      nginx:alpine sirviendo site/
nginx.conf      gzip, caché de assets, fallback a index.html
```

## Local
```bash
docker build -t golds-demo .
docker run --rm -p 8080:80 golds-demo
```

## Deploy
App `clientes/demo-golds` en EasyPanel, dominio
`clientes-demo-golds.rddxeh.easypanel.host`, puerto 80, Dockerfile en la raíz.
