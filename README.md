# Tracking-Proyectos

App de escritorio para Windows 11 que lleva el registro de mis proyectos personales, estén en la carpeta que estén.

**[⬇ Descargar la última versión](https://github.com/BMarquinaProyects/tracking-proyectos-app/releases/latest)**

## Qué hace

- **Estados claros**: cada proyecto está Activo, En pausa, Idea, Terminado, Versión anterior o Descartado.
- **Detecta sola la actividad**: lee el último commit de git y las fechas de modificación de los archivos. No hay que apuntar nada a mano.
- **Pausa automática**: si un proyecto activo lleva 4 días sin tocarse, avisa; a los 7 días lo pasa a En pausa (los días se cambian en Ajustes).
- **Sugiere retomar**: si un proyecto en pausa vuelve a tener actividad, propone reactivarlo. Nunca lo hace por su cuenta.
- **Encuentra las carpetas movidas**: identifica cada carpeta por su ID de Windows y por un pequeño marcador oculto, así que sigue al proyecto aunque lo cambies de sitio.
- **Vista de actividad**: tabla de los últimos 14 días, proyectos recientes y un mapa de actividad de 26 semanas por proyecto.
- **Abrir en un clic**: carpeta, VS Code o terminal (Warp, Windows Terminal o PowerShell).
- **Versiones enlazadas**: "Hacer nueva versión" crea el proyecto nuevo (copiando la carpeta, vacía o una existente) y deja el anterior en Versiones anteriores.
- **Sin ruido**: los avisos van en una campana dentro de la app. Sin notificaciones de Windows, sin icono en la bandeja y sin procesos en segundo plano.

## Instalación

1. Descarga `Tracking-Proyectos-2.0.0-setup.exe` desde [Releases](https://github.com/BMarquinaProyects/tracking-proyectos-app/releases/latest).
2. Ábrelo. Como el instalador no tiene firma digital de pago, Windows puede mostrar **"Windows protegió su PC"**: pulsa **Más información → Ejecutar de todas formas**.
3. Se instala para tu usuario (no pide permisos de administrador) y se abre al iniciar Windows. Puedes desactivarlo en Ajustes.

Requisitos: Windows 11 de 64 bits. Para leer los commits hace falta tener [Git](https://git-scm.com/) instalado; sin él, la app usa solo las fechas de los archivos.

## Privacidad

Todo se queda en tu PC. Los datos se guardan en `%APPDATA%\TrackingProyectos` con copias de seguridad diarias de los últimos 7 días. La app no envía nada a internet. Fuera de su carpeta de datos solo escribe tres cosas: el marcador oculto `.proyecto-id` en cada carpeta registrada, una línea en `.git/info/exclude` para que git lo ignore, y la carpeta de una nueva versión cuando la creas tú.

## Tecnología

Electron · React · TypeScript · Vite · Vitest (135 tests) · electron-builder

El código fuente es privado.
