# Support Hub — Last.app

Página pública del equipo de Soporte. Accesible para todos los empleados de Last.app sin login.

**URL:** `https://[tu-usuario].github.io/support-hub/`

---

## Cómo actualizar el contenido

Todo el contenido editable está en el bloque `const HUB = { ... }` al principio de `index.html`.

### Cambiar la guardia de la semana

```js
guardia: {
  semana: "19 – 23 mayo 2026",   // ← cambia las fechas
  personas: [
    {
      nombre: "Angie Oliveros",   // ← nombre del agente
      rol: "Guardia principal",
      badge: "Esta semana",
      badgeClass: "badge-green",  // badge-green / badge-blue / badge-purple
      color: "#6366F1"            // color del avatar
    },
    ...
  ]
}
```

### Añadir un aviso

Añade un objeto al array `avisos`:

```js
{
  titulo: "Título del aviso",
  fecha: "21 may",
  cuerpo: "Texto del aviso...",
  tag: "Importante",            // texto del tag
  tagClass: "tag-action"        // tag-info / tag-warning / tag-action / tag-ok
}
```

### Actualizar las cifras del desk

```js
desk: {
  stats: [
    { num: "42",  label: "Tickets hoy" },
    { num: "32",  label: "Cerrados" },
    { num: "10",  label: "Pendientes" }
  ],
  ultimaActualizacion: "20 may — 17:00"   // ← actualiza esto
}
```

---

## Publicar cambios

1. Edita `index.html`
2. Haz commit y push a `main`
3. GitHub Pages lo publica en ~30 segundos

```bash
git add index.html
git commit -m "Update: guardia semana 26-30 mayo"
git push
```
