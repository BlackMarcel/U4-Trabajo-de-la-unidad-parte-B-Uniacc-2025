# U4-Trabajo-de-la-unidad-parte-B-Uniacc-2025
Este es el repositorio para le trabajo de la unidad 4 Parte B, del ramo Taller de dispositivos moviles de la universidad Uniacc

---

📱 Mi Hábito – Aplicación Móvil Ionic/Angular

Proyecto desarrollado para la Unidad 3 y Unidad 4 del curso.
Incluye estructura completa de la aplicación, uso de componentes Ionic, navegación, estilos personalizados y generación del APK no firmado.


---

📝 Descripción General

Mi Hábito es una aplicación móvil creada con Ionic + Angular que permite al usuario registrar hábitos, visualizar su progreso diario, consultar estadísticas, obtener logros e ingresar a una sección de configuración.

El proyecto se desarrolló en dos entregas:

Entrega A: Creación del 50% inicial de la app (componentes, navegación y primeras pantallas).

Entrega B: Finalización del contenido, incorporación de nuevos componentes, mejoras visuales y generación del APK.

Este repositorio contiene:

Todo el código fuente

El APK no firmado, listo para instalación

---

🎯 Objetivos del Proyecto

Implementar correctamente componentes móviles de Ionic.

Construir una aplicación navegable con varias pantallas funcionales.

Completar cada fase con al menos dos componentes nuevos.

Aplicar estilos consistentes con diseño móvil.

Generar un APK instalable.

Documentar el proceso, dificultades y soluciones encontradas.
```bash
📂 Estructura del Proyecto
mi-habito/
│
├── src/
│   ├── app/
│   │   ├── inicio/
│   │   ├── dashboard/
│   │   ├── estadisticas/
│   │   ├── logros/
│   │   ├── configuracion/
│   │   └── habito-detalle/
│   ├── assets/
│   └── theme/
│
├── android/
│
├── capacitor.config.ts
├── package.json
├── README.md
└── ...
```

📌 El APK generado se encuentra en:
```bash
android/app/build/outputs/apk/debug/app-debug.apk
```


---

### 🧩 Componentes Ionic Utilizados
Entrega A

-ion-progress-bar

-ion-toggle

-Botones personalizados

-ion-content, ion-header, ion-toolbar

-Router + navegación programática

Entrega B

-ion-segment (filtro de estadísticas)

-Listas dinámicas con *ngFor

-Toast al completar hábito

-Corrección de estructura global (page-container y page-background)

-Eliminación completa del marco de teléfono

-Mejoras para Android/Emulador

---

▶️ Cómo Ejecutar el Proyecto
🛠 Requisitos
```bash
Node.js

Ionic CLI

Angular CLI

Capacitor
```
Android Studio

▶ Ejecutar en Navegador
```bash
npm install
ionic serve
``` 
▶ Ejecutar en Emulador Android
```bash
ionic build
npx cap sync android
npx cap open android
```


Luego, desde Android Studio:
Run ▶

---

📦 Cómo Generar el APK (no firmado)

Ejecutar:
```bash
ionic build
npx cap sync android
npx cap open android
```

En Android Studio:

```bash
Build → Build Bundle(s) / APK(s) → Build APK(s)
```

El archivo aparecerá en:

```bash
android/app/build/outputs/apk/debug/app-debug.apk
```

Este archivo está incluido en este repositorio.


---

🚧 Problemas Encontrados y Soluciones
🔹 1. Aparecía el “marco verde” del teléfono

Causa: Persistían clases antiguas (phone-frame, phone-notch).
Solución: Eliminar completamente esas capas y reemplazar con page-container y page-background.

🔹 2. Textos muy claros en Android

Solución: Forzar color global:

color: #264137 !important;

🔹 3. Cambios en VS Code no se reflejaban en el emulador

Solución:
```
ionic build
npx cap sync android
```

🔹 4. Botones actuaban como “submit”
```bash
Solución: agregar type="button".
```
🔹 5. Layout no ocupaba el ancho completo

Solución:
Quitar display:flex; align-items:center; del fondo y unificar diseño con .page-container.

📎 APK Incluido

El APK no firmado está disponible en:

```bash
/android/app/build/outputs/apk/debug/app-debug.apk
```

o dentro de:
```bash
/apk

👨‍💻 Autor

Iván Pareja
Ingeniería en Informática Multimedia – UNIACC (2025)
