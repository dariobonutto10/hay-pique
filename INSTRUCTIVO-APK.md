# Cómo obtener el APK de Hay Pesca con GitHub

El repositorio ya incluye un "robot" (GitHub Actions) que compila el APK solo. No necesitas instalar Android Studio.

## 1. Crear el repositorio
1. Entra en https://github.com e inicia sesión (o crea una cuenta gratis).
2. Toca **+ → New repository**.
3. Nombre: `hay-pesca`. Déjalo en **Public** (las Actions son gratis en repos públicos). No marques "Add a README".
4. Toca **Create repository**.

## 2. Subir los archivos
Descomprime `hay-pesca-github.zip`. Elige una opción:

**A) Desde el navegador (la más simple)**
1. En el repo nuevo toca **uploading an existing file**.
2. Arrastra TODO el contenido de la carpeta `hay-pesca` (incluida la carpeta `.github`, que puede estar oculta: en Windows activa "Elementos ocultos"; en Mac usa Cmd+Shift+.).
3. Abajo toca **Commit changes**.
4. Verifica que en el repo aparezca `.github/workflows/apk.yml`. Si falta, crea el archivo con **Add file → Create new file**, escribe la ruta `.github/workflows/apk.yml` y pega su contenido.

**B) Con Git**
```
cd hay-pesca
git init
git add .
git commit -m "Hay Pesca"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/hay-pesca.git
git push -u origin main
```

## 3. Compilar el APK
1. Ve a la pestaña **Actions** del repo. Si aparece un botón verde para habilitar los workflows, tócalo.
2. La subida ya dispara **Compilar APK**. También puedes tocar **Compilar APK → Run workflow → Run workflow**.
3. Espera entre 4 y 8 minutos. Un círculo amarillo significa que está trabajando; un check verde, que terminó.

## 4. Descargar el APK
1. Entra a la ejecución terminada (toca su nombre).
2. Baja hasta **Artifacts** y descarga **hay-pesca-apk** (es un .zip).
3. Descomprímelo: dentro está `app-debug.apk`.

## 5. Instalar en el Android
1. Pasa el APK al teléfono (cable, Drive, WhatsApp, correo) o descárgalo directo desde el teléfono.
2. Ábrelo. Android pedirá permitir **instalar apps desconocidas** para ese navegador o gestor de archivos: actívalo.
3. Si Play Protect avisa, toca **Instalar de todas formas** (es normal en APK que no vienen de Play Store).
4. Abre **Hay Pesca** y acepta el permiso de ubicación.

## Si algo falla
- **Cruz roja en Actions:** abre la ejecución, toca el paso en rojo y copia el error. Con ese texto se corrige rápido.
- **No aparece el workflow:** falta la carpeta `.github/workflows` en el repo (paso 2, punto 4).
- **El GPS no responde:** en Ajustes → Apps → Hay Pesca → Permisos, activa Ubicación.
- **No se actualiza al instalar una versión nueva:** desinstala la anterior primero. Ojo: se borran los piques guardados.

## Actualizar la app
Cada vez que cambies archivos y hagas commit en `main`, el robot compila un APK nuevo.

## Más adelante (opcional)
- Para publicar en Play Store necesitas un APK/AAB firmado con tu propia clave (se guarda como *Secret* del repo) y una cuenta de desarrollador.
- Esta versión es "debug": sirve para uso personal y pruebas.
