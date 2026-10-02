# Claim to Close: Georgia — versión "flyer exacto"

`index.html` + `assets/`. Estructura de arriba a abajo:
1. `assets/flyer-top.jpg` — flyer 1 tal cual, cortado justo antes del botón naranja.
2. `<section id="registro">` — formulario sobre fondo que continúa el flyer (humo lateral recortado del mismo flyer + brasas en CSS).
3. Botón grande "RESERVA TU LUGAR" (submit) con la forma/color del flyer.
4. `assets/flyer-info.jpg` — la franja de fecha · BRS Roofing Supply · Roofing en Español, tal cual del flyer (link a Google Maps).
5. `assets/flyer-footer.jpg` — flyer 2 completo como footer (el "RESERVÁ TU LUGAR" del flyer es clickeable y sube al formulario).

Preview: `python3 -m http.server 3008 --directory claim-to-close-flyer` (launch config `claim-to-close-flyer`).

GHL: reemplazar el `<form id="regForm">` (marcado con comentario) por el embed, o apuntar el `fetch()` del script al webhook. Meta Pixel: pegar en `<head>`; el submit dispara `fbq('track','Lead')`.
Si cambia el flyer, re-cortar con los mismos rangos: top 0–1046, info 1232–1500, humo lateral x 0–130 y 995–1125 (y 1046–1240) del PNG de 1125×1500.

## Cambios 2026-09-03 (tarde)
- Se quitó la franja de fecha/BRS bajo el formulario (ya está en el flyer 2 del footer).
- Botón "RESERVA TU LUGAR" = réplica CSS del botón del flyer (#e74924, radio ~37% de la altura, glow naranja). Es el submit real.
- Debajo del formulario: "Qué vas a vivir" (8 puntos), tarjeta "El Claim en Vivo", bloque de testimonio y segundo CTA.
- VIDEO TESTIMONIO: guardar como `assets/testimonio.mp4` (H.264, con subtítulos quemados). El `<video>` ya apunta ahí; el poster es `assets/testimonio-poster.jpg`.

## Live
https://siberianvito.github.io/claim-to-close-georgia/ — repo github.com/siberianvito/claim-to-close-georgia (GitHub Pages, branch main). Para publicar cambios: `git add -A && git commit -m "..." && git push`.

## 2026-10-01 — Sitio convertido a WEBINAR GRATIS (Claim to Close Virtual)
- Jueves 8 de octubre 2026, 12–2 PM ET, virtual, 100% GRATIS. Fuente: `~/Downloads/Claim_to_Close_SMS_Email_Campaign_Oct8_FINAL_LINKS.pdf`.
- Página: flyer top (igual) → ticker → hero "¿Te perdiste Claim to Close Georgia?" + chips + countdown → form GHL (mismo) → temas → "Tus preguntas, respondidas en vivo" → 3 pasos → testimonio → CTA → flyer 2 recortado (sin fecha/BRS) + tarjeta de fecha del webinar.
- Popup post-registro → nuevo grupo WhatsApp: https://chat.whatsapp.com/I1rFvQDW2kZ95p3XBFbBgz?mode=gi_t (solo se muestra después de registrarse).
- Imagen para compartir / emails: `assets/webinar.jpg` (también es el og:image).
- Versión del evento presencial guardada en el tag git `evento-presencial-sep26`.
- Pendiente en GHL (no en el sitio): agregar al form la pregunta "¿Tenés actualmente algún reclamo en el que necesitás ayuda?" (Sí / Tengo un cliente con preguntas / No, quiero aprender más); enlace real de la reunión; enlaces de consulta/referido.
