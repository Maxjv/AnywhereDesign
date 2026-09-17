<div align="center">

# AnywhereDesign by TFTE
### The First 100% Local-First Voice Cockpit for Web Development

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg?style=flat-square)](https://github.com/Maxjv/AnywhereDesign)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg?style=flat-square)](https://github.com/Maxjv/AnywhereDesign/releases)
[![VS Code Marketplace](https://img.shields.io/badge/VS_Code_Marketplace-v1.0.0-007acc?style=flat-square&logo=visual-studio-code&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=Maxjv.anywheredesign-cockpit)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Downloads](https://img.shields.io/badge/downloads-Windows-blueviolet.svg?style=flat-square)](https://github.com/Maxjv/AnywhereDesign/releases)
[![Server Status](https://img.shields.io/badge/runtime-OVH%20VPS%20Active-emerald.svg?style=flat-square)](https://anywheredesign.site)

**Direct your code by voice, preview in real time on mobile/tablet, and let local AI agents execute refactors on your workstation. Zero cloud lock-in. Zero NDA leakage.**

[Descargar Instalador (.exe)](https://github.com/Maxjv/AnywhereDesign/releases/latest) • [Extensión VS Code / Cursor](https://marketplace.visualstudio.com/items?itemName=Maxjv.anywheredesign-cockpit) • [Documentación](#quick-start) • [Manifiesto Local-First](#the-local-first-manifesto) • [Arquitectura](#architecture) • [Licencia](#license)


</div>

---

## ⚡ What is AnywhereDesign?

Writing code on touchscreens is painful. Remote desktops (RDP/VNC) are sluggish. And cloud-based code editors force you to upload private client repositories and violate NDAs.

**AnywhereDesign** decouples the **execution runtime** from the **direction cockpit**:

1. **Your machine remains the single source of truth:** The backend runs locally on port `4000`, orchestrating your Webpack/Vite dev servers (ports `3000`/`5173`) and terminal agents.
2. **Instant mobile pairing:** Scan a private QR code or access your secure persistent tunnel via dedicated **OVH VPS** with 4-digit PIN authentication.
3. **Voice-directed mutations in real time:** Speak naturally to dispatch directives to local AI agents (**Anthropic Claude Code CLI** or **Google Antigravity / Gemini Engine**).
4. **Live visual preview with state preservation:** Watch your UI mutate live without page reloads, without losing form state or modal navigation, and without touching your physical keyboard.

---

## 🛡️ The Local-First Manifesto: Why We Reject the Cloud

> *"Your proprietary code, your client NDAs, and your intellectual property should never reside on a third-party server."*

Most modern AI tools require you to sync entire codebases into remote SaaS platforms. For freelance engineers, boutique software agencies, and enterprise developers, this is an unacceptable compliance risk.

| Feature | Typical Cloud AI IDE | AnywhereDesign |
|---|:---:|:---:|
| **Code Repository Location** | Third-party cloud servers | **100% on your local disk** |
| **CLI Agent Execution** | Remote shared sandbox | **Local native subprocess** |
| **Network Exposure** | Open public ports / Web IDEs | **Encrypted tunnel on OVH VPS with PIN** |
| **Telemetry & Training** | Code used to train foreign models | **Zero telemetry, zero storage** |
| **Touchscreen Friction** | Virtual keyboards eating 60% of screen | **Spoken natural language + live tactile UI** |

---

## 🏗️ Architecture

AnywhereDesign uses an asymmetric, redundant architecture:

```
+-------------------------------------------------------------------------+
|                  MOBILE / TABLET COCKPIT (Touch & Mic)                  |
|            Browser-based SPA, Edge Neural Audio API, Touch UI           |
+-------------------------------------------------------------------------+
                                    |
                    [OVH VPS Secure Tunnel + PIN Access]
                                    |
+-------------------------------------------------------------------------+
|                    LOCAL CORE SERVER (Port 4000)                        |
|   • Reverse Proxy Dispatcher        • Neural Audio Synthesis (EdgeTTS)  |
|   • Reactive Task Queue Engine      • Pin / Session Authentication      |
|   • Multi-Context Workspace State   • Watchdog Fault Tolerance (2s)     |
+-------------------------------------------------------------------------+
       |                                   |                    |
       v                                   v                    v
+------------------+             +------------------+   +-----------------+
| CLIENT WORKSPACE |             | LOCAL AI AGENTS  |   | FAULT SUPERVISOR|
| React / Vite /   |             | Claude Code CLI  |   | Watchdog.ps1    |
| Next.js (Port 3k)|             | Google AGY CLI   |   | Auto-Recovery   |
+------------------+             +------------------+   +-----------------+
```

---

## 🚀 Quick Start

### 1. Descarga del Instalador Oficial de Windows (1 Clic)
1. Descarga **`Instalar_AnywhereDesign.exe`** desde [GitHub Releases](https://github.com/TFTE/AnywhereDesign/releases/latest) o desde la web oficial [anywheredesign.site](https://anywheredesign.site).
2. Ejecuta el asistente de 1 clic (crea accesos directos y arranca el supervisor en segundo plano).
3. Abre automáticamente `http://localhost:4000` con el código QR listo para escanear con tu móvil o tablet.
4. **Integridad del Instalador:**
   - Archivo: `Instalar_AnywhereDesign.exe` (~31.8 MB)
   - Checksum SHA-256: `C95AFA236A4069ADF151CFE484CE4D61958B8D21DB055D7F2E0C803A1D5B0CFD`

### 2. Extensión para VS Code y Cursor
Instala la extensión oficial **AnywhereDesign: Local-First Runtime & Remote Cockpit** directamente desde:
- **Visual Studio Marketplace** (para VS Code).
- **Open VSX Registry** (para Cursor, Windsurf y VSCodium).

---

## 🎙️ Supported AI Agent Engines

- **Anthropic Claude Code CLI:** Manipulación semántica ultrarrápida, generación de diffs y refactorización de repositorios.
- **Google Antigravity / Gemini Engine:** Modelos de razonamiento profundo (Gemini 3.1 Pro High/Low, Gemini 3.8 Flash, Gemini 3.7 Flash) con delimitación de contexto local.

---

## 🔒 Security & Intellectual Property

- **Author & Exclusive Rights:** Maximiliano Javier Vargas Dani (DNI: `60793097A`).
- **Official Intellectual Property Registration:** Registrado en el *Registro Central de la Propiedad Intelectual de España* (Asiento Registral: `REGAGE26e00081044871`, Expediente: `00765-03267660`).
- Cobertura internacional bajo el **Convenio de Berna para la Protección de las Obras Literarias y Artísticas** y la Directiva 2009/24/CE.
- **Reporte de Vulnerabilidades:** Ver [SECURITY.md](SECURITY.md).

---

## 📄 License

- **Open-Core Client & IDE Extensions:** [MIT License with Trademark Reservation](LICENSE).
- **Proprietary Backend & Managed OVH VPS Tunnel:** Servicio de suscripción Pro disponible en [anywheredesign.site](https://anywheredesign.site).
- Contribuciones comunitarias sujetas al acuerdo de cesión en [CONTRIBUTING.md](CONTRIBUTING.md).
