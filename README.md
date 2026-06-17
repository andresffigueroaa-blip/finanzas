# 💰 MisFinanzas PE

> Aplicación web de gestión financiera personal, hecha para el contexto peruano (S/). Controla tus ingresos, gastos, deudas de tarjeta, cuentas por cobrar y metas de ahorro — todo desde un solo lugar, con gráficos que te ayudan a tomar mejores decisiones. Ahora con **cuenta propia y sincronización en la nube**: entra desde tu PC, tu celular o cualquier dispositivo y sigue justo donde lo dejaste.

🔗 **App en vivo:** [https://andresffigueroaa-blip.github.io/finanzas/](https://andresffigueroaa-blip.github.io/finanzas/)

---

## ✨ Características

- 🔐 **Cuenta propia** — inicia sesión con correo y contraseña; tus datos te siguen a todos tus dispositivos.
- ☁️ **Sincronización en la nube** — edita en la PC y aparece en el cel (y al revés), automáticamente.
- 📊 **Dashboard** con saldo neto, ingresos, gastos y un indicador de salud financiera (🟢🟡🔴).
- 💵 **Ingresos** — registra sueldo de planilla, recibos por honorarios (4ta) y freelance.
- 🧾 **Gastos** — categorizados, con método de pago y filtros por mes.
- 💳 **Tarjetas y deudas** — seguimiento de línea usada, fechas de pago y alertas.
- 🤝 **Me deben** — cuentas por cobrar que se saldan con un clic.
- 🎯 **Metas de ahorro** — con barras de progreso (ej. inicial de depa, TOEFL).
- 📈 **Analítica** — tasa de ahorro, tendencias, proyecciones y detección de gasto hormiga.
- 🌗 **Modo claro / oscuro.**
- 💾 **Exportar / Importar** tus datos en JSON (respaldo adicional).
- 📴 **Funciona sin conexión** — guarda localmente y sube los cambios cuando vuelve el internet.

---

## 🚀 Cómo usarla

No necesitas instalar nada. Solo abre el link:

👉 **[https://andresffigueroaa-blip.github.io/finanzas/](https://andresffigueroaa-blip.github.io/finanzas/)**

1. La primera vez, pulsa **"Crear cuenta nueva"** con tu correo y una contraseña.
2. Ya dentro, registra tus finanzas como siempre.
3. Desde otro dispositivo (cel, laptop, etc.), abre el mismo link e **inicia sesión** con ese correo: verás todo igualito.

> 💡 **Tip:** guárdala en favoritos para entrar siempre rápido.
> ⚠️ Evita editar en dos dispositivos al mismo tiempo: gana el último que guarda.

---

## 🔒 Privacidad y seguridad

- Para entrar a tu perfil hace falta **tu correo + tu contraseña**. Nadie más ve tus datos.
- Cada usuario tiene un identificador único (`uid`) y sus datos viven en su propio documento. Las **reglas de seguridad de Firestore** garantizan que cada quien solo pueda leer y escribir lo suyo.
- Las claves del bloque `firebaseConfig` en el código **no son secretas** (así lo diseñó Google): solo identifican el proyecto. La seguridad real la dan el login y las reglas, no esconder el código.

### Reglas de Firestore recomendadas

Cada usuario accede solo a su propio documento:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /usuarios/{uid} {
      allow read, write: if request.auth != null && request.auth.uid == uid;
    }
  }
}
```

Si quieres que **solo tú** puedas usar la app (que nadie más pueda ni registrarse y guardar datos), reemplaza `request.auth.uid == uid` por `request.auth.uid == "TU_UID"`, con tu uid copiado de **Authentication → Users**.

---

## 🛠️ Stack técnico

- **HTML + JavaScript vanilla** (sin frameworks pesados)
- **Tailwind CSS** (vía CDN) para el diseño
- **Chart.js** (vía CDN) para los gráficos
- **Firebase Authentication** para el login con correo/contraseña
- **Cloud Firestore** para guardar y sincronizar los datos en la nube
- **localStorage** como caché local (funciona offline)
- Un solo archivo `index.html` — fácil de leer, mantener y desplegar

---

## 📦 Desplegar tu propia versión

1. Haz un fork o descarga este repo.
2. Crea un proyecto en [Firebase](https://console.firebase.google.com):
   - Activa **Authentication → Correo electrónico/contraseña**.
   - Crea una base de datos **Firestore** y publica las reglas de arriba.
3. En **⚙️ Configuración del proyecto → Tus apps → web (`</>`)**, copia tu `firebaseConfig` y pégalo en el bloque marcado con ⚠️ dentro de `index.html`.
4. Sube el `index.html` a tu repo y activa **GitHub Pages** en `Settings → Pages → Deploy from a branch → main → /(root)`.
5. ¡Listo! Tu app estará en `https://tu-usuario.github.io/tu-repo/`.

---

## 👤 Autor

Hecho por **Andrés Figueroa** (AEs · By Vigorr) — Ingeniero de infraestructura & analista de datos 🇵🇪

---

<p align="center">
  <em>Ordenar las finanzas a los 20s cambia todo el resto del juego. 📈</em>
</p>
