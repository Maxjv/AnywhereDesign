# AnywhereDesign v1.0.0 — Production Release Notes

**Release Date:** September 16, 2026  
**Author:** Maximiliano Javier Vargas Dani  
**Official IP Registration:** Ministerio de Cultura / RPI (`00765-03267660`)  
**International Legal Protection:** Convenio de Berna / WIPO

---

## 🚀 Welcome to AnywhereDesign 1.0.0

We are thrilled to present the initial production release of **AnywhereDesign by TFTE**, the first 100% local-first voice cockpit designed to direct and preview AI-assisted code changes from any mobile device without touching a physical keyboard.

---

## 🌟 Key Highlights in v1.0.0

### 1. Natural Voice Control with Neural TTS
- Ultra-low latency voice transcription via Groq / Whisper pipeline.
- Instant acoustic confirmation synthesized with Microsoft Edge Neural Voices (`es-ES-AlvaroNeural`, `en-US-JennyNeural`).
- Seamless spoken directives dispatched to CLI agent backends.

### 2. Dual Agent Engine (Anthropic Claude & Google Antigravity)
- Live bidirectional bridges with **Claude Code CLI** and **Google Antigravity (Gemini)**.
- Hot model switching between Gemini 3.1 Pro (High/Low reasoning), Gemini 3.8 Flash, and Claude 3.7 Sonnet.
- Autonomous file instruction queues in local disk storage without cloud intermediaries.

### 3. Visual Task Orchestrator (Control Board)
- Modular canvas component architecture (Screen → Card → Modal → List → Filter → Button).
- Fluid 4-column adaptive layout without intrusive horizontal scrollbars.
- Real-time serialization into `Project_Control.html`.

### 4. Zero-Friction Pairing & Dedicated OVH VPS Tunneling
- Instant QR code generation to connect smartphones and tablets in under 3 seconds.
- High-availability persistent connection powered by dedicated OVH VPS server with 4-digit PIN authentication.
- Autonomous 2-second background PowerShell watchdog (`watchdog.ps1`) for zero-downtime crash recovery.

---

## 📦 Official Download Assets & Verified Checksums

| Package | Filename | Format | File Size | SHA-256 Checksum |
|---|---|:---:|:---:|---|
| **Windows Universal Installer** | `Instalar_AnywhereDesign.exe` | `.exe` | 31.8 MB (31,807,419 B) | `C95AFA236A4069ADF151CFE484CE4D61958B8D21DB055D7F2E0C803A1D5B0CFD` |
| **AnywhereDesign Portable ZIP** | `AnywhereDesign.zip` | `.zip` | Portable | Official distribution package verified in Register |

---

## 💻 System Requirements

- **Operating System:** Windows 10 or Windows 11 (x64 architecture).
- **Runtime:** Node.js 18.0.0 or higher.
- **Hardware:** Dual-Core CPU 2.0 GHz, 4 GB RAM, 300 MB free disk space.
- **Peripherals:** Microphone input and audio output device.

---

## 📝 Checksum Verification Command

To verify the integrity of the downloaded installer on Windows PowerShell:
```powershell
Get-FileHash -Algorithm SHA256 .\Instalar_AnywhereDesign.exe
```
Expected Output:
```
Algorithm: SHA256
Hash:      C95AFA236A4069ADF151CFE484CE4D61958B8D21DB055D7F2E0C803A1D5B0CFD
Path:      Instalar_AnywhereDesign.exe
```
