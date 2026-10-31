# Git 2.56.0 para antiX 26.1 / Debian Trixie i386

![Git](https://img.shields.io/badge/Git-v2.56.0-orange)
![Platform](https://img.shields.io/badge/Platform-i386-blue)
![antiX](https://img.shields.io/badge/antiX-26.1-green)
![Debian](https://img.shields.io/badge/Debian-Trixie-red)
![License](https://img.shields.io/badge/License-GPLv2-yellow)

Paquete `.deb` de **Git v2.56.0** compilado para **antiX 26.1 / Debian Trixie (i386, 32 bits)**.

---

## 📋 Tabla de contenidos

- [Características](#-características)
- [Requisitos](#-requisitos)
- [Instalación rápida](#-instalación-rápida)
- [Instalación manual](#-instalación-manual)
- [Verificación](#-verificación)
- [Detalles de compilación](#-detalles-de-compilación)
- [Solución de problemas](#-solución-de-problemas)
- [Recompilar desde cero](#-recompilar-desde-cero)
- [Licencia](#-licencia)

---

## ✨ Características

- ✅ Git **v2.56.0** (última versión estable al momento de compilar)
- ✅ Compilado para **i386 (32 bits)**
- ✅ Incluye **Rust** compilado para i686
- ✅ Empaquetado como **.deb** instalable con `dpkg`
- ✅ Compatible con **glibc 2.41** (Debian Trixie)

---

## 📦 Requisitos

- **antiX 26.1** (o Debian Trixie i386)
- **Arquitectura i386** (32 bits)
- **glibc 2.41** o superior
- Dependencias: `libc6`, `libssl3`, `zlib1g`, `libcurl4`, `libexpat1`

---

## 🚀 Instalación rápida

```bash
wget https://github.com/JOSSEL01/debian-git-x32/raw/main/packages/git_2.56.0-1_i386.deb
sudo dpkg -i git_2.56.0-1_i386.deb
sudo apt install -f   # resuelve dependencias si faltan
git --version
```

Deberías ver: `git version 2.56.0`

---

## 🔧 Instalación manual

1. Descarga el `.deb` desde la carpeta `packages/`.
2. Instálalo:
   ```bash
   sudo dpkg -i git_2.56.0-1_i386.deb
   ```
3. Verifica:
   ```bash
   git --version
   ```

---

## ✅ Verificación

```bash
git --version
# Salida esperada: git version 2.56.0

file $(which git)
# Salida esperada: ELF 32-bit LSB executable, Intel 80386...

dpkg -l | grep git
# Debe mostrar el paquete git instalado
```

---

## 🛠️ Detalles de compilación

| Parámetro | Valor |
|---|---|
| **Versión de Git** | 2.56.0 |
| **Sistema anfitrión** | antiX 26.1 (Debian Trixie) i386 |
| **Arquitectura objetivo** | i386 (32 bits) |
| **glibc** | 2.41 |
| **Rust** | Con target `i686-unknown-linux-gnu` |
| **Empaquetado** | checkinstall |

---

## 🐛 Solución de problemas

### Error: dependencias sin satisfacer

```bash
sudo apt install -f
```

### Error: `libssl.so.3: cannot open shared object file`

```bash
sudo apt install libssl3
```

### Error: `libcurl.so.4: cannot open shared object file`

```bash
sudo apt install libcurl4
```

### Error: `libexpat.so.1: cannot open shared object file`

```bash
sudo apt install libexpat1
```

---

## 🔨 Recompilar desde cero

Usa el script `build_git_debian_x32.sh` incluido en este repositorio:

```bash
chmod +x build_git_debian_x32.sh
./build_git_debian_x32.sh
```

El script **detecta automáticamente la última versión estable de Git** desde kernel.org y la compila.

---

## 📄 Licencia

Git es software libre bajo la [licencia GPLv2](https://github.com/git/git/blob/master/COPYING).

---

## 📞 Contacto

- **Autor:** Jose Andres Mamani Mollericona
- **GitHub:** [@JOSSEL01](https://github.com/JOSSEL01)
- **Repositorio:** [debian-git-x32](https://github.com/JOSSEL01/debian-git-x32)
