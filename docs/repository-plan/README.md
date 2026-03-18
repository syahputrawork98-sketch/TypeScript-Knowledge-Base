# TypeScript Knowledge Base: Total Deconstruction Plan

> **Status Spec-Sync**: v5.7 (Full Alignment)
> **Last Updated**: 2026-03-19

Arsitektur **Source-Driven 9-Rack** ini mencerminkan taksonomi asli [typescriptlang.org/docs](https://www.typescriptlang.org/docs/).

---

## 🏗 Justifikasi Teknis (The Mirroring Principle)

Setiap Rak dipetakan langsung ke kategori navigasi utama di dokumentasi resmi.

### 1. RAK-01: Get Started
Onboarding spesifik berdasarkan latar belakang (Newbie, JS, Java, Functional).

### 2. RAK-02: The Handbook
Progresi naratif dari Basics hingga Type Manipulation.

### 3. RAK-03: Reference
Detail teknis mendalam tentang mekanika internal dan fitur khusus.

### 4. RAK-04: Modules
Membedah teori dan implementasi modul di ekosistem modern.

### 5. RAK-05: Declaration Files
Panduan authoring dan publikasi file `.d.ts`.

### 6. RAK-06: JavaScript Integration
Interaksi TS dengan codebase JS murni (JSDoc, allowJs).

### 7. RAK-07: Project Configuration
Kontrol compiler dan optimasi build (`tsconfig.json`).

### 8. RAK-08: Tutorials
Panduan praktis integrasi (React, Node, ASP.NET, Gulp).

### 9. RAK-09: Release Notes (Evolution)
Sejarah rilis dan roadmap fitur masa depan.

---

## 🗄 Peta Arsitektur Detail

| Rak | Sub-Rak (SR) | Buku (BK) | Deskripsi BK |
| :--- | :--- | :--- | :--- |
| **RAK-01** | SR-01: Basics | BK-01: Quickstart | Tutorial 5 menit & Tooling. |
| | SR-02: Backgrounds | BK-01: New Programmers | Dasar bagi pemula total. |
| | | BK-02: JS Programmers | Transisi dari JavaScript. |
| | | BK-03: Java/C# Users | Structural vs Nominal. |
| | | BK-04: Functional | FP di TypeScript. |
| **RAK-02** | SR-01: Foundations | BK-01: The Basics | Static types & Dynamics. |
| | | BK-02: Everyday Types | Primitives, Unions, Aliases. |
| | SR-02: Logic | BK-03: Narrowing | Control flow & Type guards. |
| | | BK-04: Functions | Overloads & Generics. |
| | | BK-05: Object Types | Shape & Index signatures. |
| | SR-03: Manipulation| BK-06: Type Manipulation | Generics to Template Literals. |
| | SR-04: Structure | BK-07: Classes | Visibility & Heritage. |
| | | BK-08: Modules | Import/Export syntax. |
| **RAK-03** | SR-01: Types | BK-01: Utility Types | Pick, Omit, etc. |
| | | BK-02: Enums | Numeric & String Enums. |
| | SR-02: Mechanics | BK-03: Compatibility | Subtyping rules. |
| | | BK-04: Inference | Contextual Typing. |
| | SR-03: Syntax | BK-05: JSX | UI component support. |
| | | BK-06: Decorators | Meta-programming. |
| **RAK-04** | SR-01: Practical | BK-01: ESM/CJS | Interoperability & Resolution. |
| **RAK-05** | SR-01: Authoring | BK-01: .d.ts Templates | Library structure patterns. |
| **RAK-06** | SR-01: JS Workflow | BK-01: JSDoc Ref | Type checking via comments. |
| **RAK-07** | SR-01: Config | BK-01: tsconfig.json | Complete compiler options. |
| **RAK-08** | SR-01: Frameworks | BK-01: React/Node | Specific environment guides. |
| **RAK-09** | SR-01: Versions | BK-01: Version Logs | V1.0 to V5.x. |

---

## 📜 Log Sinkronisasi (Spec-Log)

| Versi TS | Tanggal Audit | Perubahan Arsitektur | Status |
| :--- | :--- | :--- | :--- |
| **v5.7** | 2026-03-19 | Migrasi ke 9-Rack (Full Sidebar Alignment). | ✅ Synced |
. | ✅ Synced |

---

## 📈 Prinsip Pengerjaan

1.  **Source First**: Jangan menulis konten jika sumber resminya belum terpetakan.
2.  **Breadcrumb Check**: Pastikan setiap file `README.md` di level sub-folder memiliki link kembali ke Master Plan ini.
3.  **Visual Evidence**: Setiap penambahan Buku baru wajib menyertakan diagram hubungan antarentitas tipe.
