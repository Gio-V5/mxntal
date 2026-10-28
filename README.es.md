<p align="center"><img src="docs/brand/mxntal-logo-128.png" width="96" height="96" alt="Mxntal"></p>
<h1 align="center">Mxntal</h1>
<p align="center"><strong>Lavora nell'ombra. Tu giochi.</strong> · Trabaja en la sombra. Tú juegas.</p>
<p align="center">
  <a href="https://github.com/Gio-V5/mxntal/releases/latest"><img src="https://img.shields.io/github/v/release/Gio-V5/mxntal?label=versi%C3%B3n&color=8A4FD8" alt="Última versión"></a>
  <a href="https://github.com/Gio-V5/mxntal/releases"><img src="https://img.shields.io/github/downloads/Gio-V5/mxntal/total?label=descargas&color=8A4FD8" alt="Descargas"></a>
</p>
<p align="center"><a href="README.md">English</a> · <a href="README.it.md">Italiano</a> · <strong>Español</strong> · <a href="README.fr.md">Français</a></p>

Mxntal optimiza Windows 10 y 11 sin cajas negras: cada cambio tiene un motivo escrito, una copia de
seguridad del valor anterior y una restauración con un clic. Es un solo archivo, `MxntalTweaks.bat`, con
una interfaz gráfica y, para quien los prefiera, los menús clásicos de consola. Nada que instalar. La
interfaz está en italiano.

![La página Ottimizza de Mxntal](docs/screenshot-ottimizza.png)

## Descarga e inicio

1. Descarga la última versión: **[MxntalTweaks.bat](https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat)**
   (unos 640 KB).
2. Doble clic: Windows pide permisos de administrador y se abre la ventana. Si los rechazas, Mxntal se
   cierra sin cambiar nada.
3. En el primer inicio Windows puede avisar de que el editor es desconocido: pasa con cualquier archivo
   `.bat` descargado de internet.

Requisitos: Windows 10 u 11 con una cuenta de administrador; Windows PowerShell 5.1 (ya incluido en
Windows); para la página App, winget ("Instalador de aplicación" de Microsoft Store).

## Qué hace

- **Panoramica** (resumen): un chequeo con puntuación y las cosas por arreglar, cada una con el botón
  para hacerlo; CPU, memoria, tarjeta gráfica y disco en tiempo real; la ficha del PC.
- **Ottimizza** (optimizar): 36 ajustes en 7 categorías (energía y CPU; gaming y entrada; Windows e
  interfaz; inicio, RAM y segundo plano; disco y servicios; internet y red; avanzados). Cada ajuste explica
  qué cambia, los arriesgados piden confirmación; "aplicar los seguros" y "restaurar categoría" lo hacen
  todo de una vez.
- **Profili**: perfiles rápidos, Gaming y Trabajo.
- **App**: 106 programas comunes en 10 categorías (navegadores, gaming, periféricos, comunicación, multimedia, oficina, utilidades, seguridad, diagnóstico, desarrollo), instalados con winget desde los paquetes oficiales de los fabricantes. Con buscador, y los que ya están en el PC aparecen marcados.
- **Pulizia** (limpieza): archivos inútiles (temporales, volcados, registros y, si lo eliges, la
  Papelera), medidos antes de quitarlos; apps preinstaladas (43 en la lista), quitadas para el usuario
  actual y recuperables con un clic; programas que arrancan con Windows.
- **Backup**, la máquina del tiempo: cada valor guardado con su restauración, los puntos de restauración
  de Windows, el reinicio programado.
- **Miti** (mitos desmontados): los tweaks famosos que Mxntal no aplica, y por qué.

## Lo que nunca toca

- Microsoft Store, Windows Update, Optimización de entrega, servicios Xbox, Xbox Game Bar y grabación
  Game DVR.
- Nada de tweaks placebo: Win32PrioritySeparation, NetworkThrottlingIndex, HPET y similares quedan fuera;
  la página de mitos explica por qué.
- Los ajustes que Windows protege con el controlador UCPD (por ejemplo los Widgets en algunos PC): Mxntal
  no lo elude, explica el bloqueo y señala la alternativa que Windows permite.
- En un PC unido a un dominio el DNS sigue siendo el de la empresa, y los ajustes delicados (indexación,
  protecciones de seguridad, exclusiones de Defender, TCP) explican el motivo y piden confirmación.

## Copia de seguridad y restauración

- Antes de cada cambio el valor original va a `%LOCALAPPDATA%\MxntalTweaks\Backup\originali`, un archivo
  por valor, y sigue siendo el anterior a Mxntal aunque apliques un ajuste varias veces.
- Cada escritura se vuelve a leer: si el valor no es el esperado, Mxntal lo dice y el ajuste queda
  marcado como fallido.
- Restaurar desde la ventana: Backup, un valor cada vez o todos juntos; Ottimizza, apaga el interruptor o
  "Ripristina categoria"; Pulizia, "Rimetti le app tolte". En la consola: menú 9.
- El registro en `%LOCALAPPDATA%\MxntalTweaks\MxntalTweaks.log` anota fecha, acción, valor antes y
  después, y el resultado.
- Solo la limpieza de archivos no tiene vuelta atrás: por eso Mxntal mide antes y pide confirmación.

## Actualizaciones

En cada inicio, y cada hora mientras sigue abierta, la ventana comprueba si hay una versión nueva (una
petición HTTPS de 1 KB, sin enviar datos) y la instala con un clic, solo si está firmada. El botón
**Controlla aggiornamenti** comprueba al momento; "Non controllare più gli aggiornamenti" apaga la
comprobación automática. Las novedades de cada versión están en el [changelog](CHANGELOG.en.md) (en
inglés).

## Consola clásica

| Comando | Qué hace |
|---|---|
| `MxntalTweaks.bat /console` | los menús clásicos de consola, con permisos de administrador |
| `MxntalTweaks.bat /dryrun` | vista previa: muestra qué cambiaría, no toca nada y no pide permisos |
| `MxntalTweaks.bat /doctor` | diagnóstico del entorno: admin, Windows, PowerShell, herramientas, espacio, copias |
| `MxntalTweaks.bat /verify` | estado de cada ajuste y comprobación de las copias, solo lectura |
| `MxntalTweaks.bat /?` | lista de modos |

Desde la ventana, el botón "Console classica" abajo a la derecha abre los mismos menús. Si la interfaz
gráfica no puede arrancar (por ejemplo PowerShell en modo restringido en un PC de empresa), se abren los
menús de consola.

## Problemas e ideas

Abre una [issue](https://github.com/Gio-V5/mxntal/issues) con tu versión de Mxntal y, si sirve, las
líneas del registro sobre el problema. En italiano, inglés o español.
