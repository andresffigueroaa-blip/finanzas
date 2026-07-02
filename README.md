# 💰 MisFinanzas PE — v2 PRO

> Aplicación web de gestión financiera personal, hecha para el contexto peruano (S/). Controla tus ingresos, gastos, deudas de tarjeta, pasivos, patrimonio y metas — con score de salud financiera, plan para salir de deudas, regla 50/30/20, radar de suscripciones, calculadoras peruanas (CTS, grati, sueldo neto) y asesor con IA. Con **cuenta propia y sincronización en la nube**.

🔗 **App en vivo:** [https://andresffigueroaa-blip.github.io/finanzas/](https://andresffigueroaa-blip.github.io/finanzas/)

---

## ✨ Novedades de la v2 PRO

Inspiradas en lo mejor de YNAB, Monarch Money, Rocket Money, PocketGuard y Copilot — adaptadas al Perú:

- 💯 **Score de salud financiera (0-100)** en el Inicio: 6 pilares (tasa de ahorro, deuda de tarjetas, colchón de emergencia, disciplina de presupuesto, gasto hormiga y diversificación de ingresos) que se recalculan con cada movimiento, con tu mayor oportunidad de mejora señalada.
- 🧭 **Plan para salir de deudas** (pestaña Tarjetas): simula método **avalancha** (primero la TCEA más alta) vs **bola de nieve** (primero la deuda más chica). Te dice en cuántos meses quedas libre, cuánto pagarás de intereses y cuánto ahorras con cada método.
- 💳 **Resumen global de deuda**: deuda total, % de uso de tus líneas, interés mensual estimado según TCEA y tarjetas en riesgo (>30%).
- ⚖️ **Regla 50/30/20** (Analítica): necesidades / deseos / ahorro del mes vs el estándar. Cada gasto se clasifica solo por categoría, o tú lo defines al registrarlo.
- 🔁 **Radar de suscripciones**: detecta cobros recurrentes en tus pasivos y gastos y te muestra su costo real al año.
- 🏦 **Patrimonio neto**: registra tus activos (cuentas, efectivo, inversiones, CTS, cripto) y la app suma tus metas y cuentas por cobrar, resta deudas de tarjeta y cuotas pendientes → tu foto financiera real.
- 🧰 **Herramientas Perú**: sueldo bruto → neto (AFP/ONP + renta de 5ta con UIT editable, 2026: S/ 5,500), gratificación (con bono 9% EsSalud), CTS, costo real de comprar en cuotas según TCEA, conversor S/ ⇄ US$ y fondo de emergencia ideal según tu gasto real.
- 🌐 **Multi-idioma (ES/EN)** y **moneda de vista** en soles o dólares (con tipo de cambio configurable; los datos siempre se guardan en S/).
- 🤖 **IA mejorada**: el asesor ahora recibe TODO tu contexto (tarjetas con TCEA y uso, pasivos, suscripciones, patrimonio, score, fuentes de ingreso) y entrega diagnóstico + plan de acción de 30 días + "jugada maestra". Además puedes **chatearle preguntas libres** ("¿qué tarjeta pago primero?").
- 📉 **Más categorías**: 21 de gasto (Delivery, Servicios, Celular, Mascotas, Ropa, Viajes, Deudas, Ahorro e inversión...) y 10 de ingreso (Chambita extra, Negocio propio, Inversiones, Bonos y gratificaciones...). Cada gasto acepta etiqueta libre (ej: `viaje-cusco`).
- 📄 **Exportar CSV** para abrir en Excel, además del respaldo JSON.

Todo es **compatible con tus datos existentes**: la migración agrega los campos nuevos sin tocar lo que ya registraste en la nube.

---

## ✨ Características base

- 🔐 Cuenta propia (correo y contraseña) + ☁️ sincronización en la nube (Firebase).
- 📊 Dashboard con saldo neto, salud financiera y compromiso del mes.
- 💵 Ingresos, 🧾 gastos con método de pago, 📌 pasivos (recurrentes, cuotas, variables).
- 💳 Tarjetas con línea, TCEA, cierre y fecha de pago, con alertas.
- 🤝 Me deben, 🎯 metas de ahorro con proyección por regresión lineal.
- 📈 Analítica: KPIs, insights, anomalías (z-score), gasto hormiga, heatmap, presupuestos.
- 🏢 Modo empresa, 🌗 modo claro/oscuro, 📴 funciona sin conexión.

---

## 🛠️ Stack

HTML + JS vanilla · Tailwind (CDN) · Chart.js (CDN) · Firebase Auth + Firestore · un solo `index.html`.

## 📦 Despliegue

Igual que antes: sube `index.html` a tu repo con GitHub Pages activado. Las reglas de Firestore recomendadas no cambian.

> ⚠️ Las calculadoras son referenciales: verifica tasas y comisiones vigentes con tu banco, AFP o SUNAT.

---

Hecho por **Andrés Figueroa** (AEs · By Vigorr) — Ingeniero de infraestructura & analista de datos 🇵🇪

<p align="center"><em>Ordenar las finanzas a los 20s cambia todo el resto del juego. 📈</em></p>
