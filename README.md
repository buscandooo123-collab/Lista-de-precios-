# 🏷 Catálogo QR — Guía paso a paso

---

## PASO 1 — Crea el repositorio en GitHub

1. Ve a **github.com** → clic en **"New repository"**
2. Nombre: `mi-catalogo`
3. Déjalo en **Public**
4. **NO** actives ningún checkbox
5. Clic en **"Create repository"**
6. Copia la URL, ej: `https://github.com/sergio/mi-catalogo.git`

---

## PASO 2 — Sube el código

Abre la terminal, entra a esta carpeta y ejecuta:

```bash
git init
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/mi-catalogo.git
git push -u origin main
```

---

## PASO 3 — Obtén el Service Account de Firebase

1. Firebase Console → ⚙️ Configuración del proyecto
2. Pestaña **"Cuentas de servicio"**
3. Clic en **"Generar nueva clave privada"**
4. Te descarga un archivo `.json` — guárdalo

---

## PASO 4 — Agrega el Secret en GitHub

1. GitHub → tu repo → **Settings**
2. Menú izquierdo → **Secrets and variables → Actions**
3. **"New repository secret"**
4. Nombre: `FIREBASE_SERVICE_ACCOUNT`
5. Valor: abre el `.json` descargado, copia TODO el contenido y pégalo
6. **"Add secret"**

---

## PASO 5 — Primer deploy

```bash
npm install -g firebase-tools
firebase login
firebase deploy
```

---

## PASO 6 — De ahora en adelante es automático 🎉

```bash
git add .
git commit -m "Actualizo precios"
git push
# ← Firebase se actualiza solo en ~1 minuto
```

---

## Tu sitio:
- **Catálogo público:** `https://pagina-web-lista-de-productos.web.app`
- **Panel admin:**     `https://pagina-web-lista-de-productos.web.app/admin`
