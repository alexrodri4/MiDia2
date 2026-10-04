# Mi Día 2

App personal de tareas, recordatorios y gastos, con Claude (IA) integrado.

- `index.html` — la app web completa (misma versión que el artefacto de Claude **Mi Día 2**: https://claude.ai/artifact/F254FBxX2EfK77pCuGoDde).
- **APK de Android** (`com.alexrodri.midia`, Android 10+): descárgalo de [Releases](https://github.com/alexrodri4/MiDia2/releases/latest).
- `android/` — código del proyecto Android (WebView + puente nativo) y `build_apk.sh` para compilarlo sin Gradle.
- `src-ia/` — las capas añadidas: `midia-ai.js/.css` (chat con Claude, escanear tickets, informe semanal), `apk-shim.js` (Claude con tu clave de API y voz nativa en la APK) y `apk-native.js` (notificaciones, widget, botón atrás).

## Funciones de IA
- Chat con Claude que conoce tus tareas, recordatorios y gastos y puede crear, tachar o borrar cosas (siempre con confirmación).
- Escanear un ticket con la cámara y apuntar el gasto.
- Informe semanal: bien, a mejorar, dinero y consejo.
- Asistente por voz.

En el artefacto Claude usa tu cuenta de claude.ai; en la APK, tu clave de API (Más → Claude (IA)). En GitHub Pages la IA no está disponible.

## APK
Notificaciones reales (tareas que vencen, recordatorios, víspera de fechas anuales, resumen diario) y widget de pantalla de inicio.
La clave de firma (`midia-release.keystore`) y su contraseña **no** están en el repositorio: hacen falta para publicar actualizaciones que se instalen encima.

Para compilar: `export MIDIA_KS_PASS='...'` (la contraseña de la keystore) y `bash android/build_apk.sh`.

## Licencia
MIT, ver [LICENSE](LICENSE).
