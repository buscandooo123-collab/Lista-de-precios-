# Catálogo QR — Sitio Público

## ¿Cómo conectar con GitHub?

### Paso 1 — Sube estos archivos a tu repo de GitHub
Sube todos los archivos de esta carpeta a la rama `main` de tu repositorio.

### Paso 2 — Obtén el Service Account de Firebase
1. Ve a [console.firebase.google.com](https://console.firebase.google.com)
2. Tu proyecto → ⚙️ Configuración → **Cuentas de servicio**
3. Clic en **"Generar nueva clave privada"**
4. Se descarga un archivo `.json` — ábrelo con el Bloc de notas y copia TODO el contenido

### Paso 3 — Agrega el Secret en GitHub
1. Ve a tu repo en GitHub
2. **Settings → Secrets and variables → Actions**
3. Clic en **"New repository secret"**
4. Nombre: `FIREBASE_SERVICE_ACCOUNT`
5. Valor: pega el contenido del `.json` del paso anterior
6. Clic en **"Add secret"**

### Paso 4 — Activa GitHub Actions
GitHub Actions se activa automáticamente. Cada vez que hagas un `push` a `main`, el sitio se despliega solo en ~1 minuto.

### URL de tu sitio
```
https://pagina-web-lista-de-productos.web.app
```

---
El panel admin (`ADMIN-LOCAL.html`) va **solo en tu laptop**, nunca lo subas al repo.
