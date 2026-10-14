# JoeTV para computadora

Descargas de la app de escritorio de JoeTV. Se entra con la misma cuenta de la app de TV.

**[⬇ Descargar la versión más reciente](https://github.com/josemasri/joetv-descargas/releases/latest)** ·
[Todas las versiones](https://github.com/josemasri/joetv-descargas/releases)

| Sistema | Archivo |
| --- | --- |
| macOS 11 o más nuevo, con chip de Apple (M1 o posterior) | `JoeTV_<versión>_macOS_AppleSilicon.dmg` |
| Linux x86_64 (Ubuntu 22.04 o más nuevo, o equivalente) | `JoeTV_<versión>_Linux_x86_64.AppImage` |
| Linux ARM64 | `JoeTV_<versión>_Linux_arm64.AppImage` |
| Windows | Próximamente |

## Instalar

### macOS

1. Abre el `.dmg` y arrastra **JoeTV** a **Aplicaciones**.
2. La primera vez, macOS no la deja abrir porque la app todavía no está firmada por Apple.
   Ve a **Ajustes del Sistema → Privacidad y seguridad**, baja hasta el aviso de JoeTV y elige
   **Abrir de todos modos**.
3. Si macOS dice que «está dañada», abre la Terminal y escribe:

   ```sh
   xattr -dr com.apple.quarantine /Applications/JoeTV.app
   ```

### Linux

```sh
chmod +x JoeTV_*_Linux_x86_64.AppImage
./JoeTV_*_Linux_x86_64.AppImage
```

Si no abre por FUSE, instala `libfuse2` (en Ubuntu 24.04 se llama `libfuse2t64`). También se
puede abrir sin FUSE con `--appimage-extract-and-run`.

## Comprobar la descarga

Cada versión trae `SHA256SUMS.txt`:

```sh
shasum -a 256 -c SHA256SUMS.txt --ignore-missing
```

## Licencias

El video se reproduce con libmpv y FFmpeg, compilados sin partes GPL y distribuidos bajo la
LGPL. Cada versión trae `JoeTV_<versión>_fuentes-LGPL.tar`, con sus fuentes exactas y la receta
para compilarlos. Todas las licencias del software de terceros están en la app, en
**Ajustes → Acerca de → Licencias de software**.
